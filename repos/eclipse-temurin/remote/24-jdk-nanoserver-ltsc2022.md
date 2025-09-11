## `eclipse-temurin:24-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:97965f57a786ab00fc72eda75d22fb163da8a382f11c25e98e49896cfd5fd26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `eclipse-temurin:24-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull eclipse-temurin@sha256:821a84de0838e992bddcdf521c6d7ed5a7f2bce89e598f0e45e5cbf0c49bf623
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260329110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7fb77bf0d0e16ded1837c8e2684bf751c7d2666775502ab9041f417e4481d7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:19:27 GMT
SHELL [cmd /s /c]
# Wed, 10 Sep 2025 22:19:28 GMT
ENV JAVA_VERSION=jdk-24.0.2+12
# Wed, 10 Sep 2025 22:19:28 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 10 Sep 2025 22:19:28 GMT
USER ContainerAdministrator
# Wed, 10 Sep 2025 22:19:31 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Sep 2025 22:19:32 GMT
USER ContainerUser
# Wed, 10 Sep 2025 22:20:03 GMT
COPY dir:f33586a1c43306f0f604ab16c8e427c967fb5f3c79695cbcabca361a95405189 in C:\openjdk-24 
# Wed, 10 Sep 2025 22:20:06 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Sep 2025 22:20:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9a238b296b863260af62360805baa85f9d2fb272823e764b654e58032e367a`  
		Last Modified: Wed, 10 Sep 2025 23:08:42 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1edd3c08ef53e09f2bffa5ab9fff9a85fa5416735ee72079c705e5fb882bcb`  
		Last Modified: Thu, 11 Sep 2025 00:18:12 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2cffda9a8cb2c9b6b9aef0c2f3b494c4a6919478a6709eb430af745a3005e2`  
		Last Modified: Thu, 11 Sep 2025 00:18:13 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401b5f21ed45d651a28f5f5ca239e29ac4f3195601e22e63d8ac763d63e5726a`  
		Last Modified: Thu, 11 Sep 2025 00:18:12 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb84d5e9fc5db33225d56148aec63adbb974946bdabcf0e109cd4d5fae588ebe`  
		Last Modified: Thu, 11 Sep 2025 00:18:12 GMT  
		Size: 88.8 KB (88777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16086f53d7ea88bb1d231e5a384720331ac9d1678d64b3d7257501d3a1be4903`  
		Last Modified: Thu, 11 Sep 2025 00:18:13 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afcbdf485c1b3ca3ced9585cb37aecf1494081bb816fe428d91f7770d78d9aae`  
		Last Modified: Thu, 11 Sep 2025 00:18:34 GMT  
		Size: 137.4 MB (137383740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b8af8e6b52404a0939942acb4665860fda91bbf9a2a2d4e2edeaa8e40a45c7`  
		Last Modified: Thu, 11 Sep 2025 00:18:13 GMT  
		Size: 130.3 KB (130300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7276ff052005044ca6f047104410f75821a9804e865f5509256989d3b07a28b9`  
		Last Modified: Thu, 11 Sep 2025 00:18:13 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
