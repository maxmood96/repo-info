## `eclipse-temurin:25-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:6c519700c847a2e57455e6b40d5c998b3a4fc182212b50b462e2f4739ac5be00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `eclipse-temurin:25-nanoserver-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull eclipse-temurin@sha256:c92bbdb8a891ebca07f9292975a039300471b90e281055bde02fe984be732e6d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.7 MB (331679090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01522b47aa4c7a2743d2d2b3f827f62cdf91cae74280d85859b7e73e3d98ad9a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Sep 2025 02:12:39 GMT
RUN Apply image 10.0.26100.6584
# Thu, 25 Sep 2025 22:14:33 GMT
SHELL [cmd /s /c]
# Thu, 25 Sep 2025 22:14:34 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 22:14:35 GMT
ENV JAVA_HOME=C:\openjdk-25
# Thu, 25 Sep 2025 22:14:36 GMT
USER ContainerAdministrator
# Thu, 25 Sep 2025 22:14:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 25 Sep 2025 22:14:46 GMT
USER ContainerUser
# Thu, 25 Sep 2025 22:15:21 GMT
COPY dir:3b404a1cbcdf7278c6a85a2778d3f0c01bd0f1229e8c8ae0734ae7bd6fe589bb in C:\openjdk-25 
# Thu, 25 Sep 2025 22:15:30 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 25 Sep 2025 22:15:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a75a4ab04983f989d9a1442633d6c3952b863719a00dd77cf160f7055beaded9`  
		Last Modified: Tue, 09 Sep 2025 22:28:08 GMT  
		Size: 193.6 MB (193550846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfcab0fec588d4e2c2e161e84f57cd2a4d95ce15bd5088aa6a57b3e95914291`  
		Last Modified: Thu, 25 Sep 2025 22:15:57 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3b5cd56e5575a47093ffb9af2904eeb04b15dd2db1d807dc217a1a2dabf93d`  
		Last Modified: Thu, 25 Sep 2025 22:15:57 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385e65ab4a603be23d08c91d64cf82a7a706ab2fc283650e3638fe6c05e8f195`  
		Last Modified: Thu, 25 Sep 2025 22:15:57 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d891fd5b05297370e76b2bad8554012ae0fff0caf3c4523113b9891a0b450ef`  
		Last Modified: Thu, 25 Sep 2025 22:15:57 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ed264858070b1599ce4a6b8d598d40312afed6fef690e83426fc43992ed3d4`  
		Last Modified: Thu, 25 Sep 2025 22:15:57 GMT  
		Size: 70.7 KB (70739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c2b03ddba5f2c15b2cc1c9e518b4156987cf59db7f421ee7f22f3370bbfb65`  
		Last Modified: Thu, 25 Sep 2025 22:15:59 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e973385a3c829253e06111069e0032cc878f8e7551846baae7bbd87e4d6e00d0`  
		Last Modified: Fri, 26 Sep 2025 00:14:48 GMT  
		Size: 137.9 MB (137937047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdb21910fd3c1015bc8d8297a29052770384eb8e967861824c82ca6f85a455b`  
		Last Modified: Thu, 25 Sep 2025 22:16:00 GMT  
		Size: 114.0 KB (113962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f87b7e2d66987c0add749f81225c69ce131e50fe85c387f6e7ddd81bbbc0b5`  
		Last Modified: Thu, 25 Sep 2025 22:16:00 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
