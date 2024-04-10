## `eclipse-temurin:22-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:f94192755c9bfe5f8f30089f0ad66ac531fb68c98f80f1c15b1d83d269693752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `eclipse-temurin:22-jre-nanoserver-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull eclipse-temurin@sha256:05dfd78bcc6b65def515878773d9e4131f94189814ffe0112fbee82d261ae0b1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.8 MB (156815928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a68b6b5207c7cc19456dc1722020e741bdeffd395593f46c8ca67b3f53c5255`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Tue, 09 Apr 2024 23:42:55 GMT
SHELL [cmd /s /c]
# Wed, 10 Apr 2024 00:29:04 GMT
ENV JAVA_VERSION=jdk-22+36
# Wed, 10 Apr 2024 00:29:05 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 10 Apr 2024 00:29:06 GMT
USER ContainerAdministrator
# Wed, 10 Apr 2024 00:29:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Apr 2024 00:29:15 GMT
USER ContainerUser
# Wed, 10 Apr 2024 00:34:35 GMT
COPY dir:205bc28a2cfde808c3c902b087992a6d179f1f6b12b6c0fffa64f09e3dab56d1 in C:\openjdk-22 
# Wed, 10 Apr 2024 00:34:46 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b591b5f81c02344da39dc8a9084b5791cbf552c1eb85e79db1f38dfc715a681`  
		Last Modified: Wed, 10 Apr 2024 00:47:46 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4af1a61fa1468ae79b53f42f8af23a93d321f74d116f4288cd7d7babbd41b4a`  
		Last Modified: Wed, 10 Apr 2024 00:58:33 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438da6a337d2fc0f98f65dd0bdf2976cb7a23a7559a0a1977397018158346fbb`  
		Last Modified: Wed, 10 Apr 2024 00:58:33 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd60f7f19a881ba7cde39a4da8c2a6b9a7eb3101cb25974cbeeacab094ed646`  
		Last Modified: Wed, 10 Apr 2024 00:58:33 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27d27098f47173b90e24c0243907c4bc956cf59279762c933d3b236f5467350`  
		Last Modified: Wed, 10 Apr 2024 00:58:31 GMT  
		Size: 67.9 KB (67895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8380d41d8bd639dadc09f22747b99fa78fc08923e1af1f533e79f8b1a86eff0`  
		Last Modified: Wed, 10 Apr 2024 00:58:31 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf4e0153ced0f81aa9b7ed608873f7d5931268fdaf3309be51438834cffe52e`  
		Last Modified: Wed, 10 Apr 2024 00:59:50 GMT  
		Size: 48.5 MB (48477968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c943d3aa61d9f41f85314ad135dffa8c6911a0588877b1cdc9ab99d19286d6`  
		Last Modified: Wed, 10 Apr 2024 00:59:42 GMT  
		Size: 3.4 MB (3375363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
