## `openjdk:24-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:35dc3f5f00c4bcd5f8fe87a17698a348e5bd4d10dbfde0858a8ac2131d93f6a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `openjdk:24-jdk-nanoserver` - windows version 10.0.17763.6532; amd64

```console
$ docker pull openjdk@sha256:a005b4f929327550c41fa6d28898b455e84387550d16c04e487916f263920f82
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.3 MB (369289234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd271142c17494f21993834867d288a59c69fe8ab39011827994afdb0eff71b5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Thu, 14 Nov 2024 21:11:28 GMT
SHELL [cmd /s /c]
# Thu, 14 Nov 2024 21:11:29 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 14 Nov 2024 21:11:29 GMT
USER ContainerAdministrator
# Thu, 14 Nov 2024 21:11:31 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 14 Nov 2024 21:11:31 GMT
USER ContainerUser
# Thu, 14 Nov 2024 21:11:32 GMT
ENV JAVA_VERSION=24-ea+23
# Thu, 14 Nov 2024 21:11:39 GMT
COPY dir:7e2236fae53de415a6b985bfcada000d61dbc6a40126a0107213015de3141463 in C:\openjdk-24 
# Thu, 14 Nov 2024 21:11:44 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 14 Nov 2024 21:11:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1db75926f60208ee5964ab54e7173ddf22fc303fd4409a97541ba3b54a2c6f`  
		Last Modified: Thu, 14 Nov 2024 21:11:51 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20368b0d1805563849d5b6f8dabeac3aeaebfd31e0298e15ef0b5c655fa48c4`  
		Last Modified: Thu, 14 Nov 2024 21:11:50 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6240505a2f2de826f70f22901f57357b37cc11925e6727167f2ecc515e82e82`  
		Last Modified: Thu, 14 Nov 2024 21:11:50 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10aa0dde6486849a8d6ca75adb324df34e0c535cc5489ec6caf7cb2cbb36eb12`  
		Last Modified: Thu, 14 Nov 2024 21:11:50 GMT  
		Size: 74.1 KB (74113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1e9b887ba0e0ff1a4f16ba3ce958b3801914e358f999550e4383c8df6579d1`  
		Last Modified: Thu, 14 Nov 2024 21:11:48 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:867aadfa2581f7014fdee2d42177cdf85084bb24c12fd5a660e0b28986f4ecf5`  
		Last Modified: Thu, 14 Nov 2024 21:11:48 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6571b1d2f889e60696eed2ad97b2b5dd255b3667eb7ecbf6a4fb29a17fcfb6`  
		Last Modified: Thu, 14 Nov 2024 21:12:00 GMT  
		Size: 209.3 MB (209325251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2d605f5b76c7b37c3e43deb11c9409bfbd54b623790650aa3391d5c33058090`  
		Last Modified: Thu, 14 Nov 2024 21:11:49 GMT  
		Size: 4.7 MB (4669407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbb42400deb67fc50728d62665c3996e7dddfc15764ace9968175a5618f8922`  
		Last Modified: Thu, 14 Nov 2024 21:11:48 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
