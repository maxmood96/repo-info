## `eclipse-temurin:21-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:7bed751958d63ad7375fd476a8fe9a15d507f71b2bd7aaf8a480b1ecf0081d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `eclipse-temurin:21-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull eclipse-temurin@sha256:83ce83dbe16f1b6d8cd67c1826585a5ce8bb8587df24269a8916584584e7ee86
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.2 MB (393173771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b71283df01bfa9e08b7a239fe7137ed5d2902199846b94fb73b30288187eeb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 10 May 2025 00:58:48 GMT
RUN Apply image 10.0.26100.4061
# Wed, 14 May 2025 21:15:08 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 21:15:09 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 14 May 2025 21:15:10 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 14 May 2025 21:15:11 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:15:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 May 2025 21:15:16 GMT
USER ContainerUser
# Wed, 14 May 2025 21:15:24 GMT
COPY dir:db067bfbcc086396d5dfa4ac3979b5c2114a2c9ec3e102fbc339048e5a829713 in C:\openjdk-21 
# Wed, 14 May 2025 21:15:32 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 14 May 2025 21:15:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9824510349be04d2eb26f9aaba1d016eddcbed10bdcd6681f4636c948766f3d1`  
		Last Modified: Thu, 15 May 2025 20:15:30 GMT  
		Size: 191.4 MB (191412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d80b3ab37f84ec4b7e49b0056ae7b344ba596f20fd570017239a171fec3f5662`  
		Last Modified: Sun, 18 May 2025 20:41:50 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c52c19c478999018bdc5ed0b17786279f6bcd5163208e883fd77db0f6b6a39`  
		Last Modified: Sun, 18 May 2025 20:41:51 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8ef803edee4167948cbaa4cf3da1f8041f1f47781bde330155363118c99ca3`  
		Last Modified: Sun, 18 May 2025 20:41:51 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805637da0349f58ccd456e8dca6f762546bfb0001b72e835b7130846055a491c`  
		Last Modified: Sun, 18 May 2025 20:41:51 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa61e9658aff336acf2fced38dec976fc2d386897e7903af8ba516af9f43b73c`  
		Last Modified: Sun, 18 May 2025 20:41:52 GMT  
		Size: 77.0 KB (77003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e380753aadfb6b1319a7ae7cba16542424f4eec32bc63c648d6fca54b70bfc`  
		Last Modified: Sun, 18 May 2025 20:41:52 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438edec0dbb745aa3abc9dbbfb27153bcd06dd887d8e03c30c9a9ac06e939313`  
		Last Modified: Sun, 18 May 2025 20:42:09 GMT  
		Size: 201.6 MB (201552701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45ac93940f71be420b518a9685de75c302d8edd268fc29acdb902058a52c2ae`  
		Last Modified: Sun, 18 May 2025 20:41:52 GMT  
		Size: 125.8 KB (125757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76289798cc5049a76ee10abbfd45272814d2ffef79e92ac5e7eee7b4d7d8349`  
		Last Modified: Sun, 18 May 2025 20:41:53 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
