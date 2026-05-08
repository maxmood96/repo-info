## `eclipse-temurin:21-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:def3ec00082e6c7fa3d886e35fb3e95d3086f584c0af90727beb5e266632c863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `eclipse-temurin:21-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32690; amd64

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
