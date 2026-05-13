## `eclipse-temurin:17-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:a5ae6bbaca5d892bb6202ef6ca29f31e84ce13e7f8622ef31a8bbdea8aef3a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull eclipse-temurin@sha256:da231e71e34d0e2d629c36a27857e93aaebe85194843d3f106fb9b3f03eaec0b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243734239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4928fa191598b972b82af16a596fc3d2d32ed96c4e9a97350c2ca5ba67d8f4cc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 May 2026 09:46:02 GMT
RUN Apply image 10.0.26100.32860
# Wed, 13 May 2026 00:29:08 GMT
SHELL [cmd /s /c]
# Wed, 13 May 2026 00:29:09 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Wed, 13 May 2026 00:29:09 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 13 May 2026 00:29:10 GMT
USER ContainerAdministrator
# Wed, 13 May 2026 00:29:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 May 2026 00:29:15 GMT
USER ContainerUser
# Wed, 13 May 2026 00:29:24 GMT
COPY dir:2f70d7e82fbe25185baf6a6b1e05b870cb38c3ad05aac5b5932c695a93320f91 in C:\openjdk-17 
# Wed, 13 May 2026 00:29:26 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:34ab6476d71f2d23d05a00ac439000ba4c19d17e5c66f15efbe329ed79bba2bf`  
		Last Modified: Tue, 12 May 2026 22:29:47 GMT  
		Size: 199.7 MB (199739001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65bf3479a2f977f928ea1294a5058ca6c7e18cb7733c755a4ccbd0c0162ed82`  
		Last Modified: Wed, 13 May 2026 00:29:32 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c745c4ccb2b4e79daae5e945e7fe46afc420019441582f831cf05c900742ebd8`  
		Last Modified: Wed, 13 May 2026 00:29:33 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c503980863edf9c8c9aa2c21189118279e17980f195c87696556bc2c0dceeb4`  
		Last Modified: Wed, 13 May 2026 00:29:32 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2d5a781e2d1fb6257b07af79441ac7d73c075b57f5df8037109b7141343a80`  
		Last Modified: Wed, 13 May 2026 00:29:31 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7b312603f8c7dabd649982d99b5ff59a92f5a7e164508990b8514725b90d19`  
		Last Modified: Wed, 13 May 2026 00:29:31 GMT  
		Size: 71.6 KB (71618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c037f10ec1516f06a21b2bab79fa8080ff210bb55b72a5bc227537058bce912a`  
		Last Modified: Wed, 13 May 2026 00:29:31 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68bc496b9ba15bc6c60fbf61af74809fbefe97dc58017a0e91d1d322cf0adda8`  
		Last Modified: Wed, 13 May 2026 00:29:38 GMT  
		Size: 43.8 MB (43833952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7def5cd40ca68e3ba35f8d863199f0243e0327a3d0b57079697dc9a79d7f4056`  
		Last Modified: Wed, 13 May 2026 00:29:31 GMT  
		Size: 84.3 KB (84266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
