## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:600d7da995dfec9cae535b6f24c55aa74d1a6ffd5e1435f23f927d06d58a4217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1487; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1487; amd64

```console
$ docker pull eclipse-temurin@sha256:fb4792052ebba3597430b9782369a90a92e8549c0f057872e43ba89388fac440
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.5 MB (165534881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399cf19942c543de93ef62df42766016ff30d3e334a156b6acbc819fdbdebb9f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Jan 2023 23:36:49 GMT
RUN Apply image 10.0.20348.1487
# Thu, 12 Jan 2023 02:19:48 GMT
SHELL [cmd /s /c]
# Thu, 12 Jan 2023 02:23:38 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Thu, 12 Jan 2023 02:23:39 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 12 Jan 2023 02:23:40 GMT
USER ContainerAdministrator
# Thu, 12 Jan 2023 02:23:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 12 Jan 2023 02:23:53 GMT
USER ContainerUser
# Thu, 12 Jan 2023 02:24:49 GMT
COPY dir:20852dc87397947f41c5a6f7f30dc526aa127dbd27640e91343bc06b34d57a7f in C:\openjdk-17 
# Thu, 12 Jan 2023 02:25:26 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:83e9437e818022c1c28f0e07002dd46995c8614e62b9366138fa23b94f43d9ad`  
		Last Modified: Thu, 12 Jan 2023 02:51:06 GMT  
		Size: 122.1 MB (122099566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbebbf572ebe7984b715b8dfe99bc1273403a831c0079b95afa12162b7266f16`  
		Last Modified: Thu, 12 Jan 2023 02:50:38 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d6f45b3aeb713e90b16953d34b61fb78e87c6155d507fba1a45f9961f6ccd9`  
		Last Modified: Thu, 12 Jan 2023 02:52:19 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3fd926487da848d823b4941c4fe12f5f4da46397b110eff960b984af540710b`  
		Last Modified: Thu, 12 Jan 2023 02:52:19 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007ebd27f3fc1ff2dc3d698699a79150001e6baa2fa21fa90f22cb46ae486d45`  
		Last Modified: Thu, 12 Jan 2023 02:52:19 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59689ef04994653d6bf51b01b71ddaa681ad309035dccc725d5a6f52ca6fea30`  
		Last Modified: Thu, 12 Jan 2023 02:52:18 GMT  
		Size: 86.2 KB (86221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870d55487b8f6793d3a29816a146e65adfbde42c004b32e886e2fab4701999d7`  
		Last Modified: Thu, 12 Jan 2023 02:52:17 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09389c5d4d45c2eef29f802a47b694b24ed504a26de5c63d4efe75a73f00630`  
		Last Modified: Thu, 12 Jan 2023 02:52:57 GMT  
		Size: 43.3 MB (43283363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc2cddab22c9918902bb28e1bd8bff6479a87debbd3e12a370de60cd2414f47`  
		Last Modified: Thu, 12 Jan 2023 02:52:48 GMT  
		Size: 59.9 KB (59896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
