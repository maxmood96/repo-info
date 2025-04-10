## `openjdk:25-ea-17-nanoserver-1809`

```console
$ docker pull openjdk@sha256:43ab87293b097f5108c72d52bca458d7f029344364fa8ea377ca763efc39309a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `openjdk:25-ea-17-nanoserver-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull openjdk@sha256:cce01d878c73a00fca956d4c2a97b05afd270a6fc53df5bf5f9245dacc808102
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.4 MB (319392725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c2857267892b5c6688ec3ec02f9c6c82920a8e43fcc6504f75e34220930e82`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Apr 2025 01:31:28 GMT
RUN Apply image 10.0.17763.7136
# Wed, 09 Apr 2025 01:51:57 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:51:59 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 09 Apr 2025 01:52:00 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:52:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 09 Apr 2025 01:52:03 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:52:04 GMT
ENV JAVA_VERSION=25-ea+17
# Wed, 09 Apr 2025 01:52:11 GMT
COPY dir:31d4a08dd20e935927d81b33c56eb56ceaeead96529382a0c30c5f89fc836ee7 in C:\openjdk-25 
# Wed, 09 Apr 2025 01:52:17 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 09 Apr 2025 01:52:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a06e0965a0fa3715e629889bd9332aa22aadd75654cac5c9818b67c0264b3ee1`  
		Last Modified: Tue, 08 Apr 2025 20:16:02 GMT  
		Size: 106.9 MB (106922524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4649969ca3c3e4d5c4d5f747d5316968fe11da1ae6e14575ae9501414afbf22b`  
		Last Modified: Wed, 09 Apr 2025 01:52:22 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4485974b5b247c933daca6ab33b247bea2559120a3552aa087b50551530966ee`  
		Last Modified: Wed, 09 Apr 2025 01:52:21 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647044e2eae66526b8155aa7f20f679defd3402136e35b26622eb1c5de599cf7`  
		Last Modified: Wed, 09 Apr 2025 01:52:21 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdaf719fddf02a35729887893db2f262beaf98132c47aa904019b7501a2fdf9c`  
		Last Modified: Wed, 09 Apr 2025 01:52:21 GMT  
		Size: 71.0 KB (71012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777eb8ead373566fa5357484afde0be6159c11a0ad28c2076047f42f25a0c2a1`  
		Last Modified: Wed, 09 Apr 2025 01:52:20 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b014ade311506118e15e73c000215111edba25b160ed36f25996747a11f354`  
		Last Modified: Wed, 09 Apr 2025 01:52:20 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096b83ba0821b16afb90c992699094441a915fb169f2ae928ffae7b1142bb60a`  
		Last Modified: Wed, 09 Apr 2025 01:52:33 GMT  
		Size: 208.0 MB (207953398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eef4450d61dd5494a853948cad0a75cd7b53c2c7936a3ed8cad70e1a388516a`  
		Last Modified: Wed, 09 Apr 2025 01:52:21 GMT  
		Size: 4.4 MB (4439566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fcfe9e1afc3a49edeaee35f97f3227d4ae28c96a7e2b676e8fee482b636e136`  
		Last Modified: Wed, 09 Apr 2025 01:52:20 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
