## `eclipse-temurin:19-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:68feb6b52aede9013c95ef67cdcfaf2ac57b672084705e07d4e81bf1edfacaeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `eclipse-temurin:19-jre-nanoserver-1809` - windows version 10.0.17763.4131; amd64

```console
$ docker pull eclipse-temurin@sha256:e4d1636292d2c80e50e1c651f1f28fa9c7b1184c4540a3c5a881da67c9c4ba94
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (154995293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e396121a5f539b5c060226bdef2d8c97b278e19d5a0af374c7030a4f8a53f5d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 11 Mar 2023 10:09:02 GMT
RUN Apply image 10.0.17763.4131
# Thu, 16 Mar 2023 00:45:50 GMT
SHELL [cmd /s /c]
# Thu, 16 Mar 2023 01:23:09 GMT
ENV JAVA_VERSION=jdk-19.0.2+7
# Thu, 16 Mar 2023 01:23:10 GMT
ENV JAVA_HOME=C:\openjdk-19
# Thu, 16 Mar 2023 01:23:11 GMT
USER ContainerAdministrator
# Thu, 16 Mar 2023 01:23:22 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Mar 2023 01:23:23 GMT
USER ContainerUser
# Thu, 16 Mar 2023 01:29:01 GMT
COPY dir:904161e5243ae36448a284ab932eb54925cce61a8b841396759eee721890e3f8 in C:\openjdk-19 
# Thu, 16 Mar 2023 01:29:21 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:95eb2f0f3287f5ec687287cc244924aafc74c7ada3121d43f54223487f3f2d8d`  
		Last Modified: Thu, 16 Mar 2023 01:43:14 GMT  
		Size: 106.7 MB (106684240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5837fe68a36caddf38b0aaa99f4ef20ca36d8dfe2825fa6ffbcf0d38b9d59a`  
		Last Modified: Thu, 16 Mar 2023 01:42:43 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0203cee4455804fb9efd8e5ab10476e33070a8381b133321b6040a7165dc13`  
		Last Modified: Thu, 16 Mar 2023 01:52:14 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b597da8738d9af3f7b678cb69221dd791517cffd43be0c5b8827d58396fc8f`  
		Last Modified: Thu, 16 Mar 2023 01:52:14 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b13b51bc5f7e086a7933dc25e93e541c6c5567835954dccda0b9acfa548c93`  
		Last Modified: Thu, 16 Mar 2023 01:52:14 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f93025d0762ff8183a41d12c546f8e1e228d843cd806b8517d9cb7a69d6416`  
		Last Modified: Thu, 16 Mar 2023 01:52:12 GMT  
		Size: 69.0 KB (69016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e445ed55caa35f1d5ff0e86202f3d3e09a051af742b5da6b3fefcd35016367`  
		Last Modified: Thu, 16 Mar 2023 01:52:12 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0665c3fcff5ead504b68d24b691cc315de3326821f62796884b1fe289898a439`  
		Last Modified: Thu, 16 Mar 2023 01:53:39 GMT  
		Size: 45.1 MB (45143376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9273603a5ff877ca764fd0e697003ffcc1150d97fce28d6df07b1e2971d0fd0f`  
		Last Modified: Thu, 16 Mar 2023 01:53:31 GMT  
		Size: 3.1 MB (3092851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
