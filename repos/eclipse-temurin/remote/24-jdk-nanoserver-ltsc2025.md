## `eclipse-temurin:24-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:96d86162636bc3cd48f195e419a89e33c8194d7e5ebfd0130c96a3fe2052bdd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `eclipse-temurin:24-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.4652; amd64

```console
$ docker pull eclipse-temurin@sha256:94e9660a8f86a66e6277194a5ac93c6b17318018d9edd68c5c4c8ed5a1bb8953
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.7 MB (330723155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87824fd38161c35d7770f0a0433a62896719fd6a7effee8d026599b49d53d3ee`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Jul 2025 18:13:07 GMT
RUN Apply image 10.0.26100.4652
# Wed, 09 Jul 2025 19:14:46 GMT
SHELL [cmd /s /c]
# Wed, 09 Jul 2025 19:14:48 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 09 Jul 2025 19:14:49 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 09 Jul 2025 19:14:50 GMT
USER ContainerAdministrator
# Wed, 09 Jul 2025 19:14:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Jul 2025 19:14:54 GMT
USER ContainerUser
# Wed, 09 Jul 2025 19:15:01 GMT
COPY dir:ab006ab9903f5de6ad6a158af78f8d39737a3dacdd719a53420635ed01783e4e in C:\openjdk-24 
# Wed, 09 Jul 2025 19:15:08 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Jul 2025 19:15:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2fd4507679915420227c89c4f57165747b37deaa62748936e2af8c2f38de0b4e`  
		Last Modified: Wed, 09 Jul 2025 01:51:41 GMT  
		Size: 193.2 MB (193150329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad327be3c2dcaaf31352fa29583c138b4a9d24bb74742c703cf586f1a35ae0fc`  
		Last Modified: Wed, 09 Jul 2025 19:15:44 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731561573cdd816338e149bb6f983917dbf80556ca2bcd33b189971c9fc6a2ac`  
		Last Modified: Wed, 09 Jul 2025 19:15:44 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f7bed733ede79229057106f671fb45857c6d130bdaba630aa03b0cf5502f6c`  
		Last Modified: Wed, 09 Jul 2025 19:15:44 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c90095f27974300543bd8bc247a009cd7563d8749bf24d31eaa7300a4429bc5`  
		Last Modified: Wed, 09 Jul 2025 19:15:45 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a78ef53837e2bd4c30b262e9c88c950afa9c50432c75c79076896bddad41e7b`  
		Last Modified: Wed, 09 Jul 2025 19:15:45 GMT  
		Size: 76.2 KB (76166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a17b4e411b16e609be2bf3eb44c06cee6f465267f1009502d7c6386e4e6462a`  
		Last Modified: Wed, 09 Jul 2025 19:15:45 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c2266dd2ec294d9938d6668e893df8dc81df2a663044d986be924da6e6523a`  
		Last Modified: Wed, 09 Jul 2025 21:16:47 GMT  
		Size: 137.4 MB (137364451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7f9d8cc54242c69f5f0c195f1d9880ca0a4de28f48228c906c6fd102c61da3`  
		Last Modified: Wed, 09 Jul 2025 19:15:45 GMT  
		Size: 126.0 KB (125976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:284cfecb0da0f5e84ff8044c226c7ebdce77aef5070aac1b8f5a0a61affb155a`  
		Last Modified: Wed, 09 Jul 2025 19:15:45 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
