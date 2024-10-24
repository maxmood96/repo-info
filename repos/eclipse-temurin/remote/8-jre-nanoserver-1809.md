## `eclipse-temurin:8-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:300ff57015e4ad1b60e9145c5448d12e21a409bffd0700a2f8c4f80cb41ef88a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:8-jre-nanoserver-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:856136d125f0d5cb9ebc87089d30249ac671505455c4b9d4f10b44fd57d8aac2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196302554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0557dc6de955e480bc436f5b98c3f41ed365f1000b5684275a1ce6936fc1e108`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Thu, 24 Oct 2024 01:52:23 GMT
SHELL [cmd /s /c]
# Thu, 24 Oct 2024 01:52:24 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 24 Oct 2024 01:52:25 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 24 Oct 2024 01:52:25 GMT
USER ContainerAdministrator
# Thu, 24 Oct 2024 01:52:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 24 Oct 2024 01:52:30 GMT
USER ContainerUser
# Thu, 24 Oct 2024 01:52:33 GMT
COPY dir:47bf2d2ef237403b98ba2f50909368ef2c147e2a609dd71db23cc690a276ad54 in C:\openjdk-8 
# Thu, 24 Oct 2024 01:52:37 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39746c21e0bfd57387af3f20042c2bbaa69952649ecc4340a2ccd4313beff0a8`  
		Last Modified: Thu, 24 Oct 2024 01:52:42 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8045972030c7a0ac28672ad604c539afe41d650555b93ea908b67cefa3a1179a`  
		Last Modified: Thu, 24 Oct 2024 01:52:42 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c12de5558fabb9ca25edbe70fe77d2f74728fa04fd2a37fa92e8bdab25650e6`  
		Last Modified: Thu, 24 Oct 2024 01:52:42 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff755066fc203c1f3021230f80a1c178819dafea0cea015e7694101f7654cf06`  
		Last Modified: Thu, 24 Oct 2024 01:52:41 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf761e526f5837ea338ec3d30bcebae9d626a90f82a927500582be967d61f889`  
		Last Modified: Thu, 24 Oct 2024 01:52:41 GMT  
		Size: 68.0 KB (68000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa6a081b495eed1ea92f728e7542e542519be7a4461739458934b09b925fb83`  
		Last Modified: Thu, 24 Oct 2024 01:52:41 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820bab61e80711ad861f6e9601e3b81b4ad2b061183ac734575833c9a175bfc7`  
		Last Modified: Thu, 24 Oct 2024 01:52:44 GMT  
		Size: 41.1 MB (41060982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19d07ce1cb58e23f758c28420325c467807c5ebaffb9c24c8060d27770556d`  
		Last Modified: Thu, 24 Oct 2024 01:52:41 GMT  
		Size: 74.5 KB (74526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
