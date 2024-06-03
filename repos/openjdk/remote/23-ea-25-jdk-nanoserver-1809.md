## `openjdk:23-ea-25-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:34c5768e4e8211d5a528c40d9983d25dd85c580bb642dbfcdce7e4cbc4371b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `openjdk:23-ea-25-jdk-nanoserver-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull openjdk@sha256:f82d39b7bd31088570b545596002e338c40e723d00f482a17fc05815db8d6a75
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.1 MB (365058749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5dcbf9a0f63bd7d719f09c9764c76b96594034e1f4b6a88b12ef8ad499588c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Mon, 03 Jun 2024 19:55:20 GMT
SHELL [cmd /s /c]
# Mon, 03 Jun 2024 19:55:24 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 03 Jun 2024 19:55:24 GMT
USER ContainerAdministrator
# Mon, 03 Jun 2024 19:55:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 03 Jun 2024 19:55:46 GMT
USER ContainerUser
# Mon, 03 Jun 2024 19:55:46 GMT
ENV JAVA_VERSION=23-ea+25
# Mon, 03 Jun 2024 19:55:57 GMT
COPY dir:34eb27ecfecb53d87d51dfd1f5913a03ed169adbf0cca94464a7aacd689a30e8 in C:\openjdk-23 
# Mon, 03 Jun 2024 19:56:03 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 03 Jun 2024 19:56:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6795b661cab920d815cb673d945438026e7097e41daf2df98264c72ab2d7146c`  
		Last Modified: Mon, 03 Jun 2024 19:56:08 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b27a7344b2e2ded2ff067214c31c0ca5a5c11ac3c20f7dda2c1023a6e920001`  
		Last Modified: Mon, 03 Jun 2024 19:56:09 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff12c240dbad84b54bc5cc65986ea73e6ae234049967764a5a06da0583fb44d7`  
		Last Modified: Mon, 03 Jun 2024 19:56:08 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6f0e775f03759c9912084993fa7458db0ab5ebcc7a842d5e0d84739d814760`  
		Last Modified: Mon, 03 Jun 2024 19:56:08 GMT  
		Size: 68.1 KB (68107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b0c01748cb65a2a5492304a2ec41605e44032bdb2f25941d156b2998d9f264`  
		Last Modified: Mon, 03 Jun 2024 19:56:07 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eece2f588d6a76ba837071e1cc5ac0e2ea15a769dcc5003a49cff754c013a69`  
		Last Modified: Mon, 03 Jun 2024 19:56:07 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61142f2c31830890504a860d0e41f1ec0f1a4176f720913bdb0312aa4d5d619`  
		Last Modified: Mon, 03 Jun 2024 19:56:18 GMT  
		Size: 205.9 MB (205947338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76796c07d70c98c0639c722c3569194d6fd41a42b7237c00cbd019a619add303`  
		Last Modified: Mon, 03 Jun 2024 19:56:07 GMT  
		Size: 4.1 MB (4095671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5e20654bf0c49ab561d59da0c522039f1eef146940aab4c7fc87ebe9310e5b`  
		Last Modified: Mon, 03 Jun 2024 19:56:07 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
