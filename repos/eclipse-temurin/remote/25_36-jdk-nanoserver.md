## `eclipse-temurin:25_36-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:4ae536beed2320f9f7211a7477e42898e6ec65d0a453364b9d4c55d8078b7495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `eclipse-temurin:25_36-jdk-nanoserver` - windows version 10.0.26100.6584; amd64

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

### `eclipse-temurin:25_36-jdk-nanoserver` - windows version 10.0.20348.4171; amd64

```console
$ docker pull eclipse-temurin@sha256:673d4e10fd22448b857295b5cb494a48bd1e55d7f85d8b5a522f87a1a81d7eb1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260873175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff859c36ec62356905220edbb312b2fcf7151938535af2c10c645c6b5f4994d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Thu, 25 Sep 2025 22:12:47 GMT
SHELL [cmd /s /c]
# Thu, 25 Sep 2025 22:12:48 GMT
ENV JAVA_VERSION=jdk-25+36
# Thu, 25 Sep 2025 22:12:49 GMT
ENV JAVA_HOME=C:\openjdk-25
# Thu, 25 Sep 2025 22:12:49 GMT
USER ContainerAdministrator
# Thu, 25 Sep 2025 22:12:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 25 Sep 2025 22:12:58 GMT
USER ContainerUser
# Thu, 25 Sep 2025 22:13:40 GMT
COPY dir:3b404a1cbcdf7278c6a85a2778d3f0c01bd0f1229e8c8ae0734ae7bd6fe589bb in C:\openjdk-25 
# Thu, 25 Sep 2025 22:13:48 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 25 Sep 2025 22:13:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc44f684fa662a44ac5b5fdb2c6bf679052cd2d8ffbbd0649e5c186ad49ac5f5`  
		Last Modified: Thu, 25 Sep 2025 22:14:16 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c71fbba26ccdbd7a60d6ef3a48c82fbefbee275341b6784a2076f9bc61b955`  
		Last Modified: Thu, 25 Sep 2025 22:14:16 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdb1175fae153d8d5bd8ef1d8927b294bf8b3db598b2c37949a160f75b4ad6c`  
		Last Modified: Thu, 25 Sep 2025 22:14:16 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26916416afde07316880254c82e0a6ba3832ed32743e01d44435dd14d47e025a`  
		Last Modified: Thu, 25 Sep 2025 22:14:16 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db585771e906d79dcc800547cc747763294d71921f77e1df13f53ef3c4172fe8`  
		Last Modified: Thu, 25 Sep 2025 22:14:16 GMT  
		Size: 83.9 KB (83932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317ef0bf3caeb82f3ca2dd89ed5f2c21b6473555cb9a3a753888167c899fdc7c`  
		Last Modified: Thu, 25 Sep 2025 22:14:16 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ad54c159429db181b730e57bc5c182401ea2adf66591fdbb05c53c83ab03bb`  
		Last Modified: Fri, 26 Sep 2025 00:14:48 GMT  
		Size: 137.9 MB (137937223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9131119203286b751633808411b4a50733459b90ff0466ef9d0f14c78f883989`  
		Last Modified: Thu, 25 Sep 2025 22:14:16 GMT  
		Size: 125.7 KB (125747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d455ed2fe65fcebe54c26ea882a11c3526a9115654339f3e81bebd891902e563`  
		Last Modified: Thu, 25 Sep 2025 22:14:16 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
