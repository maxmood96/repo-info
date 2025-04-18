## `eclipse-temurin:11-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:e2a7668752836850722e436411df10369a41d94c348f73ab9ca3f0918ab8dfc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `eclipse-temurin:11-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull eclipse-temurin@sha256:e62c1b66a76b7c6a87402255f1aa71b7f00ed64978929baedc1bdcf9a0a0062b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.9 MB (384907912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc6953d68acc28ace2f8c17bf38a91b010bd8a33b5aa9e937ad518f9bff2adb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Fri, 18 Apr 2025 04:15:36 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:15:37 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Fri, 18 Apr 2025 04:15:38 GMT
ENV JAVA_HOME=C:\openjdk-11
# Fri, 18 Apr 2025 04:15:39 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:15:42 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:15:43 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:15:52 GMT
COPY dir:9a97e9a1ce762bb8542962ee0a2b0ca6fa379668e092b80acfc01b297b3b57a6 in C:\openjdk-11 
# Fri, 18 Apr 2025 04:15:59 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 18 Apr 2025 04:16:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 17 Apr 2025 02:52:17 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0b217e025e8405ef036eec547182d9b49b3a0943a14d9ad0a1713213f9a13b`  
		Last Modified: Fri, 18 Apr 2025 04:16:03 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7308e44a838c1fcefde8f963d3d8f3f262a89151a46d5581c01212e692ef06`  
		Last Modified: Fri, 18 Apr 2025 04:16:03 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea876a1b6afdf7742842a695eb0d34e0feb0745d1cbbdbe908de92624d824f33`  
		Last Modified: Fri, 18 Apr 2025 04:16:03 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b4e4dd7903d968b88779facb00249285d65dbce54dffdc59ed3973f6841158`  
		Last Modified: Fri, 18 Apr 2025 04:16:03 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1de73c22013dece0db770538c31bdc807c5f849ce90391a74584d2cd0ec6e7`  
		Last Modified: Fri, 18 Apr 2025 04:16:02 GMT  
		Size: 76.4 KB (76420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6dc4d8821281b7093717ab12951574efef3ea3010e6b17f3e2fc7affd91328`  
		Last Modified: Fri, 18 Apr 2025 04:16:02 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e4514419b8632d562d02e28d18fc01d74caca0b7bdeab803900537d9dd52e4`  
		Last Modified: Fri, 18 Apr 2025 04:16:12 GMT  
		Size: 194.6 MB (194557358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bea31128082eb6d749b2a7938aea5574620c8179f16deac5eb216d7ea779013`  
		Last Modified: Fri, 18 Apr 2025 04:16:02 GMT  
		Size: 125.9 KB (125865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3db1b73e8a40a628670dd6efd7ad993ec8b71948a6f57fe72c38ed02985da8a`  
		Last Modified: Fri, 18 Apr 2025 04:16:02 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
