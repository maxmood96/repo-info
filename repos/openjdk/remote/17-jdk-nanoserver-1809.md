## `openjdk:17-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:65a8aa642405d79bb08748724d7319337519015d06f32258a449551e8ad72fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `openjdk:17-jdk-nanoserver-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull openjdk@sha256:af70acbf5d8ea5db0c818a0389553090dccaa9c1fb8a542d7fbec27143a2deb0
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286295166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69aece1a81f84de92a9aaa8c8b0fab5732862ee0303b70f5d4ba45833f15f664`
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
# Wed, 13 Jan 2021 19:57:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 13 Jan 2021 19:57:07 GMT
USER ContainerUser
# Wed, 13 Jan 2021 19:57:07 GMT
ENV JAVA_VERSION=17-ea+4
# Wed, 13 Jan 2021 19:57:47 GMT
COPY dir:f4566a9c0c60841d4c036675c1cd7ed02850bad16e9b2b253e3d937ea546e17c in C:\openjdk-17 
# Wed, 13 Jan 2021 19:58:10 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Wed, 13 Jan 2021 19:58:11 GMT
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
	-	`sha256:4a588d5e7e84f7b20f460bb66a5bb1f2b7e762713923669ac453e6eda8b23eb7`  
		Last Modified: Wed, 13 Jan 2021 21:16:44 GMT  
		Size: 68.0 KB (68013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df625a811b1b58029fb5e4c987218865063cb248bd9d163cc15c8584c8af7afd`  
		Last Modified: Wed, 13 Jan 2021 21:16:40 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c893104d7a9a22927dbb1496e0218b1af5864a31f4d66e12253609b2924a50`  
		Last Modified: Wed, 13 Jan 2021 21:16:42 GMT  
		Size: 898.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f672d26d7e0176c647ed0f48d13b370d6bd7c1a7ffeb25f0ed50d37a8fd6e3`  
		Last Modified: Wed, 13 Jan 2021 21:16:59 GMT  
		Size: 181.2 MB (181196813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216f7af11c39895d434235e97fe01981332fa239753b2d0fa81116d3ff7d0cfd`  
		Last Modified: Wed, 13 Jan 2021 21:16:41 GMT  
		Size: 3.7 MB (3684978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7a6ae291131442da705296963af3e24dea2a6088180a046fb523c56d29f8be`  
		Last Modified: Wed, 13 Jan 2021 21:16:42 GMT  
		Size: 881.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
