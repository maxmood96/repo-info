## `eclipse-temurin:20-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:c2c0050e27bc871d33e34ea73295b5fb49a329e523c89ec00b5f6c1fab7e28c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1850; amd64

### `eclipse-temurin:20-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1850; amd64

```console
$ docker pull eclipse-temurin@sha256:b4969014da76e13178610c5ce990b232ccdcfedc230489b5542a9c05b4717887
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (165968498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c827997f4a00304e5ff65857f76baaada8cbd8b91bfc19509ddd91c8c68b03dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jul 2023 21:00:40 GMT
RUN Apply image 10.0.20348.1850
# Thu, 13 Jul 2023 22:10:51 GMT
SHELL [cmd /s /c]
# Thu, 13 Jul 2023 22:14:47 GMT
ENV JAVA_VERSION=jdk-20.0.1+9
# Thu, 13 Jul 2023 22:14:48 GMT
ENV JAVA_HOME=C:\openjdk-20
# Thu, 13 Jul 2023 22:14:49 GMT
USER ContainerAdministrator
# Thu, 13 Jul 2023 22:14:58 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Jul 2023 22:14:59 GMT
USER ContainerUser
# Thu, 13 Jul 2023 22:15:47 GMT
COPY dir:db4e97c4fd2cfe51abaeb1dfe2097f2044faeb2be3c3c04299b9c20e07c77033 in C:\openjdk-20 
# Thu, 13 Jul 2023 22:15:59 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:cc0a26bd90fcc4d863317c36d7ffec77a0a82a905697204d4dcbc76ec13b3920`  
		Last Modified: Tue, 11 Jul 2023 20:10:45 GMT  
		Size: 120.1 MB (120056465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb11750b624a775aa3c21a13406dfc54458855b8684e21efba5bbb9b27ee0b12`  
		Last Modified: Thu, 13 Jul 2023 22:28:35 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94bb0d0af753bf3fddc242471d62baa7d6b5bf9406352f90954681f021e614a`  
		Last Modified: Thu, 13 Jul 2023 22:30:53 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a594dc68da02e168f45e7595f8362f0ed780c40efc668ce6fd506ed4562ab55`  
		Last Modified: Thu, 13 Jul 2023 22:30:53 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e929e087fdcae2fed2b893cd030871bd95008fe41ac19b832facb0809fa8a`  
		Last Modified: Thu, 13 Jul 2023 22:30:53 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e876294035e02c2a9afcb9ff43cdcf09839ccd787032e5b50c097803c6806a`  
		Last Modified: Thu, 13 Jul 2023 22:30:51 GMT  
		Size: 80.3 KB (80254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3800e7a140cdf6e9dd3e205c30a36aa7c9fa85870a2889a49adc351ce6ba212c`  
		Last Modified: Thu, 13 Jul 2023 22:30:51 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5bf542fd4afd811a6cb743a2d562c33201dc411c37f0b1b62a88d5fbf9b09cb`  
		Last Modified: Thu, 13 Jul 2023 22:31:31 GMT  
		Size: 45.8 MB (45765391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf4ad7c1d21f1dac99276307ab599f318ebc8734ab7765992e665a841a49853`  
		Last Modified: Thu, 13 Jul 2023 22:31:22 GMT  
		Size: 61.0 KB (60974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
