## `eclipse-temurin:21-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:a75deeeaa6dea97215a1df79f54d8121204ec9db0c086ed286741092890c1ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:21-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull eclipse-temurin@sha256:05b867c67a24f5c979cba6f38acd658de7f13909dd091a0f2b262e54d943035b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.0 MB (329022851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7186c81bbd573024b39c75f7bdc42d61031427d0a8208ec1d3ae7650e228f7ce`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Fri, 08 May 2026 01:16:55 GMT
SHELL [cmd /s /c]
# Fri, 08 May 2026 01:19:02 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 08 May 2026 01:19:02 GMT
ENV JAVA_HOME=C:\openjdk-21
# Fri, 08 May 2026 01:19:03 GMT
USER ContainerAdministrator
# Fri, 08 May 2026 01:19:05 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 08 May 2026 01:19:05 GMT
USER ContainerUser
# Fri, 08 May 2026 01:19:32 GMT
COPY dir:be4fce80d476aa164b4bdafca77eddb646da4c27d929101014e2067a583f974e in C:\openjdk-21 
# Fri, 08 May 2026 01:19:36 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 08 May 2026 01:19:36 GMT
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
	-	`sha256:002aaab2d1501fa277a3848dfed54e2f153b356ba20065aca094cd0b178c700c`  
		Last Modified: Fri, 08 May 2026 01:19:43 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3975ef8469aaea9251f7a60b5ce7d31b80a9398805991407f239d0cc0e31b736`  
		Last Modified: Fri, 08 May 2026 01:19:43 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249f8af28cdd24b6b740762da5a76aea757871411493a3bbefe6f482c2f6d296`  
		Last Modified: Fri, 08 May 2026 01:19:43 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de893b522b86054659969f64662e58914af58444bbb6b059097e03f87b9abf6a`  
		Last Modified: Fri, 08 May 2026 01:19:41 GMT  
		Size: 76.6 KB (76571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1e22950f9467a7d8f7667f73cc551a0b1249a410f9240864bce2439936b78e`  
		Last Modified: Fri, 08 May 2026 01:19:41 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b5a1ac766064b34724b2942c3e54159127ad7b304ba42e39f3ad502d7370e0`  
		Last Modified: Fri, 08 May 2026 01:19:55 GMT  
		Size: 201.9 MB (201874947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4559902326869c7c3c80f6afb560d73272e69c9bc4289212ca73feb1fb0cb9f`  
		Last Modified: Fri, 08 May 2026 01:19:41 GMT  
		Size: 108.9 KB (108949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3efacfc8f9970661122f2c03c899c6ebd7bdfe5ecb979329b74541be1969361`  
		Last Modified: Fri, 08 May 2026 01:19:41 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
