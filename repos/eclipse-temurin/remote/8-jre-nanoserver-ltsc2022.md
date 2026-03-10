## `eclipse-temurin:8-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:b388970c77e68e14c67e67badeb3779097fe090b0cbeb83953eab4a35d3b4279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull eclipse-temurin@sha256:28a45b77845361ea7f13d0df7218e2e93334a64a94dc2677cf989d734806fff1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166792069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e8160ddd2a4deb7d4c4b5eeea7add6ba45c551893ee7be101efb796084035f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 22:36:11 GMT
SHELL [cmd /s /c]
# Tue, 10 Mar 2026 22:36:11 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 10 Mar 2026 22:36:11 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 10 Mar 2026 22:36:12 GMT
USER ContainerAdministrator
# Tue, 10 Mar 2026 22:36:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Mar 2026 22:36:15 GMT
USER ContainerUser
# Tue, 10 Mar 2026 22:36:19 GMT
COPY dir:e192ec1627bb02acae941746a6647cea6857b84f7daa4f746913822a0bac9dcc in C:\openjdk-8 
# Tue, 10 Mar 2026 22:36:21 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62fed3face2429e33d46c7bd16d631ccc57a3988e4f3168d9273ff5de0c9322`  
		Last Modified: Tue, 10 Mar 2026 22:36:27 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4fd65e0469201dadc3edff28384911d4def88318dc23e644b851042be30fc2`  
		Last Modified: Tue, 10 Mar 2026 22:36:27 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e059762a06d6a119ce1b465d7cea3042db7179af40d204a90b42006a393a984`  
		Last Modified: Tue, 10 Mar 2026 22:36:27 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b17203df2ee9bca3f6ee15fd7c51aa59633ab570871c467e65eb5becdace1d`  
		Last Modified: Tue, 10 Mar 2026 22:36:25 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b16b0ff42435282c5afa5b997f0637a4ffe68483ec9318c927fc3a891398b40`  
		Last Modified: Tue, 10 Mar 2026 22:36:25 GMT  
		Size: 75.6 KB (75613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcda8f8c9a37b57802a80ebc4d06357e5f00ef131a42a2c097f7934901125d6e`  
		Last Modified: Tue, 10 Mar 2026 22:36:25 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932da3ec230955558fdf6c187ef216cffc580f4931b955e22c4ccc3d962d4a48`  
		Last Modified: Tue, 10 Mar 2026 22:36:30 GMT  
		Size: 40.0 MB (39969724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6ca16d499e0bb29fc86ca2518b24b70146c5b0fc0a50748be7507f9a11da49`  
		Last Modified: Tue, 10 Mar 2026 22:36:26 GMT  
		Size: 90.9 KB (90920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
