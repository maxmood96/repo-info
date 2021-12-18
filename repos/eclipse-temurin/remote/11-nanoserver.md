## `eclipse-temurin:11-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:51b2d0e836e109e881a6826aaca8c6c44fc5c649563a3cb734383707ccbea76c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.405; amd64
	-	windows version 10.0.17763.2366; amd64

### `eclipse-temurin:11-nanoserver` - windows version 10.0.20348.405; amd64

```console
$ docker pull eclipse-temurin@sha256:1b3eb1a0771a1e8e0a291b9a3feb27fa803ac611b29463963fb9cce3754c4d97
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.3 MB (309302313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d6370456c33cb925e19f62ef1ec072bf7de93c041d6fb2ddd974f358738826`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 08 Dec 2021 01:24:33 GMT
RUN Apply image ltsc2022-amd64
# Sat, 18 Dec 2021 06:03:19 GMT
SHELL [cmd /s /c]
# Sat, 18 Dec 2021 06:04:34 GMT
ENV JAVA_VERSION=jdk-11.0.13+8
# Sat, 18 Dec 2021 06:04:35 GMT
ENV JAVA_HOME=C:\openjdk-11
# Sat, 18 Dec 2021 06:04:36 GMT
USER ContainerAdministrator
# Sat, 18 Dec 2021 06:04:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 18 Dec 2021 06:04:47 GMT
USER ContainerUser
# Sat, 18 Dec 2021 06:05:04 GMT
COPY dir:7549fd743977f7762910679960e9adfeab116385590a40bc0f1570100fce1af1 in C:\openjdk-11 
# Sat, 18 Dec 2021 06:05:18 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 18 Dec 2021 06:05:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:11961e4f2e13a442b572d4bc37edfe94ad6d8c2ed378f0dcae8b880959c4b538`  
		Size: 117.2 MB (117225770 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:29e118c52df9d671b57a04fe35f79f686c3a7038ccd41c5bf5ccfac737426ab6`  
		Last Modified: Sat, 18 Dec 2021 06:41:30 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a320057b343ea00665b5cb184e4c16c5aec5b221aef873939a31147d252a6086`  
		Last Modified: Sat, 18 Dec 2021 06:44:22 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa0a5b157043b7b6ac12e2fdaa2719960e8712f75db77e77cf2e919b94d77f6`  
		Last Modified: Sat, 18 Dec 2021 06:44:22 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f21f2bf08c9f1a1b07f02cb5f65706fe0d5a19f2b2575ba45392f1a39c9660`  
		Last Modified: Sat, 18 Dec 2021 06:44:22 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c018880232738639a467b720807d128ab4229e32e9ca8edbd573557b88a26d`  
		Last Modified: Sat, 18 Dec 2021 06:44:20 GMT  
		Size: 86.6 KB (86586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e096968802455bd77ec825c0461c2b9dfad40f7de7690dddc03066bf12750c5c`  
		Last Modified: Sat, 18 Dec 2021 06:44:20 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa86d98fdec03694d9f93c19ee9d0a7a87857db4ecfc1882af1aa31eea80489`  
		Last Modified: Sat, 18 Dec 2021 06:47:50 GMT  
		Size: 191.9 MB (191923813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7906fef8df160edb8f7b2051bfe3f782fa62c4137f8b782c1d2fbd5ddca42e`  
		Last Modified: Sat, 18 Dec 2021 06:44:20 GMT  
		Size: 59.2 KB (59219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ecf75a08298040106aa1449b9ece1e34d46bf93ce453f88ef880231c707b70e`  
		Last Modified: Sat, 18 Dec 2021 06:44:20 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-nanoserver` - windows version 10.0.17763.2366; amd64

```console
$ docker pull eclipse-temurin@sha256:e4cdddbbb2040208d90f93eeddd4447e14098468665a16bd43725a0cc6453822
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.0 MB (294984633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1408c45781ff10bef78ce67253942c5b5bfadd374a674e17892332ff69eacd7c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 07 Dec 2021 04:37:11 GMT
RUN Apply image 1809-amd64
# Sat, 18 Dec 2021 05:18:44 GMT
SHELL [cmd /s /c]
# Sat, 18 Dec 2021 05:35:01 GMT
ENV JAVA_VERSION=jdk-11.0.13+8
# Sat, 18 Dec 2021 05:35:02 GMT
ENV JAVA_HOME=C:\openjdk-11
# Sat, 18 Dec 2021 05:35:02 GMT
USER ContainerAdministrator
# Sat, 18 Dec 2021 05:35:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 18 Dec 2021 05:35:15 GMT
USER ContainerUser
# Sat, 18 Dec 2021 05:35:34 GMT
COPY dir:7549fd743977f7762910679960e9adfeab116385590a40bc0f1570100fce1af1 in C:\openjdk-11 
# Sat, 18 Dec 2021 05:35:55 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 18 Dec 2021 05:35:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:034b2f457cdf6a0d3f7024523d40fd6eeb8568e6c76d9fa56f4053fcf3a21d63`  
		Size: 102.9 MB (102904001 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4c557aac927613dd487d7c04b01a8eeb8ad174693f61b14c8f4285f1db6afdd2`  
		Last Modified: Sat, 18 Dec 2021 06:13:05 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35fa60c368d5bb9faa3ad271daca3b9a6fe74a9b5e70d653bc6d67ad3450f552`  
		Last Modified: Sat, 18 Dec 2021 06:16:33 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9255e05ef5fec9b6cd7ad18f075a54f693830ba74909a117138108f53defa97d`  
		Last Modified: Sat, 18 Dec 2021 06:16:33 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bf074477c9367c74d409e04f2b827675a3880bb0ef74271edad2042c0c749e`  
		Last Modified: Sat, 18 Dec 2021 06:16:33 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee8be34dd79508052db04b5a53af01efbafe32cb6a4d8abe7994b6a70e79481`  
		Last Modified: Sat, 18 Dec 2021 06:16:31 GMT  
		Size: 68.8 KB (68848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:488890323943c28acb7a2561bcac21b1d1073598007b7205947af2336ce64d77`  
		Last Modified: Sat, 18 Dec 2021 06:16:31 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6bffc3c0ff96966ce94f8551b64b7a105ba49bddc7f3fe8b4b030b1ffb9ade`  
		Last Modified: Sat, 18 Dec 2021 06:19:53 GMT  
		Size: 191.9 MB (191923752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b231b4a7a082270a1e2f2ecd1375704fc89f7493d9c436b7824ff50b8b27e2`  
		Last Modified: Sat, 18 Dec 2021 06:16:31 GMT  
		Size: 81.1 KB (81069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ed86430465395e6cb6bf61a3f05a64445b01c7b716a3b93d1dab698f9bdef6`  
		Last Modified: Sat, 18 Dec 2021 06:16:31 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
