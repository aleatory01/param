pipeline {
    agent any

    environment {
        CONFIG = "" //この時点ではプロジェクトの設定ファイルを読み込めないので仮の値を設定しておく
    }

    stages {
        stage('チェックアウトして設定ファイル読み込み') {
            steps {
                // プロジェクトをチェックアウト
                //checkout scm

                script {
                    // チェックアウト後に設定ファイルを読み込む
                    // Pipeline Utility Steps Pluginの関数を使う
                    CONFIG = readYaml(file: 'config.yml')
                }
            }
        }

        stage('設定ファイル参照') {
            steps {
                echo "CONFIG.someProp ＝ ${CONFIG.someProp}"
                echo "CONFIG.someCategory.prop ＝ ${CONFIG.someCategory.prop}"
                echo "CONFIG.someCategory.arrayProp[0] ＝ ${CONFIG.someCategory.arrayProp[0]}"
                echo "CONFIG.someCategory.arrayProp[1] ＝ ${CONFIG.someCategory.arrayProp[1]}"
                echo "CONFIG.someCategory.arrayProp[2] ＝ ${CONFIG.someCategory.arrayProp[2]}"
            }
        }
    }
}