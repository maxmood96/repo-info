## `eclipse-temurin:26-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:b399cf8b819a78379cb8214da186809441100ec0f2df83ff4d5c3dd5c85f25a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `eclipse-temurin:26-jre-nanoserver` - windows version 10.0.26100.32860; amd64

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

### `eclipse-temurin:26-jre-nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull eclipse-temurin@sha256:7a0478187edc86fe4a75f47b0edeb36c6588ed74f97a29f6c53d60c8b51fa573
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.5 MB (187452572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7a4d7741936ac072f4ca2c04b0d3f55fe0ee39f56a89c94a45e0e1df45e0f9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Fri, 15 May 2026 21:25:56 GMT
SHELL [cmd /s /c]
# Fri, 15 May 2026 21:25:59 GMT
ENV JAVA_VERSION=jdk-26.0.1+8
# Fri, 15 May 2026 21:25:59 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 15 May 2026 21:26:00 GMT
USER ContainerAdministrator
# Fri, 15 May 2026 21:26:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 15 May 2026 21:26:18 GMT
USER ContainerUser
# Fri, 15 May 2026 21:28:17 GMT
COPY dir:1edec5af9445e163af5cd51feafb262ed7498368c1981b477e0c90d82a11e11a in C:\openjdk-26 
# Fri, 15 May 2026 21:28:20 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb8e31ecd6facd70d76050945945bacc13c73575e37bcfbdacaa45ee57464c7`  
		Last Modified: Fri, 15 May 2026 21:27:14 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829dc88c2fb8d4e0d01dc63423d0af4225fb189b2ba60044705806b26e7aefc8`  
		Last Modified: Fri, 15 May 2026 21:27:14 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a52b5332ded073489aa2b022ddc2cf5e2625a9a12477d8b2646547c036e75e`  
		Last Modified: Fri, 15 May 2026 21:27:14 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d757993bdb31e2d63ea20d1ab1b3f100c7f15e21b4470c98818111bff54726df`  
		Last Modified: Fri, 15 May 2026 21:27:14 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da892f725214a39549711267bc98d2d13bcf12204e888de04749a0ff4e545af`  
		Last Modified: Fri, 15 May 2026 21:27:13 GMT  
		Size: 72.4 KB (72400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8510a82094720d352b84ddcb6bc6dd120fb8043d760b63802a7923c700350c7b`  
		Last Modified: Fri, 15 May 2026 21:27:12 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7135616df98d2175bcc2e55a678b6ddbb87c4eab7d49e25fc06bed3c720cfad8`  
		Last Modified: Fri, 15 May 2026 21:28:33 GMT  
		Size: 60.2 MB (60225598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b4f14e4f379dda3d636d83f8e988f5693f884fd7610be12ec2d3c9119b28aea`  
		Last Modified: Fri, 15 May 2026 21:28:25 GMT  
		Size: 110.4 KB (110448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
