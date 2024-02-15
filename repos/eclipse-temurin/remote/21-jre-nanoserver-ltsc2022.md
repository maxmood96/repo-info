## `eclipse-temurin:21-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:13b4c68cb57f75826021304f8960dafba977be8f8f320e3f714f4039c0b8ce44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull eclipse-temurin@sha256:84849250853f70ce6552788f72632dcb8b90d66f850c6d4e2e154bfefd4b9f55
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.6 MB (169638064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bdd09bf1d23b3c828b02842aabc059af0a0195db17c8e294a66d459464b902`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 07 Feb 2024 06:29:10 GMT
RUN Apply image 10.0.20348.2322
# Wed, 14 Feb 2024 20:21:03 GMT
SHELL [cmd /s /c]
# Wed, 14 Feb 2024 20:25:06 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Wed, 14 Feb 2024 20:25:07 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 14 Feb 2024 20:25:07 GMT
USER ContainerAdministrator
# Wed, 14 Feb 2024 20:25:18 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 Feb 2024 20:25:19 GMT
USER ContainerUser
# Wed, 14 Feb 2024 20:26:06 GMT
COPY dir:a5c64f66204a1ce40e58093b44657f9abbd9eecac263988d919d778d3cf84131 in C:\openjdk-21 
# Wed, 14 Feb 2024 20:26:21 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:ccff18da882d371921351307d169380d3ac22ef981f2bb4f14fb2b332b395439`  
		Last Modified: Tue, 13 Feb 2024 23:39:47 GMT  
		Size: 120.7 MB (120735093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61a8b9610542d9f544621b5b605f3c73832b279a3681d70286c37473fec95b2`  
		Last Modified: Thu, 15 Feb 2024 00:16:30 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbdac88a025f13a3d52a2c41f868ef6a818f96d83f7f1bffd097f5d6e8e1ed9`  
		Last Modified: Thu, 15 Feb 2024 00:18:41 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292e726426433285b45b2c16fc8c88e0e23960f6d07d9090e6246d79a8bd41f4`  
		Last Modified: Thu, 15 Feb 2024 00:18:41 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65995336618fe22920f72d475ef7da8c69d8bbc48214ce78aece1c38c5b5cb43`  
		Last Modified: Thu, 15 Feb 2024 00:18:41 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384e406daa042a2f6e649bc4c5784219ae46b5cce7b446be355e99d53d3962e0`  
		Last Modified: Thu, 15 Feb 2024 00:18:39 GMT  
		Size: 85.3 KB (85253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b7fc31ed1b05b2eb54050ee8a646cc9584a6417e835b1b491ebf02d7f5059c`  
		Last Modified: Thu, 15 Feb 2024 00:18:39 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9db00c8d5c815271b9636f77912ed890c60b7b64a51e464e764c7db9c057ee`  
		Last Modified: Thu, 15 Feb 2024 00:19:18 GMT  
		Size: 48.7 MB (48749888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0e40b70943d6c862a03d1f47251e3b66abbcb30496e84161f60ff6230d5e1b`  
		Last Modified: Thu, 15 Feb 2024 00:19:09 GMT  
		Size: 62.0 KB (62028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
