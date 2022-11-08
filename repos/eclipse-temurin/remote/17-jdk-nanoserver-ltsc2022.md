## `eclipse-temurin:17-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:6e9566e749473ef52bbe1af08c18ac476776a9c81aab8dc5d7c844739d803bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1249; amd64

### `eclipse-temurin:17-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.1249; amd64

```console
$ docker pull eclipse-temurin@sha256:07c3d14d4ed425ac71f56a51bdb09f48902ba0d55b197c622902086335daecd3
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307694359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ce38a96b2a0af2ee44840f69c9e78d1f332d3ec99668d0792383fd7a4b3158`
-	Default Command: `["jshell"]`
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
# Tue, 08 Nov 2022 19:32:18 GMT
COPY dir:a12ba5a18c812bc88dc6c1e12f0d0bdbacab70db88697cd6bad273d4570ac4fb in C:\openjdk-17 
# Tue, 08 Nov 2022 19:32:53 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 08 Nov 2022 19:32:54 GMT
CMD ["jshell"]
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
	-	`sha256:6725da78579eafc2a9ad8c1b02254528195968c0072793fd01b40a9392c2a997`  
		Last Modified: Tue, 08 Nov 2022 19:59:46 GMT  
		Size: 185.4 MB (185422397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd4caaa25490d73540786fdba0d6199d74089e75749de9c1cfaaaf5af2dacd8`  
		Last Modified: Tue, 08 Nov 2022 19:59:25 GMT  
		Size: 91.5 KB (91504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dee44b889dde55fd1fcdbbefc3e3f0904870acdbeebd0c672932fa715b24e9`  
		Last Modified: Tue, 08 Nov 2022 19:59:25 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
