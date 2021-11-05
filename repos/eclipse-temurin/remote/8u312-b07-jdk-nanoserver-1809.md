## `eclipse-temurin:8u312-b07-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:085c99dd5ec2be858e3c8501e23159aa954286b244cb61b151a9c78f98dd08dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2237; amd64

### `eclipse-temurin:8u312-b07-jdk-nanoserver-1809` - windows version 10.0.17763.2237; amd64

```console
$ docker pull eclipse-temurin@sha256:31ea92962d6f6d2175f05d9726692cd192b24b5573dc26d404cc9dfaa0759edb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.0 MB (202998082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5142854cd0cdf215e1ba2ab1fe97a728ceb7c0a89a6d4c1af6617a9c679344d`
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
# Fri, 05 Nov 2021 19:18:59 GMT
COPY dir:7d20e7860b874019800a6393f3930849559cf997f64b86d2d0263d858293fa37 in C:\openjdk-8 
# Fri, 05 Nov 2021 19:19:14 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:584ab9b080fd3f7e5216570d980f346631b3746e0eaaf84eb25f9a489ef6db1f`  
		Last Modified: Fri, 05 Nov 2021 20:24:12 GMT  
		Size: 100.2 MB (100179929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4d8dd4be8f14b929b59eee45b59465bb898bbad2b4e9b1cc456cf1d230b52b`  
		Last Modified: Fri, 05 Nov 2021 20:22:22 GMT  
		Size: 82.1 KB (82120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
