## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:7412198c748b9c405ce0da07cfbf7a0367e5064881d4a5156cf2c3791f364003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:e35b62a6aaa2bc7f097ad6f60dbce572feed567fac3ba24560059fca8850a442
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (242988505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba76a1c5b7d5b18b76241d51664190b957fca237dc58e0b6a3eb7feb184e3c0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Thu, 05 Feb 2026 22:39:37 GMT
SHELL [cmd /s /c]
# Thu, 05 Feb 2026 22:39:38 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Thu, 05 Feb 2026 22:39:38 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 05 Feb 2026 22:39:39 GMT
USER ContainerAdministrator
# Thu, 05 Feb 2026 22:39:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 05 Feb 2026 22:39:45 GMT
USER ContainerUser
# Thu, 05 Feb 2026 22:39:55 GMT
COPY dir:9d7273a61bdbfae69a7bd32ee7f3a7621be43375d7aad513ad72640646f9a6e0 in C:\openjdk-11 
# Thu, 05 Feb 2026 22:39:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84eb9db611480b68a9e8151c8c6f75da76723b913af9d6d537f2c64107225c4e`  
		Last Modified: Thu, 05 Feb 2026 22:40:05 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02748528f0a835af7a997b4b95dd5e6e0bc9bb16bc0479923fc15c617511a15a`  
		Last Modified: Thu, 05 Feb 2026 22:40:05 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dae745c482ed255ff84daff830a5df826ba67d181b2be78dcbce9609c0a2e32`  
		Last Modified: Thu, 05 Feb 2026 22:40:05 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a1c6387e019fefbf1d10bd1787a930560d3cf124eb6fff7874343591759dca`  
		Last Modified: Thu, 05 Feb 2026 22:40:03 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66a32fcb3a58965e7d0d86e19666ff99b38508cd151e354b2f60f0ce79042e35`  
		Last Modified: Thu, 05 Feb 2026 22:40:04 GMT  
		Size: 74.7 KB (74716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b195f981023c7cd294d5b62392bb3f2113e3b4c181a6eb9fb52fa83639377766`  
		Last Modified: Thu, 05 Feb 2026 22:40:03 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed89bb892970374a1d18cccae77beaf3e1251fb189fc974319bf5ad430307042`  
		Last Modified: Thu, 05 Feb 2026 22:40:09 GMT  
		Size: 43.7 MB (43719132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9df54723731dc80767aa6fd23ae76532f9a3400f0b0c8258a549644f42c4d7e6`  
		Last Modified: Thu, 05 Feb 2026 22:40:04 GMT  
		Size: 112.7 KB (112740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:8c67be21e258321883eea1e2255971006d42755959ccb49b1813784a8f793943
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170589151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00caa19b0d61bc52fdd941e97b2d301a504c59005a17e95c308ae67e247f8c47`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Thu, 05 Feb 2026 22:39:16 GMT
SHELL [cmd /s /c]
# Thu, 05 Feb 2026 22:39:16 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Thu, 05 Feb 2026 22:39:17 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 05 Feb 2026 22:39:18 GMT
USER ContainerAdministrator
# Thu, 05 Feb 2026 22:39:23 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 05 Feb 2026 22:39:24 GMT
USER ContainerUser
# Thu, 05 Feb 2026 22:39:32 GMT
COPY dir:9d7273a61bdbfae69a7bd32ee7f3a7621be43375d7aad513ad72640646f9a6e0 in C:\openjdk-11 
# Thu, 05 Feb 2026 22:39:35 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4c75b6a0defca9fcf399b6d239ee405e6b00e1f4ad808bd98a6eadba33d863`  
		Last Modified: Thu, 05 Feb 2026 22:39:41 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96716158a808c5f110abb8f61502664302169c4c6d6564f232c738bb81df9b78`  
		Last Modified: Thu, 05 Feb 2026 22:39:41 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7cd75b90ab7f1a7fc8417f52e61695debbbac1c4bbeca115a776181746a06a9`  
		Last Modified: Thu, 05 Feb 2026 22:39:41 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82a16c599dac72c43db3a94052809e9cfdd3899c73cd0aa46a8260eb13ab443`  
		Last Modified: Thu, 05 Feb 2026 22:39:39 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1954f08a3f001a1c17e1d823952664a511b4abfdecd431e58da6a63d7d46d5`  
		Last Modified: Thu, 05 Feb 2026 22:39:39 GMT  
		Size: 70.7 KB (70679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b62c9faaf34521122ae3ae262d8bffd023e84170adde4c18150e2d4df3f325`  
		Last Modified: Thu, 05 Feb 2026 22:39:39 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c43f7573a70f518a82ccada97e568c5b49ef84d29a5af7e9f278a835f0ee5b`  
		Last Modified: Thu, 05 Feb 2026 22:39:45 GMT  
		Size: 43.7 MB (43718607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850165b67ebb5c85c48ec5c2118e7e6e77d859c687ea82b5499f043713db9b3d`  
		Last Modified: Thu, 05 Feb 2026 22:39:39 GMT  
		Size: 97.7 KB (97707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
