## `eclipse-temurin:25-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:7ab78a17bc40c987c1cc724bbda29a36376fc7d349ab01c6d12431c865936f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:25-jre-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull eclipse-temurin@sha256:ab89ef1b45e4896aa9d573e36e21610b9abe4025ad84124f60e83bf95e99a0d2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.7 MB (185716423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459eb8b9d9a948eb11f24f155fb897775134aba3250f23b6032b23a57f0c3a84`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 22:10:54 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2026 22:11:55 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 14 Apr 2026 22:11:56 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 14 Apr 2026 22:11:56 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 22:11:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Apr 2026 22:11:58 GMT
USER ContainerUser
# Tue, 14 Apr 2026 22:12:02 GMT
COPY dir:15db28d5461f0a5f42074eb42e42a8535b9576d6847f4e637cb0dcfe9abfaabd in C:\openjdk-25 
# Tue, 14 Apr 2026 22:12:05 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb76372f891d59e4ebbbeccc9b555f61ecb435fcdb080de2d905e512c8ed9ef3`  
		Last Modified: Tue, 14 Apr 2026 22:11:20 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b578fc46676376a826a9eaa921cdd8dcbb3e97d4dcbb3b5004afe655198952d`  
		Last Modified: Tue, 14 Apr 2026 22:12:10 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf4fa0ab94917502abbac5387a079b5e5651cf23ba6ca6243b44035479f562c`  
		Last Modified: Tue, 14 Apr 2026 22:12:10 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72b9a1312b234eb11295fda8a06a0e5b7c3619d0f69f20daad576d40d891aa6`  
		Last Modified: Tue, 14 Apr 2026 22:12:09 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3704b0b2d2429ce1ce9fcc356c7eb96928d0e3673847c85350ed376efad4e5`  
		Last Modified: Tue, 14 Apr 2026 22:12:09 GMT  
		Size: 80.3 KB (80289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab236dc1da2bc1e1461ed35ae1d25e36018fd550fcfe9d22ec401d2a8964f43`  
		Last Modified: Tue, 14 Apr 2026 22:12:09 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac30925104527aa488218be1f7f17717bc387c3a5fa951c31a714f712c8afa3`  
		Last Modified: Tue, 14 Apr 2026 22:12:16 GMT  
		Size: 58.6 MB (58582955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef06ce5d9a53d8106d3ff7e30b7e18194f5c27c1f3e5095d8bfb470646134c3a`  
		Last Modified: Tue, 14 Apr 2026 22:12:09 GMT  
		Size: 91.9 KB (91917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
