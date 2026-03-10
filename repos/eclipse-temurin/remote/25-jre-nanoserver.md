## `eclipse-temurin:25-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:0ae9128f017addccc4e1963d9605b2eb42959836353c07c1a80a799b5881b7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `eclipse-temurin:25-jre-nanoserver` - windows version 10.0.26100.32522; amd64

```console
$ docker pull eclipse-temurin@sha256:9f6759bbc13fb69e2349af951df58c47ef55a5272a32c7bfde98415cc2c42a93
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.2 MB (258172792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b150985999457e62a58baacf32c60b6d4eaf1103c029e9a2d36c8726824d4c85`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Mar 2026 01:45:55 GMT
RUN Apply image 10.0.26100.32522
# Tue, 10 Mar 2026 22:44:00 GMT
SHELL [cmd /s /c]
# Tue, 10 Mar 2026 22:44:01 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 10 Mar 2026 22:44:02 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 10 Mar 2026 22:44:03 GMT
USER ContainerAdministrator
# Tue, 10 Mar 2026 22:44:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Mar 2026 22:44:10 GMT
USER ContainerUser
# Tue, 10 Mar 2026 22:44:26 GMT
COPY dir:15db28d5461f0a5f42074eb42e42a8535b9576d6847f4e637cb0dcfe9abfaabd in C:\openjdk-25 
# Tue, 10 Mar 2026 22:44:31 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:06fab7822816d5f43d6835d07ac8db280fdf81384187f36d8dc43bbb7064a76d`  
		Last Modified: Tue, 10 Mar 2026 20:41:46 GMT  
		Size: 199.4 MB (199409325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8d524efa077f1ddd71ee6061597c09a0ac277743cbbddc2d2bb18a3a907619`  
		Last Modified: Tue, 10 Mar 2026 22:44:36 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099d01224f903b1d1f217756189057a7523c13c7cb6433ca4bfc32020a1c434d`  
		Last Modified: Tue, 10 Mar 2026 22:44:36 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9d9c7fd214fedce1f0e28976e53856e8faf55eba748dcb716737f3a28fed41`  
		Last Modified: Tue, 10 Mar 2026 22:44:36 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fb769960465b84f3c4132852904bcd9f33a86c0e5e4930aae5fbebb5168f1a`  
		Last Modified: Tue, 10 Mar 2026 22:44:35 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc36a7b5a1eb211c13b1d493c05104caca92020708c121b8ed7f03680c593a12`  
		Last Modified: Tue, 10 Mar 2026 22:44:35 GMT  
		Size: 70.9 KB (70937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6814d993590f5539dcb03ac08ccc5000d8b1dc6c8c85392a98c218087cd3c25f`  
		Last Modified: Tue, 10 Mar 2026 22:44:35 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1d9c30ec5103ec45e6333db54effdc7be8fe23d3fddaacfc5da8fcb49b51ed`  
		Last Modified: Tue, 10 Mar 2026 22:44:43 GMT  
		Size: 58.6 MB (58583918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cd0a40d377669f1bce0fcf7293e448f43197b89d9e0ee89441569a704ef812`  
		Last Modified: Tue, 10 Mar 2026 22:44:35 GMT  
		Size: 103.2 KB (103236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:25-jre-nanoserver` - windows version 10.0.20348.4893; amd64

```console
$ docker pull eclipse-temurin@sha256:6d505569848ca215a2d6d664b6873ed936012aeadd529dc402791edf1b48dd5c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.4 MB (185422544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94a806d13863274ec11e12f7d7c7de77926c6e30caf78f8d4f3a677a5243a75`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 22:36:36 GMT
SHELL [cmd /s /c]
# Tue, 10 Mar 2026 22:37:33 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Tue, 10 Mar 2026 22:37:33 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 10 Mar 2026 22:37:34 GMT
USER ContainerAdministrator
# Tue, 10 Mar 2026 22:37:35 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Mar 2026 22:37:36 GMT
USER ContainerUser
# Tue, 10 Mar 2026 22:37:41 GMT
COPY dir:15db28d5461f0a5f42074eb42e42a8535b9576d6847f4e637cb0dcfe9abfaabd in C:\openjdk-25 
# Tue, 10 Mar 2026 22:37:44 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807d2824c917294d6edf619f31fd4bf4797460117c9bf4a2a6c56070bbad5671`  
		Last Modified: Tue, 10 Mar 2026 22:36:58 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b4748f25f6dedf228783035f205c871ce4de7dcb2f6a2a3ee28cfad4eda14f`  
		Last Modified: Tue, 10 Mar 2026 22:37:50 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76f47b1c8209f596d9c81e9e53f73eb70aab67b4da6f2c45144eaf71707fd79d`  
		Last Modified: Tue, 10 Mar 2026 22:37:50 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d2f38d5e5e53f11ca3f608a721d177001509af1224a5965fd3146c12e96078`  
		Last Modified: Tue, 10 Mar 2026 22:37:48 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4076b1f75252bd9ac63f717e8a7d138b87729a0660008c5ef0f5a864a44efb67`  
		Last Modified: Tue, 10 Mar 2026 22:37:48 GMT  
		Size: 76.9 KB (76941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007ef46be572acbbef8745e27ce71c89867125dc54876329e62011730be9c9d5`  
		Last Modified: Tue, 10 Mar 2026 22:37:48 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ad6276c776248d433fe6c5241c587e88dead944cee3a33105239558f861edb`  
		Last Modified: Tue, 10 Mar 2026 22:37:56 GMT  
		Size: 58.6 MB (58583037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:737f470051edba3777ffb71acefbaaf4ef6d893716c71a2e1d866aacc1468a3d`  
		Last Modified: Tue, 10 Mar 2026 22:37:48 GMT  
		Size: 106.8 KB (106760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
