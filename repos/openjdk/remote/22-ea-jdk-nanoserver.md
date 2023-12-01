## `openjdk:22-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:ec147018f3ab590c4d83f1c97cd4a2744ddcc7dfc1ad8021bb8c8437a1d27e90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `openjdk:22-ea-jdk-nanoserver` - windows version 10.0.17763.5122; amd64

```console
$ docker pull openjdk@sha256:79d8c033b81563e35316034e9687d9da5668ccec21a8507d7654bca197edc745
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308197378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022baf07d8713c423ea1feedd188ec24498748f7036ae2c2b4fb55f79cb3a35b`
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
# Fri, 01 Dec 2023 20:19:09 GMT
ENV JAVA_VERSION=22-ea+26
# Fri, 01 Dec 2023 20:19:25 GMT
COPY dir:d5f507ab61ea31e637d6da65235933874429183aa2532f04ff38e295643e6f1f in C:\openjdk-22 
# Fri, 01 Dec 2023 20:19:43 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 01 Dec 2023 20:19:44 GMT
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
	-	`sha256:18fe103381212bc575b66653497e535e30b42edd5dc5f7aac16bf218f5a1dfed`  
		Last Modified: Fri, 01 Dec 2023 20:21:51 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f570f5d66a99ae082b391eaf9a1ee6fafcfd0cf6ca8911b34136b3b911f8b63d`  
		Last Modified: Fri, 01 Dec 2023 20:22:11 GMT  
		Size: 199.8 MB (199815648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b849faa5c9333151585cac8d961ffc89a146c070a54737dc092ac187a7f57f`  
		Last Modified: Fri, 01 Dec 2023 20:21:52 GMT  
		Size: 3.8 MB (3803825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277073492679c1661b42155cc46097198bbde4034c370916b4ccc5deadee2cd8`  
		Last Modified: Fri, 01 Dec 2023 20:21:51 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
