## `eclipse-temurin:11-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:9442eaa382579d7c1a76dc2b0fe459691bfb72f94628986f4ab6083f58ce83da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.405; amd64

### `eclipse-temurin:11-nanoserver-ltsc2022` - windows version 10.0.20348.405; amd64

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
