## `eclipse-temurin:21-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:425d78b35b341e580167a6b46f2a480e7eb18c93de745257805551f40f1d8cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `eclipse-temurin:21-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull eclipse-temurin@sha256:1e4be8650ee74368e40657f1cdd503cf26140a8df8bc06b9ebc7f90332701ffa
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.6 MB (248621943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a800d654e9cc05585fda6036d59e91478f0e262e3f42d8d3389e14f8f8a9da`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Mar 2026 01:45:55 GMT
RUN Apply image 10.0.26100.32522
# Tue, 10 Mar 2026 22:44:02 GMT
SHELL [cmd /s /c]
# Tue, 10 Mar 2026 22:44:03 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 10 Mar 2026 22:44:03 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 10 Mar 2026 22:44:04 GMT
USER ContainerAdministrator
# Tue, 10 Mar 2026 22:44:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Mar 2026 22:44:15 GMT
USER ContainerUser
# Tue, 10 Mar 2026 22:44:30 GMT
COPY dir:60f2977da675e9d6a11be1282de5c19d751a1b21ff04571f86a073fb3e930423 in C:\openjdk-21 
# Tue, 10 Mar 2026 22:44:33 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:06fab7822816d5f43d6835d07ac8db280fdf81384187f36d8dc43bbb7064a76d`  
		Last Modified: Tue, 10 Mar 2026 20:41:46 GMT  
		Size: 199.4 MB (199409325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a035615a893f11be138700ca7f180423bc5cb17b342c904e1190c82890187c`  
		Last Modified: Tue, 10 Mar 2026 22:44:39 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9882776648e31560774559d71dea9cea9c907846a1b538ad59fec857754ad33a`  
		Last Modified: Tue, 10 Mar 2026 22:44:39 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e68eb2135a97f27b55f3f19fc658c5da7a94b619aa3d9d49826e15faa7ac68d`  
		Last Modified: Tue, 10 Mar 2026 22:44:39 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d27279ee58d9b933115c6c4467db8b0adb9f69d8e1323873dd1980f3e66467f`  
		Last Modified: Tue, 10 Mar 2026 22:44:37 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c26efc03772caba66537c50312e565ddec498e17834750705baa652b7ec541`  
		Last Modified: Tue, 10 Mar 2026 22:44:38 GMT  
		Size: 73.4 KB (73395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95627f7ff9c6b3cad99e26d8713456594da9af2463cf99855f7952de3dc1b3f`  
		Last Modified: Tue, 10 Mar 2026 22:44:37 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f874d0cb4441342da5e64e9181f882bc187e6e257536a81fe6ba5528a02ed7`  
		Last Modified: Tue, 10 Mar 2026 22:44:44 GMT  
		Size: 49.0 MB (49040027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651d405823a71c991088820de3219de972ebad8eb02d759ed733f9d6bc4325c7`  
		Last Modified: Tue, 10 Mar 2026 22:44:38 GMT  
		Size: 93.8 KB (93774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
