## `openjdk:24-nanoserver-1809`

```console
$ docker pull openjdk@sha256:a4dbb1b9ef318da4bf1f455e63568da8daa1a7af0662d53ba4fffba869849ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `openjdk:24-nanoserver-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull openjdk@sha256:148023389a27a64e6a436e2ba4489b8fa1fa50977d6c0ff9725e508de576b5a7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.8 MB (366762469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c0e67cbd83a1270d8aef88bec26765dae9e55e13d426491a254e194cf63292`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Fri, 12 Jul 2024 23:13:12 GMT
SHELL [cmd /s /c]
# Fri, 12 Jul 2024 23:13:13 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 12 Jul 2024 23:13:14 GMT
USER ContainerAdministrator
# Fri, 12 Jul 2024 23:13:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 12 Jul 2024 23:13:17 GMT
USER ContainerUser
# Fri, 12 Jul 2024 23:13:17 GMT
ENV JAVA_VERSION=24-ea+6
# Fri, 12 Jul 2024 23:13:24 GMT
COPY dir:f97325b4d24395b9f860cacd61ac2a4139f040cef0251ecf9e9934b30d0e2028 in C:\openjdk-24 
# Fri, 12 Jul 2024 23:13:31 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 12 Jul 2024 23:13:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7372db51eb2e16992964408f4eeebf0e7b3e8dbe2d52577c681d3daad6c0a8fc`  
		Last Modified: Fri, 12 Jul 2024 23:13:36 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8621ee0989504e8e3419702b08313c7b77b313ebd2ef59a1f233bca01d86de03`  
		Last Modified: Fri, 12 Jul 2024 23:13:35 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8afafe14d26f1d265b5cf8ad1b3fb018722a011d0988fcb65c0ecf8c84645e29`  
		Last Modified: Fri, 12 Jul 2024 23:13:35 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a952f3e926e1b12fb72227c7e901d06bc4ebc2bd9dd7e7b5029ea7ca3919968`  
		Last Modified: Fri, 12 Jul 2024 23:13:35 GMT  
		Size: 72.6 KB (72584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a372c113e59e8aebff252d6f47d050cd42e87238c1f4a3f571fdecf07b3f6b74`  
		Last Modified: Fri, 12 Jul 2024 23:13:34 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7885574eadf5b6a0e5d90fb57ddf37dc8bad42a47e790edefc3c1df4e30ece`  
		Last Modified: Fri, 12 Jul 2024 23:13:34 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac11e8583834d29f4361ccd6d3bc57c60dcf5d6a4d0aa742b39a6a1af421eefe`  
		Last Modified: Fri, 12 Jul 2024 23:13:46 GMT  
		Size: 206.3 MB (206320422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2e0294657e0806a5fbdf3dfc832f5fd3b958ff29a65a7f7dcb2eadba4110f4`  
		Last Modified: Fri, 12 Jul 2024 23:13:35 GMT  
		Size: 5.3 MB (5281847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cff69031ed69ed08102d07e4ad9b9221fd39caef4da075fe36f68529944a920`  
		Last Modified: Fri, 12 Jul 2024 23:13:34 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
