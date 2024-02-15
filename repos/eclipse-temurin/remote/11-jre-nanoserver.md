## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:aed842106663dde0f75a06e24ba2c104daeb8454304476675158311f69c3e7d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.2322; amd64

```console
$ docker pull eclipse-temurin@sha256:02b409001f37dd924ffc947c891b9856b1adaaa10da7a38768394b953cf57070
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.2 MB (164229030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137552ed957fd304bfae46b78cafadd66c7b1cfba90808b02691c81c9eea938a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 07 Feb 2024 06:29:10 GMT
RUN Apply image 10.0.20348.2322
# Wed, 14 Feb 2024 20:21:03 GMT
SHELL [cmd /s /c]
# Wed, 14 Feb 2024 20:22:22 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 14 Feb 2024 20:22:23 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 14 Feb 2024 20:22:23 GMT
USER ContainerAdministrator
# Wed, 14 Feb 2024 20:22:34 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 Feb 2024 20:22:35 GMT
USER ContainerUser
# Wed, 14 Feb 2024 20:23:22 GMT
COPY dir:dc1e2da1c34561e3d80ae1d96f99e65841adfcbd6fe35da2f57cba6532915179 in C:\openjdk-11 
# Wed, 14 Feb 2024 20:23:34 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:ccff18da882d371921351307d169380d3ac22ef981f2bb4f14fb2b332b395439`  
		Last Modified: Tue, 13 Feb 2024 23:39:47 GMT  
		Size: 120.7 MB (120735093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61a8b9610542d9f544621b5b605f3c73832b279a3681d70286c37473fec95b2`  
		Last Modified: Thu, 15 Feb 2024 00:16:30 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67473bcd18684a34d5b7cab43ef63cbde6539e7d6bc87249f46d1be862084434`  
		Last Modified: Thu, 15 Feb 2024 00:17:08 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9f0c5bc9237da5d7cb47e594d8f0f5e85f5df0016c3235f0f416cc6e4487e2`  
		Last Modified: Thu, 15 Feb 2024 00:17:07 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f98f32612f989a82f2490cb250150ffd4d8a4f4168275ec52a765c8aa70d357`  
		Last Modified: Thu, 15 Feb 2024 00:17:07 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35603fc85a8baaff0cdde1bd6974ceed6f9d62c4ec20c87a51851b41417f7c9`  
		Last Modified: Thu, 15 Feb 2024 00:17:06 GMT  
		Size: 84.1 KB (84141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a553c1181621e5ca75e31d1627e0210c3190bef3594406282743d17899e4862e`  
		Last Modified: Thu, 15 Feb 2024 00:17:05 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698ef30672c001f8635ff427641f63b9648e57d00b22efb0b1684c1512619917`  
		Last Modified: Thu, 15 Feb 2024 00:17:44 GMT  
		Size: 43.3 MB (43342092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0691ac3a52419646f670f6ad78132d9342b16c4de88fc3b2d277804cab832ee9`  
		Last Modified: Thu, 15 Feb 2024 00:17:36 GMT  
		Size: 61.8 KB (61846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.17763.5458; amd64

```console
$ docker pull eclipse-temurin@sha256:0904c6d2e971daafd85e44ee9f99d43bedcc2059ddda28a644ba006e3b040dab
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148113096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd19c0b9e69daaaf2b471737d2ffc02ce94ea475a073eca7b608cdf9d022f10c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Wed, 14 Feb 2024 19:41:52 GMT
SHELL [cmd /s /c]
# Wed, 14 Feb 2024 19:52:31 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 14 Feb 2024 19:52:31 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 14 Feb 2024 19:52:32 GMT
USER ContainerAdministrator
# Wed, 14 Feb 2024 19:52:41 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 Feb 2024 19:52:42 GMT
USER ContainerUser
# Wed, 14 Feb 2024 19:57:51 GMT
COPY dir:dc1e2da1c34561e3d80ae1d96f99e65841adfcbd6fe35da2f57cba6532915179 in C:\openjdk-11 
# Wed, 14 Feb 2024 19:58:02 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cddfc54d18bb5861232283d3ff2ca5e214ade28a46dfcf6c1e7c7243809e5e85`  
		Last Modified: Thu, 15 Feb 2024 00:06:58 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3319aab0e85c73865f54cb2011da9cc0beb9ac20f12bbdffd5e3ac1b892d8142`  
		Last Modified: Thu, 15 Feb 2024 00:09:34 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3398b3bdd700f3b8b49044299f48076e670172694acfa7bf6140095c2f05a3a0`  
		Last Modified: Thu, 15 Feb 2024 00:09:34 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d23aff9121982bcd4082fc8bbdcd54c014d60c98f573b7e5494b46846f22ce`  
		Last Modified: Thu, 15 Feb 2024 00:09:34 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f843bf4ae9ad0643e317beb4a369fe03b6ddd1b04bac045b06125626624558b`  
		Last Modified: Thu, 15 Feb 2024 00:09:32 GMT  
		Size: 67.8 KB (67849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777c40462214ee9ade29f95b6280ed8186b0d4aadfa9818fe1729313f42a9f77`  
		Last Modified: Thu, 15 Feb 2024 00:09:32 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5cdf025b125e07435609470203947b0d13ed968d3f6e17c43fc509d27140f7e`  
		Last Modified: Thu, 15 Feb 2024 00:10:46 GMT  
		Size: 43.3 MB (43337514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6300b8c7ce63e562bc2c88164681dcd0fb1b61b948c5123c823d3b801d7f03e`  
		Last Modified: Thu, 15 Feb 2024 00:10:38 GMT  
		Size: 80.3 KB (80296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
