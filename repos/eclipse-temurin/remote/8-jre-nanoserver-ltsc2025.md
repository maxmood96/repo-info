## `eclipse-temurin:8-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:13767229a0457fc58c96737113bc6d856a96ce626cdd39f9b9b0a756e49cf864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull eclipse-temurin@sha256:cde34f6650c9a2868ac3834ccbb48b2f422f888f06e88f9451f161e5250c7609
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239864901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d39748813a5bfbc50290a6f545c8350de0786b82d7d80bd168573374294324`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 06:39:57 GMT
RUN Apply image 10.0.26100.32690
# Tue, 14 Apr 2026 22:13:08 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2026 22:13:10 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 14 Apr 2026 22:13:11 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 14 Apr 2026 22:13:11 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 22:13:18 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Apr 2026 22:13:19 GMT
USER ContainerUser
# Tue, 14 Apr 2026 22:13:34 GMT
COPY dir:e192ec1627bb02acae941746a6647cea6857b84f7daa4f746913822a0bac9dcc in C:\openjdk-8 
# Tue, 14 Apr 2026 22:13:39 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:8af320c3b6d19296bcc7947e3beb8bc0c69cb12143db52efe988dc998ac088dc`  
		Last Modified: Tue, 14 Apr 2026 21:00:37 GMT  
		Size: 199.7 MB (199717094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5d43251d43f1fc3f3fd695fb2118ba9b9e47c1ad625d2e06ad3eaa048fdd83`  
		Last Modified: Tue, 14 Apr 2026 22:13:45 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b2f6cb48aee56772930e141c4278492b9854e3116fc04d042d03b6b60408ef`  
		Last Modified: Tue, 14 Apr 2026 22:13:45 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136bdb4d5201777aa9a7f2fb032f37edcd2301fea7ce2794fa236e1e818cd677`  
		Last Modified: Tue, 14 Apr 2026 22:13:45 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98162e58e1c89a20ecfd214c0ffb7b34122c9f5407048dcc41f1b16413066ae`  
		Last Modified: Tue, 14 Apr 2026 22:13:43 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28760333430efe40611654b69ba95631c4f6752b63612b925655cc3cf12aa2c`  
		Last Modified: Tue, 14 Apr 2026 22:13:44 GMT  
		Size: 70.4 KB (70360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8f5572457f9b97cf469ab49f9011a64866b253a359af92ecc7147aa15d5495`  
		Last Modified: Tue, 14 Apr 2026 22:13:43 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99297ca897e97cda3743bae7a3d8db2e20649a06818ece0b3624ab10db38faab`  
		Last Modified: Tue, 14 Apr 2026 22:13:48 GMT  
		Size: 40.0 MB (39969816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584586b5ab99eb5f219acb236424987badc76f6f40c5c6b389745e9474edcaf9`  
		Last Modified: Tue, 14 Apr 2026 22:13:44 GMT  
		Size: 102.3 KB (102262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
