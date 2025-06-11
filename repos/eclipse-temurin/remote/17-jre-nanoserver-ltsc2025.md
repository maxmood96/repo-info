## `eclipse-temurin:17-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:06158d9ddfce64e3d73a40990919c8d47989fd892df87fc95da0426937ba231e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull eclipse-temurin@sha256:98ceba0e25fec160ae0c5573fed039bef1abf9bfbcecf3062f2cde207af8aed7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.0 MB (236004574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e499e44138549cb445caf10186ce6008f18cf8a461e9e5267652ef3019eb87a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jun 2025 15:19:59 GMT
RUN Apply image 10.0.26100.4349
# Tue, 10 Jun 2025 22:15:23 GMT
SHELL [cmd /s /c]
# Tue, 10 Jun 2025 22:15:25 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Tue, 10 Jun 2025 22:15:27 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 10 Jun 2025 22:15:29 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:15:34 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Jun 2025 22:15:36 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:15:42 GMT
COPY dir:6f6fcea1890c098492beafa1d6f550d144651035b2d4a098a7658e545737cf82 in C:\openjdk-17 
# Tue, 10 Jun 2025 22:15:49 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:709fa8bff22087ae5c45c65a3b0777eb6ee12afd1b773aece2a322e84b66b1d1`  
		Last Modified: Tue, 10 Jun 2025 22:41:49 GMT  
		Size: 192.1 MB (192082516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39506ff5c070656342c50a467bfe3e734602f750f5e5f48bc9446607261d33e1`  
		Last Modified: Tue, 10 Jun 2025 22:16:35 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c79bf47e5d338f129262716b4db6683c322f7478a6a424c54de823eaa4325d`  
		Last Modified: Tue, 10 Jun 2025 22:16:36 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a974e7e23117bb0c0cf493fde2db4404c603c95ed4b74c31e1f9e7228bf9a771`  
		Last Modified: Tue, 10 Jun 2025 22:16:36 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034f8acc33ca0d3a476151542d9ecabf05fca53971d3038f1175dc7130a1127f`  
		Last Modified: Tue, 10 Jun 2025 22:16:36 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a157966164e4e65d1f6432ab7918a9d7217048cb0aa72a458dd290ea4627a2`  
		Last Modified: Tue, 10 Jun 2025 22:16:36 GMT  
		Size: 76.5 KB (76482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2899d84e9d7ccdc1cb18873c1b20d5749d8971bd74817e59f11d13e001d0b20`  
		Last Modified: Tue, 10 Jun 2025 22:16:37 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046aefa37e15175a8928903ccc04a0c1cfdae3f7d1bdcf2e824ff288c453d352`  
		Last Modified: Tue, 10 Jun 2025 22:16:39 GMT  
		Size: 43.7 MB (43736515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7086c63cb8566ad25440bdbd217c98fcfb9211b5a943660ebf3b0093f03aa4`  
		Last Modified: Tue, 10 Jun 2025 22:16:37 GMT  
		Size: 103.8 KB (103790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
