## `openjdk:20-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:7f8e38c99f8822eaa62fa1cd486dcc27204bff8c7649f190aad2aca652dca615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `openjdk:20-ea-jdk-nanoserver` - windows version 10.0.17763.3650; amd64

```console
$ docker pull openjdk@sha256:371d12b9ac87f99956d694f70a792a5e99ca638f019da655abfc8cad1d1057c6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303800666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84b39e884b9018b4c6010fd780c2297f726298cf75f4d3d54e04dabbffe2fbf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Nov 2022 18:06:28 GMT
RUN Apply image 10.0.17763.3650
# Tue, 08 Nov 2022 18:36:25 GMT
SHELL [cmd /s /c]
# Wed, 09 Nov 2022 17:26:48 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 09 Nov 2022 17:26:49 GMT
USER ContainerAdministrator
# Wed, 09 Nov 2022 17:27:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 09 Nov 2022 17:27:07 GMT
USER ContainerUser
# Wed, 09 Nov 2022 17:27:08 GMT
ENV JAVA_VERSION=20-ea+22
# Wed, 09 Nov 2022 17:27:26 GMT
COPY dir:aad69aed6f652d82aa51467e9aa3388f27a3c781e2cc620a3dc458bdb415983c in C:\openjdk-20 
# Wed, 09 Nov 2022 17:27:54 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 09 Nov 2022 17:27:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:35ab4104a4d9df6a0d1eac84cc8fbc13511ef6c8aef5ced04fdf63e7e20803a3`  
		Last Modified: Tue, 08 Nov 2022 19:45:20 GMT  
		Size: 106.7 MB (106723592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e8f4bb4b79b67857c1e4ac5c66026fd5ff5badbde5a8b59b11251b02699586`  
		Last Modified: Tue, 08 Nov 2022 19:44:52 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5380ecadb3b5072bd5e7cf41fa446b5ae89ef7d71fde34772d7b32062aca954b`  
		Last Modified: Wed, 09 Nov 2022 17:37:09 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de19002dcea365821038023716e28374a8210ac45b5a63b539639130ad9b6bd8`  
		Last Modified: Wed, 09 Nov 2022 17:37:08 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc05d65ddfbc35592002f4ae7726cad3fa9b8777ac1f0cbb66bad8963c18cc7`  
		Last Modified: Wed, 09 Nov 2022 17:37:08 GMT  
		Size: 74.7 KB (74716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0517802e30312d5724623bf6cc9fe338f7330d522b267fad48ae4f85da52072`  
		Last Modified: Wed, 09 Nov 2022 17:37:06 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c363ddc0d44bffff40d6aaa2e1c310cf679a14fe8e948273b484265199e81b`  
		Last Modified: Wed, 09 Nov 2022 17:37:06 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb3d3e1e17cc37ba5eb5fe1a3fa38f6f0516dd3caee45e5c8ec3dc744dc0e83`  
		Last Modified: Wed, 09 Nov 2022 17:37:29 GMT  
		Size: 193.2 MB (193205849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb78d7d88b341ca904e4c8b3f78bd9f7370e3cce27c87d0fdba4dcdf5fe75a52`  
		Last Modified: Wed, 09 Nov 2022 17:37:07 GMT  
		Size: 3.8 MB (3789988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692cc5d37143a5b6228f9053769bb1796aa9f4dc3c926b9152f2dbe2be81f878`  
		Last Modified: Wed, 09 Nov 2022 17:37:05 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
