## `eclipse-temurin:11-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:71daf5116aa15468def21a9b6f9bd560fb984f91a05d899c28e770aadd92006e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:11-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull eclipse-temurin@sha256:3ada2094bdb18061fd5bfee5d1d81bce27d5f50986d34c9f020f863f418acffd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.9 MB (321926366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d5de5b431aa241bf2652ddd86acd85e8f7ce16484eacace81711e43debff0dd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Wed, 29 Apr 2026 23:09:34 GMT
SHELL [cmd /s /c]
# Wed, 29 Apr 2026 23:09:35 GMT
ENV JAVA_VERSION=jdk-11.0.31+11
# Wed, 29 Apr 2026 23:09:36 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 29 Apr 2026 23:09:37 GMT
USER ContainerAdministrator
# Wed, 29 Apr 2026 23:09:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 29 Apr 2026 23:09:47 GMT
USER ContainerUser
# Wed, 29 Apr 2026 23:10:22 GMT
COPY dir:508f69ae524938b28a83a19a9aeade10facf00325b620c7a836698644d966097 in C:\openjdk-11 
# Wed, 29 Apr 2026 23:10:26 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 29 Apr 2026 23:10:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ed8c965b428245bbbc880bcc6f88cfabd990adaaab5a88c1e8a2755c1a6364`  
		Last Modified: Wed, 29 Apr 2026 23:10:32 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ddb68717a8c191029680fea651cbbb49db2ef5299240a741bd1545fc9e6d3d`  
		Last Modified: Wed, 29 Apr 2026 23:10:32 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e443464f57c4151048398b49b9e09dd6482e6c9f0c6b6ecdd2c1698192aa595f`  
		Last Modified: Wed, 29 Apr 2026 23:10:32 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15d1f81cb4c6bd23965f5fd1baa512c80c43aa2b725f7146ba394af3574477b`  
		Last Modified: Wed, 29 Apr 2026 23:10:32 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7936d1db855cb885ee70e227a95d3e28ba11ad1c413e0afbb148eb071570128c`  
		Last Modified: Wed, 29 Apr 2026 23:10:31 GMT  
		Size: 72.3 KB (72290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c77821736370f7ba2587a6c75906357c3ff8f5c7591687d51e25d9d94ef6d15`  
		Last Modified: Wed, 29 Apr 2026 23:10:31 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e45e3c369bb67cbc57fa944fbd98052b3ecaba2c7ea2f7cd57e62973df4a668`  
		Last Modified: Wed, 29 Apr 2026 23:10:43 GMT  
		Size: 194.8 MB (194785112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c3622aaae815e68a9348b7a12db7f5b58a159bffa512535ba3ff06257501d2`  
		Last Modified: Wed, 29 Apr 2026 23:10:31 GMT  
		Size: 106.7 KB (106651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4769dd28e15a1c463917fc80254a6f571fa7cfb485368435de64ed3782bd92b4`  
		Last Modified: Wed, 29 Apr 2026 23:10:31 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
