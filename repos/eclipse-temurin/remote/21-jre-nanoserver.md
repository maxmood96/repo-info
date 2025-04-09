## `eclipse-temurin:21-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:9f6b205469e9c74cbb7308c66cb8659ef57e84f862d92ca0ea84a4002d733738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7009; amd64

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

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull eclipse-temurin@sha256:1332509bda2f2c8ca3afd0351f327521cf9dbdec518cb96477e437ad3d6ec335
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159294181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b52d811aea392bc6702042aee76f354d87c54e6c32fc73c85409c0cb8f1566`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Wed, 12 Mar 2025 19:17:31 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:17:33 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Wed, 12 Mar 2025 19:17:34 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 12 Mar 2025 19:17:34 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:17:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:17:38 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:17:42 GMT
COPY dir:c0b7c132c85049081486a93cd76fe016c559b0b921796f63592a768b082ae9e2 in C:\openjdk-21 
# Wed, 12 Mar 2025 19:17:46 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f348ec31fb415c72de1fe5d9bead7b72e79fdea52c1fbf873cfe2968a12f145`  
		Last Modified: Wed, 12 Mar 2025 19:17:51 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a6e0db99e71cc00e09e21e082b4d2e7928a095680af042db76f80ebbe60bf5`  
		Last Modified: Wed, 12 Mar 2025 19:17:51 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea74402b9c0815bdd86961d6395a401a74b2722e949e5ec8a9ecffb75da687c7`  
		Last Modified: Wed, 12 Mar 2025 19:17:51 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a0cf7792a9544429a3fde9cac8e446ab42d27fb6ad8a7ab7f3c160dc602235`  
		Last Modified: Wed, 12 Mar 2025 19:17:49 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5b33de4bf5cdd2254a4a1aa99e18f43624a57e757f71c8eaa02643cac3188e`  
		Last Modified: Wed, 12 Mar 2025 19:17:49 GMT  
		Size: 69.6 KB (69592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d005618b8d7f8b04b9d824a922f5ca5232ba93a7faaf06e249de24311ed421`  
		Last Modified: Wed, 12 Mar 2025 19:17:49 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5c40a5c05593d44dad5e15652e503eaaa28b8f002f086563b31ae55a65ec97`  
		Last Modified: Wed, 12 Mar 2025 19:17:55 GMT  
		Size: 48.9 MB (48940927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a95225247050ce916d02689338c79c470f1db12d6061d864e773570cda584b`  
		Last Modified: Wed, 12 Mar 2025 19:17:50 GMT  
		Size: 3.4 MB (3370779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
