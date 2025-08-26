## `openjdk:26-ea-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:6db57e75d7fad613d35f9e25e9040f495517491707dba844589fedf7051f9bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `openjdk:26-ea-nanoserver-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull openjdk@sha256:452b817347066d6f786b283b1f4146c9a682e7c6f7ad80041fe694450fc4536c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.3 MB (412335532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f271e96f4569ceeeba50afed99f576ca3928f5a2d68b05d3341baadc3dc30853`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 Aug 2025 02:44:20 GMT
RUN Apply image 10.0.26100.4946
# Mon, 25 Aug 2025 21:13:53 GMT
SHELL [cmd /s /c]
# Mon, 25 Aug 2025 21:13:53 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 25 Aug 2025 21:13:54 GMT
USER ContainerAdministrator
# Mon, 25 Aug 2025 21:13:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 25 Aug 2025 21:13:58 GMT
USER ContainerUser
# Mon, 25 Aug 2025 21:13:59 GMT
ENV JAVA_VERSION=26-ea+12
# Mon, 25 Aug 2025 21:14:06 GMT
COPY dir:23627f427415b3b023db24eb5c90428360be7dfe45222aac34ba93035dd0822d in C:\openjdk-26 
# Mon, 25 Aug 2025 21:14:13 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 25 Aug 2025 21:14:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6d63d98dae9e3419e8c965c24a11d30e40947cf35ee17c204c5d8b7bae7ff2ef`  
		Last Modified: Tue, 12 Aug 2025 21:13:38 GMT  
		Size: 193.5 MB (193469373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54477384ccb0b27825f319a094057b103a40430b1a30947fad4e8063258684ee`  
		Last Modified: Mon, 25 Aug 2025 21:14:48 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea59ff801b951fcd0fa502f4aa7d90aa21a67e835db7cf5bed42439d104e116b`  
		Last Modified: Mon, 25 Aug 2025 21:14:48 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3605a706c175c29fde6f40e90e6c93a812205206164250ea98f3e251290e056d`  
		Last Modified: Mon, 25 Aug 2025 21:14:48 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faddcb503ff18f1b7071fc6a10b4b5d3619f42581c8d69f3ca32ea5b738fe33c`  
		Last Modified: Mon, 25 Aug 2025 21:14:50 GMT  
		Size: 76.2 KB (76169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e9113bd4a4b02545b8fff63bda2f16548c2a67f093dc609563be6e1b04bba8`  
		Last Modified: Mon, 25 Aug 2025 21:14:49 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09460bae10b55688345943d4f5ddf31a7c7f7724ac5ece98482760b2e6e85a2c`  
		Last Modified: Mon, 25 Aug 2025 21:14:49 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633ccd8e4113d7e410dfb9f1e3a261f8619cfba826c6158965452880af966f7b`  
		Last Modified: Tue, 26 Aug 2025 00:24:39 GMT  
		Size: 218.7 MB (218669796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3fd6fc4388fbbe17738232b13c85a31b9852004fe5d4ec27c9ddfda1692b2e`  
		Last Modified: Mon, 25 Aug 2025 21:14:50 GMT  
		Size: 113.8 KB (113834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db0c807ebe7b2848f4fe694481dacab66ad7e7f31b5014542b268700a5b33f6`  
		Last Modified: Mon, 25 Aug 2025 21:14:51 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
