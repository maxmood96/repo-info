## `eclipse-temurin:8u462-b08-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:71c6930ab5a0857213661f6de50b414e88fc441ecde7ee8e1ad3bfa578213016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `eclipse-temurin:8u462-b08-jre-nanoserver-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull eclipse-temurin@sha256:617978d739498ed3120c2062476836dfe04147ed2a0f65e294353443a7a21eb1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163390763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3fdf1c0f679cce45d74a57a2425a5b7752d374b533194f7f91c99bea147eba7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 08 Aug 2025 18:24:51 GMT
RUN Apply image 10.0.20348.4052
# Tue, 12 Aug 2025 20:49:55 GMT
SHELL [cmd /s /c]
# Tue, 12 Aug 2025 20:49:56 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Tue, 12 Aug 2025 20:49:57 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 12 Aug 2025 20:49:58 GMT
USER ContainerAdministrator
# Tue, 12 Aug 2025 20:50:01 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 12 Aug 2025 20:50:02 GMT
USER ContainerUser
# Tue, 12 Aug 2025 20:50:05 GMT
COPY dir:3a0e2241911cff37ef92eeb46012c4bf9f32f9301b3cfbba190d8fdd900a0568 in C:\openjdk-8 
# Tue, 12 Aug 2025 20:50:10 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:8aaaec81c2904f6f09241b477558fb79967c10222e2028e5fcd142ec6b1f43c6`  
		Last Modified: Tue, 12 Aug 2025 20:23:56 GMT  
		Size: 122.7 MB (122660330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e520b634d8ee3eab66925c61f0e019e692e0fe212183172786a7eeb6b5c62ce5`  
		Last Modified: Tue, 12 Aug 2025 20:51:00 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7d5215baf4d8b057d49ba12fbaba74702a1881a1049fabcbd7f51d44262b77`  
		Last Modified: Tue, 12 Aug 2025 20:51:00 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788e76d062bdf1ac2f015c11fe46438525e54921bb04a765ac802785d880a3be`  
		Last Modified: Tue, 12 Aug 2025 20:51:00 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25ac7afa6697848d6ffb94cfce7d1846cb5091cd37237cd724ceeec3b370621`  
		Last Modified: Tue, 12 Aug 2025 20:51:01 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2eb4ebc49738c03527748baca95a0cb52f8ab5946b2382bf1888a5f9727eca4`  
		Last Modified: Tue, 12 Aug 2025 20:51:01 GMT  
		Size: 76.5 KB (76452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb93f88c36b04951d32268e837e8d79fc3b2d44391342ff9a116548050f628e`  
		Last Modified: Tue, 12 Aug 2025 20:50:55 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94fc0edac43c2d4b4e992b82997ae78beb9bcb593a5d50b1f82307f1b9f73d1`  
		Last Modified: Tue, 12 Aug 2025 20:51:06 GMT  
		Size: 40.5 MB (40547823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc910a2e3136db383dfccc4e71cf73f780ebdd7012d5ada38fe115f83f86743`  
		Last Modified: Tue, 12 Aug 2025 20:50:58 GMT  
		Size: 101.0 KB (100970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
