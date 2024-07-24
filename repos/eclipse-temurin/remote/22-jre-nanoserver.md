## `eclipse-temurin:22-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:817eb9bfa77189485b0c2b20af73240e6fd90ea6470ba1e15176c2b6545247a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:22-jre-nanoserver` - windows version 10.0.20348.2582; amd64

```console
$ docker pull eclipse-temurin@sha256:ab5ab84682d2c4b59008b508f9b3b4f610e91b56830849cb4a6d7ca36cdf95ed
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.0 MB (169004291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02ea5b7a9478c34a35023c9cda3ddd5d7191f98e33dc0d78da9aa9ff5bf34a1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 09:30:07 GMT
RUN Apply image 10.0.20348.2582
# Wed, 10 Jul 2024 17:17:20 GMT
SHELL [cmd /s /c]
# Wed, 24 Jul 2024 01:38:21 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Wed, 24 Jul 2024 01:38:21 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 24 Jul 2024 01:38:22 GMT
USER ContainerAdministrator
# Wed, 24 Jul 2024 01:38:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Jul 2024 01:38:31 GMT
USER ContainerUser
# Wed, 24 Jul 2024 01:39:12 GMT
COPY dir:65be971618b84fe71c044bdca6efe8a2b46f4ab6c5b677a6f304a9c5505af541 in C:\openjdk-22 
# Wed, 24 Jul 2024 01:39:23 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:652774a5d82a114642848f8b0b8d486ec1b4995f9dda56e36fe4ac7563429990`  
		Last Modified: Tue, 09 Jul 2024 20:33:26 GMT  
		Size: 120.5 MB (120490378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dbb650483c31087741ccfe7cfef17abfd7465711d0851e35d39eabc775bdae`  
		Last Modified: Wed, 10 Jul 2024 17:38:52 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ae3e35c1f7e9276c646c0634f2ec6887c8c30d2cd8bd29518fa9f969e8d84e`  
		Last Modified: Wed, 24 Jul 2024 02:28:06 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c92a9d9a53d01d0d02e81f16578e349e9c6c45b10fa6c95c20341b93df7b82`  
		Last Modified: Wed, 24 Jul 2024 02:28:06 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b95688648192b3604e7c7d4ca26b0aa24b0d722436ac4b7feac4c85f40834c`  
		Last Modified: Wed, 24 Jul 2024 02:28:06 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7175626526d0587619df800faf2989fbab0ab480efb6cf9d76b76632bd486307`  
		Last Modified: Wed, 24 Jul 2024 02:28:04 GMT  
		Size: 79.9 KB (79870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d5c4d0ce92d8abe6e949e65e8cd34417ec5cf0a2cfd41aeed3043870800db5`  
		Last Modified: Wed, 24 Jul 2024 02:28:04 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233b305467fa39fcab18581ef45a4b42ceb276edc2b24dfbf0c5050274d593f8`  
		Last Modified: Wed, 24 Jul 2024 02:28:41 GMT  
		Size: 48.4 MB (48367261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9fbc9d57cde9a4e487cf4eab5cc76102c238aa970e411dc348506dc4ae9409c`  
		Last Modified: Wed, 24 Jul 2024 02:28:33 GMT  
		Size: 61.0 KB (61025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-jre-nanoserver` - windows version 10.0.17763.6054; amd64

```console
$ docker pull eclipse-temurin@sha256:ddf1447856aecea609a5e08882233e69bc3017a2537f421c1e410fcb8006bca1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.9 MB (206912772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18056e00b52129adc128d1412d2da900f8c31807de01bd1382d31926ce925412`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 16:38:43 GMT
SHELL [cmd /s /c]
# Wed, 24 Jul 2024 01:31:35 GMT
ENV JAVA_VERSION=jdk-22.0.2+9
# Wed, 24 Jul 2024 01:31:36 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 24 Jul 2024 01:31:36 GMT
USER ContainerAdministrator
# Wed, 24 Jul 2024 01:31:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Jul 2024 01:31:44 GMT
USER ContainerUser
# Wed, 24 Jul 2024 01:36:12 GMT
COPY dir:65be971618b84fe71c044bdca6efe8a2b46f4ab6c5b677a6f304a9c5505af541 in C:\openjdk-22 
# Wed, 24 Jul 2024 01:36:22 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00a79547db1bc3ab4a5550f2ec9ba165e302f4a4984af3c1bfbbbe1726a3bf6`  
		Last Modified: Wed, 10 Jul 2024 17:28:00 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c82941c8847f46f3abb44013c628dce3a04bd9b35c64e0c75ad1e3efeb5d14`  
		Last Modified: Wed, 24 Jul 2024 02:25:50 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d4093fa16807be9336588c4af670f751fe872cace5bd8c244992868f2da30d4`  
		Last Modified: Wed, 24 Jul 2024 02:25:50 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9617cc683bc9bcad6d3f3c19a5574f82d364531847b57f9ec1adc031901237`  
		Last Modified: Wed, 24 Jul 2024 02:25:50 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679086a23836613457fe0818e8a433c17497f677ae6958b7fc0cdda845b1374d`  
		Last Modified: Wed, 24 Jul 2024 02:25:48 GMT  
		Size: 68.4 KB (68417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e5b91d2a5fe412cb2a8c2f7be0f2e0e67aed42c5de9a1ef55bf0d2e60b01b0`  
		Last Modified: Wed, 24 Jul 2024 02:25:48 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79621f44972abae854e157b38a9d52504208bd43ddfc48b28b37b047033e7cf`  
		Last Modified: Wed, 24 Jul 2024 02:27:06 GMT  
		Size: 48.4 MB (48367185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444e26792409a915046ca4a5eb969ba9bcc067943f23c7ddd654b7fc64c89015`  
		Last Modified: Wed, 24 Jul 2024 02:26:58 GMT  
		Size: 3.4 MB (3390036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
