## `openjdk:27-ea-4-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:01cef57ef16a37bd4361c286101854bcaa85cef6ae880a7f4ffeb0899bd23c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `openjdk:27-ea-4-jdk-nanoserver` - windows version 10.0.26100.32230; amd64

```console
$ docker pull openjdk@sha256:9310d667c82c5e908769f1a9c3a8e13f0829da6e3e6b881d968dcf2bdfd9b05a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.2 MB (423178025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7420c5b3487194b43fb3ced9bcd5d0a64c5c7efd9fcbb67b2a46e19e4296a5f4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 23:38:54 GMT
SHELL [cmd /s /c]
# Tue, 13 Jan 2026 23:41:14 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 13 Jan 2026 23:41:15 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:41:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 13 Jan 2026 23:41:17 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:41:17 GMT
ENV JAVA_VERSION=27-ea+4
# Tue, 13 Jan 2026 23:41:29 GMT
COPY dir:55417311536b64386669c9f543375752cfd39486cb0c7d8403a74e4cd382a3c4 in C:\openjdk-27 
# Tue, 13 Jan 2026 23:41:34 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 13 Jan 2026 23:41:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c3018f35c73af59a36350615c430cd199174009bb767471c37deb2372b9478`  
		Last Modified: Tue, 13 Jan 2026 23:40:03 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b920187cb8760844464774283ff95fcf01301f7e3cc842892daeb2624b47ca27`  
		Last Modified: Tue, 13 Jan 2026 23:42:01 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691147dfcbe8301285335d769a1c70061cceb5574c03d46c3ab767f5d498c941`  
		Last Modified: Tue, 13 Jan 2026 23:42:01 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958751a94a73dd3a4d8731f93cff6e654960d10ac00c51cacab3e4be530a81ca`  
		Last Modified: Tue, 13 Jan 2026 23:42:01 GMT  
		Size: 72.2 KB (72199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a88b91c95110895ef47b5b5357ba8138bb4ee2571fcefa1d0d038ce1823db0f`  
		Last Modified: Tue, 13 Jan 2026 23:41:39 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66729df7c3e3821bbc23c376a0cd578d423f364fbfd31b86e39c18a743fb3fb2`  
		Last Modified: Tue, 13 Jan 2026 23:42:01 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71385906499c269e4caa262136395ae2b9e4d9262aa199914f1c8d2ff4ae80ac`  
		Last Modified: Tue, 13 Jan 2026 23:41:53 GMT  
		Size: 223.9 MB (223909637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb166faacfb089411f8bbd22ff901598b1763d3841af642a03c1b1865156344`  
		Last Modified: Tue, 13 Jan 2026 23:41:39 GMT  
		Size: 113.2 KB (113202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb46690aadd5cf416cde10a120b43794dd313c6f1206a1af27bd326a07537fa`  
		Last Modified: Tue, 13 Jan 2026 23:42:01 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-4-jdk-nanoserver` - windows version 10.0.20348.4648; amd64

```console
$ docker pull openjdk@sha256:b2288e1ca3c8d3296fd2c7b6b7a7ac2703bc6e2d3ed08388ddb98d735c6555ab
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.8 MB (350797607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6808af0cf439b6e5d28f2cb75f013f26748545851594ed2b97ff5782bdfcb30`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Tue, 13 Jan 2026 23:34:00 GMT
SHELL [cmd /s /c]
# Tue, 13 Jan 2026 23:38:00 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 13 Jan 2026 23:38:01 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:38:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 13 Jan 2026 23:38:03 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:38:03 GMT
ENV JAVA_VERSION=27-ea+4
# Tue, 13 Jan 2026 23:38:13 GMT
COPY dir:55417311536b64386669c9f543375752cfd39486cb0c7d8403a74e4cd382a3c4 in C:\openjdk-27 
# Tue, 13 Jan 2026 23:38:17 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 13 Jan 2026 23:38:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:12:21 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc58112f1d1d638f65a75c8bcdb844fc8acda257ce27f49b05ca59ae6852b63`  
		Last Modified: Tue, 13 Jan 2026 23:34:26 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa03b16520aea2fa8eb29c31534a0c08d1c8067728eaa17345b748e7bbb65695`  
		Last Modified: Tue, 13 Jan 2026 23:38:47 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b8813b4bdc60f023a6e919a3b78482397e49ee81051787d63f7f26223bd913`  
		Last Modified: Tue, 13 Jan 2026 23:38:47 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5285190dc88e56daaeef5b0754bea2797618c2840cf70c414fcc6b505a05f1`  
		Last Modified: Tue, 13 Jan 2026 23:38:47 GMT  
		Size: 77.5 KB (77475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb2b17ded86de039fb4db92f289ddcd5a067b3c53057ec23fc2816267300697`  
		Last Modified: Tue, 13 Jan 2026 23:38:47 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6715b1cb11bc90a591c5c5ffde7b7178ac04deea5054857166a0ab6d3648d32e`  
		Last Modified: Tue, 13 Jan 2026 23:38:47 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cac925a220fcdb32368a407f2ad4f75c21a9179448c3853da622bf80bc42d6`  
		Last Modified: Tue, 13 Jan 2026 23:38:38 GMT  
		Size: 223.9 MB (223909749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2891f29e715372b12f3b3cf1617726414c3187231726b2ff67357ff8d635ca`  
		Last Modified: Tue, 13 Jan 2026 23:38:22 GMT  
		Size: 107.2 KB (107190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e03fb3d053cd1e2e1948eb001c10b43260f1c243077527b1bf8529135517240`  
		Last Modified: Tue, 13 Jan 2026 23:38:47 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
