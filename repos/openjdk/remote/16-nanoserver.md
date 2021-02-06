## `openjdk:16-nanoserver`

```console
$ docker pull openjdk@sha256:ec1ad2c384b28388d775fa79f919b0f516d00fab034fcc02e37a50a79f184a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `openjdk:16-nanoserver` - windows version 10.0.17763.1697; amd64

```console
$ docker pull openjdk@sha256:4ff466d7cb28a7451d442d54b931475cf6532ca11118ae24ab7e217e995ced1b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285111019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dce0ac314e30cbfc3e3c14ab21f8f54d0606de3b4371f788e3d5b16651cd9be`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 19:56:48 GMT
SHELL [cmd /s /c]
# Wed, 13 Jan 2021 20:35:00 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 13 Jan 2021 20:35:01 GMT
USER ContainerAdministrator
# Mon, 01 Feb 2021 19:27:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 01 Feb 2021 19:27:44 GMT
USER ContainerUser
# Fri, 05 Feb 2021 22:23:06 GMT
ENV JAVA_VERSION=16
# Fri, 05 Feb 2021 22:23:20 GMT
COPY dir:8cfdd9250e382800ba1fb4a6be20f45b5dda5b9351262a1210a73a6ffb109ce7 in C:\openjdk-16 
# Fri, 05 Feb 2021 22:23:32 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 05 Feb 2021 22:23:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:62239e9aa1a352a20b0d4969c2b508b8a18d10e799d4db72e6f24ccbb2c724d9`  
		Size: 101.3 MB (101340070 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c2b6c001c337f812bceb3b03d15a70d1d9905540658e751e42f20f7cc0ddc819`  
		Last Modified: Wed, 13 Jan 2021 21:16:47 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22f53d1f631e14bb9677766dc089ce4caf4dae9627d1513773cfff289e94f42`  
		Last Modified: Wed, 13 Jan 2021 21:19:22 GMT  
		Size: 920.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43af010a68e2978961a3d63887efbc1230811009f66bd683e9fc4174f4185177`  
		Last Modified: Wed, 13 Jan 2021 21:19:20 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc21fd6a90ecf4bad3b3c8e7bb04983c6f83066e69902b8ca81fa59689840b66`  
		Last Modified: Mon, 01 Feb 2021 19:59:49 GMT  
		Size: 64.4 KB (64370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31594dace4b4fb71f33733dfe040fcaa15873767a452b1cd4fc5f9c40298a9a3`  
		Last Modified: Mon, 01 Feb 2021 19:59:46 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ef26a409d849e20b4c2e70ce1e18e3cce8c37d0fcc1794f1ab1df285b08e46`  
		Last Modified: Fri, 05 Feb 2021 22:32:00 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c380c717ccbe5e7833d11a5cc1a105857fe46bf7f36315b57b6c9e209265e39f`  
		Last Modified: Fri, 05 Feb 2021 22:32:19 GMT  
		Size: 180.0 MB (180035996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e039591ed4cda4bbff1a64daa45ab0ccde201335f7357b8ffe8874829e2f445b`  
		Last Modified: Fri, 05 Feb 2021 22:32:01 GMT  
		Size: 3.7 MB (3664473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f4d87f71781a984a78b2c62a22e6fc6cd9bc8020e4da2420df7158915752f2`  
		Last Modified: Fri, 05 Feb 2021 22:32:00 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
