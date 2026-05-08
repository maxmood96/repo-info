## `eclipse-temurin:17-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:994f12d4d152604fcf22534114ae632fbbd3f5da570c156f40ccf7c24971bceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:17-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull eclipse-temurin@sha256:8af10f163df8bbe0baf948904ab92adf5f93345c88bd5dee242ea09cac4c2982
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.8 MB (314752495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08266f0048dc4bde585bb1d008f6c62ab374f64c3e7f1d7a018577bf62b8de2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Fri, 08 May 2026 01:16:55 GMT
SHELL [cmd /s /c]
# Fri, 08 May 2026 01:16:56 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 08 May 2026 01:16:57 GMT
ENV JAVA_HOME=C:\openjdk-17
# Fri, 08 May 2026 01:16:58 GMT
USER ContainerAdministrator
# Fri, 08 May 2026 01:17:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 08 May 2026 01:17:11 GMT
USER ContainerUser
# Fri, 08 May 2026 01:17:59 GMT
COPY dir:efa343062fcab6068fd499c77aea77fee33bf19a70fc27fbcf8f5891917744d1 in C:\openjdk-17 
# Fri, 08 May 2026 01:18:04 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 08 May 2026 01:18:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c932f1703fc4158049513ac39c89d71779184c39d2a72e9e2433220182b07689`  
		Last Modified: Fri, 08 May 2026 01:18:13 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324587036b9527b515d973d9781907ee10da860b67b60906753edb8b66d31e34`  
		Last Modified: Fri, 08 May 2026 01:18:13 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adbea167f8a435a3b8522856721a7eaacdad2a08a16bb4faff2c4166ef7484af`  
		Last Modified: Fri, 08 May 2026 01:18:13 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71b5010181278fb5d0d3f89ae309368389aeb83b5e8f444f6c9b27aeadc1891`  
		Last Modified: Fri, 08 May 2026 01:18:13 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54869b7a0e517167a88666c3e31d170aacce4ef021f6c97721ed071902a5d731`  
		Last Modified: Fri, 08 May 2026 01:18:12 GMT  
		Size: 71.1 KB (71058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12340ece17c5f306b49d39f6efc5f7be913cb34206fdb86fa24fb834a6dca847`  
		Last Modified: Fri, 08 May 2026 01:18:12 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc3561f3a3db3937fa716fc69dc94c1c1a141e2b33525036e7d7e92d6c895b0`  
		Last Modified: Fri, 08 May 2026 01:18:24 GMT  
		Size: 187.6 MB (187622111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6eeb2178203b76a974e8e023cef6a1fa1b5c2673caacb443a26d9d596698fa`  
		Last Modified: Fri, 08 May 2026 01:18:12 GMT  
		Size: 97.0 KB (97001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a8ee30fd5e508445695144d07af10ff18556971fba25dd277f801360c95c14`  
		Last Modified: Fri, 08 May 2026 01:18:12 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
