## `eclipse-temurin:11-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:515b1840cf2228fd63356205714f9b79f4746346b95fe2733ec81fc40336099a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.825; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2022` - windows version 10.0.20348.825; amd64

```console
$ docker pull eclipse-temurin@sha256:0a9e11f1f86df01f530fee1f2986d18636404b70246d9d76bb5c37451ca449dd
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161117971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33018fca8ff4672a1c3affe9a08797f402936f76c767402d2183111461eac043`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Jul 2022 17:25:17 GMT
RUN Apply image 10.0.20348.825
# Wed, 13 Jul 2022 15:22:06 GMT
SHELL [cmd /s /c]
# Thu, 28 Jul 2022 16:37:40 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 28 Jul 2022 16:37:41 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 28 Jul 2022 16:37:42 GMT
USER ContainerAdministrator
# Thu, 28 Jul 2022 16:38:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 28 Jul 2022 16:38:03 GMT
USER ContainerUser
# Thu, 28 Jul 2022 16:39:00 GMT
COPY dir:ed8aecf12b2f8b5c8236f0bd623d348ed23ce1dd32f70bd039c8f6b01f0feff1 in C:\openjdk-11 
# Thu, 28 Jul 2022 16:39:16 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:3719b23d309b17276277110a008a58133c9fc92465d2519f2f32c9961c39887d`  
		Size: 118.0 MB (118046090 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:569505cbc9e1bcad1fbbdd7edca170e5a914864bcad2f53e1fc5d5816ecc8aa5`  
		Last Modified: Wed, 20 Jul 2022 12:54:13 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1252b05e04415b932e0493ebb1c1d9630862699553a73c59de593de5037f231b`  
		Last Modified: Thu, 28 Jul 2022 16:49:16 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685c91e252aaa6220a6877517bdf3c005bd968d17423f3048bde56276159d52a`  
		Last Modified: Thu, 28 Jul 2022 16:49:15 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db05847b29dbb1bab6b2c49599195bffe75394e90dd8b8adf44ff003e6853d5b`  
		Last Modified: Thu, 28 Jul 2022 16:49:15 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9ffb9642495dfdf16069f58704735111679b78d9810a36cd142d0b28cd02981`  
		Last Modified: Thu, 28 Jul 2022 16:49:13 GMT  
		Size: 84.6 KB (84552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8f95fa92d264d501d6e5872398e021530227e929f92756d32bab884109acf6`  
		Last Modified: Thu, 28 Jul 2022 16:49:13 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f5953bfada8c2cdae724547dd2c95462b3313513c1f166babbc7e45db2ce02`  
		Last Modified: Thu, 28 Jul 2022 16:49:54 GMT  
		Size: 42.9 MB (42919669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8494a3605798a7147ba13db9f1021fff3a16e13034db4fc42f45017f84d5ae48`  
		Last Modified: Thu, 28 Jul 2022 16:49:46 GMT  
		Size: 61.9 KB (61876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
