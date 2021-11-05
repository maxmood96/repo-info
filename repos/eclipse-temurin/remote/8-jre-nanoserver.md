## `eclipse-temurin:8-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:11cf904861dbcb1a0a8baab736cfffc216acdb5140c31bab38e418158623d388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.288; amd64
	-	windows version 10.0.17763.2237; amd64

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.20348.288; amd64

```console
$ docker pull eclipse-temurin@sha256:a3e771e8b4e02b4532b86cdd3800e7fbc86bd570ca9581b25b54eb1d4531d5ea
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156185883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022b375afcbc449dd6a8cebcc5e4a59c5ea71f2ccb5ad1cf3a68b724da4a5534`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Oct 2021 11:15:04 GMT
RUN Apply image ltsc2022-amd64
# Wed, 13 Oct 2021 19:02:30 GMT
SHELL [cmd /s /c]
# Fri, 05 Nov 2021 19:43:06 GMT
ENV JAVA_VERSION=jdk8u312-b07
# Fri, 05 Nov 2021 19:43:07 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 05 Nov 2021 19:43:07 GMT
USER ContainerAdministrator
# Fri, 05 Nov 2021 19:43:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 05 Nov 2021 19:43:22 GMT
USER ContainerUser
# Fri, 05 Nov 2021 19:44:02 GMT
COPY dir:f43ebde5893522b38a147191e5e447aa435ef67c7d947aeb3e536f25bc61cdb3 in C:\openjdk-8 
# Fri, 05 Nov 2021 19:44:14 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:91284e7e8fd4bd7ebcfa98544a3e4f59639f38281225c81c34b6fe22e0dba4e5`  
		Size: 116.9 MB (116939483 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ba797e8f93823c3d71c52fcae413f3a33ca28ff2711c09ba5141432948f8298`  
		Last Modified: Wed, 13 Oct 2021 19:43:54 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9dec6b507607ca08e638c7d3ae3128972c49650144c514f4c38fc57ceb5c43`  
		Last Modified: Fri, 05 Nov 2021 20:39:18 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9a6e263cf49da630f6760ba1b585fef5f0428dd256021064f116c34a3d2b98`  
		Last Modified: Fri, 05 Nov 2021 20:39:17 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee96e2b9d26ffc56e72b87fb9a7157aef8e02be14bc87c86f5eec89c492dc13`  
		Last Modified: Fri, 05 Nov 2021 20:39:15 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a309d0ae1eba4bee66a057c942a2f0bc3ecf5ce3637bb386e7302db6911bc8f3`  
		Last Modified: Fri, 05 Nov 2021 20:39:15 GMT  
		Size: 94.4 KB (94354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5beb7d50903a50966a72f48c7e65fa918cc57be153a73d494e86add07b2e55b9`  
		Last Modified: Fri, 05 Nov 2021 20:39:15 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44ad19fb5a27fafeaaa77e7d4f10a7d11183eaf730832028390cb96a4413f89`  
		Last Modified: Fri, 05 Nov 2021 20:39:45 GMT  
		Size: 39.1 MB (39087853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfae76da586894d284cc5d965833fc106e98e574ba5b86263e5bed3aa02cfe9f`  
		Last Modified: Fri, 05 Nov 2021 20:39:39 GMT  
		Size: 58.4 KB (58375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.17763.2237; amd64

```console
$ docker pull eclipse-temurin@sha256:66b429f4c6cfabb61e853bec483a14d3c9ccb789ddfa199447167fa76979f031
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141902500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14ebc3fbeef054c1a2c22340d3f5452891e0c4b3aae83727bc9e2ea8bfc0332`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Oct 2021 08:01:14 GMT
RUN Apply image 1809-amd64
# Wed, 13 Oct 2021 18:17:55 GMT
SHELL [cmd /s /c]
# Fri, 05 Nov 2021 19:18:23 GMT
ENV JAVA_VERSION=jdk8u312-b07
# Fri, 05 Nov 2021 19:18:24 GMT
ENV JAVA_HOME=C:\openjdk-8
# Fri, 05 Nov 2021 19:18:25 GMT
USER ContainerAdministrator
# Fri, 05 Nov 2021 19:18:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 05 Nov 2021 19:18:49 GMT
USER ContainerUser
# Fri, 05 Nov 2021 19:25:40 GMT
COPY dir:f43ebde5893522b38a147191e5e447aa435ef67c7d947aeb3e536f25bc61cdb3 in C:\openjdk-8 
# Fri, 05 Nov 2021 19:25:50 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:934e212983f208dc2bebc5de38259a6a62f1761868aacfee2cb3585a13b1e24b`  
		Size: 102.7 MB (102661372 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ceff24c3c0c2c360cd3788fcde5c41e1d6601339f4944623c732558a6030e631`  
		Last Modified: Wed, 13 Oct 2021 19:12:58 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177724a0db674e21ef5312fec420a4b52d5d2cc11f50b1618560b353b3d6b504`  
		Last Modified: Fri, 05 Nov 2021 20:22:24 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1511463fd5cb415be8764921c481a9f4720730625030680aef2b9733b3b9209b`  
		Last Modified: Fri, 05 Nov 2021 20:22:24 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb07f50c4396ee11e0efa3fb5bd2266c5659d6bcbaab9f40b250dc35be13699`  
		Last Modified: Fri, 05 Nov 2021 20:22:22 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6006aacda1e222839c9f38b6f5c75362b53fbd85435ebbf419bb1993c309be`  
		Last Modified: Fri, 05 Nov 2021 20:22:22 GMT  
		Size: 69.0 KB (69001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a878a822d6235e0372f72239020c185d094c9e0141c1320b4f04b43614b1579`  
		Last Modified: Fri, 05 Nov 2021 20:22:22 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d60413b504acd4bfd839521d568e21ecddaa4e6dfdf532f4b2ef00dadf7f88`  
		Last Modified: Fri, 05 Nov 2021 20:26:37 GMT  
		Size: 39.1 MB (39085322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9fef68564fbc005171c45bde017c6c7e0cb107965a4383dab2f5f396bb30f97`  
		Last Modified: Fri, 05 Nov 2021 20:26:31 GMT  
		Size: 81.1 KB (81145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
