## `eclipse-temurin:8-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:0ad50e1a9790d1e97722979c58237507a589626e20df44b218b79de83f01836f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.26100.32370; amd64

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

### `eclipse-temurin:8-jdk-nanoserver` - windows version 10.0.20348.4773; amd64

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
