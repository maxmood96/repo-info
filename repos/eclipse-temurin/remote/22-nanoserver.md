## `eclipse-temurin:22-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:b2519896cc5e2650f35f63bdb08908e20443f7f894a5fd303496f6843fffb819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `eclipse-temurin:22-nanoserver` - windows version 10.0.20348.2582; amd64

```console
$ docker pull eclipse-temurin@sha256:89910cf0dc4d345512e6bef8e1e56928a3821af1ad60ad3a28cf994bb2c5e669
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.3 MB (320261528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92357a2012b85371221830af291a48567c402840f3ff52437df5b23170ef7c93`
-	Default Command: `["jshell"]`
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
# Wed, 24 Jul 2024 01:38:47 GMT
COPY dir:bb8037d92e17293fdab4a72c09c9eb83e6a7b620b5e832c71d656bbaf7bd694c in C:\openjdk-22 
# Wed, 24 Jul 2024 01:38:59 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Jul 2024 01:39:00 GMT
CMD ["jshell"]
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
	-	`sha256:9878ea694d57674df47d487ae301f4ec17813fc173f87159312035ebd6d4d882`  
		Last Modified: Wed, 24 Jul 2024 02:28:22 GMT  
		Size: 199.6 MB (199623386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b6f965212caac27bdd9f33d4266980e3c28fca39c7feef698777c419796a49`  
		Last Modified: Wed, 24 Jul 2024 02:28:04 GMT  
		Size: 61.0 KB (61015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461e4e5c7cf7623c68324abbbd6eab266e6b393edb8614671749f07edc724eab`  
		Last Modified: Wed, 24 Jul 2024 02:28:04 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-nanoserver` - windows version 10.0.17763.6054; amd64

```console
$ docker pull eclipse-temurin@sha256:6fbcab6da732c486f85d62a2f54df874d78f3324f8ea88237284d26a30161a7d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.6 MB (358616326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab181accf0f64cbd8a1100565908dfad2728aa206124b5a43ec1f51249c66291`
-	Default Command: `["jshell"]`
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
# Wed, 24 Jul 2024 01:31:56 GMT
COPY dir:bb8037d92e17293fdab4a72c09c9eb83e6a7b620b5e832c71d656bbaf7bd694c in C:\openjdk-22 
# Wed, 24 Jul 2024 01:32:07 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Jul 2024 01:32:08 GMT
CMD ["jshell"]
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
	-	`sha256:b6227cdf5e9616d385c15de9781fd1749b3ff7b5a1e79144f055715da4b9601a`  
		Last Modified: Wed, 24 Jul 2024 02:26:07 GMT  
		Size: 199.6 MB (199623271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca53c743c4c3c9ad1e44b0c350ae366c559068e47fa97227b74f0829bcef416`  
		Last Modified: Wed, 24 Jul 2024 02:25:49 GMT  
		Size: 3.8 MB (3836387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801e25086323f3ed9d381865a2459e31e173f9123557daac17cdd3b00ef91640`  
		Last Modified: Wed, 24 Jul 2024 02:25:48 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
