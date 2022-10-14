## `openjdk:20-nanoserver-1809`

```console
$ docker pull openjdk@sha256:a5d321a8519efaa90f55bf67393e2272a928691e325ac2beff03712069a82edd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `openjdk:20-nanoserver-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull openjdk@sha256:9243de7f06c9b3ab0bce994e0879d29fc896e82b472e744224fe47bd7f587eec
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.2 MB (299243841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce617193cac2846060e499ccfe387bce466824721f3e6b2160194dd9d414819e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Oct 2022 01:37:47 GMT
RUN Apply image 10.0.17763.3532
# Wed, 12 Oct 2022 15:20:49 GMT
SHELL [cmd /s /c]
# Wed, 12 Oct 2022 16:43:51 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 12 Oct 2022 16:43:51 GMT
USER ContainerAdministrator
# Wed, 12 Oct 2022 16:44:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 12 Oct 2022 16:44:03 GMT
USER ContainerUser
# Thu, 13 Oct 2022 23:30:01 GMT
ENV JAVA_VERSION=20-ea+19
# Thu, 13 Oct 2022 23:30:16 GMT
COPY dir:c96ad2d02dc7805e12f6571713754b1c1282da5f4a5c19c8a709be6d00375b94 in C:\openjdk-20 
# Thu, 13 Oct 2022 23:30:38 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 13 Oct 2022 23:30:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5ead999142ecce15e02523c49706a633fa708374d94bb65a254e3a3c117d609b`  
		Size: 103.4 MB (103377244 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4a6a667d76c19fca171390d60fb90c40e16c777050e943a7fe17ad7686841f0f`  
		Last Modified: Wed, 12 Oct 2022 16:02:59 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4315d417eb7958a05c7977d0ea6b1b4745e46725d02f23235173bbad2c73101d`  
		Last Modified: Wed, 12 Oct 2022 16:53:09 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c783713d738fc9dfff161ad3ff4369333cd0881466ab886feb09e6ef3508512e`  
		Last Modified: Wed, 12 Oct 2022 16:53:09 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05686fefb2145f84031cd9cae616dd90496d078df87f19c080931972eb700e7c`  
		Last Modified: Wed, 12 Oct 2022 16:53:09 GMT  
		Size: 67.2 KB (67186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab8462cae193737dba91e48900abf79d1b7234b48f337497ae0abfe9d8189e5`  
		Last Modified: Wed, 12 Oct 2022 16:53:07 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09370002ad510bcee1a28fb0f0b5165d64b0da0df7cb0fd2dd6f383d519ac6b3`  
		Last Modified: Thu, 13 Oct 2022 23:33:48 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a40bac9776410496b9708c98cb6ae27b2239aac39db149df26daea5038b81f`  
		Last Modified: Thu, 13 Oct 2022 23:34:06 GMT  
		Size: 192.0 MB (192021503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4068e1da9294951e35ddccd8846ac093e004cd5ec35c6000bd2f21edf6b9b7f7`  
		Last Modified: Thu, 13 Oct 2022 23:33:49 GMT  
		Size: 3.8 MB (3770979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9210eb20448d061fb24735bc8b361b24dd101191af787b4b3107bf239b395964`  
		Last Modified: Thu, 13 Oct 2022 23:33:48 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
