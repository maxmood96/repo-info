## `openjdk:22-nanoserver`

```console
$ docker pull openjdk@sha256:eef6eac344c1217325f86c504c760be4fd8e9563afc4481b68422c0a3a7f7d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `openjdk:22-nanoserver` - windows version 10.0.17763.5122; amd64

```console
$ docker pull openjdk@sha256:087ccd1f7d916d38c21f7d05bd6a1f723e131b3d41afa83d1421a63e201bc57b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.4 MB (308382998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee82777f163d3e0a532654cfc3b2c6277d94675489592703898c81ba6d22264`
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
# Thu, 16 Nov 2023 05:24:56 GMT
ENV JAVA_VERSION=22-ea+23
# Thu, 16 Nov 2023 05:25:12 GMT
COPY dir:7a47213a9d830d9c4246c0f1198f6179f788435f5144076c8867ff083c4a5bcd in C:\openjdk-22 
# Thu, 16 Nov 2023 05:25:25 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 16 Nov 2023 05:25:26 GMT
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
	-	`sha256:48542ac1cf304690a0884c97bbf32da040f6abbb1abe5c169ce0fc525376cc51`  
		Last Modified: Thu, 16 Nov 2023 05:27:28 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ea1902f631182a85f0411a3af0e500c09bc6ce3881bd3467fd4778d87ad0d7`  
		Last Modified: Thu, 16 Nov 2023 05:27:49 GMT  
		Size: 200.0 MB (199993736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb21adc7f3da6a86cc3d9ce35a98cf5ea05d382e3cb60b2bf59dabf61926049`  
		Last Modified: Thu, 16 Nov 2023 05:27:29 GMT  
		Size: 3.8 MB (3811367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e5cb05d9616b63456912a522d8f87f8a790b3c1b4e64aae4ddb7f40c87fd6c`  
		Last Modified: Thu, 16 Nov 2023 05:27:28 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
