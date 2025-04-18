## `eclipse-temurin:11-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:0f3c304a176bb20dbca68d6a452c1e5f3ff259ad6c005b04f9aa44bb9be2a6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.26100.3781; amd64

```console
$ docker pull eclipse-temurin@sha256:e62c1b66a76b7c6a87402255f1aa71b7f00ed64978929baedc1bdcf9a0a0062b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.9 MB (384907912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc6953d68acc28ace2f8c17bf38a91b010bd8a33b5aa9e937ad518f9bff2adb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Fri, 18 Apr 2025 04:15:36 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:15:37 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Fri, 18 Apr 2025 04:15:38 GMT
ENV JAVA_HOME=C:\openjdk-11
# Fri, 18 Apr 2025 04:15:39 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:15:42 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:15:43 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:15:52 GMT
COPY dir:9a97e9a1ce762bb8542962ee0a2b0ca6fa379668e092b80acfc01b297b3b57a6 in C:\openjdk-11 
# Fri, 18 Apr 2025 04:15:59 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 18 Apr 2025 04:16:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 17 Apr 2025 02:52:17 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0b217e025e8405ef036eec547182d9b49b3a0943a14d9ad0a1713213f9a13b`  
		Last Modified: Fri, 18 Apr 2025 04:16:03 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7308e44a838c1fcefde8f963d3d8f3f262a89151a46d5581c01212e692ef06`  
		Last Modified: Fri, 18 Apr 2025 04:16:03 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea876a1b6afdf7742842a695eb0d34e0feb0745d1cbbdbe908de92624d824f33`  
		Last Modified: Fri, 18 Apr 2025 04:16:03 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b4e4dd7903d968b88779facb00249285d65dbce54dffdc59ed3973f6841158`  
		Last Modified: Fri, 18 Apr 2025 04:16:03 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1de73c22013dece0db770538c31bdc807c5f849ce90391a74584d2cd0ec6e7`  
		Last Modified: Fri, 18 Apr 2025 04:16:02 GMT  
		Size: 76.4 KB (76420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6dc4d8821281b7093717ab12951574efef3ea3010e6b17f3e2fc7affd91328`  
		Last Modified: Fri, 18 Apr 2025 04:16:02 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e4514419b8632d562d02e28d18fc01d74caca0b7bdeab803900537d9dd52e4`  
		Last Modified: Fri, 18 Apr 2025 04:16:12 GMT  
		Size: 194.6 MB (194557358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bea31128082eb6d749b2a7938aea5574620c8179f16deac5eb216d7ea779013`  
		Last Modified: Fri, 18 Apr 2025 04:16:02 GMT  
		Size: 125.9 KB (125865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3db1b73e8a40a628670dd6efd7ad993ec8b71948a6f57fe72c38ed02985da8a`  
		Last Modified: Fri, 18 Apr 2025 04:16:02 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:e4de637974f70460651d5fea6ab58e601d67b0e2f6d25766c6a1e6c8617dee0c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.3 MB (317288538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c631ba08ea43fc2f41086b2c75eb3e72c74bac46f8b3546209bb893e3cc932`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Fri, 18 Apr 2025 04:20:15 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:20:16 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Fri, 18 Apr 2025 04:20:17 GMT
ENV JAVA_HOME=C:\openjdk-11
# Fri, 18 Apr 2025 04:20:17 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:20:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:20:20 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:20:28 GMT
COPY dir:9a97e9a1ce762bb8542962ee0a2b0ca6fa379668e092b80acfc01b297b3b57a6 in C:\openjdk-11 
# Fri, 18 Apr 2025 04:20:34 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 18 Apr 2025 04:20:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2e338753d274d117fd77fac167028fe73f9d3e057a6f9ae12e3bc22dee45a2`  
		Last Modified: Fri, 18 Apr 2025 04:20:39 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743d2d559648cdd490d0784be2361825aa0f940325540d55b7b8fd6cbb4e3d60`  
		Last Modified: Fri, 18 Apr 2025 04:20:39 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1b8150b6d1af5350b390f88e9325444568d3d80ec742c8ddbaa8a66fff3734`  
		Last Modified: Fri, 18 Apr 2025 04:20:39 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f921f27c98c380b1aac572a1549ff2ad64dc3cd5108cff45b425633a9f78ec`  
		Last Modified: Fri, 18 Apr 2025 04:20:39 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac32e73a5e488c12cca128a5ad6d240bff29774dee18290127b6350ca0bb3b6`  
		Last Modified: Fri, 18 Apr 2025 04:20:38 GMT  
		Size: 78.3 KB (78335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6594cdb2638d2979d2998501d7cabf8b71557823c652f88d611e69e820942b8`  
		Last Modified: Fri, 18 Apr 2025 04:20:38 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd03706d13c3663503ca642a189fde21b3b153811a1a69b76936535ca5c92eb`  
		Last Modified: Fri, 18 Apr 2025 04:20:48 GMT  
		Size: 194.6 MB (194557050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd44006fe69f762e0e949f6d5e74f70394ee1ed63875afc883cd6ce0176493f`  
		Last Modified: Fri, 18 Apr 2025 04:20:38 GMT  
		Size: 107.7 KB (107700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b669a45eff72f2ff5a4003b9c40ef7791c4d69563954addda4dc9fbc0b1bfaa`  
		Last Modified: Fri, 18 Apr 2025 04:20:38 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.17763.7249; amd64

```console
$ docker pull eclipse-temurin@sha256:3755b93acbb4dee856fafa87ec655c701a491a37c9783a340f3c44f787adf4f4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.5 MB (303477812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f15f6d99a7d11dc67dd9744368f6bdc1ac15e9003ff072162efa857d1ef8691`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:17:32 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:17:34 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Fri, 18 Apr 2025 04:17:35 GMT
ENV JAVA_HOME=C:\openjdk-11
# Fri, 18 Apr 2025 04:17:36 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:17:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:17:39 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:17:47 GMT
COPY dir:9a97e9a1ce762bb8542962ee0a2b0ca6fa379668e092b80acfc01b297b3b57a6 in C:\openjdk-11 
# Fri, 18 Apr 2025 04:17:52 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 18 Apr 2025 04:17:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325a99aa1a9a0b042e06a5f98805176ea96b4746f16132a8a9fc5b48084db324`  
		Last Modified: Fri, 18 Apr 2025 04:17:56 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a33e4e3ef58a1e4abd494bb415364d5baf8aac0b7c38dd5e7daa04ad83e784`  
		Last Modified: Fri, 18 Apr 2025 04:17:56 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3653fdb29c5cf95a1233655090701afe15a5ff85a0da129093baeff4e3ac9aae`  
		Last Modified: Fri, 18 Apr 2025 04:17:56 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f6843d060d4086a8d2640e5a3193753fdfb92b38eeb7c9fa9539d0eae3a6e9`  
		Last Modified: Fri, 18 Apr 2025 04:17:56 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc62a8073c5a684ab1b6b24803ce5a99fc802561787c8eb0d96e665dda25bca9`  
		Last Modified: Fri, 18 Apr 2025 04:17:55 GMT  
		Size: 70.6 KB (70584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aafda8821e7bb8e4d8750b67ff412182073681e28364417bad7152ab479b645`  
		Last Modified: Fri, 18 Apr 2025 04:17:55 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbef775813a9c35ad86a28a8688772d04ffcf5ea7b4cfe29a8c50a812ba8a5a4`  
		Last Modified: Fri, 18 Apr 2025 04:18:05 GMT  
		Size: 194.6 MB (194556390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3347ea6fdd6dc5b46a68d8a1b6a6b88470a98f2a61032d46d909fc6d66804677`  
		Last Modified: Fri, 18 Apr 2025 04:17:55 GMT  
		Size: 92.4 KB (92382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1829adb57324eb40bfd635b64204488a2866c66d6e8ed7fd8e8a9b68fda611`  
		Last Modified: Fri, 18 Apr 2025 04:17:55 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
