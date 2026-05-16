## `eclipse-temurin:26-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:7e411565671062be7f73aeaa1cd4bf005059f27268eb4c5fdac5c86e19d01d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `eclipse-temurin:26-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull eclipse-temurin@sha256:49a9fc84fac6bd8a416c19d4fd7482914c7dfc2b31bb7697e78c56799daa30e7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.2 MB (260153481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e754e32e07a99dc580382c93bccfb9b98227dda61c9bbf58a3df47b65519fa44`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 May 2026 09:46:02 GMT
RUN Apply image 10.0.26100.32860
# Fri, 15 May 2026 21:40:58 GMT
SHELL [cmd /s /c]
# Fri, 15 May 2026 21:40:59 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Fri, 15 May 2026 21:41:00 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 15 May 2026 21:41:00 GMT
USER ContainerAdministrator
# Fri, 15 May 2026 21:41:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 15 May 2026 21:41:13 GMT
USER ContainerUser
# Fri, 15 May 2026 21:41:43 GMT
COPY dir:1edec5af9445e163af5cd51feafb262ed7498368c1981b477e0c90d82a11e11a in C:\openjdk-26 
# Fri, 15 May 2026 21:41:50 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:34ab6476d71f2d23d05a00ac439000ba4c19d17e5c66f15efbe329ed79bba2bf`  
		Last Modified: Tue, 12 May 2026 22:29:47 GMT  
		Size: 199.7 MB (199739001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2dce0688119cf1207d8fcd841a74caaa718dcbe368ffc9ffb384f6f11023719`  
		Last Modified: Fri, 15 May 2026 21:41:56 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74786d9fc84c53cc7a7dc07dedd8bcab72ea59c6c46bf3661b6589bdd774052`  
		Last Modified: Fri, 15 May 2026 21:41:56 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0329e454b9ca6f26dba647be08071de921c87efbf344349bbf174dfef0dbc76d`  
		Last Modified: Fri, 15 May 2026 21:41:55 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e216579bb4a78a511a2726801db4491d8033b3a6cb5787f4e8c4e1be37fda0dc`  
		Last Modified: Fri, 15 May 2026 21:41:54 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4170a1a4bc5aa99a931437ba840aee375d48fe3a24800591f2aed459ecfa02d6`  
		Last Modified: Fri, 15 May 2026 21:41:54 GMT  
		Size: 70.9 KB (70868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e62da3f1dc1bad8dfa738a2acb4e41fa68286e39bfa7164d5e0afd4ad2b8a982`  
		Last Modified: Fri, 15 May 2026 21:41:54 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3fc86fd1b12a162a3341c40e01d670412ac5f90ac68a7c68f54e71c2d49faa`  
		Last Modified: Fri, 15 May 2026 21:42:03 GMT  
		Size: 60.2 MB (60225778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a4b42b81b0601ec8673567316c5cd1842793c2c9403ed145da503dc2e460a0`  
		Last Modified: Fri, 15 May 2026 21:41:54 GMT  
		Size: 112.6 KB (112593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
