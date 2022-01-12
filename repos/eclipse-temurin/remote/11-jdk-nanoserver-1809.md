## `eclipse-temurin:11-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:3dc1b6abde9d0c183272accf48a0e36a25b343dad48b73cad9b482b17d398d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2451; amd64

### `eclipse-temurin:11-jdk-nanoserver-1809` - windows version 10.0.17763.2451; amd64

```console
$ docker pull eclipse-temurin@sha256:2b8087f2795cd7e1c0519bec580689e916fde73c566b6728f91b361d3f7016ed
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295113163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a766f62c262887dd2f8cbc836416c0794c81c566140d1ab72bab009c799486c`
-	Default Command: `["jshell"]`
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
# Tue, 11 Jan 2022 21:50:40 GMT
COPY dir:7549fd743977f7762910679960e9adfeab116385590a40bc0f1570100fce1af1 in C:\openjdk-11 
# Tue, 11 Jan 2022 21:50:57 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 11 Jan 2022 21:50:57 GMT
CMD ["jshell"]
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
	-	`sha256:474e957c40ad52593a45b1e72faab7becb1886e64e8291380730e3054bec8bb9`  
		Last Modified: Tue, 11 Jan 2022 22:59:35 GMT  
		Size: 191.9 MB (191942580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088a3df303e23e313e69e60d028ff61378691bd0258470dd8a6750ab3cbc6679`  
		Last Modified: Tue, 11 Jan 2022 22:56:05 GMT  
		Size: 80.9 KB (80881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4b8a975af6678a23577098bc4f7fbeb91fa03c5ea48c7bf4a2709458b85d27`  
		Last Modified: Tue, 11 Jan 2022 22:56:05 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
