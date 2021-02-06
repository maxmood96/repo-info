## `openjdk:17-ea-nanoserver`

```console
$ docker pull openjdk@sha256:16a1b2a0b7f4febc5437217292889245992488b3c53acb4c31e347b99d37f6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `openjdk:17-ea-nanoserver` - windows version 10.0.17763.1697; amd64

```console
$ docker pull openjdk@sha256:492d2f88259a7094894bcc6cdf85ecff1f7375f10930b7edc6e19953ad238f14
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286052406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6425052bc56b63a3f0b9a10f3288096c56037cdd3358e3ccc0890869c51c975c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 19:56:48 GMT
SHELL [cmd /s /c]
# Wed, 13 Jan 2021 19:56:48 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 13 Jan 2021 19:56:49 GMT
USER ContainerAdministrator
# Mon, 01 Feb 2021 19:22:27 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 01 Feb 2021 19:22:28 GMT
USER ContainerUser
# Fri, 05 Feb 2021 22:18:54 GMT
ENV JAVA_VERSION=17-ea+8
# Fri, 05 Feb 2021 22:19:07 GMT
COPY dir:20f6b1b89449cd2d6043cf14b19a668ea48d02f09bb58513c15c1b288ce85129 in C:\openjdk-17 
# Fri, 05 Feb 2021 22:19:20 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 05 Feb 2021 22:19:21 GMT
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
	-	`sha256:788a0bd344d2eb3850ddd4570305cbcf959de9a743a310f941c297081c240d8f`  
		Last Modified: Wed, 13 Jan 2021 21:16:46 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db311194c9cbd0c67151ee177949a18a7ad83e5551b659b30ef3151062c5a98`  
		Last Modified: Wed, 13 Jan 2021 21:16:47 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df1939641b7f54cacd46e02c3a2331df7de05527860cba622a289f0c5e195c7`  
		Last Modified: Mon, 01 Feb 2021 19:57:33 GMT  
		Size: 68.4 KB (68408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2725371e5f3ecc54b6264bcd3123ec0bd036d480a3110dba6761e7999496c08c`  
		Last Modified: Mon, 01 Feb 2021 19:57:30 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad6cba154c6080d55f7a5a73d3511fa983e9078d92ff4b382a26caa6312b3c3`  
		Last Modified: Fri, 05 Feb 2021 22:30:07 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986b4c95e2f55d61ac408ee54ac501bd311b155edd1b2e378ae194c1fce084fa`  
		Last Modified: Fri, 05 Feb 2021 22:30:33 GMT  
		Size: 181.0 MB (180992938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bad422174219a996af3ed40cb7280b8f96e13ee61d00ca400360b9e599cbbd`  
		Last Modified: Fri, 05 Feb 2021 22:30:08 GMT  
		Size: 3.6 MB (3644986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af6d24f20ad52b60d6b65f01a0428b90b9c5acee480a0dff9aeb94d9ebec55c`  
		Last Modified: Fri, 05 Feb 2021 22:30:07 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
