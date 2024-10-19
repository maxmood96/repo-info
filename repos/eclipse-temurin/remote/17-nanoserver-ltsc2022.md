## `eclipse-temurin:17-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:1527ebc80653d925c4f04317f6e79fc3e958f6d2cfbbbd448080b1b123f438e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `eclipse-temurin:17-nanoserver-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:2e0f09bfd9fa0ae305d627019184f0a07afea39c6a3cf0950513db6e620b968b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307120398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02355cd03e76f50ad4efae2355bfadee83defde1349632a643ac3f4c50bbb24c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Sat, 19 Oct 2024 02:16:00 GMT
SHELL [cmd /s /c]
# Sat, 19 Oct 2024 02:16:00 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Sat, 19 Oct 2024 02:16:01 GMT
ENV JAVA_HOME=C:\openjdk-17
# Sat, 19 Oct 2024 02:16:02 GMT
USER ContainerAdministrator
# Sat, 19 Oct 2024 02:16:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 19 Oct 2024 02:16:04 GMT
USER ContainerUser
# Sat, 19 Oct 2024 02:16:10 GMT
COPY dir:90bd01c2ed4c0253f6ac9cf5667f45dc63e1de5f60f2ba53c8784cd5f813ea62 in C:\openjdk-17 
# Sat, 19 Oct 2024 02:16:16 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 19 Oct 2024 02:16:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9879ba4a5eae57d2c44af47978586bb4cf87ea5dd9ffb6def0ee7ae34b4bd164`  
		Last Modified: Sat, 19 Oct 2024 02:16:21 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2467c22d9157b976fd454fc988cb9a4c4b09e25cebc3f8ba8cc6549a4a5940`  
		Last Modified: Sat, 19 Oct 2024 02:16:21 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6acf0630ef26554876055752afeddd5d771a5e5e21431e4c41fd0fcc130f30`  
		Last Modified: Sat, 19 Oct 2024 02:16:20 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133f05a7831fba5b26f0e83e4e71cbc35c12d17ab5ca87d0ffa68e15b47a39b3`  
		Last Modified: Sat, 19 Oct 2024 02:16:20 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb1b37c478be681cc1d9c00757e99622fc9c6a14d452685a3b8bf8c3d8eda3c`  
		Last Modified: Sat, 19 Oct 2024 02:16:19 GMT  
		Size: 77.0 KB (77017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c31635c300a5e0bf75206f5694416ccd92c53381022cb8f8435189d4b6e17f6`  
		Last Modified: Sat, 19 Oct 2024 02:16:19 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728695cb21ab8644ab9f7907b4a4f8bc99bd2344a1670289504fb6f6881b743b`  
		Last Modified: Sat, 19 Oct 2024 02:16:29 GMT  
		Size: 186.4 MB (186419009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ed815b0023ff3f1ca8a74e93609873a1f7273848096287c5d11037997c1699`  
		Last Modified: Sat, 19 Oct 2024 02:16:20 GMT  
		Size: 107.1 KB (107149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3d2772d116b31c7af91be88ea66e7e9b498b9a1c79cc620a751d5be94d6c13`  
		Last Modified: Sat, 19 Oct 2024 02:16:19 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
