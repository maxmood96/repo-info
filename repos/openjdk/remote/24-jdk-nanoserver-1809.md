## `openjdk:24-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:8e6313c1dea7a375d3f91b242edf19dba391e71d1e0a81f4fdfc7c39f748b1fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `openjdk:24-jdk-nanoserver-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull openjdk@sha256:2a6ee6c3c94da25f537c08677485dde067bef207861b8fa0c6f44c7eb57247ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.3 MB (365340296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a6602a0fc213ace372a7d01c918a434e8224eeb03ae2cc84d638d0e42914c1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 19:14:46 GMT
SHELL [cmd /s /c]
# Wed, 12 Jun 2024 19:14:48 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 12 Jun 2024 19:14:48 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 19:14:50 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 12 Jun 2024 19:14:51 GMT
USER ContainerUser
# Wed, 12 Jun 2024 19:14:52 GMT
ENV JAVA_VERSION=24-ea+1
# Wed, 12 Jun 2024 19:14:59 GMT
COPY dir:65f162ff11cc2a31de446754da8c804d9d59bb6267610365535eba662147bf29 in C:\openjdk-24 
# Wed, 12 Jun 2024 19:15:04 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 12 Jun 2024 19:15:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ec0b570a0fd546de3dc14648705badbd3c3bcd46b51427f8720fbbd26f0410`  
		Last Modified: Wed, 12 Jun 2024 19:15:10 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e16e463eda9e064f9580a6f4f333f6190f5a4c9cc67691e1ad08954b38d2eb4`  
		Last Modified: Wed, 12 Jun 2024 19:15:09 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a96d0d5607b280c266af7571b8c22fb511aec4716cfd02595df3f72557009fa`  
		Last Modified: Wed, 12 Jun 2024 19:15:08 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0227e56f4aceef033f719693c55f55c041911375958775e07990b14e8254ec`  
		Last Modified: Wed, 12 Jun 2024 19:15:08 GMT  
		Size: 71.8 KB (71765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e5e4612e61bbe440b108012bb61e717533be12d54658df39aff27b679e98ba`  
		Last Modified: Wed, 12 Jun 2024 19:15:07 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c859d824870881affe873cb834d014f860e30b090d89d661996c41918cbed9`  
		Last Modified: Wed, 12 Jun 2024 19:15:07 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c0c5b822d7858f416d41c57747beb1dea26cb62f89162edcbe6e283dec08e9`  
		Last Modified: Wed, 12 Jun 2024 19:15:21 GMT  
		Size: 206.1 MB (206107289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f03b1e0bf074d9d77a89ea21b4db64248f6ea5ee12a64840bfc4957be426a23`  
		Last Modified: Wed, 12 Jun 2024 19:15:08 GMT  
		Size: 4.1 MB (4121777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4518842e4a5ca7202caf5a82fee2e3b6134bd6e9e3c40091826f06f4fb82891e`  
		Last Modified: Wed, 12 Jun 2024 19:15:07 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
