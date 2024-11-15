## `eclipse-temurin:8u432-b06-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:b061675014c9a6c90857ef535ed8d87f86ed2ba2cc1419f167cc50848972609d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `eclipse-temurin:8u432-b06-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull eclipse-temurin@sha256:e10099610a103b2721942f6e967837c4f600a325b61b8aa0934d26f2e8827743
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.8 MB (161848805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c456c2206a3157967972bd2488e928e88e98d03f554d7a5b9c47860e657b4d6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 02 Nov 2024 23:34:35 GMT
RUN Apply image 10.0.20348.2849
# Thu, 14 Nov 2024 21:18:38 GMT
SHELL [cmd /s /c]
# Thu, 14 Nov 2024 21:18:39 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 14 Nov 2024 21:18:39 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 14 Nov 2024 21:18:40 GMT
USER ContainerAdministrator
# Thu, 14 Nov 2024 21:18:42 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 14 Nov 2024 21:18:43 GMT
USER ContainerUser
# Thu, 14 Nov 2024 21:18:45 GMT
COPY dir:47bf2d2ef237403b98ba2f50909368ef2c147e2a609dd71db23cc690a276ad54 in C:\openjdk-8 
# Thu, 14 Nov 2024 21:18:48 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:815d6b7f925aef8327c34c34073ae54cc1c82120f1058682eac4c8c14ca21c70`  
		Last Modified: Tue, 12 Nov 2024 22:44:32 GMT  
		Size: 120.6 MB (120604951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f5c135be763e5ed04d4cd012b052a154fef9032ee0e338132c1b702287efcc`  
		Last Modified: Thu, 14 Nov 2024 21:18:54 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b38ba156726859099e63b3cd2abfdaa8128b2c6337c5cb1c315a22042db522`  
		Last Modified: Thu, 14 Nov 2024 21:18:54 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3e747f0b190de91f60614cdb2ad982f45ffd18ed104c05be85b124e2dede9b`  
		Last Modified: Thu, 14 Nov 2024 21:18:53 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d01d2a46372e643d92d1a62fb1efcdf8ae43cdf387f749dc1aefd2148e58b98`  
		Last Modified: Thu, 14 Nov 2024 21:18:52 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1148e5e149f399879f1cc996c5d0c0785583d4c2d7166129168abee497b73b5d`  
		Last Modified: Thu, 14 Nov 2024 21:18:52 GMT  
		Size: 76.7 KB (76661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d99f31f1f561edde797d6ffaae4f4de0bd2491e4370b616be54cecc4822812b`  
		Last Modified: Thu, 14 Nov 2024 21:18:52 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77322e160804f61856645a43718fdf1f2c5eaa9a239a7cd312bd143c274a54e7`  
		Last Modified: Thu, 14 Nov 2024 21:18:55 GMT  
		Size: 41.1 MB (41061137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb17ec6aa2b01b2e523b85baa4c176cf5119a159917e69b9cb7bf1dfaaf09d2`  
		Last Modified: Thu, 14 Nov 2024 21:18:52 GMT  
		Size: 100.9 KB (100904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
