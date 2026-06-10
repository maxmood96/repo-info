## `eclipse-temurin:25-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:aa22c2c4f5a54152af8c6dd394e79a73f84fe6be7b8729b05b7f3c50833a5f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `eclipse-temurin:25-jre-nanoserver` - windows version 10.0.26100.32995; amd64

```console
$ docker pull eclipse-temurin@sha256:a5fc03d72668dad3242e699b928a00064c6d0e0664ccacf84cc4f0051ad4f595
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255470334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6cf113898edb9a4d641b20059be69072041f588c8755fcec3f459ea2d3e1d08`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 07:06:15 GMT
RUN Apply image 10.0.26100.32995
# Tue, 09 Jun 2026 23:18:08 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2026 23:19:09 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 09 Jun 2026 23:19:10 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 09 Jun 2026 23:19:10 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2026 23:19:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Jun 2026 23:19:12 GMT
USER ContainerUser
# Tue, 09 Jun 2026 23:20:26 GMT
COPY dir:fd8baea77fa86bd13952f69621f69e815eb87406af0c0441c94fb1b8a78482df in C:\openjdk-25 
# Tue, 09 Jun 2026 23:20:29 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:64f5cd94d3bcd0fae94830b1fad0f8b3dc33677f8d7dc15c5219b56fe2a6584e`  
		Last Modified: Tue, 09 Jun 2026 22:11:30 GMT  
		Size: 196.7 MB (196668131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee5a15e6c0ae33d8458f16b5e982a3e6eb3be95d54d8918eb8862671f3dd652`  
		Last Modified: Tue, 09 Jun 2026 23:18:35 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d434ce39a94cb42837489ac5f874e842e95c28229676a028d0657e3ddc3d013`  
		Last Modified: Tue, 09 Jun 2026 23:19:41 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1464cd31e07129fb4c5043089b75fe7aa75ede3af2d22f3f457c5c3b4f0ecd4d`  
		Last Modified: Tue, 09 Jun 2026 23:19:41 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864e1450bf94e58601592313310a4e3629bfde4f1201241a37247e2be054168f`  
		Last Modified: Tue, 09 Jun 2026 23:19:41 GMT  
		Size: 1.0 KB (1009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa44cbfb3f8bad29f9e0693678d2233155c291af9be0c4d889bb258191e6557`  
		Last Modified: Tue, 09 Jun 2026 23:19:40 GMT  
		Size: 72.1 KB (72143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4074c51f5bb1638e60bae7da2d292dcba51153746120d25d4ba4d89c8cd3bc`  
		Last Modified: Tue, 09 Jun 2026 23:19:39 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0c8b9076860f258799fe381029ad2830d9edac336b1cd3102e80bcf8992830`  
		Last Modified: Tue, 09 Jun 2026 23:20:41 GMT  
		Size: 58.6 MB (58620328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9346b1f13af12bcaf732684338c0aa5d91937fd764109f79edf58c8bfcbe88ff`  
		Last Modified: Tue, 09 Jun 2026 23:20:33 GMT  
		Size: 104.6 KB (104556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:25-jre-nanoserver` - windows version 10.0.20348.5256; amd64

```console
$ docker pull eclipse-temurin@sha256:c1ddd640c64fcf7e189e0056e3ee4a2131a7393454ffb0785df8464644aed97f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182811988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295df5ba92c07832b54e5596b20ffb8970f32af45b7b53d1a2793bcf76900a4e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 06:26:15 GMT
RUN Apply image 10.0.20348.5256
# Tue, 09 Jun 2026 23:21:49 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2026 23:22:39 GMT
ENV JAVA_VERSION=jdk-25.0.3+9
# Tue, 09 Jun 2026 23:22:39 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 09 Jun 2026 23:22:40 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2026 23:22:42 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Jun 2026 23:22:43 GMT
USER ContainerUser
# Tue, 09 Jun 2026 23:22:53 GMT
COPY dir:fd8baea77fa86bd13952f69621f69e815eb87406af0c0441c94fb1b8a78482df in C:\openjdk-25 
# Tue, 09 Jun 2026 23:22:56 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:8fc8662767a8f63038f8f45ce82f52438fd89b4444ed43648c9e6a7f06330686`  
		Last Modified: Tue, 09 Jun 2026 17:48:06 GMT  
		Size: 124.0 MB (123997505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e97e8b9098cc4d050c642b320fe6d5a7ddda866e0c41c7a307e5ca8734409b`  
		Last Modified: Tue, 09 Jun 2026 23:22:09 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4ac2226abdf401f6a9f19ad659e88e229401ad2eec8f154d29869b7df5634d`  
		Last Modified: Tue, 09 Jun 2026 23:23:02 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7891d3419bc79115a202f01b799fcf2d4e246dd786406bd1ddbaa8e720f4d2f0`  
		Last Modified: Tue, 09 Jun 2026 23:23:02 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be63db47c9ff52a29796782e2b7898c67a996cc667aeaedb470c48840295879`  
		Last Modified: Tue, 09 Jun 2026 23:23:00 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc63edcdf4f79f38a787da1e8ed698735412a27968edc3afd287626999f0a30`  
		Last Modified: Tue, 09 Jun 2026 23:23:00 GMT  
		Size: 85.8 KB (85789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04716c18d4f2d34e6128b3f850ff5dc1e710d4c528e1a8f261f63abbe914ea9`  
		Last Modified: Tue, 09 Jun 2026 23:23:00 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5638800a1e4d2076308ab89d41ac4892f89156afac6d3d69ad031949874593`  
		Last Modified: Tue, 09 Jun 2026 23:23:08 GMT  
		Size: 58.6 MB (58619917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5035a31724b9a6295ce5f191bed2d2d039b642e9057ecc6e4cce8e73d4a40dc2`  
		Last Modified: Tue, 09 Jun 2026 23:23:00 GMT  
		Size: 103.5 KB (103489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
