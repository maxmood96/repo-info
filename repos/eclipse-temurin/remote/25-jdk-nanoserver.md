## `eclipse-temurin:25-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:2c253e7a5bb127e8660add24e2ee23ed520999c115ed2fa0f3468188aa14cfcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `eclipse-temurin:25-jdk-nanoserver` - windows version 10.0.26100.32522; amd64

```console
$ docker pull eclipse-temurin@sha256:4c6a356bddaa505e3ba066a0a8c8356a08bf0f9a55ae6dd040db863f1c7d3ab8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.5 MB (337521771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33e8630024efbd0d8392b363c7dc0b107abf11caa8d4bd92e0ea38c9d441f16`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Mar 2026 01:45:55 GMT
RUN Apply image 10.0.26100.32522
# Tue, 10 Mar 2026 22:44:02 GMT
SHELL [cmd /s /c]
# Tue, 10 Mar 2026 22:44:02 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 10 Mar 2026 22:44:03 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 10 Mar 2026 22:44:03 GMT
USER ContainerAdministrator
# Tue, 10 Mar 2026 22:44:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Mar 2026 22:44:10 GMT
USER ContainerUser
# Tue, 10 Mar 2026 22:44:23 GMT
COPY dir:ebca1fed269853ebca056470dac79e7ebf8f2b759d9752408e0c7f2313fb3842 in C:\openjdk-25 
# Tue, 10 Mar 2026 22:44:30 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 10 Mar 2026 22:44:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:06fab7822816d5f43d6835d07ac8db280fdf81384187f36d8dc43bbb7064a76d`  
		Last Modified: Tue, 10 Mar 2026 20:41:46 GMT  
		Size: 199.4 MB (199409325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e61f5348397c570d7aecf06deb2ba50cb439efc28796c03eb9f795b6eeff59e`  
		Last Modified: Tue, 10 Mar 2026 22:44:36 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e795ce995bd1cf7b0cc7f9e6709ca98ee1124a889524c55807c6c98017e233`  
		Last Modified: Tue, 10 Mar 2026 22:44:36 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a1b63778efca2015c6e0fa76db779784bba3e28463ddf11c658c977b4217e1`  
		Last Modified: Tue, 10 Mar 2026 22:44:36 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab5a097615209dec52a7a213175c7b1c5a1210c570da731948bc79aa230370a`  
		Last Modified: Tue, 10 Mar 2026 22:44:36 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca8c42b91ab4a50196a56c61281d1fe903cfb52b87ff5de087b5c744deb93e5`  
		Last Modified: Tue, 10 Mar 2026 22:44:34 GMT  
		Size: 70.1 KB (70077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:422bafbc83ae717ad1779aced661f4380f6d62880d2b20b01a67dcdeb66803f1`  
		Last Modified: Tue, 10 Mar 2026 22:44:34 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e318251a8f05dddb4c6d7a11d1d2330f1aad10dc0f583e61460c9d4122c1dd`  
		Last Modified: Tue, 10 Mar 2026 22:44:47 GMT  
		Size: 137.9 MB (137932772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2555bf4180e018dfcb9f720283100111569886445ce7e9e99ea51b040e8c7a2`  
		Last Modified: Tue, 10 Mar 2026 22:44:34 GMT  
		Size: 103.2 KB (103188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9425ca258a3ac4071bf78c43bfb90715fc50d06ec4626166d0cb72fe082ec303`  
		Last Modified: Tue, 10 Mar 2026 22:44:34 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:25-jdk-nanoserver` - windows version 10.0.20348.4893; amd64

```console
$ docker pull eclipse-temurin@sha256:6f319724e447e5809ca4243f929c601333429fa525ca1d5f8fb8b43532011aba
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264784546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d205c1f2fba58b17d71bd29e7ad4fe557fab1b88e4910a85b9a6931173c40f4c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 22:36:30 GMT
SHELL [cmd /s /c]
# Tue, 10 Mar 2026 22:37:27 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 10 Mar 2026 22:37:27 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 10 Mar 2026 22:37:28 GMT
USER ContainerAdministrator
# Tue, 10 Mar 2026 22:37:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Mar 2026 22:37:29 GMT
USER ContainerUser
# Tue, 10 Mar 2026 22:37:36 GMT
COPY dir:ebca1fed269853ebca056470dac79e7ebf8f2b759d9752408e0c7f2313fb3842 in C:\openjdk-25 
# Tue, 10 Mar 2026 22:37:41 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 10 Mar 2026 22:37:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3193fa96cb5f59168e86269680a94e06b22fe26237dbd8daa994296244ce8a`  
		Last Modified: Tue, 10 Mar 2026 22:36:54 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf95d467770b86e1d32cbe8db63919d7d1efd17edec1f5e47041554b6b3b2bc`  
		Last Modified: Tue, 10 Mar 2026 22:37:47 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff8921ceddad1609c3263360e345ff634e078abcc4f144476d3aa0d8aaa87ef`  
		Last Modified: Tue, 10 Mar 2026 22:37:47 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67154e9caa7b6515cb8114be862c09bb1a0c8e8af0cba824965bbf5ea28112f`  
		Last Modified: Tue, 10 Mar 2026 22:37:47 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3a75d1cb6dee938a4607944382ccb6d7ece3b8fb0f215a2b8f4c4f02e5c075`  
		Last Modified: Tue, 10 Mar 2026 22:37:45 GMT  
		Size: 77.1 KB (77053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91f096d39232bf04efe38e57f5e0fa57bf15302b2808dd6cbb7cc00bebe7110`  
		Last Modified: Tue, 10 Mar 2026 22:37:45 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a14e1d6b2f17613f48bfe1867ba438abacc98a80d1e34a37da0fa32e472b7c`  
		Last Modified: Tue, 10 Mar 2026 22:37:58 GMT  
		Size: 137.9 MB (137932610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8343b9d6495023dac2f7a639146a1ad4750fde355e41d097b5613823b147b5c`  
		Last Modified: Tue, 10 Mar 2026 22:37:45 GMT  
		Size: 118.0 KB (117990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5a338c7dc05fbe80a50c8f894474b206349d196e1e2b4ed52f479b82da47a6`  
		Last Modified: Tue, 10 Mar 2026 22:37:45 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
