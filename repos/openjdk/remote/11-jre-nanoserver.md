## `openjdk:11-jre-nanoserver`

```console
$ docker pull openjdk@sha256:c86a9696149f8640b6ba0c974df68f7d6b32549bee8070be4d6999aea6eae427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3046; amd64

### `openjdk:11-jre-nanoserver` - windows version 10.0.17763.3046; amd64

```console
$ docker pull openjdk@sha256:1528d06a546a619e0decb14367fc7386e811490fcebe3f4d3e8e2cb16b186424
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142779993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8f3289793f96e9276d3405dea97a5f94a07528fd778c4b9f083f16b4274ca2c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jun 2022 19:20:11 GMT
RUN Apply image 10.0.17763.3046
# Wed, 15 Jun 2022 17:30:58 GMT
SHELL [cmd /s /c]
# Wed, 15 Jun 2022 19:47:29 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 15 Jun 2022 19:47:29 GMT
USER ContainerAdministrator
# Wed, 15 Jun 2022 19:47:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 15 Jun 2022 19:47:40 GMT
USER ContainerUser
# Wed, 15 Jun 2022 19:47:41 GMT
ENV JAVA_VERSION=11.0.15
# Wed, 15 Jun 2022 19:51:00 GMT
COPY dir:b19a7bc4e0a7772217140b5b5a40fc0497b9874821c6267cef822ccc10258697 in C:\openjdk-11 
# Wed, 15 Jun 2022 19:51:19 GMT
RUN echo Verifying install ... 	&& echo   java --version && java --version 	&& echo Complete.
```

-	Layers:
	-	`sha256:d555a7e4de4dd775379d5c43c1419374bff7908670dc7444be5e8e8f386f3d26`  
		Size: 103.2 MB (103153235 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92b4c385cd5cbb12fb09cb31c12b5e5de38cf7b380c8681286caac242c06d3ed`  
		Last Modified: Wed, 15 Jun 2022 18:22:11 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38df7c262b7d94033fa5fd9f9d88f748a7f307c2fd804ad9312eb140310e4e3`  
		Last Modified: Wed, 15 Jun 2022 20:20:52 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048b697c322c179bc7e3ff92245e7e2c7679c66602a5c1ddec001e1f335b03c9`  
		Last Modified: Wed, 15 Jun 2022 20:20:52 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726e1b75911d2264ae69e2e92dc20e6094fdfd57421877c68676e0574e0d884e`  
		Last Modified: Wed, 15 Jun 2022 20:20:52 GMT  
		Size: 81.6 KB (81603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28483f3b39db90d5987fa3958b0f89acaf859fda719842e45c023daf9f243ec`  
		Last Modified: Wed, 15 Jun 2022 20:20:49 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e3cda1b1f3997880c55e17936f864b449938825a4233f14496cfc9b4766e8c`  
		Last Modified: Wed, 15 Jun 2022 20:20:49 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db60367686ab9eca0951f5dc8793ab7cb593db07dea69aa15886d096c88adba0`  
		Last Modified: Wed, 15 Jun 2022 20:23:34 GMT  
		Size: 39.5 MB (39486608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c89a8f092cf46436b9085c3e1bb75f742de3672dadc4db41608f6fca092f2b`  
		Last Modified: Wed, 15 Jun 2022 20:22:50 GMT  
		Size: 52.7 KB (52679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
