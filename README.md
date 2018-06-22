# maven-repository

- 将生成的jar包拷贝到maven-repository 的 release分支下
```
mvn clean deploy -Dmaven.test.skip  -DaltDeploymentRepository=self-mvn-repo::default::file:/path/to/github/maven-repository
```

- 将本地jar commit到远程仓库

```
git push origin release:release
```

- 本仓库地址

```
	<repositories>
		<repository>
			<id>xingePush</id>
			<url>https://raw.githubusercontent.com/xingePush/maven-repository/release/</url>
		</repository>
	</repositories>
```
