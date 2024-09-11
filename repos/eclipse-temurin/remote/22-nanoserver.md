## `eclipse-temurin:22-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:bdefaca2c86fe8e2ae3fa27f4f019b76938c337756669e9046432c542b5c42a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `eclipse-temurin:22-nanoserver` - windows version 10.0.20348.2700; amd64

```console
$ docker pull eclipse-temurin@sha256:9f24a771fb966fa90d73fe4e264c2b0381ee3ac0a849a817b431afa6e5667603
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.3 MB (320281266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05430820039e4f0238fbf32b3cd1d7397f19ea7888e3634ab6078ba5265e4ae`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Sep 2024 23:48:03 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 01:05:47 GMT
SHELL [cmd /s /c]
# Wed, 11 Sep 2024 01:10:15 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Wed, 11 Sep 2024 01:10:16 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 11 Sep 2024 01:10:17 GMT
USER ContainerAdministrator
# Wed, 11 Sep 2024 01:10:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Sep 2024 01:10:27 GMT
USER ContainerUser
# Wed, 11 Sep 2024 01:10:41 GMT
COPY dir:bb8037d92e17293fdab4a72c09c9eb83e6a7b620b5e832c71d656bbaf7bd694c in C:\openjdk-22 
# Wed, 11 Sep 2024 01:10:54 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 11 Sep 2024 01:10:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a447243899be39b01c34fc7e1bcecb47ce42b14668876fdd121f8b5e2d4d4a86`  
		Last Modified: Tue, 10 Sep 2024 22:28:02 GMT  
		Size: 120.5 MB (120509521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015f530aeae2fa9f5c34641a19099e9949880479ad7319678bd0506ba1927a95`  
		Last Modified: Wed, 11 Sep 2024 01:33:11 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c15ff28a04e3c5ab83230cbf1486435a5b786b9d7494f43fcaf43db9d0c21a3`  
		Last Modified: Wed, 11 Sep 2024 01:36:02 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1784ae43d89492094e7c81136584db5a16e046a072ad5d9376cf9761faa84cff`  
		Last Modified: Wed, 11 Sep 2024 01:36:02 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f209785f413c702bf81478c11ef09ca6c892aedaf858164ca5da4b8cec492f5e`  
		Last Modified: Wed, 11 Sep 2024 01:36:01 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912b8a2ddda6465609f033fd816e8f010fab0d33aa0e271c0b06f3d6aa25847e`  
		Last Modified: Wed, 11 Sep 2024 01:36:00 GMT  
		Size: 80.0 KB (79962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ee15bbe53851dffcbc58c1a3e915f32564f8b65a9e160c601def941717708f`  
		Last Modified: Wed, 11 Sep 2024 01:36:00 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c560223149bf3848b3fcdad5a80dfd9bcfef9f28ab7f3a9742ebc1e41fa007a7`  
		Last Modified: Wed, 11 Sep 2024 01:36:17 GMT  
		Size: 199.6 MB (199623527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19050f15129681b51c0801ebacbb46e05b615a9f8583e86ce4226781e170b91`  
		Last Modified: Wed, 11 Sep 2024 01:36:00 GMT  
		Size: 61.4 KB (61370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027810e0d232263d5fe0400e4b3e7a392b5c132c971862a9c4ec5998af9f87b4`  
		Last Modified: Wed, 11 Sep 2024 01:36:00 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-nanoserver` - windows version 10.0.17763.6293; amd64

```console
$ docker pull eclipse-temurin@sha256:e18396513a8cc310e975f11cda1fdb97b8536b17de46abaa67719a8ddb703cac
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.6 MB (358615162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb2232d73f3cd9504e2761de62a569378ebd292683d3cade7004087ce369fcd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:38:01 GMT
SHELL [cmd /s /c]
# Wed, 11 Sep 2024 01:02:38 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Wed, 11 Sep 2024 01:02:39 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 11 Sep 2024 01:02:40 GMT
USER ContainerAdministrator
# Wed, 11 Sep 2024 01:02:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Sep 2024 01:02:48 GMT
USER ContainerUser
# Wed, 11 Sep 2024 01:03:03 GMT
COPY dir:bb8037d92e17293fdab4a72c09c9eb83e6a7b620b5e832c71d656bbaf7bd694c in C:\openjdk-22 
# Wed, 11 Sep 2024 01:03:12 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 11 Sep 2024 01:03:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340318059288cbbdb326eea5b7079e789361251409038a37867d4e395c9404a5`  
		Last Modified: Wed, 11 Sep 2024 01:21:36 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c236eabf1692aa5b9df809f05092ea123d2981c2f03c8c2614a56a6dc91f38e4`  
		Last Modified: Wed, 11 Sep 2024 01:31:52 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95ad8e46da66c1f7d579def1a776f99e3b63d710d2db74aa6108b45614c19e9`  
		Last Modified: Wed, 11 Sep 2024 01:31:51 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd8eb7d82b9037502824973aead7bb4bc553b067d394f8dcb440e4bfacafd3f`  
		Last Modified: Wed, 11 Sep 2024 01:31:51 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439205c68ff44a87736d8463b1b27aa383bef80fa5013e85c4bc42a1022cdf54`  
		Last Modified: Wed, 11 Sep 2024 01:31:50 GMT  
		Size: 67.9 KB (67899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b19966c2ae318bd6bf3301b5a61b21486fb24665cd8f377895d8d3410b2ca5`  
		Last Modified: Wed, 11 Sep 2024 01:31:50 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f9de0457dbfa7facbc68d86f300ff52d56f6b54063f3b5a6cce4541f9e5a3b`  
		Last Modified: Wed, 11 Sep 2024 01:32:07 GMT  
		Size: 199.6 MB (199623959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27e6f3559f9dc715923229987f35f916a2710d9615fd391906aca5a4632e545`  
		Last Modified: Wed, 11 Sep 2024 01:31:51 GMT  
		Size: 3.8 MB (3835579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e886b85a4bf5a34b42682020fb037c94e930f6d567885192e6633cada960f8`  
		Last Modified: Wed, 11 Sep 2024 01:31:49 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
