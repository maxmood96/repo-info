## `openjdk:24-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:42eca193f107102a4eef24589b42af9a61edd921b0b86391bf560f9f1e572905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `openjdk:24-jdk-nanoserver` - windows version 10.0.17763.6293; amd64

```console
$ docker pull openjdk@sha256:b1949270d3927c1a44e14c297710f251758ce50b03b58ef0aa1946a5c746c6ee
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.4 MB (367358420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9adf9ab50db34ebb57256e09bec80c226134dc9e2d0b3392e9ee3bbf4de5909`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Mon, 16 Sep 2024 19:56:37 GMT
SHELL [cmd /s /c]
# Mon, 16 Sep 2024 19:56:38 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 16 Sep 2024 19:56:39 GMT
USER ContainerAdministrator
# Mon, 16 Sep 2024 19:56:41 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 16 Sep 2024 19:56:42 GMT
USER ContainerUser
# Mon, 16 Sep 2024 19:56:42 GMT
ENV JAVA_VERSION=24-ea+15
# Mon, 16 Sep 2024 19:56:58 GMT
COPY dir:f58405521a7a90d3a046111848e6fe52efce492b94ef23578bb34118c2e27c5b in C:\openjdk-24 
# Mon, 16 Sep 2024 19:57:02 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 16 Sep 2024 19:57:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1f6f3f6b35bf1d9310cf7d526b59c9f001d52ca780158a47ab92b9dc0b6f6e`  
		Last Modified: Mon, 16 Sep 2024 19:57:10 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c756788ec94a24e3516ed8a895f7b55b28de18334c50c36078194a147639ac12`  
		Last Modified: Mon, 16 Sep 2024 19:57:09 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e888c1f553cde8ce5ac470f54360bc6f23973e6986a96d0fd7fcb02222b8b2f1`  
		Last Modified: Mon, 16 Sep 2024 19:57:09 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108df3b94962776ce0cebaaa3077a5ebd2dc0be9ddc869f9543ab0149593665c`  
		Last Modified: Mon, 16 Sep 2024 19:57:09 GMT  
		Size: 84.0 KB (83992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fec29599649b00f88ffb1c11e7258fde42e8e09ee40b1405c846161a130fa1`  
		Last Modified: Mon, 16 Sep 2024 19:57:07 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada43a452f73c0251a3185414c8d9ab8a510ef354d70ec36bd7be8fb01c312f6`  
		Last Modified: Mon, 16 Sep 2024 19:57:07 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b011d94d9c1727f7f5799c77859b347353793fb8fb4b3dc6cfdcd6eb8a066633`  
		Last Modified: Mon, 16 Sep 2024 19:57:19 GMT  
		Size: 207.6 MB (207647707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe144d4c8cdba4aaf263f8b115ca471cf427d04679510ef07255c63e9f9dae5`  
		Last Modified: Mon, 16 Sep 2024 19:57:08 GMT  
		Size: 4.5 MB (4539591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e832d37be9b42d3a157f1e5fcdaeec23481b638ee639a9515bfa3918ec4a04`  
		Last Modified: Mon, 16 Sep 2024 19:57:07 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
