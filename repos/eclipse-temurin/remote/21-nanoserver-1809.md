## `eclipse-temurin:21-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:d93601fb254d7c01d465f0241c0a3bdb8a9a4d7ecda6f3b1a6ca142e1d75c2fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `eclipse-temurin:21-nanoserver-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull eclipse-temurin@sha256:5180037ce42b45d446d69166e21ca6913f1868c418a56136781e4265596a6e50
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.6 MB (309639549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834925368703fb866fb9b90217961396f23f18aa0cc498642082e44dc4ff0e59`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 00:41:38 GMT
SHELL [cmd /s /c]
# Wed, 13 Mar 2024 01:15:13 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Wed, 13 Mar 2024 01:15:14 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 13 Mar 2024 01:15:14 GMT
USER ContainerAdministrator
# Wed, 13 Mar 2024 01:15:23 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Mar 2024 01:15:24 GMT
USER ContainerUser
# Wed, 13 Mar 2024 01:15:38 GMT
COPY dir:ef01cec12ba2d7ca328dd166c68dc318e8666a1382b059655285e6e080af62b8 in C:\openjdk-21 
# Wed, 13 Mar 2024 01:15:51 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 Mar 2024 01:15:51 GMT
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
	-	`sha256:5f2a4287941008944a771e7303adc0fe34dae600d04a88a2a4801f943368b788`  
		Last Modified: Wed, 13 Mar 2024 01:38:58 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cd3c4943c07a2ce8dda98e2064fc5250e5cfb00be821232c623fefe881666b`  
		Last Modified: Wed, 13 Mar 2024 01:38:58 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3d5e15f5a67bec2b3837fbdd9d9b53e3c559507352db87b240dd9a18519e6a`  
		Last Modified: Wed, 13 Mar 2024 01:38:58 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ae2b43cfa06f4f8dee3385edeccfbad111ee4ef72cb34375433628a971ee8e`  
		Last Modified: Wed, 13 Mar 2024 01:38:56 GMT  
		Size: 68.8 KB (68831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c8baa61a5bbf475bcc2bd6199af0dd2cfcbeed38ec7e3ab81b205b860e125d2`  
		Last Modified: Wed, 13 Mar 2024 01:38:56 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f222ab93cd25b7630d0e102d7fdb55b660fcc3d186bb44dd203ace8507da1096`  
		Last Modified: Wed, 13 Mar 2024 01:39:15 GMT  
		Size: 201.1 MB (201125650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6ca0e0752304735b823900bc70342c96c7684d3d77ff748897d982416027d0`  
		Last Modified: Wed, 13 Mar 2024 01:38:57 GMT  
		Size: 3.8 MB (3818081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a823680162ed8db8e1ff68a1e07e57c9c20397bcbbf5ce76e139f6179086fef5`  
		Last Modified: Wed, 13 Mar 2024 01:38:56 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
