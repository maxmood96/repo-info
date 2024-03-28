## `eclipse-temurin:22_36-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:839831d60ae796bd3086f7f0623f052ee9b4fbfc8888ce13159d92b5d17a3e8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `eclipse-temurin:22_36-jdk-nanoserver` - windows version 10.0.20348.2340; amd64

```console
$ docker pull eclipse-temurin@sha256:cb2f5469770278bb90b85c6850ebce2c55fcaa6f46e34bf9b7f7dc1d56aece05
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320887176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4565298a94babc314f79d1347e1e028d59327ac10d7cdd66067851fff805baf3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 05 Mar 2024 19:20:30 GMT
RUN Apply image 10.0.20348.2340
# Wed, 13 Mar 2024 01:20:55 GMT
SHELL [cmd /s /c]
# Thu, 28 Mar 2024 01:33:01 GMT
ENV JAVA_VERSION=jdk-22+36
# Thu, 28 Mar 2024 01:33:01 GMT
ENV JAVA_HOME=C:\openjdk-22
# Thu, 28 Mar 2024 01:33:02 GMT
USER ContainerAdministrator
# Thu, 28 Mar 2024 01:33:24 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 28 Mar 2024 01:33:25 GMT
USER ContainerUser
# Thu, 28 Mar 2024 01:33:40 GMT
COPY dir:50e69279b8e7c7c9492973898e59a003d16331dced94fbda5fe70c6e2f10acc9 in C:\openjdk-22 
# Thu, 28 Mar 2024 01:33:54 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Mar 2024 01:33:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:94ec3b200bababb5c0b6605ad82c23779d8f918fbfe1ef5d1cf51be6f12fa749`  
		Last Modified: Tue, 12 Mar 2024 19:42:37 GMT  
		Size: 120.7 MB (120702694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e98336f720b829e374bd1d59306210d3700861b11d3df51506afbc0b50d039`  
		Last Modified: Wed, 13 Mar 2024 01:40:26 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cae91a355f117e36f8601eb8bbecd3204be41a74eb3c060e221d3473c7fc480`  
		Last Modified: Thu, 28 Mar 2024 01:40:26 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:701197661d7d6b1888ca71f6fdbe3a8dba48b4a4520819924d7a2ac894746350`  
		Last Modified: Thu, 28 Mar 2024 01:40:26 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27eec842d09161a6d90b7bfecb4bd349fd3e5786ad48ffce9234936523fc3f46`  
		Last Modified: Thu, 28 Mar 2024 01:40:26 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef885139e5bbccead0be23fca4419f1cf65a5779b37207ce1767e6ff73821e4a`  
		Last Modified: Thu, 28 Mar 2024 01:40:24 GMT  
		Size: 78.3 KB (78256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747f96e45555c2291908aea8e63c4e52c087a3e6862a8152ca3f63664fc70909`  
		Last Modified: Thu, 28 Mar 2024 01:40:24 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13be9a7e2c07ef465d8f4bb7ac9d2848cef30b998e4d8ce87797abd5b89b801e`  
		Last Modified: Thu, 28 Mar 2024 01:40:43 GMT  
		Size: 200.0 MB (200037890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3dd4cd9d59e536e9f59dbf1d23dd5a99e7bc97da6e95c281faaf2644a5c2e6`  
		Last Modified: Thu, 28 Mar 2024 01:40:24 GMT  
		Size: 61.4 KB (61420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfbab86d86a7a64b77c508f9d1cf5eb9b3c3d30dbb90afd83976fbc0884b755`  
		Last Modified: Thu, 28 Mar 2024 01:40:24 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22_36-jdk-nanoserver` - windows version 10.0.17763.5576; amd64

```console
$ docker pull eclipse-temurin@sha256:6673911172dfa7619215b08bc32820fe1a4f5266f5ecac862f393fd06938159a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308567012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300eea1626425d8ac83da99ba35aae5427612f123b968c7aa7cc759fc24c33c6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 00:41:38 GMT
SHELL [cmd /s /c]
# Thu, 28 Mar 2024 01:25:00 GMT
ENV JAVA_VERSION=jdk-22+36
# Thu, 28 Mar 2024 01:25:01 GMT
ENV JAVA_HOME=C:\openjdk-22
# Thu, 28 Mar 2024 01:25:01 GMT
USER ContainerAdministrator
# Thu, 28 Mar 2024 01:25:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 28 Mar 2024 01:25:21 GMT
USER ContainerUser
# Thu, 28 Mar 2024 01:25:36 GMT
COPY dir:50e69279b8e7c7c9492973898e59a003d16331dced94fbda5fe70c6e2f10acc9 in C:\openjdk-22 
# Thu, 28 Mar 2024 01:25:48 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Mar 2024 01:25:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9569a24b1d9b596a48436098ac5fe49c52e3153cd3bd147e365a80a4059570fd`  
		Last Modified: Wed, 13 Mar 2024 01:31:07 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57cb9c24ea67642372d52c48fd29ea184f577c493da96e7582cb21988f552c86`  
		Last Modified: Thu, 28 Mar 2024 01:38:49 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9c0feed8d9a7949e6c0a11940c910c82470fee50ac0f29eef348b61f48b260`  
		Last Modified: Thu, 28 Mar 2024 01:38:49 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c45826021dd09b48f82f606aacc2162cda51c6c39996b3af9982654d63888a6`  
		Last Modified: Thu, 28 Mar 2024 01:38:48 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3277bafd8f072d26debee2e8da6934103c9058785ea67a0a27363fd519cb1f7`  
		Last Modified: Thu, 28 Mar 2024 01:38:47 GMT  
		Size: 67.8 KB (67769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65288dd7c5e5daed3e41f2428a4d2b9a964f365e3c0ec0ebd0615e95ad3141e5`  
		Last Modified: Thu, 28 Mar 2024 01:38:46 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be3138027ba1de33679499cf13a30c267e6be61aeafd41396fcc2be7bf091f7`  
		Last Modified: Thu, 28 Mar 2024 01:39:06 GMT  
		Size: 200.0 MB (200037860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bf1ee16d11fcab241f4a2baa17b1fec5d3f1e31ec4d1f30890b7590fb20b73`  
		Last Modified: Thu, 28 Mar 2024 01:38:48 GMT  
		Size: 3.8 MB (3834282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d34e3af8cfeb00e3b4202e47809cfe7f157266206023834b8ffa4be8bd7a1e`  
		Last Modified: Thu, 28 Mar 2024 01:38:47 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
