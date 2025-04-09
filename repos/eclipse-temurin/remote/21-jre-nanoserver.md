## `eclipse-temurin:21-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:a676140243613ea4f1dff1ff704716e68d59d7780968ce7b9efc8d93bd6b33d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.26100.3775; amd64

```console
$ docker pull eclipse-temurin@sha256:2883c1e45a1f3efe744762baf054e46d045ea544219665d5297f1722b75db316
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.2 MB (239228880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dd52d1e81c5e42054b29c4d9aa6307503c57b87cd36f6f801665fd14a28e0fc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Apr 2025 07:26:08 GMT
RUN Apply image 10.0.26100.3775
# Wed, 09 Apr 2025 01:17:58 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:17:58 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Wed, 09 Apr 2025 01:17:59 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 09 Apr 2025 01:18:00 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:18:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:18:03 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:18:07 GMT
COPY dir:c0b7c132c85049081486a93cd76fe016c559b0b921796f63592a768b082ae9e2 in C:\openjdk-21 
# Wed, 09 Apr 2025 01:18:11 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:79b2ed45f890e91d23d7d22491a8fb6909c9268c668dc6a0e3b40131da02ed74`  
		Last Modified: Wed, 09 Apr 2025 00:36:30 GMT  
		Size: 190.1 MB (190113206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01399613f2c93f045104a55047ac020d1c85f721bccb9770a01b50c8a71c01d3`  
		Last Modified: Wed, 09 Apr 2025 01:18:17 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef0f99b87da67075440ff4b47430d7c7b9e2132e3526443a8403f15c92acbc2`  
		Last Modified: Wed, 09 Apr 2025 01:18:17 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a17943be4be3c6267dcc1c4eb4c9e89bc8c235fdd6a4cc742b81257fae6a5d8`  
		Last Modified: Wed, 09 Apr 2025 01:18:17 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a038192a4d762b26824c222869b6e476edb5bbe41eaa2c5b29e47873893d13f7`  
		Last Modified: Wed, 09 Apr 2025 01:18:15 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72af05e7dea4a3c392be36a9328a6a91e8863e3f36f844ebc5d9d05eaa83a9a9`  
		Last Modified: Wed, 09 Apr 2025 01:18:15 GMT  
		Size: 76.1 KB (76123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf952cd3aedcf96015490c0f5136d177846f265e79b1c2d11748bf7d749e6e3`  
		Last Modified: Wed, 09 Apr 2025 01:18:15 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044212d0f5f2731209febaeecdb648571e60b46e8fcbc1cf80d96d8f6c82a994`  
		Last Modified: Wed, 09 Apr 2025 01:18:21 GMT  
		Size: 48.9 MB (48940549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a11761655603bfc285b6cbcdab2d639912342a7a28f90307ef1dcb51025f5b`  
		Last Modified: Wed, 09 Apr 2025 01:18:15 GMT  
		Size: 93.8 KB (93773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.20348.3453; amd64

```console
$ docker pull eclipse-temurin@sha256:8863bf40cbe6bce65f2232b1c5ebe71ab19dda414ce05f12b60b610816d08275
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.9 MB (169857994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08348961e2ab0b967a3c182f398a19b68d68a447b21d9be293c5297ae6c30cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Apr 2025 22:57:50 GMT
RUN Apply image 10.0.20348.3453
# Wed, 09 Apr 2025 01:22:29 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:22:30 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Wed, 09 Apr 2025 01:22:31 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 09 Apr 2025 01:22:31 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:22:34 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:22:34 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:22:39 GMT
COPY dir:c0b7c132c85049081486a93cd76fe016c559b0b921796f63592a768b082ae9e2 in C:\openjdk-21 
# Wed, 09 Apr 2025 01:22:44 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:5caa30147a287e99992660f7f85276c53fe3299503a06c47d476387410721453`  
		Last Modified: Wed, 09 Apr 2025 01:13:36 GMT  
		Size: 120.7 MB (120736312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23404123b46aa3beaa1c038fe5e51576fe1d9ada488308744d194edd17e974f7`  
		Last Modified: Wed, 09 Apr 2025 01:22:48 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ba376caa405f610a2d0e102b6844ecdab2a85a3471a047891cdd0bf397f798`  
		Last Modified: Wed, 09 Apr 2025 01:22:47 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da77ad8a01a2dc8ffb1221dda404789bcebcb121d242789d99ca6a6a74b43e45`  
		Last Modified: Wed, 09 Apr 2025 01:22:47 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c868425b713bbb80bdf33eb132be89f1eea406eda3b1664856b74ca212e336c`  
		Last Modified: Wed, 09 Apr 2025 01:22:46 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb487723b55022486001621bd321a5444e96eb4bde942b253be1e61cb1624d19`  
		Last Modified: Wed, 09 Apr 2025 01:22:46 GMT  
		Size: 76.6 KB (76608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5be79e3655ba947f89775f4c0e0671a38e5e352c528250306cd5bb88850754`  
		Last Modified: Wed, 09 Apr 2025 01:22:46 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b74224e4d54e85f4ec60a5f38ee6db07e231c744d7f067c0ef8c2ff48c0ef1`  
		Last Modified: Wed, 09 Apr 2025 01:22:52 GMT  
		Size: 48.9 MB (48941160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d27d1eb433502bd1d44d69b3817bd96c40c346fa8ac2cbf89e9419e5ae41e30`  
		Last Modified: Wed, 09 Apr 2025 01:22:46 GMT  
		Size: 98.5 KB (98537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.17763.7136; amd64

```console
$ docker pull eclipse-temurin@sha256:8ddc39fc6d5de2a10fa09cea63c637bee55fd0ec9f8b41cb242ca7b8da3e6133
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159305009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b40df849f8c460a52c1812f6e9604f0b9c305f72ffe819eb5ec53c5e8ef1f76`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Apr 2025 01:31:28 GMT
RUN Apply image 10.0.17763.7136
# Wed, 09 Apr 2025 02:48:34 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 02:48:36 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Wed, 09 Apr 2025 02:48:37 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 09 Apr 2025 02:48:37 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 02:48:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 02:48:40 GMT
USER ContainerUser
# Wed, 09 Apr 2025 02:48:44 GMT
COPY dir:c0b7c132c85049081486a93cd76fe016c559b0b921796f63592a768b082ae9e2 in C:\openjdk-21 
# Wed, 09 Apr 2025 02:48:48 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:a06e0965a0fa3715e629889bd9332aa22aadd75654cac5c9818b67c0264b3ee1`  
		Last Modified: Tue, 08 Apr 2025 20:16:02 GMT  
		Size: 106.9 MB (106922524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae59fc3d956527eb385790dd6757c2506944546c5fd7b1f844b253b0677907a3`  
		Last Modified: Wed, 09 Apr 2025 02:48:52 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a60c465d39daa356fe1ff52c6fc848caa3a9cfeb8369ef2b573dd057afc8a1b`  
		Last Modified: Wed, 09 Apr 2025 02:48:52 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c938cb4b933193118295a11996328ac1633cf05a9711ed7de139d6d274fe2a3`  
		Last Modified: Wed, 09 Apr 2025 02:48:52 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b63e86600b2dfb7a27186010e1339a699e256e783a7695c347c037c195e13e`  
		Last Modified: Wed, 09 Apr 2025 02:48:51 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0dae61f3582cf7a520911ddfc21c039b34b2abc5618f0745274a11da66df536`  
		Last Modified: Wed, 09 Apr 2025 02:48:51 GMT  
		Size: 71.4 KB (71447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628e8c2df97e98be5b729aad1b85e8b08bdf6d04a76a0425a2efcd08b9d5dee9`  
		Last Modified: Wed, 09 Apr 2025 02:48:51 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93bd191a34d864c7030cad792d38739dda38b0ad7d1f6e9df3b8d570f9b33ad7`  
		Last Modified: Wed, 09 Apr 2025 02:48:57 GMT  
		Size: 48.9 MB (48941122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f858c3db20c1296e5f6a402fe2ff42363b0c7c53764209dbc13d0658589ce17`  
		Last Modified: Wed, 09 Apr 2025 02:48:52 GMT  
		Size: 3.4 MB (3364697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
