## `eclipse-temurin:17-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:dfa207524e68007f14599e2d98b388969f800a92f88a6afb8ad1d3a70f91ddcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `eclipse-temurin:17-nanoserver-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull eclipse-temurin@sha256:84a3d6618566eb08581a691777623afe8790434b4fa73aac1965380156b323b5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.5 MB (384471988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd8e3db0a48717bb24468c8de90f71826982cc61be812faa00dc37a36e945e4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 07 Jun 2026 07:06:15 GMT
RUN Apply image 10.0.26100.32995
# Tue, 09 Jun 2026 23:20:27 GMT
SHELL [cmd /s /c]
# Tue, 09 Jun 2026 23:20:28 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Tue, 09 Jun 2026 23:20:29 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 09 Jun 2026 23:20:29 GMT
USER ContainerAdministrator
# Tue, 09 Jun 2026 23:20:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 09 Jun 2026 23:20:37 GMT
USER ContainerUser
# Tue, 09 Jun 2026 23:21:00 GMT
COPY dir:efa343062fcab6068fd499c77aea77fee33bf19a70fc27fbcf8f5891917744d1 in C:\openjdk-17 
# Tue, 09 Jun 2026 23:21:06 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 09 Jun 2026 23:21:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:64f5cd94d3bcd0fae94830b1fad0f8b3dc33677f8d7dc15c5219b56fe2a6584e`  
		Last Modified: Tue, 09 Jun 2026 22:11:30 GMT  
		Size: 196.7 MB (196668131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4ee1d74d5e111920765b9d27a3c592fd4c87738ba6e1727eb4f56dc2aa28dc`  
		Last Modified: Tue, 09 Jun 2026 23:21:12 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5340b196999fa823779d1ee0d8c2b3799fe9a7155ecbc1812662f106f7627191`  
		Last Modified: Tue, 09 Jun 2026 23:21:12 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b238d8d9eae5f3438244aeeb1b8ad74db188ca4ebd1d9fb92316847a902c58e`  
		Last Modified: Tue, 09 Jun 2026 23:21:12 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa7b8677d1f84f19d3b19b5b0ec473301fc222e9c1e59cfc9e1e5987c5268a5`  
		Last Modified: Tue, 09 Jun 2026 23:21:12 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03bd586cfdf0261e894a4ab4e58e43b890ba6ab9189315bee1cbfdc65a7be848`  
		Last Modified: Tue, 09 Jun 2026 23:21:10 GMT  
		Size: 72.9 KB (72870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f117dfb8d681d91f7f1fc8608f3953a275bd7569163fe58be788eb33edd67ad7`  
		Last Modified: Tue, 09 Jun 2026 23:21:10 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1817d4e7d945a39f18fc26449eecab3a215c7a602323ee65e195d7ac1ea4afc`  
		Last Modified: Tue, 09 Jun 2026 23:21:22 GMT  
		Size: 187.6 MB (187622133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518660174f9beff564638c0ce4948cae0a6a6412415c6df324acd4c21e17132b`  
		Last Modified: Tue, 09 Jun 2026 23:21:10 GMT  
		Size: 102.6 KB (102596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3aae7a9290ec2d6623968f1765a282d058e536303d64903e7aadd67755efeb2`  
		Last Modified: Tue, 09 Jun 2026 23:21:10 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
