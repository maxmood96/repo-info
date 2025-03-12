## `eclipse-temurin:23-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:237f81d26f3487aa838cc06a2024726a5cd32ac99d427015967d1c26d5923b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:23-nanoserver` - windows version 10.0.26100.3476; amd64

```console
$ docker pull eclipse-temurin@sha256:76a871a4bad0270c8adf29c6d31cf7e5ba5d6607ff8774930bb13aca15a281db
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.5 MB (415542330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c41e31affc04a1a079c5483c066e826952382c2027ae9ea9660ecd2137c3a05`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Wed, 12 Mar 2025 19:17:10 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:17:11 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Wed, 12 Mar 2025 19:17:13 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 12 Mar 2025 19:17:15 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:17:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:17:22 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:17:30 GMT
COPY dir:0c46af2d3f44e3815e12a14e71a026bbbb77855831f9730ea0c94836a2ee7de2 in C:\openjdk-23 
# Wed, 12 Mar 2025 19:17:38 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Mar 2025 19:17:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26bf3c3542309e7f1d5728352eb25c5544785e5ee6e9ee048fe6358f67df791e`  
		Last Modified: Wed, 12 Mar 2025 19:17:43 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30d3622ca71fda8d23fee1e0871fcba44ebdd584716dda853fdc67b2a58c4e2`  
		Last Modified: Wed, 12 Mar 2025 19:17:43 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8913103197db4778e1a9567b916c6fd74c0df05527a4f3cc4e964149ef739641`  
		Last Modified: Wed, 12 Mar 2025 19:17:43 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48356f74a40d035851128ab860c4bd353c3002d7a008a3274e29bb0e91298c3e`  
		Last Modified: Wed, 12 Mar 2025 19:17:43 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17f88f196234a4db067428f8767ae60f76c85ff1d26a4d8dfa86379a61b58fa`  
		Last Modified: Wed, 12 Mar 2025 19:17:42 GMT  
		Size: 78.0 KB (78004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90af6aa9621f82fecc4747ac5fe607cf8ddb161df5506530a65ef54eb10f7bf6`  
		Last Modified: Wed, 12 Mar 2025 19:17:42 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58266192d4250a20831c50ad8163d749b7d8ccd15c7ab702878480ef3469ecdd`  
		Last Modified: Wed, 12 Mar 2025 19:17:54 GMT  
		Size: 209.0 MB (209029484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33bfe8685f0408c6b9049e7a4918318ba4b15449a010e60169dded314b14cfd`  
		Last Modified: Wed, 12 Mar 2025 19:17:42 GMT  
		Size: 126.3 KB (126297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ecba42d76a865f68b0c26f87b05075833047c1538e4c6d64fda40c7fda76ebd`  
		Last Modified: Wed, 12 Mar 2025 19:17:42 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-nanoserver` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:e9484ea851eff8794429ead499fdff676c1f378dadf5520abeaa9316059ce702
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.9 MB (329926828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6fa091fa69f01d4dd95f94a25f55600b732ca6204d809ba3cbed67083d6ee22`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Wed, 12 Mar 2025 19:26:33 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:26:34 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Wed, 12 Mar 2025 19:26:35 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 12 Mar 2025 19:26:36 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:26:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:26:40 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:26:49 GMT
COPY dir:0c46af2d3f44e3815e12a14e71a026bbbb77855831f9730ea0c94836a2ee7de2 in C:\openjdk-23 
# Wed, 12 Mar 2025 19:26:55 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Mar 2025 19:26:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59a7a5651d78cd15abd7272ebdae517aa220469ef1a2f61071e5eac0c6b1bd3`  
		Last Modified: Wed, 12 Mar 2025 19:27:00 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb9a4bbb9b4a5a69e01b2732b513cc92b2870cadf04c72e0126ff63bb3731c2`  
		Last Modified: Wed, 12 Mar 2025 19:27:00 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00162926c5d8ecb3645a71ae9dbfb9054e35fa76f0f9a8bac359a834c4a1a83c`  
		Last Modified: Wed, 12 Mar 2025 19:27:00 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36022970fa794028b0c3eb806887ffa99111c8dad73a0032556a0afb2ad8a71`  
		Last Modified: Wed, 12 Mar 2025 19:27:00 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b3d4daba062d2a413e97f9832006a3ecdc3b4256a0aea9654e476366f91f39b`  
		Last Modified: Wed, 12 Mar 2025 19:26:58 GMT  
		Size: 79.2 KB (79165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27c5a2a7ca77b7706aa96c828abd4f718b324ba632be2193f3fc4176dc74b30`  
		Last Modified: Wed, 12 Mar 2025 19:26:58 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d5b535152fa5704da518afc4044c0e89b74754bce843141ed38d2cd0f291dd`  
		Last Modified: Wed, 12 Mar 2025 19:27:11 GMT  
		Size: 209.0 MB (209028194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a4a2bfcd2da4cddbe5c1dbf3e7f8c43ebf1e984b174c0c6ae4cf215403b1bc`  
		Last Modified: Wed, 12 Mar 2025 19:26:58 GMT  
		Size: 117.7 KB (117737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993f1a72d30bd5a89041016e4983666cca30b1578245bb3b1aa9c8b9ae74b65f`  
		Last Modified: Wed, 12 Mar 2025 19:26:58 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull eclipse-temurin@sha256:d619a5fa4844fc65c71adb0a62c94c905dd45f829cf5c3b088b60099b7e72712
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.1 MB (320134360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7613c765b94091770c68f291c74758c1d29ca4d436632bd3c3d69aaa43086868`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Wed, 12 Mar 2025 19:25:58 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:26:01 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Wed, 12 Mar 2025 19:26:02 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 12 Mar 2025 19:26:03 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:26:05 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:26:06 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:26:15 GMT
COPY dir:0c46af2d3f44e3815e12a14e71a026bbbb77855831f9730ea0c94836a2ee7de2 in C:\openjdk-23 
# Wed, 12 Mar 2025 19:26:21 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Mar 2025 19:26:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefcc01086d9fa8b905cb10365742d4d6df3f5896f389dd47ad0fa2d1d442118`  
		Last Modified: Wed, 12 Mar 2025 19:26:25 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274d7f3c2ffbcc24682a6ab7519d38fd99e56c115111b4f442fb8255389ad806`  
		Last Modified: Wed, 12 Mar 2025 19:26:25 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f3dc73f476caeb6f5ac51ae5cb652d1aa820949f748c2d2eea2160cd000d56b`  
		Last Modified: Wed, 12 Mar 2025 19:26:25 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74029140d19d88930ee732f6f5a2393b858c2edcd8e395ab097920534e6384d`  
		Last Modified: Wed, 12 Mar 2025 19:26:25 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13cf63f6764c694efa91e8ff9f3a2073312ff058d4483fade83129d28fae680`  
		Last Modified: Wed, 12 Mar 2025 19:26:24 GMT  
		Size: 69.1 KB (69087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87207bbcb2596554d3ef364f04d0eebe0b82ddd747853064ec7cd6b34b974caa`  
		Last Modified: Wed, 12 Mar 2025 19:26:24 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e3f2d6f41fdf357ead86c1cc87a3241110993b833ecc04bb0bce7b82a02923`  
		Last Modified: Wed, 12 Mar 2025 19:26:35 GMT  
		Size: 209.0 MB (209027997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58f5760b9b93066d6b00cd0d7bf80b0f8535ca8f17bcf0b950e8d5be98acc14`  
		Last Modified: Wed, 12 Mar 2025 19:26:24 GMT  
		Size: 4.1 MB (4123271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f7c85056c93db51a27f250a4cd3363c90ded3dab17aca70cc3fd3f48b6b4a6`  
		Last Modified: Wed, 12 Mar 2025 19:26:24 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
