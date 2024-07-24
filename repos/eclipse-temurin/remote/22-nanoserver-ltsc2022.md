## `eclipse-temurin:22-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:8a4b436dda2258b7f77ed8e8b9a507f6d9ef1e2b4c775d6efd1ed0cea41139a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `eclipse-temurin:22-nanoserver-ltsc2022` - windows version 10.0.20348.2582; amd64

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
