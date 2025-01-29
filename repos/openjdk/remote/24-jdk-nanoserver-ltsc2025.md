## `openjdk:24-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:d8f882667099b90f4117e202ff33361bc3b2d2a58451e8f85c96c8907c7a59c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `openjdk:24-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:bcf8b01a54764b075bfccbfb1b0ca8f6b7e08b4a622e0b5ba4028757c3d8d7b8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.7 MB (407719326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7c4cba251fbb2e166225f79e4abec8c128f821a2ac6735b9aa8f261127fd2d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Wed, 29 Jan 2025 01:32:19 GMT
SHELL [cmd /s /c]
# Wed, 29 Jan 2025 01:32:20 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 29 Jan 2025 01:32:21 GMT
USER ContainerAdministrator
# Wed, 29 Jan 2025 01:32:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 29 Jan 2025 01:32:27 GMT
USER ContainerUser
# Wed, 29 Jan 2025 01:32:29 GMT
ENV JAVA_VERSION=24-ea+33
# Wed, 29 Jan 2025 01:32:36 GMT
COPY dir:0501e586ce21e14cfb645b0134706225edb213a038c5d5da062ef05b40a90877 in C:\openjdk-24 
# Wed, 29 Jan 2025 01:32:45 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 29 Jan 2025 01:32:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbb17a334e2267dfe34c8a6e200b6502ad432dd0919391b20a2f30b5ff78c90`  
		Last Modified: Wed, 29 Jan 2025 01:32:52 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d8e560c3709e0fc7b9a087928022003bc163ef5293433a7ef6af2ce24ffb96`  
		Last Modified: Wed, 29 Jan 2025 01:32:52 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d858a86d10254d90e4bb3d00c0e799a7f71649e8d2bdcbd142e3120808ebcf`  
		Last Modified: Wed, 29 Jan 2025 01:32:52 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343c87c9944bd1bccafabf2c3acded582f324980aae928064f537f3548f8f126`  
		Last Modified: Wed, 29 Jan 2025 01:32:52 GMT  
		Size: 75.4 KB (75440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7038b340b796648be80e40ba746d0ac585f591a90c3f20e03b9bbffd4a4279`  
		Last Modified: Wed, 29 Jan 2025 01:32:51 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a2abb6b5b71edc0f89e02a40284bf895e1d83159a3c4b22492a7d667c004c1`  
		Last Modified: Wed, 29 Jan 2025 01:32:51 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8fa42baa1d2b21660c2a6164114a089b3ef60062e8353201a7f06bfe4649c5`  
		Last Modified: Wed, 29 Jan 2025 01:33:03 GMT  
		Size: 208.5 MB (208491486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7870d8d078737bb1cfb4e21816993c67032d8f698865a56f3c3a1dcdb623127`  
		Last Modified: Wed, 29 Jan 2025 01:32:51 GMT  
		Size: 91.7 KB (91709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e98bd40113562c1cca0bba0356b666482b9d771ba53ca88a2570af2f6b12aab`  
		Last Modified: Wed, 29 Jan 2025 01:32:51 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
