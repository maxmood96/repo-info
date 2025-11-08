## `eclipse-temurin:21-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:034dff6dd6bd30d60a9595b157ba10878624ee11f2d4d9b59aed08407561d9de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:21-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull eclipse-temurin@sha256:7b00c1a56feae3369f9537a4cb64401584fe735c67061250f5723ffdf8cb3993
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.7 MB (324680470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab93e3ad8fdc879e72a383c047c5fef7dba62a7fdc20dc8c2564deab0fa955b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Sat, 08 Nov 2025 19:18:59 GMT
SHELL [cmd /s /c]
# Sat, 08 Nov 2025 19:19:00 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 19:19:01 GMT
ENV JAVA_HOME=C:\openjdk-21
# Sat, 08 Nov 2025 19:19:02 GMT
USER ContainerAdministrator
# Sat, 08 Nov 2025 19:19:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 08 Nov 2025 19:19:12 GMT
USER ContainerUser
# Sat, 08 Nov 2025 19:20:14 GMT
COPY dir:ca3f22bac3b96b31650dd9d8b46eabc8cfc824f09a5d61f04cd758713bcc4892 in C:\openjdk-21 
# Sat, 08 Nov 2025 19:20:21 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 08 Nov 2025 19:20:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e245ee6827f11c7dc03f8a52339f69b0e6f8d34f71084cb063bf9bddfe87e3`  
		Last Modified: Sat, 08 Nov 2025 19:20:49 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67bc5575f77576263fae409c0bd38573f20e419587f891fb6b2bb25cee03769`  
		Last Modified: Sat, 08 Nov 2025 19:20:49 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf134b2837ad650fd283f700bcf51c60b4b40a537dca813ec46b05139d3865e1`  
		Last Modified: Sat, 08 Nov 2025 19:20:50 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914bd7b377a22e4301be969a68b0da18d39e7fc659e729bc8899f2bf63f5fbdc`  
		Last Modified: Sat, 08 Nov 2025 19:20:50 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7aa8c074f992245f86a92ee273e01f951f5c0ef07b508032ef86167767df8df`  
		Last Modified: Sat, 08 Nov 2025 19:20:49 GMT  
		Size: 78.9 KB (78870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3e98ba2453c9e6cf358845d88fb81ae7b6126505b12727c08618ce6b71867b`  
		Last Modified: Sat, 08 Nov 2025 19:20:50 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82cbdff0b3b9b8d3ef7f13dde60e313faf39ad90261a9d2c1a5ad12c111f7375`  
		Last Modified: Sat, 08 Nov 2025 22:18:01 GMT  
		Size: 201.8 MB (201782452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6b47a990903318dd5e5e57239e473dcb979bf11ae88302948f41ebab7b57aa`  
		Last Modified: Sat, 08 Nov 2025 19:20:50 GMT  
		Size: 128.7 KB (128715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da4b668e168e0d3896f6a3c633f7f4b03698287317ec29e75c8a65354a7f61d`  
		Last Modified: Sat, 08 Nov 2025 19:20:50 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
