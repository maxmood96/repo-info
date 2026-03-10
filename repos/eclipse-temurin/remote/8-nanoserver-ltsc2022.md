## `eclipse-temurin:8-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:e5113caa1ff752587882a63d1f74b6abc365d4d54006af99bcf4781adc476a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `eclipse-temurin:8-nanoserver-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull eclipse-temurin@sha256:af19342c1d6b2bcd8069479e3e313bb920fae926dc823c48e469a50c677012e9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228769493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e49435326c2f7d70015630b4acdc6411871ef23d97ec7336f5545da4676e18e5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 22:36:18 GMT
SHELL [cmd /s /c]
# Tue, 10 Mar 2026 22:36:19 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 10 Mar 2026 22:36:19 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 10 Mar 2026 22:36:19 GMT
USER ContainerAdministrator
# Tue, 10 Mar 2026 22:36:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Mar 2026 22:36:22 GMT
USER ContainerUser
# Tue, 10 Mar 2026 22:36:28 GMT
COPY dir:076949d8a0679d24528f11c4150b1ea7a552717f0bf1fb11a9fa610f7e5e2ea0 in C:\openjdk-8 
# Tue, 10 Mar 2026 22:36:31 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba2425154dbe4f9c92a7daa50ee78f1d65a2f56409da6f247f3870c5a1f698a`  
		Last Modified: Tue, 10 Mar 2026 22:36:37 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3214c439796ba09db71fefc8d898d91c4eef64e873539261683b4945c47ce635`  
		Last Modified: Tue, 10 Mar 2026 22:36:37 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf30ee737e1f79c802d876af8e5fdebeb629dbfbaa3ee6644eab6b6327a938e`  
		Last Modified: Tue, 10 Mar 2026 22:36:36 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e8fcad1a6aa17ca0a004bc244cbeaf4497de91de7bdb421164ae04501170ea`  
		Last Modified: Tue, 10 Mar 2026 22:36:35 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d050d977f214389297a4d15cf16b47c5a679c95b4573c56b4b1274ddc753666c`  
		Last Modified: Tue, 10 Mar 2026 22:36:35 GMT  
		Size: 80.9 KB (80877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd4e2b0537cfefa422f04c252cadeb2c34e5d4d371800b8ebc4484887d80155`  
		Last Modified: Tue, 10 Mar 2026 22:36:35 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656f9e347817d293e02b5b805008f118a883ffeeefe0490f8e314ef15c65faee`  
		Last Modified: Tue, 10 Mar 2026 22:36:43 GMT  
		Size: 101.9 MB (101908665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be41809abd33fc97be0cfed5e98c7be3c3aed9f45cae573545903bbae5b584e`  
		Last Modified: Tue, 10 Mar 2026 22:36:35 GMT  
		Size: 124.1 KB (124073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
