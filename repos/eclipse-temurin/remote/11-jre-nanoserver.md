## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:4bcc46558dfb224efa1a533ffa83543f3f8827917d0a65f61cf5c5f99cc992f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.825; amd64
	-	windows version 10.0.17763.3165; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.825; amd64

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

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.17763.3165; amd64

```console
$ docker pull eclipse-temurin@sha256:8cc90be39ff4324972d202751c2b8b8f25ac98f8d9095ba5d74f551dccd7853f
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146217316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea369cc1e0c86f7621432aba653e757bf46564375d8ec05ca41f553ab916a94`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 06 Jul 2022 22:15:10 GMT
RUN Apply image 10.0.17763.3165
# Wed, 13 Jul 2022 14:50:41 GMT
SHELL [cmd /s /c]
# Thu, 28 Jul 2022 16:21:12 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Thu, 28 Jul 2022 16:21:13 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 28 Jul 2022 16:21:14 GMT
USER ContainerAdministrator
# Thu, 28 Jul 2022 16:21:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 28 Jul 2022 16:21:30 GMT
USER ContainerUser
# Thu, 28 Jul 2022 16:26:07 GMT
COPY dir:ed8aecf12b2f8b5c8236f0bd623d348ed23ce1dd32f70bd039c8f6b01f0feff1 in C:\openjdk-11 
# Thu, 28 Jul 2022 16:26:24 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:5d24e1a2f5c566b0afb1e46fc24e5cec821c8ebf44220276a95a2b91f44a2f2a`  
		Size: 103.2 MB (103155009 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3b09c07c6aeead64423fdefc240fe2e1b6330c96732fd2705113030da84416be`  
		Last Modified: Mon, 18 Jul 2022 21:22:33 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea12bb691aaa5d39e320d6c853d1f72c4f8a5cf6ea617ae2993a322713c92bcc`  
		Last Modified: Thu, 28 Jul 2022 16:44:40 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb07b488c8049fc65ecfb4ece07bd17ca87edc4bc3a924090d12c38a915a89c`  
		Last Modified: Thu, 28 Jul 2022 16:44:40 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4af14d5e4431703d40fe5c49f8ddd4cf832f851de381cfc75cd5e101f9d07f0`  
		Last Modified: Thu, 28 Jul 2022 16:44:40 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c60b48cbcf85422570b793d7032b6f380d04f09aea72ecaf4b378309ccff98e`  
		Last Modified: Thu, 28 Jul 2022 16:44:38 GMT  
		Size: 70.6 KB (70584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e6b078b4a6303e9ef5314be0c4dac84047bc0b7226e9591025e14f1e56777b`  
		Last Modified: Thu, 28 Jul 2022 16:44:37 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a879c55abbe0d2cfc91ae828d066ef79330e16a8cdc39f93e80e6a2c3aaa85dc`  
		Last Modified: Thu, 28 Jul 2022 16:46:00 GMT  
		Size: 42.9 MB (42903944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491befbfe82e5198b77d222be6f4fd51b0e730cb40c7d4773a46f3854f55a5d6`  
		Last Modified: Thu, 28 Jul 2022 16:45:51 GMT  
		Size: 82.0 KB (82009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
