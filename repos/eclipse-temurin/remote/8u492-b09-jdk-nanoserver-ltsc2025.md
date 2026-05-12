## `eclipse-temurin:8u492-b09-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:1ee9cb1fcf3c4b4afb97e8a0c2203e11228067f01715860811ed91887aac0666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `eclipse-temurin:8u492-b09-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32690; amd64

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
