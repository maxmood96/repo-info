## `eclipse-temurin:22-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:8c140f8a19005ffa3ee4f3a8b8381f3ed76e02c7d4fa1dc0ea9b1743c0147884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `eclipse-temurin:22-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2402; amd64

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
