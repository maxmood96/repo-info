## `openjdk:27-ea-4-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:8f5293fdb6e96156afff8ecf27f654da97e2094cb9c48ccad6734476d098b518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `openjdk:27-ea-4-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

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
