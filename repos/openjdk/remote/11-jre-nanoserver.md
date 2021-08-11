## `openjdk:11-jre-nanoserver`

```console
$ docker pull openjdk@sha256:84d336f625b90e825f44baede6700e0ea7500e3a8f3071b641325837ee71a995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `openjdk:11-jre-nanoserver` - windows version 10.0.17763.2114; amd64

```console
$ docker pull openjdk@sha256:35973646395fa7c399bbabffbeaec20e0f384e851d3a6732d8860e4264f49e0d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142390617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c9a516054088bfc5dcd3db629c7845030a887edea3eb94b442676f76c8dc4d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Aug 2021 19:15:20 GMT
RUN Apply image 1809-amd64
# Wed, 11 Aug 2021 17:30:38 GMT
SHELL [cmd /s /c]
# Wed, 11 Aug 2021 17:56:37 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 11 Aug 2021 17:56:40 GMT
USER ContainerAdministrator
# Wed, 11 Aug 2021 17:56:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 11 Aug 2021 17:56:57 GMT
USER ContainerUser
# Wed, 11 Aug 2021 17:56:59 GMT
ENV JAVA_VERSION=11.0.12
# Wed, 11 Aug 2021 18:01:53 GMT
COPY dir:cfe6877c6b81ca46843a524b803b574bd01e43f05b821b8b183eb47cd476c286 in C:\openjdk-11 
# Wed, 11 Aug 2021 18:02:11 GMT
RUN echo Verifying install ... 	&& echo   java --version && java --version 	&& echo Complete.
```

-	Layers:
	-	`sha256:bc8517709e9cfff223cb034ff5be8fcbfa5409de286cdac9ae1b8878ebea6b84`  
		Size: 102.7 MB (102741177 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ae0a5a946be2ad0e39a8260e454c0060a31a9f7e5be75d1f9038dc13730abc0a`  
		Last Modified: Wed, 11 Aug 2021 18:21:28 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d8f68938e271e20bb9893ef64646ec7a0b9907210902dda1d53a450c29869e`  
		Last Modified: Wed, 11 Aug 2021 18:34:23 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecadcc53422b0085a871d9071a90120063a791bbc3b5c562f3e911039ab16d5`  
		Last Modified: Wed, 11 Aug 2021 18:34:23 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672ba26a0a0a0db2c9bba8edaeefdea833fee6155f5ccec1bf897303badb1e4a`  
		Last Modified: Wed, 11 Aug 2021 18:34:22 GMT  
		Size: 68.1 KB (68095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd613157f094f5b53629b6b6f243a92fb89c05ea8ace58f17f670c24a039d408`  
		Last Modified: Wed, 11 Aug 2021 18:34:20 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddb7f875a979df89be8f26d9be268a10656e87790d813899974958c2f87eea0`  
		Last Modified: Wed, 11 Aug 2021 18:34:20 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf215643062905ed0c51174261b7bb62a67920a3125c3bf6d838e8307e1cdbc3`  
		Last Modified: Wed, 11 Aug 2021 18:39:34 GMT  
		Size: 39.5 MB (39494048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e732952b88a3e1d5ab240f558a480bec24dcfd7582c274fa5217e5700d21ddb`  
		Last Modified: Wed, 11 Aug 2021 18:39:26 GMT  
		Size: 81.5 KB (81467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
