## `eclipse-temurin:17-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:1bebf54c3579d9d4c14993ca2b5f033434f88de7249319db1d1189c59eb1de7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.26100.32690; amd64

```console
$ docker pull eclipse-temurin@sha256:e079ebc89f6543060c79ba66c8e336beed9803245dfa93299a3349990d4d9395
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.5 MB (387499919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e82ea0ab068a5bf08987d1742ac66b26e818b3495f87e2cbbf9a91dec0c3dc3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 06:39:57 GMT
RUN Apply image 10.0.26100.32690
# Fri, 08 May 2026 00:18:41 GMT
SHELL [cmd /s /c]
# Fri, 08 May 2026 00:18:42 GMT
ENV JAVA_VERSION=jdk-17.0.19+10
# Fri, 08 May 2026 00:18:43 GMT
ENV JAVA_HOME=C:\openjdk-17
# Fri, 08 May 2026 00:18:44 GMT
USER ContainerAdministrator
# Fri, 08 May 2026 00:18:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 08 May 2026 00:18:53 GMT
USER ContainerUser
# Fri, 08 May 2026 00:19:31 GMT
COPY dir:efa343062fcab6068fd499c77aea77fee33bf19a70fc27fbcf8f5891917744d1 in C:\openjdk-17 
# Fri, 08 May 2026 00:19:36 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 08 May 2026 00:19:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8af320c3b6d19296bcc7947e3beb8bc0c69cb12143db52efe988dc998ac088dc`  
		Last Modified: Tue, 14 Apr 2026 21:00:37 GMT  
		Size: 199.7 MB (199717094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad347274f05cd0a39f458f225ae71910741d1ac8af66bd1d3081aae8de1ec0b5`  
		Last Modified: Fri, 08 May 2026 00:19:46 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b2c256238bd573044477a5fdf1ee40ec211196a7435612559242aca4c10948`  
		Last Modified: Fri, 08 May 2026 00:19:46 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0046d9e798640903be77963046c8f99f57f0cfa95c19fe97d20acedde23ac44`  
		Last Modified: Fri, 08 May 2026 00:19:46 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25907ed21c74f36618ad093e7dcc0ef8f5afd5e5aef738f9e00b426f7b43c43f`  
		Last Modified: Fri, 08 May 2026 00:19:46 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a7bbfa6785a69c968d93d2d7cbbfb209017368d49ecf5f9a38a91e039047b2`  
		Last Modified: Fri, 08 May 2026 00:19:44 GMT  
		Size: 70.4 KB (70421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eeb69d5b9d9798ccdddb0172df47f7d2dfdf49ddeb90a07e435fb44913bfcd4`  
		Last Modified: Fri, 08 May 2026 00:19:44 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9b01e0a505c6435c4b29900a795b126af93f5da8c49e36308d542ae076cdbd`  
		Last Modified: Fri, 08 May 2026 00:19:56 GMT  
		Size: 187.6 MB (187621795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2b4eb565a36c6b4e8fb63cae08706a8036492315354767347196faf4c79743`  
		Last Modified: Fri, 08 May 2026 00:19:44 GMT  
		Size: 84.2 KB (84182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b801d654cdf1e6388f6f78eb9992eacb796af244012da25d2cfd382c3c2d09`  
		Last Modified: Fri, 08 May 2026 00:19:44 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-jdk-nanoserver` - windows version 10.0.20348.5020; amd64

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
