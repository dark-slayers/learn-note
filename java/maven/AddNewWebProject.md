# 新建Web项目的流程
---
1. 在GITHUB上创建新项目
2. 将项目clone至本地
3. 在Eclipse中创建新的Web项目（Maven）
4. 将创建的项目的文件复制到项目的colne目录，修改.gitignore文件
5. 删除Eclipse中的项目，使用导入方式将colne目录中的项目导入Eclipse
6. 修改项目的编译运行环境、pom.xml文件
7. 打开项目.settings目录
8. 修改org.eclipse.jdt.core.prefs文件：1.5修改为1.8
9. 修改org.eclipse.wst.common.component文件：把project-version="1.5.0"改成project-version="1.8.0"
10. 修改org.eclipse.wst.common.project.facet.core.xml文件：<br>
把`<installed facet="java" version="1.5"/>`改成`<installed facet="java" version="1.8"/>`<br>
把`<installed facet="jst.web" version="2.3"/>`改成`<installed facet="jst.web" version="3.1"/>`
11. 修改项目属性，java编译器,一致性级别改为1.8，构建路径：JRE系统库，修改为JDK
12. 修改pom.xml文件的build部分：
<pre>
<code>
	`<build>
		<plugins>
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-compiler-plugin</artifactId>
				<version>3.3</version>
				<configuration>
					<source>1.8</source>
					<target>1.8</target>
				</configuration>
			</plugin>
		</plugins>
		<finalName>项目名称</finalName>
	</build>`
</code>
</pre>
13. Maven->Update Project ...
