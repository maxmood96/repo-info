## `eclipse-temurin:8-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:ced517e2853287303210d4372a78b4aab78f75889e5e1841e55e504faa7744bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.26100.32690; amd64

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

### `eclipse-temurin:8-jre-nanoserver` - windows version 10.0.20348.5020; amd64

```console
$ docker pull eclipse-temurin@sha256:548fdf994cc1a7d09afc9ad99e7afd86d581058122aa77b03a9aa2ebe9b7bbb8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.1 MB (167103526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:465e994c2d7f365930a998a237eda47e57fb7e13aa03f1f3011623941b63f20a`
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
# Tue, 12 May 2026 22:10:39 GMT
COPY dir:deea9cd49fa78c2b910137007aed467626dd46389507789da1635093de3df40f in C:\openjdk-8 
# Tue, 12 May 2026 22:10:42 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:983a59f5db5315cf38392e7d93afe085eb90d74abfc5761ef635f64ecb9e4aab`  
		Last Modified: Tue, 12 May 2026 22:10:50 GMT  
		Size: 40.0 MB (39988120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac31f573e96e2b23f994b6d63eba7212d3b498a7d04d60b8a413e8d92f8978e`  
		Last Modified: Tue, 12 May 2026 22:10:46 GMT  
		Size: 83.6 KB (83627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
