## `eclipse-temurin:11-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:91933f05b6e10cad97faf9992351a80e6c3ae9c0ceb5f7d035274d0dd7b4e7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `eclipse-temurin:11-jre-nanoserver-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull eclipse-temurin@sha256:492153042dc035e1d0cc594b231708b5e3b9fd509cb91c9c1ab928989cf3aafa
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145908031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f48b77f53515d987e2284605229da6ef705726ef8c672e0ff22c4918274fc29`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jan 2022 05:19:42 GMT
RUN Apply image 1809-amd64
# Tue, 11 Jan 2022 21:33:30 GMT
SHELL [cmd /s /c]
# Tue, 11 Jan 2022 21:49:57 GMT
ENV JAVA_VERSION=jdk-11.0.13+8
# Tue, 11 Jan 2022 21:49:58 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 11 Jan 2022 21:49:59 GMT
USER ContainerAdministrator
# Tue, 11 Jan 2022 21:50:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 11 Jan 2022 21:50:10 GMT
USER ContainerUser
# Tue, 11 Jan 2022 21:58:59 GMT
COPY dir:6031cfac1e4bd8de6c5533bea0aabc25715779d854db7f41b8aea3e1449ff0bf in C:\openjdk-11 
# Tue, 11 Jan 2022 21:59:11 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:f9d5f05eef69cdb907192f860ff14ce569d925f1f53ac5255a5b37631124fd4d`  
		Size: 103.0 MB (103014618 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6cc5785ab09c66739c3205c3a26410f1cf4bf85c377fa81b240e754cf0659c58`  
		Last Modified: Tue, 11 Jan 2022 22:44:40 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c631e6fd097cbb2c567e65314f289e8c6f25271d826134deb37e896949b681c8`  
		Last Modified: Tue, 11 Jan 2022 22:56:07 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4275da636a39fa6869cb200e28126b14ee6577828242ee62ad04e6a6a0902f5`  
		Last Modified: Tue, 11 Jan 2022 22:56:07 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a14996a9d65b46149cf4b8f6e6cfd1f36eb911cf8f1d9d2e985f7d17166109`  
		Last Modified: Tue, 11 Jan 2022 22:56:07 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e5754f2462f2d79793337f2b5fd207a7ce771c1d722d9230e66385d0661723`  
		Last Modified: Tue, 11 Jan 2022 22:56:05 GMT  
		Size: 68.3 KB (68261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d44c79847d5679fac223a6e171d5dfecfd1fb065806fb8839e42cb3f90fa3d8`  
		Last Modified: Tue, 11 Jan 2022 22:56:05 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97dd1825eddd974c21b55190cc92f013a7fb993baefc79af88e8f5e3ed2f536d`  
		Last Modified: Tue, 11 Jan 2022 23:01:20 GMT  
		Size: 42.7 MB (42739104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892c076dac7e68f49ab102f5f46f73328ddcffdf59d96e93c097652cc55b38c2`  
		Last Modified: Tue, 11 Jan 2022 23:01:12 GMT  
		Size: 80.4 KB (80399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
