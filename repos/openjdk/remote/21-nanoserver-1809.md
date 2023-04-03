## `openjdk:21-nanoserver-1809`

```console
$ docker pull openjdk@sha256:9f472fc6ae6232041efdabaa017e0978219fc6566318b6f1c7469fc6db5cf206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `openjdk:21-nanoserver-1809` - windows version 10.0.17763.4131; amd64

```console
$ docker pull openjdk@sha256:4593c5de08f1fc2aa400e44ea2a145475cf422365abeec73f8af1697d7c30de5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.6 MB (306635738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ede7e4ca789415985256ec63a1f5a94d03724e087a90f2120ee21ea4bfe53a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 11 Mar 2023 10:09:02 GMT
RUN Apply image 10.0.17763.4131
# Thu, 16 Mar 2023 00:45:50 GMT
SHELL [cmd /s /c]
# Thu, 16 Mar 2023 04:21:31 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 16 Mar 2023 04:21:32 GMT
USER ContainerAdministrator
# Thu, 16 Mar 2023 04:21:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 16 Mar 2023 04:21:45 GMT
USER ContainerUser
# Mon, 03 Apr 2023 21:20:18 GMT
ENV JAVA_VERSION=21-ea+16
# Mon, 03 Apr 2023 21:20:36 GMT
COPY dir:b0156aa1a396e595f52fec76f5c6208468124e601c9781ed0666ce045452386d in C:\openjdk-21 
# Mon, 03 Apr 2023 21:21:23 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 03 Apr 2023 21:21:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:95eb2f0f3287f5ec687287cc244924aafc74c7ada3121d43f54223487f3f2d8d`  
		Last Modified: Thu, 16 Mar 2023 01:43:14 GMT  
		Size: 106.7 MB (106684240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5837fe68a36caddf38b0aaa99f4ef20ca36d8dfe2825fa6ffbcf0d38b9d59a`  
		Last Modified: Thu, 16 Mar 2023 01:42:43 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450d272e24dcd824ed0a2cfaab457791740701be7e655050f5a344dba0111120`  
		Last Modified: Thu, 16 Mar 2023 04:32:07 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375c9b367947b6469eed8f3b494a27778599dd1e8ab85682d96eee96a8d38097`  
		Last Modified: Thu, 16 Mar 2023 04:32:07 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d48b42b9c3192f6ddd8ce43c9c7a2c8b1fb3f906fe4eea3aa9b1e4fc28b4161`  
		Last Modified: Thu, 16 Mar 2023 04:32:08 GMT  
		Size: 72.2 KB (72190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44544dc6ee19ff5b39d3756cbc6d53830c65429f0d1ad05b8422c3c33ac8311`  
		Last Modified: Thu, 16 Mar 2023 04:32:05 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa665a932182ab83825772fdd05acbf1291fd4d46751ee093ad0533d6f0b02a`  
		Last Modified: Mon, 03 Apr 2023 21:23:43 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498d9ca2c5324a5b2d8edaba22acdc4732fff836eeea205241e1b694df6ea13e`  
		Last Modified: Mon, 03 Apr 2023 21:24:08 GMT  
		Size: 196.1 MB (196096132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89c0e22420f333989ae1df114fae4d0abf8315d4d015f0c93c9877fc584eef5`  
		Last Modified: Mon, 03 Apr 2023 21:23:45 GMT  
		Size: 3.8 MB (3776258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320ccf9fadff9e22feecb376b03e1200b24c25f4f2395cd16dd8d5b657c764b9`  
		Last Modified: Mon, 03 Apr 2023 21:23:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
