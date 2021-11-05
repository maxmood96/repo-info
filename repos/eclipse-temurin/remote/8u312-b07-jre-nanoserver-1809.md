## `eclipse-temurin:8u312-b07-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:219a08a64e5c838a61de5df31b455e78bf5babec4486d129d9aca3dc1894a74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `eclipse-temurin:8u312-b07-jre-nanoserver-1809` - windows version 10.0.17763.2237; amd64

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
