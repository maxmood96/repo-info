## `eclipse-temurin:21-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:b8160f4dbd1106bf3fcb7924f7fa094a9aa1e9760133ba4bfd0b4f841eeca910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:21-jdk-nanoserver` - windows version 10.0.26100.32690; amd64

```console
$ docker pull eclipse-temurin@sha256:52dbf5dd1401937736f951f813515fd4f517ea69c4ed7123d4c229e5345e4343
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.8 MB (401770599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad3e341a5770b805579dbf81e4183e95584193190e2a0d8f563e4e080dfe2b2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 06:39:57 GMT
RUN Apply image 10.0.26100.32690
# Fri, 08 May 2026 01:16:28 GMT
SHELL [cmd /s /c]
# Fri, 08 May 2026 01:16:29 GMT
ENV JAVA_VERSION=jdk-21.0.11+10
# Fri, 08 May 2026 01:16:29 GMT
ENV JAVA_HOME=C:\openjdk-21
# Fri, 08 May 2026 01:16:30 GMT
USER ContainerAdministrator
# Fri, 08 May 2026 01:16:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 08 May 2026 01:16:46 GMT
USER ContainerUser
# Fri, 08 May 2026 01:17:37 GMT
COPY dir:be4fce80d476aa164b4bdafca77eddb646da4c27d929101014e2067a583f974e in C:\openjdk-21 
# Fri, 08 May 2026 01:17:42 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 08 May 2026 01:17:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8af320c3b6d19296bcc7947e3beb8bc0c69cb12143db52efe988dc998ac088dc`  
		Last Modified: Tue, 14 Apr 2026 21:00:37 GMT  
		Size: 199.7 MB (199717094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc78f0e0bd2cb417d9b8cc2243ad6d30282bfe576edb32de92827596f7fb434`  
		Last Modified: Fri, 08 May 2026 01:17:48 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518e83bec2c2b502449068a542133968952663aabad8d09dafc07fff9da4ed01`  
		Last Modified: Fri, 08 May 2026 01:17:48 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9866dcc5da18c5d58b28a08dff2abe8b6e364a1cd54ca5546368b896fb0d80f`  
		Last Modified: Fri, 08 May 2026 01:17:48 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97eebd44ca877d43befe65b8bcaeef8254920747b13e1a231656d0d70a6be7df`  
		Last Modified: Fri, 08 May 2026 01:17:48 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce34f502e8ef07d7bce3a1023378be60e55efc37832697e14e3f00021696e06`  
		Last Modified: Fri, 08 May 2026 01:17:47 GMT  
		Size: 69.8 KB (69797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0528f043046898446172dfcc24cb5c88f556fe4aafe528d8c86de31978220fa3`  
		Last Modified: Fri, 08 May 2026 01:17:47 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14bbebc55cad88cafdbbf2cdbd2b39fedcd0371cd3687e818571612704a0cf0`  
		Last Modified: Fri, 08 May 2026 01:18:01 GMT  
		Size: 201.9 MB (201874946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b022b6af247bc76ccf0f9644b4f1ad4ddd4ebfb4d206dcaef34e346354a16562`  
		Last Modified: Fri, 08 May 2026 01:17:47 GMT  
		Size: 102.3 KB (102342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe13beeb484cc9046e9e41e2ca10c50d5f50ce6307701ef406c46cc99a64104`  
		Last Modified: Fri, 08 May 2026 01:17:47 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jdk-nanoserver` - windows version 10.0.20348.5020; amd64

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
