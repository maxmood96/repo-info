## `eclipse-temurin:22-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:4256429ec8836cbbc32f39e833b9855c762d3d7fa45e82b326a5fc05c21b6b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `eclipse-temurin:22-jre-nanoserver` - windows version 10.0.20348.2402; amd64

```console
$ docker pull eclipse-temurin@sha256:12c8636744ac1c0cd0c44ed8bf8ab3ba9be276a241c9d2564d93cd9630e81895
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.6 MB (169620646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec69ed9249a8205610c80296fa59ed5d898263d388ace9fbdb6d9c69adaae72`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Apr 2024 08:53:11 GMT
RUN Apply image 10.0.20348.2402
# Wed, 10 Apr 2024 00:34:53 GMT
SHELL [cmd /s /c]
# Wed, 24 Apr 2024 19:28:21 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Wed, 24 Apr 2024 19:28:22 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 24 Apr 2024 19:28:22 GMT
USER ContainerAdministrator
# Wed, 24 Apr 2024 19:28:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Apr 2024 19:28:34 GMT
USER ContainerUser
# Wed, 24 Apr 2024 19:29:22 GMT
COPY dir:b356dfbfb05ab2ab46133b6b7ad4e4cb6a7442df8599937d6806166f02780fa5 in C:\openjdk-22 
# Wed, 24 Apr 2024 19:29:34 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:755fc767289b8847bd0d0d8d75efc308c040140acf2a3426973ba9fbf022c4c0`  
		Last Modified: Tue, 09 Apr 2024 23:50:18 GMT  
		Size: 121.0 MB (120993754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70887eeae6a5d6d5fd81661024afc84fee637f674dee5e7127112cbfce90750`  
		Last Modified: Wed, 10 Apr 2024 01:00:01 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54e00206cef5e76da3486dde342f4a50eb01cc49b8c1042b7701342348b7255`  
		Last Modified: Wed, 24 Apr 2024 19:49:11 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acdffbb40e6de7011c4567368181f7e153429174910a93038c555799fbdc511`  
		Last Modified: Wed, 24 Apr 2024 19:49:11 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d38fce880c0326fcf2b6af9ae5e85d7a617eaf1ffe97825619c4caf9bed4de`  
		Last Modified: Wed, 24 Apr 2024 19:49:11 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4131893637a6e4817646c84b0cf0afc69b50df6c8b33a5e8070696e2335855`  
		Last Modified: Wed, 24 Apr 2024 19:49:09 GMT  
		Size: 79.9 KB (79911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb232994dc1be2b521d2770debb36a482c6c3833f2201fc1ed14434e306e8d0`  
		Last Modified: Wed, 24 Apr 2024 19:49:09 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc0bc4e7288d1c168844093f10b8fa6086316d93034d4389e1ba0f26b6a1bf9e`  
		Last Modified: Wed, 24 Apr 2024 19:49:50 GMT  
		Size: 48.5 MB (48487999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7517d1e50b5abaf9e18e14b2c9c0fcbe93c37ad2a4455c318d2aaded82801138`  
		Last Modified: Wed, 24 Apr 2024 19:49:41 GMT  
		Size: 53.3 KB (53325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-jre-nanoserver` - windows version 10.0.17763.5696; amd64

```console
$ docker pull eclipse-temurin@sha256:6da5773d8b69d71f981613e1874d36c8acb1e38d50a5797c749a7d711e8cdf5d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.8 MB (156819387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded7d09b9ef5c03f84d101b63402f6a3e7a1f1627f1886be7f43ba0e46ca5bde`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Tue, 09 Apr 2024 23:42:55 GMT
SHELL [cmd /s /c]
# Wed, 24 Apr 2024 19:16:44 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Wed, 24 Apr 2024 19:16:45 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 24 Apr 2024 19:16:45 GMT
USER ContainerAdministrator
# Wed, 24 Apr 2024 19:16:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Apr 2024 19:16:56 GMT
USER ContainerUser
# Wed, 24 Apr 2024 19:22:15 GMT
COPY dir:b356dfbfb05ab2ab46133b6b7ad4e4cb6a7442df8599937d6806166f02780fa5 in C:\openjdk-22 
# Wed, 24 Apr 2024 19:22:28 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b591b5f81c02344da39dc8a9084b5791cbf552c1eb85e79db1f38dfc715a681`  
		Last Modified: Wed, 10 Apr 2024 00:47:46 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99162cf301795a2934b58cb175b4b9bd833ba4ef022bdf311a3f5b6d4253f33`  
		Last Modified: Wed, 24 Apr 2024 19:44:34 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e333a85e4f99df6b7264ead3c9f8fc3447fc23c4a3283ca9a48b984c2213ed`  
		Last Modified: Wed, 24 Apr 2024 19:44:34 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92c1295a14273c026102afacdde9b5d3af241cc9b1e82084b9123fd995bf59b`  
		Last Modified: Wed, 24 Apr 2024 19:44:33 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cecf7884caa59b9e435973a173d2f68fcc934dc652a84735cd11fe9c51e8ed`  
		Last Modified: Wed, 24 Apr 2024 19:44:32 GMT  
		Size: 64.1 KB (64142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04fdbc0e3b8be01e12d59ba00b6ec0dcf8b86b227d058381f045173a941252b`  
		Last Modified: Wed, 24 Apr 2024 19:44:31 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028dd2e25fbdf916c4b2b1352db76dbf5f6c369e5a631f30f3211d4f0aee88b8`  
		Last Modified: Wed, 24 Apr 2024 19:45:57 GMT  
		Size: 48.5 MB (48487696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cd6916cf95a86dab65876b3556ea59030e0e1450160360385b36c8b6c4e9a0`  
		Last Modified: Wed, 24 Apr 2024 19:45:48 GMT  
		Size: 3.4 MB (3373161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
