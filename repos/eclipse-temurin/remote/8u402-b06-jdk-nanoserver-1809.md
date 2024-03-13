## `eclipse-temurin:8u402-b06-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:859003079a7293de300096f6251a1fa7f095c4cf886fc151ea198ced5cef16ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `eclipse-temurin:8u402-b06-jdk-nanoserver-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull eclipse-temurin@sha256:2471445e1a4933dec5ea8cbd9b1e49647c11f00a6bd2fedcc0194e6d50394d76
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.5 MB (206477877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f301120d567b411f405383ea37894c1368bc7d64dd5a698e5049bc35a1d333ad`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 00:41:38 GMT
SHELL [cmd /s /c]
# Wed, 13 Mar 2024 00:41:38 GMT
ENV JAVA_VERSION=jdk8u402-b06
# Wed, 13 Mar 2024 00:41:39 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 13 Mar 2024 00:41:40 GMT
USER ContainerAdministrator
# Wed, 13 Mar 2024 00:41:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Mar 2024 00:41:51 GMT
USER ContainerUser
# Wed, 13 Mar 2024 00:42:02 GMT
COPY dir:9ab35a15e19e8247451d444f7de2a75fe407ec1749c1b49082dcaaef6c80dafd in C:\openjdk-8 
# Wed, 13 Mar 2024 00:42:14 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9569a24b1d9b596a48436098ac5fe49c52e3153cd3bd147e365a80a4059570fd`  
		Last Modified: Wed, 13 Mar 2024 01:31:07 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ac6979d3018020e5d56f24192e72d677112ce70959b875a73d0ceb74f7ab4a`  
		Last Modified: Wed, 13 Mar 2024 01:31:07 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a09b00f17d16e8707c45a7f82c7b23111fc4386bb12c142f745c8f3d75630a0`  
		Last Modified: Wed, 13 Mar 2024 01:31:07 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d598c02e10beef0b23187e3090a387054f0aaba86c9b427e0e59a2b6cf0375cf`  
		Last Modified: Wed, 13 Mar 2024 01:31:05 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df21f9058d8a1bfd11006bb0255f88c7865c2c34851a191447c198e670ea384b`  
		Last Modified: Wed, 13 Mar 2024 01:31:05 GMT  
		Size: 68.9 KB (68906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c8255b1c5b4f751fb254a0543c26a87c06339f37b1f99fb38054529a1941b9`  
		Last Modified: Wed, 13 Mar 2024 01:31:05 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7179b12259b55aee7730300ceac3742f580f42d965894cdd49824bdc24c04001`  
		Last Modified: Wed, 13 Mar 2024 01:31:18 GMT  
		Size: 101.7 MB (101701462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a16ce7549abd7d18c55d766699875c4b83a0423280084fda7ac8ffa7d7e14a6`  
		Last Modified: Wed, 13 Mar 2024 01:31:05 GMT  
		Size: 81.6 KB (81606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
