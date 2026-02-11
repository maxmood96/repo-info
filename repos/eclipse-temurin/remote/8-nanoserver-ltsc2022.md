## `eclipse-temurin:8-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:4468be2772985f5af4a2e3abdebedfb59ce01123ec6f71b1cec1b955c29d6349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `eclipse-temurin:8-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull eclipse-temurin@sha256:45e8a8d0e494ee808fdd5ceab55ce593fabc44c45bb3a5ee4323c7fe23655042
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228739016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbad4f44493742bf56172a2fb72a143d1b292eafbd2ffea3306bdc5df83a210d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Tue, 10 Feb 2026 23:30:05 GMT
SHELL [cmd /s /c]
# Tue, 10 Feb 2026 23:30:05 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 10 Feb 2026 23:30:06 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 10 Feb 2026 23:30:06 GMT
USER ContainerAdministrator
# Tue, 10 Feb 2026 23:30:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Feb 2026 23:30:09 GMT
USER ContainerUser
# Tue, 10 Feb 2026 23:30:15 GMT
COPY dir:076949d8a0679d24528f11c4150b1ea7a552717f0bf1fb11a9fa610f7e5e2ea0 in C:\openjdk-8 
# Tue, 10 Feb 2026 23:30:18 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88bd703ad3be2a352cd766b66162d651fa380534f38e60a0bd66c13f3a03b45b`  
		Last Modified: Tue, 10 Feb 2026 23:30:24 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0659a08d4698b43055fc8d9a05a15faa93b7c298606fcaec1986fa16355c9b87`  
		Last Modified: Tue, 10 Feb 2026 23:30:24 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9a81ba2441d0dce28d72e014a3a9c35bdc4bc51c6a6cd1c8a3b9c3378cb286`  
		Last Modified: Tue, 10 Feb 2026 23:30:24 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd015d50af96ffbe8d3fbbcff87fd8882b7b397e563fead037331bf9f36459e9`  
		Last Modified: Tue, 10 Feb 2026 23:30:22 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f87ea702031060d3267e11a7df081b3f20ed162b634d842b6174c602a05431`  
		Last Modified: Tue, 10 Feb 2026 23:30:22 GMT  
		Size: 80.8 KB (80813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ab5b015a3bcd26e90e48a8760e10f19d67c094630c2e816de46f5b9f9d6115`  
		Last Modified: Tue, 10 Feb 2026 23:30:22 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:248dbb34cf0de28ce98b425ceedc8b29c89b5ffa3beb9b64124210d3d4c27005`  
		Last Modified: Tue, 10 Feb 2026 23:30:31 GMT  
		Size: 101.9 MB (101908320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:054d9c7394312d3de7f7b561a94f3fcb50551298e7d4a38d35cdebb9beaecd9c`  
		Last Modified: Tue, 10 Feb 2026 23:30:22 GMT  
		Size: 98.7 KB (98737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
