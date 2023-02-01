```bash
# 安装jar到本地仓库目录中
$ mvn org.apache.maven.plugins:maven-install-plugin:2.5.2:install-file \
	-Dfile=/Users/xiaojingjing/Downloads/buildvu-html-trial.jar \
	-DgroupId=com.idrsolutions \
	-DartifactId=buildvu-html-trial \
	-Dversion=2023.01 \
	-Dpackaging=jar \
	-DlocalRepositoryPath=/Users/xiaojingjing/tmp/maven-repo/repository

# 将本地目录提交到本仓库中


```

# 在pom.xml中配置私服地址

```xml
<repositories>
    <repository>
        <id>jianbing-maven-repo</id>
        <url>https://raw.githubusercontent.com/jianbingguozi/maven-repo/master/repository</url>
    </repository>
</repository>

<dependencies>
    <dependency>
        <groupId>com.idrsolutions</groupId>
        <artifactId>buildvu-html-trial</artifactId>
        <version>2023.01</version>
    </dependency>
</dependencies>
```