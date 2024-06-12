## `eclipse-temurin:17-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:0c08ab5878e4f398bd3face4d78ac7138163555af3c3a9f9f5ede957e0d27897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2527; amd64

### `eclipse-temurin:17-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2527; amd64

```console
$ docker pull eclipse-temurin@sha256:12d5447fbbdf7f700dadb1aa3aceac92aa5887ade29e153d350683c9f6fc4a2a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.5 MB (307473494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd97f75ac6b6023b34a1f60cb648c22d1d1cfc01cb9e56a74287a72d3c689776`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 08:41:16 GMT
RUN Apply image 10.0.20348.2527
# Wed, 12 Jun 2024 18:27:44 GMT
SHELL [cmd /s /c]
# Wed, 12 Jun 2024 18:30:22 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 12 Jun 2024 18:30:22 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 12 Jun 2024 18:30:23 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 18:30:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Jun 2024 18:30:33 GMT
USER ContainerUser
# Wed, 12 Jun 2024 18:30:48 GMT
COPY dir:58180deb8c422e61d331dbc12d9d7d83d7afe3e9097adb59bd0860aff4211c36 in C:\openjdk-17 
# Wed, 12 Jun 2024 18:31:02 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Jun 2024 18:31:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f9825bcd6f9509654677a23b5fa1d32b32e1e32ff51914ebfaa76d5e79c22b50`  
		Last Modified: Wed, 12 Jun 2024 02:27:19 GMT  
		Size: 120.5 MB (120488969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ae17666c85b2b00f8e5aa24951a59f0b01a1eb41704faa32e1282e0f0ef217`  
		Last Modified: Wed, 12 Jun 2024 18:52:48 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379f1a30d61a338b36299534cf82fb4e3627f57850ce24f5404a5afda9eea752`  
		Last Modified: Wed, 12 Jun 2024 18:54:19 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5c4d9582b52aadd1d2bb6e492d05ba62d6cb0338b3fc03ef015824dd5ba7f1`  
		Last Modified: Wed, 12 Jun 2024 18:54:19 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93d6b8c3ba849e7f0cec95f9690a297dbb27ab15f9cf2684e52e501d8fb37f6`  
		Last Modified: Wed, 12 Jun 2024 18:54:19 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a51cf5df365f8a070fdaaae831ad485c407b3870516e0e9b243f747fb45aa62`  
		Last Modified: Wed, 12 Jun 2024 18:54:17 GMT  
		Size: 81.2 KB (81221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e39326053ebbd46753185cabac599579c906fa6f4d81c2263b8f581c46055b4`  
		Last Modified: Wed, 12 Jun 2024 18:54:17 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d85313b022339fe691fcf5a7bfd04425416b8794e327800d15e717932f2cfb`  
		Last Modified: Wed, 12 Jun 2024 18:54:35 GMT  
		Size: 186.8 MB (186837756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2380cca1bc6a1aff323ef70a6e2a32111f883c10a7b304e4072c499899bbcf83`  
		Last Modified: Wed, 12 Jun 2024 18:54:17 GMT  
		Size: 58.6 KB (58637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ec10960038c97979ca38845d37225a01a70d66df3386bc5e058ff0e3a5ffe1`  
		Last Modified: Wed, 12 Jun 2024 18:54:17 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
