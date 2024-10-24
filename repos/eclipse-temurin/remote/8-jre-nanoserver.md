## `eclipse-temurin:8-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:9c766349c42cfa0d3f8ed9973550c7a6240f9182f85afc389e63b02ca13f6b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:63317c5111edc7c6461cda7ad2a8dbd63d9743fa2dffe5d4449ccf40a262726e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.8 MB (161758975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337fdaf38d43e74f38d4eda3df7c372fbb20aebb922059371e48cd3d653e8f67`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Thu, 24 Oct 2024 01:53:01 GMT
SHELL [cmd /s /c]
# Thu, 24 Oct 2024 01:53:02 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 24 Oct 2024 01:53:02 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 24 Oct 2024 01:53:03 GMT
USER ContainerAdministrator
# Thu, 24 Oct 2024 01:53:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 24 Oct 2024 01:53:29 GMT
USER ContainerUser
# Thu, 24 Oct 2024 01:53:33 GMT
COPY dir:47bf2d2ef237403b98ba2f50909368ef2c147e2a609dd71db23cc690a276ad54 in C:\openjdk-8 
# Thu, 24 Oct 2024 01:53:38 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9006cd878565e0783ea9060f882cc0ac70de8b44dd222e305a62cf0fae50d3`  
		Last Modified: Thu, 24 Oct 2024 01:53:41 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9bdf0a336432b3903ba9511e55bb935cb8cbc07b86302ec53e0eecd46ed75f`  
		Last Modified: Thu, 24 Oct 2024 01:53:41 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de3c647f3744dceac40e6f3c98a46e6e1345489c0b538b5aab11f04d93d12137`  
		Last Modified: Thu, 24 Oct 2024 01:53:41 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57dee900e924768e915861529ad1db38905d6646457949017f6695657061cc4d`  
		Last Modified: Thu, 24 Oct 2024 01:53:40 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1de77e69b62e8669ccfa6bc6f26a211bf754873acdd2a489d559dfd461cfba`  
		Last Modified: Thu, 24 Oct 2024 01:53:40 GMT  
		Size: 88.4 KB (88388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee4616a1b70fbf09fac352bf1986f2be2bd841d5679a4d06c7746ea63029922`  
		Last Modified: Thu, 24 Oct 2024 01:53:40 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01d76b20c71e76a3bf6939e0b15298ff2db9178ad53df36656ecfdd80d9144f`  
		Last Modified: Thu, 24 Oct 2024 01:53:43 GMT  
		Size: 41.1 MB (41060644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:becb3e8bc76700142631198f3d440a69dcbdfda14839a5995498733323b2a9b8`  
		Last Modified: Thu, 24 Oct 2024 01:53:40 GMT  
		Size: 93.8 KB (93754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.17763.6414; amd64

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
