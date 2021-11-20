## `openjdk:18-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:9cf56c97169303648fa72d40dae69b95309fc4d5e2acb4807aea64cdfe9b1754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `openjdk:18-ea-jdk-nanoserver` - windows version 10.0.17763.2300; amd64

```console
$ docker pull openjdk@sha256:507ce9a35503dd9ec9351a0ba08371c8a22a4e30867454af48c3096f1a624e64
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290182674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c113b54ab0bcd028284e7008b1308f7f65bbe6194003c5af0459528b6375c760`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:13:20 GMT
SHELL [cmd /s /c]
# Wed, 10 Nov 2021 20:31:55 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 10 Nov 2021 20:31:55 GMT
USER ContainerAdministrator
# Wed, 10 Nov 2021 20:32:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Nov 2021 20:32:07 GMT
USER ContainerUser
# Fri, 19 Nov 2021 23:26:41 GMT
ENV JAVA_VERSION=18-ea+24
# Fri, 19 Nov 2021 23:26:55 GMT
COPY dir:77acf4374db06f4078bba64fa913da190ecfaf865022b6d403d351b2a3429576 in C:\openjdk-18 
# Fri, 19 Nov 2021 23:27:16 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 19 Nov 2021 23:27:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b9dc943b4e8df8f472d444248152fa0920172ec630a60ada316e1603600dd1c7`  
		Size: 102.8 MB (102782944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e60ec86b90e1492e0e0ed2cbebcf624990a34862e24207343fd85b84b3544c8e`  
		Last Modified: Wed, 10 Nov 2021 18:01:59 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d97d878bac5dd9dcbe1bb5f45ade2111fc77e8d4a5a348163bd9c3ddddbaf0`  
		Last Modified: Wed, 10 Nov 2021 21:11:37 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5a46fd95d3a8e8b5949c49cc0d70b858bddbe38c8c33e0a6a3e0f157d7795a`  
		Last Modified: Wed, 10 Nov 2021 21:11:37 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88539ad3f1fb0ea6957da9a7298c1f6546afbb52b2deb7199763195fca993d98`  
		Last Modified: Wed, 10 Nov 2021 21:11:37 GMT  
		Size: 74.2 KB (74205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d133fe2173015750539b2d0a8fb86dbdbe0c6b44c8d75ddeb714a82814f98e00`  
		Last Modified: Wed, 10 Nov 2021 21:11:33 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3a2466fd4297ad1cbbcaaa25035a6b35ea5975cb561001da9db0675375185c`  
		Last Modified: Sat, 20 Nov 2021 00:35:47 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934ed6a769c7997fb8acdc6fe481d9b7d81ad6bae44fa6a623610f3605a8a4eb`  
		Last Modified: Sat, 20 Nov 2021 00:39:11 GMT  
		Size: 183.8 MB (183791014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14182fc8b3708e056f013d2a3322a961513d9d03b8188742f3200272109f69d`  
		Last Modified: Sat, 20 Nov 2021 00:35:51 GMT  
		Size: 3.5 MB (3527641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96bc9afe5c8a2cf7eb7ff8af22a7b431fa357108b1faebedbb85c1b03e7495f7`  
		Last Modified: Sat, 20 Nov 2021 00:35:47 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
