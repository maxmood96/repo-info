## `eclipse-temurin:8-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:30df317d1694cd22958efe54e0128e5a242a1d94ea3629fbb52f981359083b08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:8-nanoserver` - windows version 10.0.26100.32690; amd64

```console
$ docker pull eclipse-temurin@sha256:137c2c51789e9da4b0a239eaf386d8d2f2b73a9ccb48baddb6b3e1e193165924
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.8 MB (301828754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0d241b29114e5953cec4a98f4a6ffbf2bec6a0b21b9e3b44a29fe8638f0216`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 06:39:57 GMT
RUN Apply image 10.0.26100.32690
# Tue, 12 May 2026 21:49:48 GMT
SHELL [cmd /s /c]
# Tue, 12 May 2026 21:49:49 GMT
ENV JAVA_VERSION=jdk8u492-b09
# Tue, 12 May 2026 21:49:49 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 12 May 2026 21:49:50 GMT
USER ContainerAdministrator
# Tue, 12 May 2026 21:50:05 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 12 May 2026 21:50:05 GMT
USER ContainerUser
# Tue, 12 May 2026 21:50:46 GMT
COPY dir:25077d8770e7edce418eff57fe3a0561246eac55d5c42b7efa90e67ec851bbed in C:\openjdk-8 
# Tue, 12 May 2026 21:50:56 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:8af320c3b6d19296bcc7947e3beb8bc0c69cb12143db52efe988dc998ac088dc`  
		Last Modified: Tue, 14 Apr 2026 21:00:37 GMT  
		Size: 199.7 MB (199717094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb032b1190615a317f409ee2e3b102c05217ee0e7f44bcf50b553c6f41da2618`  
		Last Modified: Tue, 12 May 2026 21:51:02 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af04a060962ad8ba8aaff774f10ac52f50a7dc97d1c2cee30cc1a66dd703ad94`  
		Last Modified: Tue, 12 May 2026 21:51:02 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ecf2ba5dcd7f328fcb8ddf6d125bd450b96671af8b0e4a84093e86cc42ffc3`  
		Last Modified: Tue, 12 May 2026 21:51:02 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc40bb8557c99f05641d4156c9b1f9a7cf62176540549baa6494d10568be85fc`  
		Last Modified: Tue, 12 May 2026 21:51:00 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c19ce0bf028930c83b42da58d1fe799b93860c584de70d19239ccd1422b3e509`  
		Last Modified: Tue, 12 May 2026 21:51:00 GMT  
		Size: 71.1 KB (71057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24d5218d85e39dfffc40e97a0be7205d0608208b37d2fe4498687297b5c99ae`  
		Last Modified: Tue, 12 May 2026 21:51:00 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d85fe316b79a04de098e03878390e156dc053ed489aed205007e1af07f33f0a9`  
		Last Modified: Tue, 12 May 2026 21:51:09 GMT  
		Size: 101.9 MB (101915771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cc74ad0188113d1426f622a38ea52ed1bf5a9f2e4b5d7aa749155ad471487a`  
		Last Modified: Tue, 12 May 2026 21:51:00 GMT  
		Size: 119.5 KB (119511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-nanoserver` - windows version 10.0.20348.5020; amd64

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
