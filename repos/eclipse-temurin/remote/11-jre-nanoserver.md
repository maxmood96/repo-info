## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:c75a233494add924e7dd8eac32099816b80c0a2fe9fb67e6c7ce50ebec43e3eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.230; amd64
	-	windows version 10.0.17763.2183; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.230; amd64

```console
$ docker pull eclipse-temurin@sha256:70ddb40c70cc6d162fbab3652b0733b1e3bcd3eef914ed90c812c7699954ded0
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159727868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf992bda4f787ddaf6f587687e204585efcd1bc7b0b29fab97a0cbaf8ddb7ac6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Sep 2021 06:44:45 GMT
RUN Apply image ltsc2022-amd64
# Tue, 05 Oct 2021 22:17:48 GMT
SHELL [cmd /s /c]
# Tue, 05 Oct 2021 22:19:26 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Tue, 05 Oct 2021 22:19:26 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 05 Oct 2021 22:19:27 GMT
USER ContainerAdministrator
# Tue, 05 Oct 2021 22:19:38 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 05 Oct 2021 22:19:39 GMT
USER ContainerUser
# Tue, 05 Oct 2021 22:20:33 GMT
COPY dir:37196d51db7ddeb5d9f84ac7a3abd0b4eaec3c6dcffe01db917f682d6ae15f0d in C:\openjdk-11 
# Tue, 05 Oct 2021 22:20:48 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:521b4ff1716af921a5cfbf2119d97dc479e9b1eb487d17d0f576ff856ab68e61`  
		Size: 116.9 MB (116897071 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:51c1c5356f69c33525116c868524e16b83d783420a64f7a7793348f61595daf2`  
		Last Modified: Tue, 05 Oct 2021 22:35:06 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edc7e29224497ed401b82fe374a10fe05e262938b81b05709c74a2e6a4237b1`  
		Last Modified: Tue, 05 Oct 2021 22:36:21 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcf684521bfd09befb28a1dbcc18422bd669beabf509264924a58b5d5a3d1cd`  
		Last Modified: Tue, 05 Oct 2021 22:36:20 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac9350ab58ddb34982b28e2446baa230228ea607e3556af4654940aec80b078`  
		Last Modified: Tue, 05 Oct 2021 22:36:20 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0eda7d53bfc7370384240fa06e543b8521cab7fb215c2e0673cce351b771c61`  
		Last Modified: Tue, 05 Oct 2021 22:36:18 GMT  
		Size: 76.2 KB (76161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4b23e44de226665a527d6ab39cb77d7b1697184128c3dff16d38477e5e1128`  
		Last Modified: Tue, 05 Oct 2021 22:36:18 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360b75fc6299c926a99cd8652b59247f87f638ae2b667556a5f3b2ac077dd846`  
		Last Modified: Tue, 05 Oct 2021 22:36:57 GMT  
		Size: 42.7 MB (42687557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4d78161b93f4be122a2abdda93f9bb31c395af82eab77ff4e091f8993a9b90`  
		Last Modified: Tue, 05 Oct 2021 22:36:50 GMT  
		Size: 61.4 KB (61357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.17763.2183; amd64

```console
$ docker pull eclipse-temurin@sha256:fc82379fe3a3382b330b2d5c1d21457332b2ece03a616a5800ddb49627ef4ab1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145516740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5234568421f98af929abe24bb58eb1214b61cd5f1c74740dad5f3b1c81c7a06b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Sep 2021 03:45:12 GMT
RUN Apply image 1809-amd64
# Wed, 15 Sep 2021 00:38:23 GMT
SHELL [cmd /s /c]
# Wed, 15 Sep 2021 16:30:46 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Wed, 15 Sep 2021 16:30:46 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 15 Sep 2021 16:30:47 GMT
USER ContainerAdministrator
# Wed, 15 Sep 2021 16:30:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Sep 2021 16:30:55 GMT
USER ContainerUser
# Thu, 16 Sep 2021 19:21:54 GMT
COPY dir:37196d51db7ddeb5d9f84ac7a3abd0b4eaec3c6dcffe01db917f682d6ae15f0d in C:\openjdk-11 
# Thu, 16 Sep 2021 19:22:08 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:3585a81ca503e6c63dce938a5606f4171d7461e51000a92054b3f5692786d6c9`  
		Size: 102.7 MB (102703785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:807d06303c39b2317729754a4c7ad6501e59c16ee464f8f671f9947774f62f72`  
		Last Modified: Wed, 15 Sep 2021 01:10:56 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f0b46abc08dd348231f30302591eb106f2509c46e439c7735e18ffc04a3745`  
		Last Modified: Wed, 15 Sep 2021 16:51:52 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e03a155046076cc9ecbc1c5926012b18963df9b9df8ba86ff3ae4fb54efbbf6`  
		Last Modified: Wed, 15 Sep 2021 16:51:52 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fdd1cbc2a15e3bb42a7a8c1a542472bcbd16a3c372e40cf219996050315fa3`  
		Last Modified: Wed, 15 Sep 2021 16:51:52 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9056cfe69fb43064c5f5849e7f4328d6cffb416bfa2fdfc39b124fcf2f4cdce0`  
		Last Modified: Wed, 15 Sep 2021 16:51:50 GMT  
		Size: 72.3 KB (72298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0a8abfaee4320d08e0142a1a43aa4330b43ed44f42af47dde036d39183459e`  
		Last Modified: Wed, 15 Sep 2021 16:51:49 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00c270c8e55cb2f330129ec575c15c28347bad20bbd03bf222ee9b358df7eb7`  
		Last Modified: Thu, 16 Sep 2021 19:26:36 GMT  
		Size: 42.7 MB (42686554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23931c2a7aca273b201b83b8274a5217135323ff97aadae7dba4e6aa59f57413`  
		Last Modified: Thu, 16 Sep 2021 19:25:51 GMT  
		Size: 48.4 KB (48366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
