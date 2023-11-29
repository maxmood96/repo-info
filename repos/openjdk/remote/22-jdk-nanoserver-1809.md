## `openjdk:22-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:fde3119aefd026d6e5f7c3aa504b5862a5712589bc67a8eb70b4f5b0e399d62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `openjdk:22-jdk-nanoserver-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull openjdk@sha256:4d1ae23a9bfb4cd48d26551215ea8930e7276776fdd17408070fb24c6413b90d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307361821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:465792f124219daa1f657522fac0826db2df4bf9cb2ae951ca29aadd6c52c6cf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Nov 2023 17:21:05 GMT
RUN Apply image 10.0.17763.5122
# Thu, 16 Nov 2023 01:41:12 GMT
SHELL [cmd /s /c]
# Thu, 16 Nov 2023 05:24:44 GMT
ENV JAVA_HOME=C:\openjdk-22
# Thu, 16 Nov 2023 05:24:45 GMT
USER ContainerAdministrator
# Thu, 16 Nov 2023 05:24:55 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 16 Nov 2023 05:24:56 GMT
USER ContainerUser
# Wed, 29 Nov 2023 02:15:11 GMT
ENV JAVA_VERSION=22-ea+25
# Wed, 29 Nov 2023 02:15:26 GMT
COPY dir:20ce11e128488de5873ada484935d15380979339c2efe0e6a32887b0ca6c51a9 in C:\openjdk-22 
# Wed, 29 Nov 2023 02:15:40 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 29 Nov 2023 02:15:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:24e10ec0ecb89022cf68752b9f9196dcf2f423f9589b14401693fb2a1b3de37f`  
		Last Modified: Tue, 14 Nov 2023 22:06:25 GMT  
		Size: 104.5 MB (104497517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e5c133738aab79d4c21c47e77cb838e2d00166f5e3e2632177622f67488259`  
		Last Modified: Thu, 16 Nov 2023 02:28:08 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d4362f257916ef69830b46ba8a0aacd5f6e2d4673fbd0dd7e4aac8cf3a6fb4`  
		Last Modified: Thu, 16 Nov 2023 05:27:30 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbc097ffc72e1215bdcee71d660b96a870a6af75ff16317f8a06d1555574aaa`  
		Last Modified: Thu, 16 Nov 2023 05:27:30 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765165baea11820cc78dbfb0922d099fef71e3cab0a77276be9bf3096bc3d841`  
		Last Modified: Thu, 16 Nov 2023 05:27:30 GMT  
		Size: 73.6 KB (73582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279359aca9bd1c2c8d38ba732e66b1a8948268dbc2347c4add167c46cc62574c`  
		Last Modified: Thu, 16 Nov 2023 05:27:28 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ca27e3eafbc905444f8a4a81a7b8e2dbb5f919d856dbf4ad6d489fcb0e1a82`  
		Last Modified: Wed, 29 Nov 2023 02:17:58 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b76d6b6e4b3528a5b59b49443ab65ef856beebc177bffa328c34de3cc92915a`  
		Last Modified: Wed, 29 Nov 2023 02:18:17 GMT  
		Size: 199.0 MB (198979721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe8b241e0b8b79c5571d374d51fc1c43e099b323a54045465acd6770df504aa`  
		Last Modified: Wed, 29 Nov 2023 02:17:59 GMT  
		Size: 3.8 MB (3804319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d12a1cc8c577c126780a1012e2815212eefe9535087164ebcdbcf81baadac20`  
		Last Modified: Wed, 29 Nov 2023 02:17:58 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
