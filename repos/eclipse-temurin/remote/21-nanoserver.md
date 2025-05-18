## `eclipse-temurin:21-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:40984af9a6ff63c2e55edbad1a725930c36b99426174e6c2f961075699d78949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64

### `eclipse-temurin:21-nanoserver` - windows version 10.0.26100.4061; amd64

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

### `eclipse-temurin:21-nanoserver` - windows version 10.0.20348.3692; amd64

```console
$ docker pull eclipse-temurin@sha256:a22fb75d041de441bd87249772e758a3aca9a1105673974f2ba05c81bf7bc36c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.3 MB (324317634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e29ff9d0d7ec0e94ab1a8a358e8106a079cd79a9d74c142fe6bcb7eb74063e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Wed, 14 May 2025 21:21:02 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 21:21:03 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 14 May 2025 21:21:03 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 14 May 2025 21:21:04 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:21:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 May 2025 21:21:08 GMT
USER ContainerUser
# Wed, 14 May 2025 21:21:15 GMT
COPY dir:db067bfbcc086396d5dfa4ac3979b5c2114a2c9ec3e102fbc339048e5a829713 in C:\openjdk-21 
# Wed, 14 May 2025 21:21:22 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 14 May 2025 21:21:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bedd84aee1625a6fb286eb4e52210c28051c7da71ad8043503a85dc0b76ff7`  
		Last Modified: Fri, 16 May 2025 14:05:37 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9069cab3dd72f7a589ff52d4d5d034eab7ab4218ebae88795d6354eee1fc39f`  
		Last Modified: Fri, 16 May 2025 14:05:37 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021a07171e30786c2115302d21eea6874a7325b355abc6e27bee82472d2cd1d4`  
		Last Modified: Fri, 16 May 2025 14:05:38 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b7e1372e1ed8cb1a5311ff77b9da6aa02ee61ee915dc47e8c0b41bc9ba7614`  
		Last Modified: Fri, 16 May 2025 14:05:38 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265ba4748a0bfcaa6ba75646972f3e55a9f293f052de118ca532d183bf398be4`  
		Last Modified: Fri, 16 May 2025 14:05:38 GMT  
		Size: 76.2 KB (76205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2862f20c7c4beb93c2a2641e1e03b93a12880d55903f55dcb17f79924c8f48ea`  
		Last Modified: Fri, 16 May 2025 14:05:38 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2feea30433009b6149a96ad3d74d799d4038e2f410511a13ec700630d6190be5`  
		Last Modified: Fri, 16 May 2025 14:05:48 GMT  
		Size: 201.6 MB (201551242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577e9a7fc2afbf0b72361e52e984e7cb1fb88ef0feb1b508f43cda164513e88b`  
		Last Modified: Fri, 16 May 2025 14:05:38 GMT  
		Size: 107.4 KB (107386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132d8eab90b4863b8a3bfe3513a8d969e6b952fc2c40330b28fe231b60774777`  
		Last Modified: Fri, 16 May 2025 14:05:38 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
