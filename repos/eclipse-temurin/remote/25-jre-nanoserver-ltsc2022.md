## `eclipse-temurin:25-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:1d3858e88a3b9e7911380c615c32a3c9ce6d86c38c66e3b53d0c730c6b862655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `eclipse-temurin:25-jre-nanoserver-ltsc2022` - windows version 10.0.20348.4893; amd64

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
