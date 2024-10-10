## `eclipse-temurin:17-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:ec2aabe192d7ae5c269ec19a810e91947a7b376e4ad77bb70c5fdef40edd7ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:17-jre-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:35c6014a1954e35c882b47c12a4be86c69d7e891ca5b9be4e8c3ff467468f766
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.5 MB (201506197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b02138f66f8bf5b62e07c844c52b868aa3c4e38b78c8081349882a260bed547`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Wed, 09 Oct 2024 23:37:31 GMT
SHELL [cmd /s /c]
# Wed, 09 Oct 2024 23:52:38 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 09 Oct 2024 23:52:38 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 09 Oct 2024 23:52:39 GMT
USER ContainerAdministrator
# Wed, 09 Oct 2024 23:52:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Oct 2024 23:52:49 GMT
USER ContainerUser
# Wed, 09 Oct 2024 23:56:26 GMT
COPY dir:4243678b5415f703b690863e65df7851d84efb271bd792cb5cbd95ab7bb17263 in C:\openjdk-17 
# Wed, 09 Oct 2024 23:56:37 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6adfd98d9a05d48859cfa5f6e1dc162be56797c9e86e7647518192a16af3d27`  
		Last Modified: Thu, 10 Oct 2024 00:20:41 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd5871594ea0edb1cbe05e7b9044e155182eaf5c9ff9fa5e5003755aaf045d3`  
		Last Modified: Thu, 10 Oct 2024 00:26:36 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b34251fd4c18da8ae9561441a25ac8a0daa460833af4ed83b4241ebcb6dab21`  
		Last Modified: Thu, 10 Oct 2024 00:26:35 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9aa5d601461ab6ddd6030a5b48aa92a7f868c149bae892010555b52b3faa863`  
		Last Modified: Thu, 10 Oct 2024 00:26:34 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce71e9d146261dcf74a7ede1fc033cc346be0af1c36fc62864c309bf46621b17`  
		Last Modified: Thu, 10 Oct 2024 00:26:32 GMT  
		Size: 68.2 KB (68222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d66c591d22da5ec7ed481cc918f39f364764653592e3d3dc7eaf3086bd2078f`  
		Last Modified: Thu, 10 Oct 2024 00:26:32 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cccb8a679751e39f8715f2acd2deb5c98b8d4e1724096979024193fa39954234`  
		Last Modified: Thu, 10 Oct 2024 00:27:45 GMT  
		Size: 43.4 MB (43357554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2700bde26fb1640522f929fa20249921aa781a9d98c2232c855db7c9beef855`  
		Last Modified: Thu, 10 Oct 2024 00:27:39 GMT  
		Size: 3.0 MB (2981099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
