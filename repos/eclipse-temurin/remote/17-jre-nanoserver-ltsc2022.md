## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:94c1c43513816334ae16d85355642b3cb43b0b4d2ab44cee4fe4f93e5ea9c9da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1249; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1249; amd64

```console
$ docker pull eclipse-temurin@sha256:ea9c0f7f4b2bb9f7c0e3715f8ebf1ecde418f0050a08cf75f722516cf0e353a7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.5 MB (165521749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc33543a9b0610ae9b4622ab785ab0a701f9bc21ce68212ee1fd820ec1bae5c9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Nov 2022 07:21:30 GMT
RUN Apply image 10.0.20348.1249
# Tue, 08 Nov 2022 19:27:23 GMT
SHELL [cmd /s /c]
# Tue, 08 Nov 2022 19:31:41 GMT
ENV JAVA_VERSION=jdk-17.0.5+8
# Tue, 08 Nov 2022 19:31:42 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 08 Nov 2022 19:31:43 GMT
USER ContainerAdministrator
# Tue, 08 Nov 2022 19:31:59 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 08 Nov 2022 19:32:00 GMT
USER ContainerUser
# Tue, 08 Nov 2022 19:33:27 GMT
COPY dir:20852dc87397947f41c5a6f7f30dc526aa127dbd27640e91343bc06b34d57a7f in C:\openjdk-17 
# Tue, 08 Nov 2022 19:33:51 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:72e5d750fe8c1a32d4a26ef3b4a4e1f6124ac079b142f12724af2abfcba1c8b3`  
		Last Modified: Tue, 08 Nov 2022 19:57:58 GMT  
		Size: 122.1 MB (122092167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd83067a7e6c6d9dab3ac0265a21919de95a0bf4e737e647fbf3e43c9874b0`  
		Last Modified: Tue, 08 Nov 2022 19:57:27 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df9fbea36ffc078ae0e4b51819bb0a036f7e4ed68b0ab258a75a21d3cff70968`  
		Last Modified: Tue, 08 Nov 2022 19:59:27 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69bb56c987d6ccea4c4faf4e59e21868ba4b671a45348326f2f3a0635d36e7b6`  
		Last Modified: Tue, 08 Nov 2022 19:59:28 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2826d5cbecf5e352a40c64be93a8435927f58594941d3700c3b66bd1a4ea5a12`  
		Last Modified: Tue, 08 Nov 2022 19:59:27 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c698d6626dffc79e30d4b30ee1b35f3196235422377db691449c4479ecf335`  
		Last Modified: Tue, 08 Nov 2022 19:59:25 GMT  
		Size: 81.4 KB (81405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e989e10d6bdbb37e4d9ae67fff479d4652dc06b485f73ae4607bbd93cfcdb14e`  
		Last Modified: Tue, 08 Nov 2022 19:59:25 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38accb0fdc7b406c97ce7785386a64171076234c3f2291bba9761f83d322e797`  
		Last Modified: Tue, 08 Nov 2022 20:00:09 GMT  
		Size: 43.3 MB (43280621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d85d738a63f3cf0eb9eade568dff788fa63ebc360f9bd29a37db27035996a0`  
		Last Modified: Tue, 08 Nov 2022 20:00:00 GMT  
		Size: 61.8 KB (61840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
