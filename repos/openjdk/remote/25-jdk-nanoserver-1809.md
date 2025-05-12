## `openjdk:25-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:48ca3312fd40cbca6ec5adecff1fc06f912c354b95cccd17d977c21652548ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `openjdk:25-jdk-nanoserver-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull openjdk@sha256:926b9585fca615eb2013e3a20e263744ad615f6839758abec130f47f33b3b983
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321587645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85fff3f245a29de2565ec20898a04125cb060e1af4dc093b7ceb7c23c9649b3c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Mon, 12 May 2025 20:08:47 GMT
SHELL [cmd /s /c]
# Mon, 12 May 2025 20:08:48 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 12 May 2025 20:08:49 GMT
USER ContainerAdministrator
# Mon, 12 May 2025 20:09:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 12 May 2025 20:09:08 GMT
USER ContainerUser
# Mon, 12 May 2025 20:09:08 GMT
ENV JAVA_VERSION=25-ea+22
# Mon, 12 May 2025 20:09:22 GMT
COPY dir:d2aeeab016ce5cfb722c90fbb6527341de5d03dac18528814b93fc4084ba77f8 in C:\openjdk-25 
# Mon, 12 May 2025 20:09:28 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 12 May 2025 20:09:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e964c72fb5be77163e031462fb094de88283b07d7b694a1e06e08577ef266c1a`  
		Last Modified: Mon, 12 May 2025 20:09:33 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e626c765b94ec57ed5f50b939f21ee2d0be3aa1adc540b1567ec3cd1024726f`  
		Last Modified: Mon, 12 May 2025 20:09:33 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17472dd1e6f52a08563f2cf262b3d6ed3c49f036cdb601b141e4842ae8db9fc`  
		Last Modified: Mon, 12 May 2025 20:09:33 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e142497424f839ea9c8c174c1e875d275ec0adea7aeca018df4891cdd7b87cf`  
		Last Modified: Mon, 12 May 2025 20:09:32 GMT  
		Size: 66.1 KB (66134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb0aa579060a21967ee8e77e0c4a7c1e5f70829cda8bd1d521dc943d9c8d56d`  
		Last Modified: Mon, 12 May 2025 20:09:31 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32f2b0fc35797a070ccbbc6a305869237591334964315ce4294d1e87f83259a`  
		Last Modified: Mon, 12 May 2025 20:09:32 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73206b21d37a9fa0e78b3ca856735ce020bd60662a324497e253030731c2a0e7`  
		Last Modified: Mon, 12 May 2025 20:09:42 GMT  
		Size: 208.4 MB (208365658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730101272a379512d83bf33c8fe9f96ade95bcf3bcf196b1a499d79d200536f9`  
		Last Modified: Mon, 12 May 2025 20:09:32 GMT  
		Size: 4.4 MB (4397389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78165f53b601b351eeacb4d3416ac1eb64a0e5f61b39f0a10e7add1dcab737a4`  
		Last Modified: Mon, 12 May 2025 20:09:31 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
