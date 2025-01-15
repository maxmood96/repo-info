## `eclipse-temurin:23-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:927670578988997d2399ac3f10d8eba9365041732a59b34b12fdf8fbc7bd672d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `eclipse-temurin:23-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:1ae21a6b22aab158d3b6e38abebf46f8119588bb17571e33df1ba7efa7e81d53
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.5 MB (170463804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1abbbeb494c58efa3c01e747585fcca1c01669274a988f8288e856858347ba5c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Wed, 15 Jan 2025 18:03:13 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2025 18:03:14 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 15 Jan 2025 18:03:14 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 15 Jan 2025 18:03:15 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 18:03:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jan 2025 18:03:18 GMT
USER ContainerUser
# Wed, 15 Jan 2025 18:03:22 GMT
COPY dir:d9adc234ed2c06cd6b72c0beb8933c6d824941dbd1cece41e4fd2578b0632fbd in C:\openjdk-23 
# Wed, 15 Jan 2025 18:03:26 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532e17b0790b6e1832e11f22a266a6a5eb69fd84f07da121233952b8684e4a31`  
		Last Modified: Wed, 15 Jan 2025 18:03:29 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d3721bf7befffb6a5852d6b67f152c8805f3cdf7991cf7d119d90795331960`  
		Last Modified: Wed, 15 Jan 2025 18:03:30 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d319c145a80c264d644ff527851a1d329c2fc6866ba71f10d47495af3f174131`  
		Last Modified: Wed, 15 Jan 2025 18:03:30 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4a7e78e2aa821c81a1559ae141a5f472fa836e75248784e9631b78ac4097c9`  
		Last Modified: Wed, 15 Jan 2025 18:03:29 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22abe115225a59da232cf27d122bb82f6927012f05e1f7ac1781e17874c0e2e1`  
		Last Modified: Wed, 15 Jan 2025 18:03:29 GMT  
		Size: 78.7 KB (78739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5fecf51c175fbb713b083d695d63c13638bd163a7308c955227fcf1f43e7a2`  
		Last Modified: Wed, 15 Jan 2025 18:03:29 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab86d41bf3788ae8fdc29998f809f5a056623d87ed1c74d0230bda8ff0330c9`  
		Last Modified: Wed, 15 Jan 2025 18:03:34 GMT  
		Size: 49.6 MB (49609827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb88b9b50f4b394798e55a3d4e346e017510b93738dc04a745294868fcbacc1`  
		Last Modified: Wed, 15 Jan 2025 18:03:29 GMT  
		Size: 108.5 KB (108514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
