## `eclipse-temurin:24-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:4c0d332e9c74301d5ec5f64f04cb259d3eb5564c6c0c652bac74e770389a7b0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:24-jdk-nanoserver` - windows version 10.0.26100.3775; amd64

```console
$ docker pull eclipse-temurin@sha256:3bbc3e3bd864ec3b776ce4faf3227c79fe3a1fb715fc447a0c6902d0e89ec7a8
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.6 MB (327646860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98392ed01f6fc59d57444de32550c17b7caac53d7d73e68044e9517010f720df`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Apr 2025 07:26:08 GMT
RUN Apply image 10.0.26100.3775
# Wed, 09 Apr 2025 01:18:16 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:18:17 GMT
ENV JAVA_VERSION=jdk-24+36
# Wed, 09 Apr 2025 01:18:18 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 09 Apr 2025 01:18:19 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:18:22 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:18:23 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:18:31 GMT
COPY dir:82098476e422c0fd1b27846be91131b5a5073542830e51603132b80cd94d4318 in C:\openjdk-24 
# Wed, 09 Apr 2025 01:18:38 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Apr 2025 01:18:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:79b2ed45f890e91d23d7d22491a8fb6909c9268c668dc6a0e3b40131da02ed74`  
		Last Modified: Wed, 09 Apr 2025 00:36:30 GMT  
		Size: 190.1 MB (190113206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49afa67ee8fbfc00c93f889d47ed7a472fdc767a94d580f3f169dafe6c3cfa2`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d3e42f13e523cf73059c3b59e2adeea54050c54049bb5f18bc97df5b12c1f0`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493a3871065d26b8e44f6008e4bc5a76006909cb8192cf15a980b14d2e13aa6d`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe276d3de633e8ca8be2e6abb8d9897fb753c6989cb4d967eb66da1708cc17e3`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7be48ba4e61770f2a54495e23132a0eca0273c3be120057996889650469a4dc`  
		Last Modified: Wed, 09 Apr 2025 01:18:41 GMT  
		Size: 77.6 KB (77571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f728c86efa53c02cf32345e2429b5358af46348efe09fefab946872cafcfce9`  
		Last Modified: Wed, 09 Apr 2025 01:18:41 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a773a527c3f916b3ffaaece8264c65345dee34f322a15d5bc83616f12df909`  
		Last Modified: Wed, 09 Apr 2025 01:18:52 GMT  
		Size: 137.4 MB (137355571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba764c8af9f3a294ae2dd71e7137bbb2a7cf69009a58114f4a5f77a58bd8ed77`  
		Last Modified: Wed, 09 Apr 2025 01:18:41 GMT  
		Size: 94.2 KB (94246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c7ae72265d75f6229747ed6be8eb9035f5b4433b80de20ac34583d1d5359c10`  
		Last Modified: Wed, 09 Apr 2025 01:18:41 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:24-jdk-nanoserver` - windows version 10.0.20348.3453; amd64

```console
$ docker pull eclipse-temurin@sha256:4bf2300ef01a762b4cdce20c8559a5ee3b832c97b4a31e719d83056ded799899
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 MB (258283375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9429174889f0ce76b21c63d60b2f1bfbc468d49855ffd3d970061650d00936d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Apr 2025 22:57:50 GMT
RUN Apply image 10.0.20348.3453
# Wed, 09 Apr 2025 03:23:04 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 03:23:05 GMT
ENV JAVA_VERSION=jdk-24+36
# Wed, 09 Apr 2025 03:23:06 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 09 Apr 2025 03:23:07 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 03:23:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 03:23:10 GMT
USER ContainerUser
# Wed, 09 Apr 2025 03:23:16 GMT
COPY dir:82098476e422c0fd1b27846be91131b5a5073542830e51603132b80cd94d4318 in C:\openjdk-24 
# Wed, 09 Apr 2025 03:23:22 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Apr 2025 03:23:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5caa30147a287e99992660f7f85276c53fe3299503a06c47d476387410721453`  
		Last Modified: Wed, 09 Apr 2025 01:13:36 GMT  
		Size: 120.7 MB (120736312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53544d368e00e4889b4048eea5da485e332af34e3732759ebf10db0cefa53bc4`  
		Last Modified: Wed, 09 Apr 2025 03:23:26 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e890853897b6c268ace6d3b20da988c9d85a0c0adb0f0c7e5b38cec722abecf`  
		Last Modified: Wed, 09 Apr 2025 03:23:26 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbd650df70cdb8b90e55d45ac1146596648dbf98d71bc483e43a34bb0f09294`  
		Last Modified: Wed, 09 Apr 2025 03:23:26 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497c1bf08c047c50e98b65f2233b319bb9ceec754976cae1ccf8c7ae1fb1ba68`  
		Last Modified: Wed, 09 Apr 2025 03:23:26 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1cbefaebda5890807556bbcab9999d0a8bbb2608cbdfb1f01825157827a2a3`  
		Last Modified: Wed, 09 Apr 2025 03:23:25 GMT  
		Size: 78.6 KB (78644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ccab3e3df286bed0d85ec279c400052c365c01279d8169fa5bb599b3e925ee`  
		Last Modified: Wed, 09 Apr 2025 03:23:25 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea53424b3aabdb0a88a4a889cf199fc6c3e5d496b9756b4fd390cd32d9bee54e`  
		Last Modified: Wed, 09 Apr 2025 03:23:36 GMT  
		Size: 137.4 MB (137355259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e648837a4c97551dda79dae6a1e6f4e5efea313a1ea6039fd8b8d28d617235`  
		Last Modified: Wed, 09 Apr 2025 03:23:25 GMT  
		Size: 107.0 KB (107002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d34858a36b4dc377a3bbb86f0a8208fd4abca5a91cc686bd34ec7f06b531aa9`  
		Last Modified: Wed, 09 Apr 2025 03:23:25 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:24-jdk-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull eclipse-temurin@sha256:a0553dbe1c4406e7c4b677c1f915fddee600fbf45d9992129a0b4ccb73f62fda
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.7 MB (248740091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c2c8d17ce2a1307d0c67396ed39a2426b2290146e8afad638e402877e0b623`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Tue, 25 Mar 2025 23:14:57 GMT
SHELL [cmd /s /c]
# Tue, 25 Mar 2025 23:15:00 GMT
ENV JAVA_VERSION=jdk-24+36
# Tue, 25 Mar 2025 23:15:00 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 25 Mar 2025 23:15:01 GMT
USER ContainerAdministrator
# Tue, 25 Mar 2025 23:15:03 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 25 Mar 2025 23:15:04 GMT
USER ContainerUser
# Tue, 25 Mar 2025 23:15:11 GMT
COPY dir:82098476e422c0fd1b27846be91131b5a5073542830e51603132b80cd94d4318 in C:\openjdk-24 
# Tue, 25 Mar 2025 23:15:17 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 25 Mar 2025 23:15:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d870e42e7f6c7d99a4db68ec41feb180a4f0eb340ba043353d93752fc4aa5f3`  
		Last Modified: Tue, 25 Mar 2025 23:15:23 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1863918c094b9495e054f76ec871fb75161dedaae8fc03ffed0f6e414952833a`  
		Last Modified: Tue, 25 Mar 2025 23:15:22 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e89ee47c80546632a1b01a7ad5a332f48d1645836837b9200fea8e4e9fb944`  
		Last Modified: Tue, 25 Mar 2025 23:15:22 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc4a27e48af860be19436024decfab0152b011ef1ebc390e11d8d11ced061a3`  
		Last Modified: Tue, 25 Mar 2025 23:15:22 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb6875e454342557657bbb77921bb05e0af7d038946343eb435260340035648`  
		Last Modified: Tue, 25 Mar 2025 23:15:21 GMT  
		Size: 69.8 KB (69753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3a49255455a5ebeafcdf8db812a0e1e71f834773641c89c0f2c41ccd47c46f`  
		Last Modified: Tue, 25 Mar 2025 23:15:21 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb71b271686991f336591f6e191f7665b6ced81a998f829cce05005940af9ca`  
		Last Modified: Tue, 25 Mar 2025 23:15:32 GMT  
		Size: 137.4 MB (137354928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13a0676d6fdbef7bdedf6cd62b48d6b84a9bbc20d1caa2aa864740e5fcacebf`  
		Last Modified: Tue, 25 Mar 2025 23:15:21 GMT  
		Size: 4.4 MB (4401317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4865b5f4e44b21eaebd875f1faeeeb14ca7dfbee5d9687c5c86064e98844d597`  
		Last Modified: Tue, 25 Mar 2025 23:15:21 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
