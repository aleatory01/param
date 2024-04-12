pipeline {
    agent any

    environment {
        CONFIG = "" //この時点ではプロジェクトの設定ファイルを読み込めないので仮の値を設定しておく
        CONFIG = readYaml(file: 'config.yml')
    }

    stages {
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