## `eclipse-temurin:8-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:796ccea2ca4599c3c69503fd69759317b0fe126d632e368180bcfcc97e7a7af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `eclipse-temurin:8-nanoserver-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull eclipse-temurin@sha256:d4f3c9d798b164180321d2a6b6ac6692b312bd20e88b0a4e0437a71c49d0d80f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.3 MB (301340601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ac548569c3ae688c6f64e8e9f28c46f71d830a8cb1d859b989368717c48f50`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 22:06:41 GMT
RUN Apply image 10.0.26100.32370
# Tue, 10 Feb 2026 23:35:53 GMT
SHELL [cmd /s /c]
# Tue, 10 Feb 2026 23:35:54 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 10 Feb 2026 23:35:54 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 10 Feb 2026 23:35:55 GMT
USER ContainerAdministrator
# Tue, 10 Feb 2026 23:36:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Feb 2026 23:36:00 GMT
USER ContainerUser
# Tue, 10 Feb 2026 23:36:12 GMT
COPY dir:076949d8a0679d24528f11c4150b1ea7a552717f0bf1fb11a9fa610f7e5e2ea0 in C:\openjdk-8 
# Tue, 10 Feb 2026 23:36:16 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:77321bd03612cfa46920e790ae0c3b142758a5803ad759fdb406c98b6f2e4ed0`  
		Last Modified: Tue, 10 Feb 2026 22:50:26 GMT  
		Size: 199.3 MB (199251619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3dcd8522d90357855aa8c34b4879a2f8b02cfa8defc783b9a2c51f14855fd1`  
		Last Modified: Tue, 10 Feb 2026 23:36:22 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e410e74d6fba321bbe34aeee745a12fc2744a212bb1bb211477ce03b6c83bbb9`  
		Last Modified: Tue, 10 Feb 2026 23:36:22 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf272ddc3b2bd868d2f43b7fd25fbb39ba8c161e607aac9a9a84e8ba7337d9f`  
		Last Modified: Tue, 10 Feb 2026 23:36:22 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ebf92950e2d230c0180c5d39c6e54426cf23d88afa8bdf76a14cc365e711aba`  
		Last Modified: Tue, 10 Feb 2026 23:36:20 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7419aed1f1e74f7e7a9bca06226b01fc34ca896b4f0d6e16a97879a7b10269c`  
		Last Modified: Tue, 10 Feb 2026 23:36:20 GMT  
		Size: 77.5 KB (77465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873839309bb9214515be574c1dc0e9af7fff8b56525c8f66650578d265077967`  
		Last Modified: Tue, 10 Feb 2026 23:36:20 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3244989e5d864025b91cdda1417d304efefe1b3adb28b9904daffcc158ebb5`  
		Last Modified: Tue, 10 Feb 2026 23:36:28 GMT  
		Size: 101.9 MB (101908795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56ac7d4be71ccb908305ceaefeacc28d0f6ba024661f20653351f69bfb3d7fa`  
		Last Modified: Tue, 10 Feb 2026 23:36:20 GMT  
		Size: 97.4 KB (97386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
