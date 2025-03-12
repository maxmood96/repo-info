## `eclipse-temurin:23-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:9a6f0c8588971d914f5e8039d690d505f65951ff6cf348e6495b354cd9c43120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `eclipse-temurin:23-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3328; amd64

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
