## `eclipse-temurin:8u492-b09-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:53773240c7137879f1461f1448d70311be9b14e5a9f6b6160c3d03258236ae6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:8u492-b09-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull eclipse-temurin@sha256:dafc25fd7a7c5aaaa2469ca70f6328e06e98f9c5a6485eb7175d6d057adad1de
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (229023414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b8994318733e1281f42fa6c5a06b3d26c6201bc3be6eedf5c9ce71bca52132`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 12 May 2026 22:09:20 GMT
SHELL [cmd /s /c]
# Tue, 12 May 2026 22:09:20 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 22:09:21 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 12 May 2026 22:09:21 GMT
USER ContainerAdministrator
# Tue, 12 May 2026 22:09:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 12 May 2026 22:09:33 GMT
USER ContainerUser
# Tue, 12 May 2026 22:09:53 GMT
COPY dir:25077d8770e7edce418eff57fe3a0561246eac55d5c42b7efa90e67ec851bbed in C:\openjdk-8 
# Tue, 12 May 2026 22:09:57 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef25a6bd0a5d088fd7d161f38a6fa9b306a38e4561457d556a3a61b32ca47fa`  
		Last Modified: Tue, 12 May 2026 22:10:03 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57fe2a0cb5c6bec4aacef0184e263f63388571a29a942d6dcfd0fc52a3bf481`  
		Last Modified: Tue, 12 May 2026 22:10:03 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3714022026eec71fe9060545f20ebea9d412d41f4c8892478e5eed5edc4ee7`  
		Last Modified: Tue, 12 May 2026 22:10:03 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02f613aeef7e06ed751ec3858b8e274ea3ac03273e226122ec78f70679b7afd3`  
		Last Modified: Tue, 12 May 2026 22:10:01 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:535e9b3adb43e9ee223b45aa1474371709a6dddb57f9d8c8bdcbc9de4d9853ee`  
		Last Modified: Tue, 12 May 2026 22:10:01 GMT  
		Size: 70.5 KB (70528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91807aeb1d0113c7e8cbc36cda06c2d4e01945e53bd7ccf6132619163b4cf67f`  
		Last Modified: Tue, 12 May 2026 22:10:01 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e80cce25d0d9092291aedb60dbf231526649562dabbb72a7d6620bee1b8ff52`  
		Last Modified: Tue, 12 May 2026 22:10:09 GMT  
		Size: 101.9 MB (101915855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a04dc4c6387b14ddcb20b05496d36dfc8e2462d352a47ca9d79444907ae2a52`  
		Last Modified: Tue, 12 May 2026 22:10:01 GMT  
		Size: 75.8 KB (75780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
