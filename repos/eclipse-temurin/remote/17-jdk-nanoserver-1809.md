## `eclipse-temurin:17-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:481bb6a352099a1a7d2c83725a63eb1d8456ee70741e200c7be7e5d3a924da2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `eclipse-temurin:17-jdk-nanoserver-1809` - windows version 10.0.17763.2366; amd64

```console
$ docker pull eclipse-temurin@sha256:4f24bbf49edfba34ce7d7fd95b90017d30d38c04735efde896ad07982b9b44f1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.6 MB (291575635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee2c034e8d73e473f9640b1c632de74adb76c162ae655f74ff8c11a7bcf15bd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 07 Dec 2021 04:37:11 GMT
RUN Apply image 1809-amd64
# Sat, 18 Dec 2021 05:18:44 GMT
SHELL [cmd /s /c]
# Sat, 18 Dec 2021 05:58:50 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Sat, 18 Dec 2021 05:58:50 GMT
ENV JAVA_HOME=C:\openjdk-17
# Sat, 18 Dec 2021 05:58:51 GMT
USER ContainerAdministrator
# Sat, 18 Dec 2021 05:59:05 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 18 Dec 2021 05:59:05 GMT
USER ContainerUser
# Sat, 18 Dec 2021 05:59:22 GMT
COPY dir:75727e79a870c9066772bd3811959a8f3c491ac4b54ae3b2c145d1638b6bc93f in C:\openjdk-17 
# Sat, 18 Dec 2021 05:59:38 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 18 Dec 2021 05:59:38 GMT
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
	-	`sha256:b26306f8e8a4f4dfe20500528de7aa39df4e7dee0979f58489a2ded09004ffbd`  
		Last Modified: Sat, 18 Dec 2021 06:40:15 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9362cfac01213205fa1c339e140a340bb1905cb5e0a78c93e0c6a0e5bbfef6d0`  
		Last Modified: Sat, 18 Dec 2021 06:40:14 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec169fd6feabc29f6922c4666746164f5167e3d65707e55174b9a8f12cabf094`  
		Last Modified: Sat, 18 Dec 2021 06:40:14 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0099d82d3944a044d664e71f334526a8d7d2ed1bd7096d3acb142c80c2ea7bb7`  
		Last Modified: Sat, 18 Dec 2021 06:40:12 GMT  
		Size: 66.9 KB (66924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0ed6216ade0a806a34dbf8eed2a100bee72f70e7f01a8403826a5a189e8e6b`  
		Last Modified: Sat, 18 Dec 2021 06:40:12 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419ce8782a3dde51b60edb3f88b696dd08416fb57ee41eb8422c472b76be43a2`  
		Last Modified: Sat, 18 Dec 2021 06:40:34 GMT  
		Size: 185.0 MB (184952186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1e4303c6b1ab8286719a578cb08c3b8ac43de4752ec8581c0b394952d5f35c`  
		Last Modified: Sat, 18 Dec 2021 06:40:13 GMT  
		Size: 3.6 MB (3645616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91876cedd38acf2de753af5ad6afd968d4450fb8baf1979d0e7ca75ad8cdeab1`  
		Last Modified: Sat, 18 Dec 2021 06:40:12 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
