## `eclipse-temurin:25-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:3a503fc8f9ebc717ee637e26c7e92e97c1111f397e2a379c4d54bb1f1d8890c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:25-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull eclipse-temurin@sha256:e52350a6fc4fdb12c332a6f84415894b1b4c64e44e8ea4c4c4f656424ff38691
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.8 MB (260823678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd938b1c1e73d96ba57bcd513db7f5a7416314dc5eac4fc995e478297286d8c3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 24 Oct 2025 19:19:18 GMT
SHELL [cmd /s /c]
# Fri, 24 Oct 2025 19:23:01 GMT
ENV JAVA_VERSION=jdk-25+36
# Fri, 24 Oct 2025 19:23:01 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 24 Oct 2025 19:23:02 GMT
USER ContainerAdministrator
# Fri, 24 Oct 2025 19:23:03 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 24 Oct 2025 19:23:04 GMT
USER ContainerUser
# Fri, 24 Oct 2025 19:23:36 GMT
COPY dir:3b404a1cbcdf7278c6a85a2778d3f0c01bd0f1229e8c8ae0734ae7bd6fe589bb in C:\openjdk-25 
# Fri, 24 Oct 2025 19:23:40 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 24 Oct 2025 19:23:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde8d3892490c03c6867f198f3dc45e69fe1049b2d63e6fc8a4a21f54095e87d`  
		Last Modified: Fri, 24 Oct 2025 19:20:16 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b280aec029efaa0908863ee11571f8770e30f25ead5d32e0440c719da9b1b38`  
		Last Modified: Fri, 24 Oct 2025 19:24:16 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c89db9749a495c28d3d7797be02b4cf85b4566e0fdc7d071381b178bc67232`  
		Last Modified: Fri, 24 Oct 2025 19:24:16 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89296ccd8eec444571111c04c222a57411c03e12f106fc7c205dc572eee8cb0`  
		Last Modified: Fri, 24 Oct 2025 19:24:16 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffebd762ccf9581d2f8e6feb3b2e15efc5e1c3a539c599685ce24a27f7883adb`  
		Last Modified: Fri, 24 Oct 2025 19:24:16 GMT  
		Size: 77.4 KB (77394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461628cb1b6deddc19c560a64b3839bbb3b63f0129dda56b72df2338ff251008`  
		Last Modified: Fri, 24 Oct 2025 19:24:16 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6d6a96ae8b3338f43ae6bd59e2e2dca6f8cd51f15d452291e1731cf02faa0c`  
		Last Modified: Fri, 24 Oct 2025 21:18:23 GMT  
		Size: 137.9 MB (137937349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2935b56fbeedb99a5d0a1f11ddaf6bb3e72d9d70baa886e176270f5226a2b1`  
		Last Modified: Fri, 24 Oct 2025 19:24:16 GMT  
		Size: 118.5 KB (118490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ed1714cdc3d663e1a662e319b9f46938127d2a26c1b4df1a1e41c1cca7ec1c`  
		Last Modified: Fri, 24 Oct 2025 19:24:16 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
