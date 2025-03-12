## `eclipse-temurin:8-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:00c74feced5be85878e90d1f04736739027f07eb7d59b0ce09e3e599ee267020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `eclipse-temurin:8-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull eclipse-temurin@sha256:2d6d63e3d11fe4559983c3b1a9cbcaaa70c402f9bee5315923277d6c0d3487df
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.9 MB (308943632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5ae0a70102c7a5f4155fd486edcd15c7d94d2c403cd42c464f98aaee0f6cdf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Wed, 12 Mar 2025 19:15:58 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:15:59 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 12 Mar 2025 19:16:00 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 12 Mar 2025 19:16:00 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:16:03 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:16:04 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:16:09 GMT
COPY dir:bdaea23e3e57be9dfb95abf135786259c631aa0db2125cb7a86f299ac37b3921 in C:\openjdk-8 
# Wed, 12 Mar 2025 19:16:15 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a96ee8de066214a90d726dbf3318f38966a00b7cbb68db3ecf9dc2005ba219`  
		Last Modified: Wed, 12 Mar 2025 19:16:21 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5a628fb7d91aded698969d1043521992e0c010450740447986500322a8cedd`  
		Last Modified: Wed, 12 Mar 2025 19:16:20 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f5c09f828b46874359177943857b39271b5d8d21335f2515de2b3ac8d56bcff`  
		Last Modified: Wed, 12 Mar 2025 19:16:20 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e9e843e842d0b78bf8782a7f5d1130dda87e1489122a537d614503db314072`  
		Last Modified: Wed, 12 Mar 2025 19:16:19 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d51b829bdf4d1aa5cd293bae5180b030f87d9f5f9082e9fb34cf9c270e4732`  
		Last Modified: Wed, 12 Mar 2025 19:16:19 GMT  
		Size: 76.3 KB (76327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29095f0104bfcf1ecccc42367c5ec02aea3b53aa9038b51999618b2e2c2d1214`  
		Last Modified: Wed, 12 Mar 2025 19:16:18 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0893e0d750f3a447f51bb9c6fa3bacd6ab08d8a2242fcebe44b5d081e029153`  
		Last Modified: Wed, 12 Mar 2025 19:16:25 GMT  
		Size: 102.4 MB (102433887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8e86718474b43aab68d7f1c917283d1df5ef0ac991592553e67e3945cdb32a`  
		Last Modified: Wed, 12 Mar 2025 19:16:19 GMT  
		Size: 126.0 KB (125965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
