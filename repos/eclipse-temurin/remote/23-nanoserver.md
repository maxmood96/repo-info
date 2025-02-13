## `eclipse-temurin:23-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:977c3eb4894dd592b2ff00eb6d34c32f752333bc4cb48a9611d817d034a6ee96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:23-nanoserver` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:7c4fe25d70b13040b2685ad29c01fcc4b512fdf3774269c60a9f1e8f80839f3b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.3 MB (408262296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa85f47b9e63f3c9465e9b782e69ecad8253a273c48ecfc525992878a5e0664`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Fri, 31 Jan 2025 02:17:27 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 02:17:27 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Fri, 31 Jan 2025 02:17:28 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 31 Jan 2025 02:17:29 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 02:17:31 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 02:17:32 GMT
USER ContainerUser
# Fri, 31 Jan 2025 02:17:39 GMT
COPY dir:0c46af2d3f44e3815e12a14e71a026bbbb77855831f9730ea0c94836a2ee7de2 in C:\openjdk-23 
# Fri, 31 Jan 2025 02:17:46 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 31 Jan 2025 02:17:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Wed, 22 Jan 2025 08:02:27 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6b5f40b86f9fb30a774131b42f8beb4b7c5e87a57f06add607abf865b77fed`  
		Last Modified: Fri, 31 Jan 2025 02:17:50 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d334c3db862cca288884361979938e08f15480be833ff7e6d72643b3ad1f49`  
		Last Modified: Fri, 31 Jan 2025 02:17:50 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5f1f35d30850044b66dfe9aa006b2e5d31ee2d1731397d2df63585bda5039a`  
		Last Modified: Fri, 31 Jan 2025 02:17:50 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6eb6d7983e1878a19431f28973091b40dbe740310b4edbc14272b2de6778426`  
		Last Modified: Fri, 31 Jan 2025 02:17:50 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9130cd2a93fade2d3e9b6ad1386174c725bfd86b343a54f7ed2b37b6d2720b96`  
		Last Modified: Fri, 31 Jan 2025 02:17:49 GMT  
		Size: 79.2 KB (79247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87790e4b98bcb47113e24effba4c67cea60e01984ae96245d0498f77545f0d76`  
		Last Modified: Fri, 31 Jan 2025 02:17:49 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d853ab627528bf0a6fcf87423d9b25bbf6a73440efd5fa65b01fd6146fcfa7ee`  
		Last Modified: Fri, 31 Jan 2025 02:18:02 GMT  
		Size: 209.0 MB (209029316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45da4b2bca5cee38d1b54febf841cd3c8d19f80f07ac07507437ccf03718f707`  
		Last Modified: Fri, 31 Jan 2025 02:17:49 GMT  
		Size: 93.2 KB (93181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c31975bd0aae60c12d932b92916e1b472f79899a3ff0817f54984fe4b79b71e`  
		Last Modified: Fri, 31 Jan 2025 02:17:49 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-nanoserver` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:0d80ee0dc25da09b4ff2a0ec7bb3c3b91213ac0419756c52fa2183b17bbcb8f6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.9 MB (329865333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5327a0013a3f43c20306c61c002627e6e8645f0a8a364053b995df1c4158188`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Fri, 31 Jan 2025 02:11:37 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 02:11:38 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Fri, 31 Jan 2025 02:11:38 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 31 Jan 2025 02:11:39 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 02:11:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 02:11:58 GMT
USER ContainerUser
# Fri, 31 Jan 2025 02:12:06 GMT
COPY dir:0c46af2d3f44e3815e12a14e71a026bbbb77855831f9730ea0c94836a2ee7de2 in C:\openjdk-23 
# Fri, 31 Jan 2025 02:12:12 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 31 Jan 2025 02:12:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Wed, 15 Jan 2025 01:24:28 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4aeecee15c4932f6ccf5fced631f60493956d32c7e0907e902d8d9311660577`  
		Last Modified: Tue, 11 Feb 2025 07:14:39 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a167c645929beda61db7270444d293efb00fac015429d142994ac5e8137d995`  
		Last Modified: Fri, 31 Jan 2025 02:12:17 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46f0877cd2b07d3e52828d7a412f8231d8bb4d38c2d62ddb395e6f40d783e0eb`  
		Last Modified: Tue, 11 Feb 2025 07:14:39 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db7f9fccfc2d0db0fbd06fe8a73b54437f82fcd014bd791e2ec3bb74a8626a2`  
		Last Modified: Fri, 31 Jan 2025 02:12:17 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7918a2b505fa6cbafbc0e1a5669c9d1b1961837915671f1daa522e677539edb4`  
		Last Modified: Tue, 11 Feb 2025 07:14:39 GMT  
		Size: 72.5 KB (72470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249d5ec76522032760e1cd0c754f7b3a7e3b620b1dacaaa9e8ddbbec995ad16c`  
		Last Modified: Fri, 31 Jan 2025 02:12:16 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8373a216a1d0ffac427364495484fb500c92cff1b4fd28db41e3c97f3d695fe4`  
		Last Modified: Tue, 11 Feb 2025 07:14:49 GMT  
		Size: 209.0 MB (209027942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87aa2796f810eb953e30cf116c3cfb42cdfddb4b207d2971a21175254337ee0`  
		Last Modified: Fri, 31 Jan 2025 02:12:16 GMT  
		Size: 97.2 KB (97171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9b49b87896fcbdc80a873c334e44af1b44acca390d65822f713e1c720883d5`  
		Last Modified: Fri, 31 Jan 2025 02:12:16 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-nanoserver` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:64c4acc3746dd534941920a48770712cfc18bc94fae7578d8bf3775dd8c0a1ed
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.5 MB (368453162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33d9d5b0451f5bf7ccface2223ef8109c13a00fa8e8c7acf5715caa960fbc5c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Fri, 31 Jan 2025 02:12:04 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 02:12:06 GMT
ENV JAVA_VERSION=jdk-23.0.2+7
# Fri, 31 Jan 2025 02:12:06 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 31 Jan 2025 02:12:07 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 02:12:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 02:12:32 GMT
USER ContainerUser
# Fri, 31 Jan 2025 02:12:46 GMT
COPY dir:0c46af2d3f44e3815e12a14e71a026bbbb77855831f9730ea0c94836a2ee7de2 in C:\openjdk-23 
# Fri, 31 Jan 2025 02:12:53 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 31 Jan 2025 02:12:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Wed, 15 Jan 2025 07:23:16 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e737ac5508e866496944da08191b6b2d78b987fca5bad30c5d4aa6f1b7bc26`  
		Last Modified: Fri, 31 Jan 2025 02:12:58 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a4ad27d258480dc73df4856594aa1a5cb488ded66223552cf150e2e7211864`  
		Last Modified: Sun, 09 Feb 2025 09:50:36 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94dd882b3de0c33394a25589360480863907bde7774dbf0c365837fedf725be0`  
		Last Modified: Sun, 09 Feb 2025 09:50:36 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6263f90d047fd028a87c9001a04418143cbf22b1b1956fb8ef32c05a5df619b3`  
		Last Modified: Fri, 31 Jan 2025 02:12:57 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34282ab5585e4c156d8a08a145f2fe02660b8c9088da22ac8abd79ec47621e98`  
		Last Modified: Sun, 09 Feb 2025 09:50:38 GMT  
		Size: 67.1 KB (67146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e524b335755bda8421873eec0fd42191a29b740c12a61e1223b81ddf3157e6ac`  
		Last Modified: Sun, 09 Feb 2025 09:50:37 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d16831d7390cabd4085ed02383f87109a04fbdc80afc8d344e9ecbe7f46dd2`  
		Last Modified: Sun, 09 Feb 2025 09:51:05 GMT  
		Size: 209.0 MB (209028178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bfd7645ac1d37b3ee701893ab1245de5b7556ab479c4a0dc3fd66aed83088d`  
		Last Modified: Sun, 09 Feb 2025 09:50:39 GMT  
		Size: 4.1 MB (4084025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c58fcd6d489f87b5f6ff7afe2224e9f0f610a2a707d0942434f1b551ef4d530`  
		Last Modified: Fri, 31 Jan 2025 02:12:56 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
