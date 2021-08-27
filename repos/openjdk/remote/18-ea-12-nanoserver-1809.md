## `openjdk:18-ea-12-nanoserver-1809`

```console
$ docker pull openjdk@sha256:da1331364359132137cc1932f47683386474b5da7d933382b4c81a03f2e25f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `openjdk:18-ea-12-nanoserver-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull openjdk@sha256:834f51f32181d78f06da855d73eac538cc22326653cb34c5e1ed033339915795
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289052776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314ad5c42ea445b02cbba5cfe6f7cba231a5a342f8a80ba1d6ecae6ee8a2dc92`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Aug 2021 19:15:20 GMT
RUN Apply image 1809-amd64
# Wed, 25 Aug 2021 16:34:07 GMT
SHELL [cmd /s /c]
# Wed, 25 Aug 2021 17:06:45 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 25 Aug 2021 17:06:46 GMT
USER ContainerAdministrator
# Wed, 25 Aug 2021 17:06:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 25 Aug 2021 17:06:55 GMT
USER ContainerUser
# Fri, 27 Aug 2021 17:47:46 GMT
ENV JAVA_VERSION=18-ea+12
# Fri, 27 Aug 2021 17:48:01 GMT
COPY dir:62a53954ec767af424e4183414590327f82439f40b0a1a10bd3e0e8f4a92e7c0 in C:\openjdk-18 
# Fri, 27 Aug 2021 17:48:24 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 27 Aug 2021 17:48:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bc8517709e9cfff223cb034ff5be8fcbfa5409de286cdac9ae1b8878ebea6b84`  
		Size: 102.7 MB (102741177 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9191bd6656c8ea186f621f667fb09a30387fae304b3e7817fd7e8258c022d185`  
		Last Modified: Wed, 25 Aug 2021 23:21:14 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529f54617b19374dc6ae56b7cbadea820f6613c38ef8eb5b3780625f824e7f70`  
		Last Modified: Thu, 26 Aug 2021 00:39:57 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17928612bd587dae3533403ae499232eb58f410a5e0875cca4930241ef47caa3`  
		Last Modified: Thu, 26 Aug 2021 00:39:56 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6b2868a6eab69d3ff3c1ab6e50f537ef7b5671cd3a888b7fa6fcc521e63759`  
		Last Modified: Thu, 26 Aug 2021 00:39:56 GMT  
		Size: 71.1 KB (71120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1f7631bcd8fcfd1b84d19c43b45e42f54be2bafdb008157e4d2e8d7a64430a`  
		Last Modified: Thu, 26 Aug 2021 00:39:53 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513ee7ba393d5258cb07f33e14d4c169df8f9215835e8667cd94c7d6d849ea0b`  
		Last Modified: Fri, 27 Aug 2021 17:56:44 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ec4650e21f8698d302cad4baed35d5f43e8be1ef3724fc3938c5ccc43056a9`  
		Last Modified: Fri, 27 Aug 2021 17:57:00 GMT  
		Size: 182.6 MB (182626399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ade06fc85fa521c7bda4889cc404fddd653e9728518fc03458e94c65d57836`  
		Last Modified: Fri, 27 Aug 2021 17:56:45 GMT  
		Size: 3.6 MB (3607282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567657427b1ab2bd93122dbd9fd7fefa32c1d68439711abbbe6b7ef27886b5ef`  
		Last Modified: Fri, 27 Aug 2021 17:56:44 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
