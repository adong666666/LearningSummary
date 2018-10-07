```
apply plugin: 'org.greenrobot.greendao'
```

```
//数据库
implementation 'org.greenrobot:greendao:3.2.2'
```
```
    buildTypes {
        release {
            minifyEnabled false
            proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.pro'
        }

        /**
         * 数据库
         */
        greendao {
            schemaVersion 1//数据库版本号
            daoPackage 'com.study.help.db.dao'//设置DaoMaster、DaoSession、Dao包名
            targetGenDir 'src/main/java'//设置DaoMaster、DaoSession、Dao目录
            generateTests false       //设置自动生成单元测试用例
            targetGenDirTests "src/androidTest/java"       //设置生成单元测试目录
        }
    }
```    
```
GreenDao数据库升级数据迁移

allprojects {
    repositories {
        google()
        jcenter()
        maven {url"http://jitpack.io"}
    }
}

//数据库升级数据迁移
implementation 'com.github.yuweiguocn:GreenDaoUpgradeHelper:v2.0.1'
```