## `openjdk:23-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:f2fa6a5709cb9685f66807174ea0a8f1732e091423c78a8d18d9d9cfaa51a260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `openjdk:23-ea-jdk-nanoserver` - windows version 10.0.17763.5696; amd64

```console
$ docker pull openjdk@sha256:97be03f484932ad64fbd6c19a60b76a3fac25772f8e6b70021d02ee29db6907b
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.5 MB (314501116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae05ab78abed42e2478fe0c20079394fa3a2481343f446e733a1233860b2d34`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Mon, 15 Apr 2024 19:05:17 GMT
SHELL [cmd /s /c]
# Mon, 15 Apr 2024 19:05:19 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 15 Apr 2024 19:05:19 GMT
USER ContainerAdministrator
# Mon, 15 Apr 2024 19:05:22 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 15 Apr 2024 19:05:22 GMT
USER ContainerUser
# Mon, 15 Apr 2024 19:05:23 GMT
ENV JAVA_VERSION=23-ea+18
# Mon, 15 Apr 2024 19:05:31 GMT
COPY dir:e392fdb799e3623d41fed1d2851ee42c5d035a842ecf6258d3e8df762c490fec in C:\openjdk-23 
# Mon, 15 Apr 2024 19:05:36 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 15 Apr 2024 19:05:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2f4fb4b499f8c33b457af982db9a118225279738ceeb78ba1281c496ecbb901`  
		Last Modified: Mon, 15 Apr 2024 19:05:42 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f38895a640251b7f5c95038f7c908c859ef868173cf0af2ff6c2d93de16f58a`  
		Last Modified: Mon, 15 Apr 2024 19:05:41 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10ae9145e339c7eb576a8660482e21c3c09fd148a774f92ba94bdf1b29c308e`  
		Last Modified: Mon, 15 Apr 2024 19:05:41 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cc55f1e38b268398e9665a37416bc8001a90ef540b5a03d034b1d713d87185`  
		Last Modified: Mon, 15 Apr 2024 19:05:41 GMT  
		Size: 81.4 KB (81356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ebde1f2c1811e2a576e23c6effe05f63d0217ef80d8eeebfd89b148a46a52ba`  
		Last Modified: Mon, 15 Apr 2024 19:05:39 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcf5ffe4c4ca87ca12f6ed112d6c40049782fbea97e2c6edec4b9698037715d`  
		Last Modified: Mon, 15 Apr 2024 19:05:39 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c99d1642ddaf9bbcf3ba0dfb7cdea6f6c7647795cf3b729582a82a6e52a3b119`  
		Last Modified: Mon, 15 Apr 2024 19:05:52 GMT  
		Size: 205.3 MB (205305612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df76bbf2780d66cb43960ade61e4a147f2de62f8916b08c1bfd9ddcb6684dfa7`  
		Last Modified: Mon, 15 Apr 2024 19:05:40 GMT  
		Size: 4.2 MB (4218832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c0a19b808a9e6a6ed592eeca0627af92c2b75b935712a13a45487b4dfc03b3`  
		Last Modified: Mon, 15 Apr 2024 19:05:39 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
