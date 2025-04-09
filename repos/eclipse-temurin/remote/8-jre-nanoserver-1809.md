## `eclipse-temurin:8-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:8fe0b800ba303a9fa96980f4defb96e2f6d4a5f383350058f2057d5f17524716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:8-jre-nanoserver-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull eclipse-temurin@sha256:531030d58a11f6d6f2b316e1d96cd8fed8e94afc32952486f27a2e264a942544
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147650264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581c56bd093cdc6ad4c3a05dd669728585a728d4202f593497a2227e64ab98c5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Wed, 12 Mar 2025 19:14:04 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:14:05 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 12 Mar 2025 19:14:06 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 12 Mar 2025 19:14:06 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:14:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:14:09 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:14:12 GMT
COPY dir:5687adced9ba5f2555526fe07fa3e848c7771941703db13fa4b29a0f81d58070 in C:\openjdk-8 
# Wed, 12 Mar 2025 19:14:15 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9948c6d4a8081bafb3e44259f9e3fce5ef86e361a0955afcfdfa0b7cdd6ccc`  
		Last Modified: Wed, 12 Mar 2025 19:14:21 GMT  
		Size: 1.1 KB (1113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baab9c6eb823887093207600e822b957d420615820f710822064d689464857ad`  
		Last Modified: Wed, 12 Mar 2025 19:14:21 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e89d9dc06cb725e9e0b07869ed1b5c7d68fdfdbd04b7fe446b6214193c7c303`  
		Last Modified: Wed, 12 Mar 2025 19:14:21 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b4ae3decb161cf6ebd1c8316c43d9da1da905b300c3bf224c52ebbed32995e`  
		Last Modified: Wed, 12 Mar 2025 19:14:19 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32bbaea4c6bfc079dd808efa140d8a0dceb309967016eeffd5135a12d5896272`  
		Last Modified: Wed, 12 Mar 2025 19:14:19 GMT  
		Size: 73.2 KB (73150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a009101e50ff6bfa5540b557b72aa4b9f7b8240ba6f324b337152f08e9a4af`  
		Last Modified: Wed, 12 Mar 2025 19:14:19 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3579eb782a10a212f5dd9f4a1baebf49fab2df96eabae9eb2345fec92763fb6`  
		Last Modified: Wed, 12 Mar 2025 19:14:23 GMT  
		Size: 40.6 MB (40552702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22a27a4d65fc81d85d9efdc6fffcd1681c51fa922c690f22b09c6c4aceeb401`  
		Last Modified: Wed, 12 Mar 2025 19:14:19 GMT  
		Size: 111.2 KB (111181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
