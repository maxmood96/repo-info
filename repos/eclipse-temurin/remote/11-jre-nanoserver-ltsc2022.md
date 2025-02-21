## `eclipse-temurin:11-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:81ad6d1950e0998eff6ae07d0586f0255f50c1bb4820343ed34547af9dd39024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull eclipse-temurin@sha256:b6a59ba7f660f503e3343ccd0ad0804529cdf26d8654a8e00e021dfb9941631f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 MB (164504583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2085b5ed99e6d5b8bffd378311981d871c7bfd296353d22700c62d6533c8b11`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Thu, 13 Feb 2025 01:16:29 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:16:29 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 13 Feb 2025 01:16:30 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 13 Feb 2025 01:16:30 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:16:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:16:33 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:16:36 GMT
COPY dir:e7319a06d2b9171c954fc18de0614fa7d0eb408950b795be61492806db04a6ea in C:\openjdk-11 
# Thu, 13 Feb 2025 01:16:39 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:43:09 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84b9361672150f6122c04cf4fff6343213f665f38eda134a99af68c22b17926`  
		Last Modified: Thu, 13 Feb 2025 01:16:45 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fcdb7bf09d85ff6e864d840657d33158d189bb2af76374e2d0ec152e015a75d`  
		Last Modified: Thu, 13 Feb 2025 01:16:45 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8bee2434bc2eb9a7f63ad386fb11a140096c1591d1b73d6e1203a8bbeff054`  
		Last Modified: Thu, 13 Feb 2025 01:16:45 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf4264f641802aa08bcc626cc8ea055a10bac5d1e422c4f12de629719aa2b20`  
		Last Modified: Thu, 13 Feb 2025 01:16:43 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4163a1a3ebde03da75961cda9490f17acb20966630645765aed774799d85a10`  
		Last Modified: Thu, 13 Feb 2025 01:16:43 GMT  
		Size: 76.8 KB (76777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d46a99f0f09d0527640040aea0e6b380fdd5541605a556dce7a3c8ca28d4d5`  
		Last Modified: Thu, 13 Feb 2025 01:16:43 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbcce110fc393fa71dd45591b3e1869697276f26d43dd8fa17c5df1650b03f4d`  
		Last Modified: Thu, 13 Feb 2025 01:16:47 GMT  
		Size: 43.7 MB (43656316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd973ce35b75d796cfb04ab75e9b69e505b50ee80c4355f95718551bf318c8d4`  
		Last Modified: Thu, 13 Feb 2025 01:16:43 GMT  
		Size: 99.5 KB (99484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
