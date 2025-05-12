## `openjdk:25-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:ae5a7598feba641f1678f36ee31a1d723c32bbd52174cc307497e66de55ba458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `openjdk:25-nanoserver-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull openjdk@sha256:eb7c8215b3894a2eef99b9d29861a0a86fa5838310e9a6f1e449c838a8939fc5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.7 MB (398715878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce15741a25571dba8a487204f981ffea9ab6810d02a85e84703a09a73c7fe486`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Mon, 12 May 2025 20:14:24 GMT
SHELL [cmd /s /c]
# Mon, 12 May 2025 20:14:25 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 12 May 2025 20:14:26 GMT
USER ContainerAdministrator
# Mon, 12 May 2025 20:14:31 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 12 May 2025 20:14:32 GMT
USER ContainerUser
# Mon, 12 May 2025 20:14:33 GMT
ENV JAVA_VERSION=25-ea+22
# Mon, 12 May 2025 20:14:41 GMT
COPY dir:d2aeeab016ce5cfb722c90fbb6527341de5d03dac18528814b93fc4084ba77f8 in C:\openjdk-25 
# Mon, 12 May 2025 20:14:49 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 12 May 2025 20:14:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 17 Apr 2025 02:52:17 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa69cba76f2e76e6ea2f7fbc14d5c8749db1a4068cb2e0083d9e2eb3a2c6c402`  
		Last Modified: Mon, 12 May 2025 20:14:55 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2719773166b5d19a1173bfa522a49f34f7c294c866818cd18426082d9531e74b`  
		Last Modified: Mon, 12 May 2025 20:14:54 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f2d04c58919510454a32b0dcc98993ff1a5282a54bc6aaa12fbe5e21792e12`  
		Last Modified: Mon, 12 May 2025 20:14:54 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace9caea87efcc581055a12de97feb83f18915b83f4492f8f629219dcf4fcc15`  
		Last Modified: Mon, 12 May 2025 20:14:54 GMT  
		Size: 76.3 KB (76337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc4a509e8eb01590bb463ccccce8b9e9abc4424942b44686385832b26e245d7`  
		Last Modified: Mon, 12 May 2025 20:14:53 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e792ee4e77170efadbb84ceccd4fef37edd0f8389dc6343d855127a70eec115f`  
		Last Modified: Mon, 12 May 2025 20:14:53 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2cd6bbffb3dc880dd8b18be6945c3a133de647f4725a27ec4753dc10390a6ab`  
		Last Modified: Mon, 12 May 2025 20:15:05 GMT  
		Size: 208.4 MB (208366883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926b1301fdec750c43a61c4d012feea550182a0e468e5e81c99651e40e5a4b5c`  
		Last Modified: Mon, 12 May 2025 20:14:53 GMT  
		Size: 124.1 KB (124103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c54e8fda92be470437bf75b8fa283296cf4c314b101e19f3044d5a09bc1e33a`  
		Last Modified: Mon, 12 May 2025 20:14:54 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
