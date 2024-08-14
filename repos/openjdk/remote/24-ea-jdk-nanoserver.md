## `openjdk:24-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:3e00d1c946f3c00ae0e05082abb671281ed8cba2f89578a3fbb7062e5c69dfcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `openjdk:24-ea-jdk-nanoserver` - windows version 10.0.17763.6189; amd64

```console
$ docker pull openjdk@sha256:17bdab6bdcc2578ed0ae2ede2474c76c26f5547ddac2cb513520ccfb32eb5608
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.8 MB (365795742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047a97fe6005cb7e09a4f781dbb293f8f898787cfb4bdc642827ad57f2a08f74`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 21:11:44 GMT
SHELL [cmd /s /c]
# Tue, 13 Aug 2024 21:11:46 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 13 Aug 2024 21:11:47 GMT
USER ContainerAdministrator
# Tue, 13 Aug 2024 21:11:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 13 Aug 2024 21:11:49 GMT
USER ContainerUser
# Tue, 13 Aug 2024 21:11:50 GMT
ENV JAVA_VERSION=24-ea+10
# Tue, 13 Aug 2024 21:11:57 GMT
COPY dir:a0005413b1ff002c67299af627065453fb2f1c08570e500b2c608b78686ad9ab in C:\openjdk-24 
# Tue, 13 Aug 2024 21:12:02 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 13 Aug 2024 21:12:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0c9d9838f878d51759ad3ea158ac5f7db6ea83e2543c24ca82bd8f38cdfd61`  
		Last Modified: Tue, 13 Aug 2024 21:12:07 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3db8b2056c64f0bb9fe0dbeef230155b7e63868c98465a90affb93ed9364f1`  
		Last Modified: Tue, 13 Aug 2024 21:12:07 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0ca69fb7382d65c09322cbde7c889b5cf5b0893f413dac93e7bf0a1078c088`  
		Last Modified: Tue, 13 Aug 2024 21:12:07 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd3fb8a5aecd835ba4a76a0d81dadc37814faf57d08918def7ce06ed1c00a40`  
		Last Modified: Tue, 13 Aug 2024 21:12:07 GMT  
		Size: 74.7 KB (74654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1999958567abcc0038fea0763771a8ce44660142bfd21c25109623c983a974a`  
		Last Modified: Tue, 13 Aug 2024 21:12:06 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8a56e526277758ffcad8c99d3eb98e37ee00e559f60e2dbf356a31463bb292`  
		Last Modified: Tue, 13 Aug 2024 21:12:06 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc5350acf6190d41d3014d9348ff9d34a82b5309c3bdd5262a1436ec8f7577c`  
		Last Modified: Tue, 13 Aug 2024 21:12:17 GMT  
		Size: 206.5 MB (206548352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff10f0316e2c68a3313ff0ffb8fdd0019e756af24ff9eec28ddfe38fd1ee674`  
		Last Modified: Tue, 13 Aug 2024 21:12:06 GMT  
		Size: 4.1 MB (4083357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ae09c45f2860bf22c90fb12bd65d4cf23c1cb113c7cdf71d124fc7efaa6590`  
		Last Modified: Tue, 13 Aug 2024 21:12:06 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
