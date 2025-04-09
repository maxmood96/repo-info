## `eclipse-temurin:24_36-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:dfadf3287386b56c89fc03de3f826ebac833602dc46def6e5047fa409994496d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `eclipse-temurin:24_36-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3453; amd64

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
