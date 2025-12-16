## `openjdk:27-ea-2-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:33f2af1eededefa18687744eecbb421eb70225b06219cae74cf00ef5d99f3f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `openjdk:27-ea-2-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.7462; amd64

```console
$ docker pull openjdk@sha256:a7f5e49757f9757d20cd631cd7312700c66a3ddf3973c9d928528d53e56ae24f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.9 MB (422939659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46eef366e5817d57b66a05b236cc0ccd4c774f48f3747c6776686fe1c19b46b1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Dec 2025 21:31:34 GMT
RUN Apply image 10.0.26100.7462
# Tue, 16 Dec 2025 01:09:47 GMT
SHELL [cmd /s /c]
# Tue, 16 Dec 2025 01:11:59 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 16 Dec 2025 01:12:00 GMT
USER ContainerAdministrator
# Tue, 16 Dec 2025 01:12:01 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 16 Dec 2025 01:12:02 GMT
USER ContainerUser
# Tue, 16 Dec 2025 01:12:02 GMT
ENV JAVA_VERSION=27-ea+2
# Tue, 16 Dec 2025 01:12:40 GMT
COPY dir:1fbd408005587e5be2ee9227fb6a081e87d3544117c99f827373a71a72099927 in C:\openjdk-27 
# Tue, 16 Dec 2025 01:12:45 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 16 Dec 2025 01:12:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a092205b76ca656d8483e99445def9f0619cb3acb2688bf9a33244c43ad44ce`  
		Last Modified: Tue, 09 Dec 2025 22:15:12 GMT  
		Size: 198.9 MB (198873947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3806e5e70ef53bf57ac133d64c6630554cf260d0b0feb9af79e0888e162db0e6`  
		Last Modified: Tue, 16 Dec 2025 01:11:48 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba4b2c88e58a27dfda65105b78671b65047471f9035fae5e9d9983009db8ff3f`  
		Last Modified: Tue, 16 Dec 2025 01:13:17 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e20f638bb9caa437ca0642baad947d542535445e73785a3a94329f97eb66bab`  
		Last Modified: Tue, 16 Dec 2025 01:13:17 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be1d4040927d7c21bdf90d8adac9460892ad7ba977e0b1715410455ddd1009d4`  
		Last Modified: Tue, 16 Dec 2025 01:13:17 GMT  
		Size: 73.2 KB (73245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1754119d4a9c81e4d68575fab2fad83e535eea4f69f1699083a667680f396662`  
		Last Modified: Tue, 16 Dec 2025 01:13:17 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4a9a0d7c385154ff311983c497f6556162e075f449806f8fd9224e0fcbb931`  
		Last Modified: Tue, 16 Dec 2025 01:13:17 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ddbb3cc62b665a4f30d55b421e4e50ceb4d6d6077458ff3f5be46978a5939cf`  
		Last Modified: Tue, 16 Dec 2025 01:13:59 GMT  
		Size: 223.9 MB (223873530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7894c01b48a8a36792b0f61eef3cd3661469941d8334e307c7fe343be7b69090`  
		Last Modified: Tue, 16 Dec 2025 01:13:17 GMT  
		Size: 112.4 KB (112447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d8151db7a2430eb96abd1ca67704972864e580f76f22a17e104419c4944e37`  
		Last Modified: Tue, 16 Dec 2025 01:13:17 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
