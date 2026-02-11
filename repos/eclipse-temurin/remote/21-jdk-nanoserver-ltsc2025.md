## `eclipse-temurin:21-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:68e521fab5f465a217a3456c5271916143285e367e567603412ff375203b21f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `eclipse-temurin:21-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull eclipse-temurin@sha256:ba58d07b7b72dd352b02e03d18a017397f39eec7aa10826dbc8966df4318edee
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.2 MB (401165684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc799843238d873318b15ed596c3887d6bacb8b9c7813263c64ab0107607692`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 22:06:41 GMT
RUN Apply image 10.0.26100.32370
# Tue, 10 Feb 2026 23:37:15 GMT
SHELL [cmd /s /c]
# Tue, 10 Feb 2026 23:37:16 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 10 Feb 2026 23:37:16 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 10 Feb 2026 23:37:17 GMT
USER ContainerAdministrator
# Tue, 10 Feb 2026 23:37:22 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Feb 2026 23:37:23 GMT
USER ContainerUser
# Tue, 10 Feb 2026 23:37:37 GMT
COPY dir:a00a0ee8f4ae82aa8e2b5d2b9cb5c2941887de3e7b021ae64d7924c257e6915c in C:\openjdk-21 
# Tue, 10 Feb 2026 23:37:41 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 10 Feb 2026 23:37:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:77321bd03612cfa46920e790ae0c3b142758a5803ad759fdb406c98b6f2e4ed0`  
		Last Modified: Tue, 10 Feb 2026 22:50:26 GMT  
		Size: 199.3 MB (199251619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93736301ad57fe9fddc39e5ea57399e8e5546e2bf93ca52e548cb21fbda892df`  
		Last Modified: Tue, 10 Feb 2026 23:37:48 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fea7461ffd132728ee6d27eced5dc27a76b15e852a6a9326d8def3aee1ce7d`  
		Last Modified: Tue, 10 Feb 2026 23:37:47 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b80f8adf426519b905aafc30087ead54129d4dfce2d2642e6940735afa216c9`  
		Last Modified: Tue, 10 Feb 2026 23:37:48 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5dc20ad0a17468218b7637453c403c395194dd18f1c96bc97ae0107c240e89c`  
		Last Modified: Tue, 10 Feb 2026 23:37:47 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce388279c821399df24b0e675c6c1197ccf69a60a73dfffd2df563722f3c9a6`  
		Last Modified: Tue, 10 Feb 2026 23:37:46 GMT  
		Size: 70.6 KB (70562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594489b425dd53f46ff12061febb6ff5a05207d0ec38621cb2e34b3333513772`  
		Last Modified: Tue, 10 Feb 2026 23:37:46 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0c0ee960a8bc872f71b22fafe65b3684608768695da05ef3fb4062cfb56a5a`  
		Last Modified: Tue, 10 Feb 2026 23:37:59 GMT  
		Size: 201.8 MB (201752634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdbf280cd5c35092879490e7abcd3ae992266c789cc9c487138fd32fe1f2d98e`  
		Last Modified: Tue, 10 Feb 2026 23:37:46 GMT  
		Size: 84.3 KB (84345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef5fcf3c51b66c8db4d979c5ba518bc34ca1e5a3dfeb9bc5a7c5d611939d949`  
		Last Modified: Tue, 10 Feb 2026 23:37:46 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
