## `eclipse-temurin:17-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:853c9e263a6de75112e4599aaffdf599b4761961975b626ae92f4482a667ea20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `eclipse-temurin:17-nanoserver-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull eclipse-temurin@sha256:1b06feffb4d56378f08052718ea853b2fa7c5e13816a75659640d3efedfbe1f1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.0 MB (295033132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2d371367e6c63696ed36f7d01814a7e34831b8efb96a28f27d8bce18f76931`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 00:41:38 GMT
SHELL [cmd /s /c]
# Wed, 13 Mar 2024 01:03:38 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 13 Mar 2024 01:03:39 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 13 Mar 2024 01:03:39 GMT
USER ContainerAdministrator
# Wed, 13 Mar 2024 01:03:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Mar 2024 01:03:48 GMT
USER ContainerUser
# Wed, 13 Mar 2024 01:04:03 GMT
COPY dir:7333be24703ce46ff700c9b5bb2dfb5bd5b8a7a43d54ae48c80af36d6e10746c in C:\openjdk-17 
# Wed, 13 Mar 2024 01:04:15 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 Mar 2024 01:04:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9569a24b1d9b596a48436098ac5fe49c52e3153cd3bd147e365a80a4059570fd`  
		Last Modified: Wed, 13 Mar 2024 01:31:07 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b004111afff76cb75f39c8c6f4251185dd9f738ed992ef2a89e8d6251e304467`  
		Last Modified: Wed, 13 Mar 2024 01:36:20 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d37c6efe630448bec07d35d80b2295ea96ac30a7ff7cf344308fe0c21c9b9c`  
		Last Modified: Wed, 13 Mar 2024 01:36:20 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc1bc0efecf259b7805a518e3d7ed83e8a7f34765b04ba2c3f811b94f5a62f1`  
		Last Modified: Wed, 13 Mar 2024 01:36:20 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8698d8050ec92bd86ad863033aa3b4da5555023733bef3265a438c2356ee148d`  
		Last Modified: Wed, 13 Mar 2024 01:36:18 GMT  
		Size: 70.2 KB (70175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a3c2e23c70f8bcd2d14265a5bb75f69b1b641cdaa4580753fbeb8f933bcf62`  
		Last Modified: Wed, 13 Mar 2024 01:36:18 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a7bee21b7b38b21b177e998c3abf25ec31d7b32ea9bdcb2b25ab464bb0c1d0`  
		Last Modified: Wed, 13 Mar 2024 01:36:35 GMT  
		Size: 186.7 MB (186730531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a5f49832ade22e95a9ba7bfee689f4ac352e0ea9835570fe7fa32cbd5de4c2`  
		Last Modified: Wed, 13 Mar 2024 01:36:19 GMT  
		Size: 3.6 MB (3605428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e83e8b4587210753cc8648f2955287f54e123b224478237aadb60329d2addf80`  
		Last Modified: Wed, 13 Mar 2024 01:36:18 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
