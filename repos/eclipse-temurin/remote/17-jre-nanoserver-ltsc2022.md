## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:f57a9e1e9caaa894ed3dc728ee0ddc39948498ef95f5e1529b4bdc3c2153773f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull eclipse-temurin@sha256:7a9b30e2bb17c54555618d734b261c9bf6a6264ab6e00c41911d33bd7d75f2df
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166458891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08eb6f8e38438d3c3b3d7a62ed26b7b1b02528fc633bad922cca3b3c1064b4a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Tue, 10 Jun 2025 22:20:46 GMT
SHELL [cmd /s /c]
# Tue, 10 Jun 2025 22:20:47 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Tue, 10 Jun 2025 22:20:48 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 10 Jun 2025 22:20:48 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:20:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Jun 2025 22:20:52 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:20:56 GMT
COPY dir:6f6fcea1890c098492beafa1d6f550d144651035b2d4a098a7658e545737cf82 in C:\openjdk-17 
# Tue, 10 Jun 2025 22:21:00 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17adbcfc495f7986d4762127a73866940371a2e15d719866d98d1ed9e48f576d`  
		Last Modified: Tue, 10 Jun 2025 22:21:43 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7c502d8b266a2c97671046dc41568c04ecf9273e066cc6298abdd1d0f1f4a3`  
		Last Modified: Tue, 10 Jun 2025 22:21:43 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d67fcba3634751200faa62f0116e2cbe59e6363ce4a3da1f233830310c4ea0`  
		Last Modified: Tue, 10 Jun 2025 22:21:43 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255f8e7f02a73ec209d5a16b87f40e9bfc9174e3e5834ecec235b92c9950446e`  
		Last Modified: Tue, 10 Jun 2025 22:21:44 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1dfbf90e72ac4bab593151ec67210faf5a31bfa957996aa1ac10fc386634216`  
		Last Modified: Tue, 10 Jun 2025 22:21:44 GMT  
		Size: 79.9 KB (79915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02326ff6725311eaa0cdfb816449bf88204cc01c390232282b4f2438a14cf1f9`  
		Last Modified: Tue, 10 Jun 2025 22:21:45 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2990379d8a65e1f84dc89a433a6b7de5a62515557e82a127a46904ddd7ba5229`  
		Last Modified: Wed, 11 Jun 2025 00:14:36 GMT  
		Size: 43.7 MB (43736838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aa4746fb6bdd38e9edc95e171c9d9dde4fac6c857f95706d52b072f7dd56d99`  
		Last Modified: Tue, 10 Jun 2025 22:32:43 GMT  
		Size: 96.5 KB (96460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
