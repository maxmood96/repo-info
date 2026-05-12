## `eclipse-temurin:8-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:55a9e64f31c7dd441042eaa4e538d05f8a99360f1ac839df861cb3d152601eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull eclipse-temurin@sha256:ee03e3e3464b9640cd1f2dbb1f4cb4ceeb63c2220f4f99e7a9396952bb19af33
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239894264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29fa84aeca56dc135fb8eddbc679f1d382358bd90b90f12c4b566db3584c081c`
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
# Tue, 12 May 2026 22:09:32 GMT
COPY dir:deea9cd49fa78c2b910137007aed467626dd46389507789da1635093de3df40f in C:\openjdk-8 
# Tue, 12 May 2026 22:09:38 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:4359797bb0ab1b038af3cce8bc971f9d839d457bf432d1a1ca19685463d119a3`  
		Last Modified: Tue, 12 May 2026 22:09:47 GMT  
		Size: 40.0 MB (39988188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cd4064b97be57d18076bac90d8a19cbed07e8c615a08a06c12860aa39276b3`  
		Last Modified: Tue, 12 May 2026 22:09:42 GMT  
		Size: 112.6 KB (112604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
