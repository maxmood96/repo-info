## `eclipse-temurin:8u482-b08-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:fe6ec6ebf2fd80c30287711d1d8213fb2170866f88dfbbb05f03bf19d771b909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:8u482-b08-jre-nanoserver` - windows version 10.0.26100.32690; amd64

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

### `eclipse-temurin:8u482-b08-jre-nanoserver` - windows version 10.0.20348.5020; amd64

```console
$ docker pull eclipse-temurin@sha256:4a2c6a1efad9afc8136c87f9380aa1c8327a24b192a4ffd6430300fe9066e293
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.1 MB (167108580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8a8b10d7455f4035a3c2138cd7e8826121e3c59018732f69b55bf7645afb3f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 22:10:49 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2026 22:10:49 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 14 Apr 2026 22:10:49 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 14 Apr 2026 22:10:50 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 22:10:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Apr 2026 22:10:52 GMT
USER ContainerUser
# Tue, 14 Apr 2026 22:10:55 GMT
COPY dir:e192ec1627bb02acae941746a6647cea6857b84f7daa4f746913822a0bac9dcc in C:\openjdk-8 
# Tue, 14 Apr 2026 22:10:58 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f577f04bf25fbe8b679de7ed1a1bb3aec05c54b5f22de311414b5b7e7dbe8fb5`  
		Last Modified: Tue, 14 Apr 2026 22:11:03 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627115c5acf0bbe2330d834f939b20ec42ae5eccd56fe9cdc017539a89542ace`  
		Last Modified: Tue, 14 Apr 2026 22:11:03 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3840c2e36b7730ef3c32fe05845e820a3d16d81acf6cb3c6d8eb64c4e10a88f4`  
		Last Modified: Tue, 14 Apr 2026 22:11:03 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2715f7d177c97b6cb40ef5e323b3c5b65fe73120058fc834a067470896507b8f`  
		Last Modified: Tue, 14 Apr 2026 22:11:02 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d645f38d3a895b39f6a169b107fe4293e94cd4b03e37d1475b8c8d7909dbabc`  
		Last Modified: Tue, 14 Apr 2026 22:11:02 GMT  
		Size: 76.7 KB (76726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5528f1e81988ed88686c4b1383a4eace5ee00eca1b1b30f2dfffc3d700711381`  
		Last Modified: Tue, 14 Apr 2026 22:11:02 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856de40e90ad12b653314e3c03cdef514e268b3a4140ba50e8f7c329bf5502e6`  
		Last Modified: Tue, 14 Apr 2026 22:11:06 GMT  
		Size: 40.0 MB (39969915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3a9e1809fc6cd00f664b50fc8b7ccf54c66c7290510c6051a79acfd153c60c`  
		Last Modified: Tue, 14 Apr 2026 22:11:02 GMT  
		Size: 100.7 KB (100692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
