## `eclipse-temurin:11-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:104d8be91303efd3c77431260560e0d9ea17c61d3b26a380d890bb14b4f1ab49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32230; amd64

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
