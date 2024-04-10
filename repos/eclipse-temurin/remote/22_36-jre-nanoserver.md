## `eclipse-temurin:22_36-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:5abc48c8dda5c5bf929f44187d6af3bd3d09fa10acfb4a601e2f2c3ccdffa445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `eclipse-temurin:22_36-jre-nanoserver` - windows version 10.0.20348.2402; amd64

```console
$ docker pull eclipse-temurin@sha256:8771f8198353599c3bf8b72bf7e73f1c4c0f1277a023c1eed0f6b077bfeefbda
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.6 MB (169613674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369562ee4c3e9a2c690d9c39f309a0de9348ededa2d89a272e77ae5926bf01cd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Apr 2024 08:53:11 GMT
RUN Apply image 10.0.20348.2402
# Wed, 10 Apr 2024 00:34:53 GMT
SHELL [cmd /s /c]
# Wed, 10 Apr 2024 00:40:19 GMT
ENV JAVA_VERSION=jdk-22+36
# Wed, 10 Apr 2024 00:40:20 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 10 Apr 2024 00:40:21 GMT
USER ContainerAdministrator
# Wed, 10 Apr 2024 00:40:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Apr 2024 00:40:31 GMT
USER ContainerUser
# Wed, 10 Apr 2024 00:41:21 GMT
COPY dir:205bc28a2cfde808c3c902b087992a6d179f1f6b12b6c0fffa64f09e3dab56d1 in C:\openjdk-22 
# Wed, 10 Apr 2024 00:41:32 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:755fc767289b8847bd0d0d8d75efc308c040140acf2a3426973ba9fbf022c4c0`  
		Last Modified: Tue, 09 Apr 2024 23:50:18 GMT  
		Size: 121.0 MB (120993754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e70887eeae6a5d6d5fd81661024afc84fee637f674dee5e7127112cbfce90750`  
		Last Modified: Wed, 10 Apr 2024 01:00:01 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fb0d9a77a72d9bcd9e2571d43678ec7cdbd36fa04817c766e3629434c90ace`  
		Last Modified: Wed, 10 Apr 2024 01:03:20 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7584ce14c659083fbc4898e8fc6dd6813e919285f680b44a48916c549504fb`  
		Last Modified: Wed, 10 Apr 2024 01:03:20 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113fffa2e102ada8b3611a56f23c0b15a5118850881d7c58ce938c8190d3e4f8`  
		Last Modified: Wed, 10 Apr 2024 01:03:20 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf022c1012c448e2444fd3ac66c18203719fe5307e49ac8c8823db4428296274`  
		Last Modified: Wed, 10 Apr 2024 01:03:18 GMT  
		Size: 76.9 KB (76881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3d2f58650e4ea177e80de5227843bec54db0abfad8bcf0a22549cb7fa9d5ff`  
		Last Modified: Wed, 10 Apr 2024 01:03:18 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7148e0b7781746b4fcd09c30ba9106aa0515e7e535800a1db7ae0de6c1f459e`  
		Last Modified: Wed, 10 Apr 2024 01:03:58 GMT  
		Size: 48.5 MB (48477962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210ab2d260fc6520971c354fd04951930ceb52e024c6d04dd60c3379d6abf48e`  
		Last Modified: Wed, 10 Apr 2024 01:03:49 GMT  
		Size: 59.7 KB (59719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22_36-jre-nanoserver` - windows version 10.0.17763.5696; amd64

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
