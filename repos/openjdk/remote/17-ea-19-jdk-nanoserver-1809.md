## `openjdk:17-ea-19-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:7bb1921d83fdb9dbcd7bfe5d12e41f200fb465c210729e2a22eef40e86624ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64

### `openjdk:17-ea-19-jdk-nanoserver-1809` - windows version 10.0.17763.1879; amd64

```console
$ docker pull openjdk@sha256:b8cb1345436133d3ef439690bac334f3e6a63fae90f8542dc9eaa8aa2d66ddfd
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (286021054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7467db13ecf344e0ece3d9ec8201090967b55981e8a39d14f636c15e0b85a9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Apr 2021 16:02:06 GMT
RUN Apply image 1809-amd64
# Wed, 14 Apr 2021 16:53:40 GMT
SHELL [cmd /s /c]
# Wed, 14 Apr 2021 16:53:41 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 14 Apr 2021 16:53:42 GMT
USER ContainerAdministrator
# Wed, 14 Apr 2021 16:54:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 Apr 2021 16:54:03 GMT
USER ContainerUser
# Mon, 26 Apr 2021 23:17:42 GMT
ENV JAVA_VERSION=17-ea+19
# Mon, 26 Apr 2021 23:17:58 GMT
COPY dir:cf0b923f41eedb4ea71f23d7e7844f75e3b62d7162c1415afde24909d67dfe0b in C:\openjdk-17 
# Mon, 26 Apr 2021 23:18:23 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 26 Apr 2021 23:18:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ea84579f6cd5b58fe78732be37450bd188c8923de3a2062664f3992861449b5c`  
		Size: 101.3 MB (101340157 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c2c727299531adc7c2aacb1f062d72fd42cec96a0d235b3e5b0afe03e9ddbc7d`  
		Last Modified: Wed, 14 Apr 2021 17:41:13 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4846a68a532c85058f47e1e9b777bab26eb5ad132cdeb3d646bc51d43346f1f8`  
		Last Modified: Wed, 14 Apr 2021 17:41:12 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dede727741920ec94cb8aac2b231667fd531dbedb64b47f6dddc1577123fcd85`  
		Last Modified: Wed, 14 Apr 2021 17:41:10 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7be7a926f02c08c32de5bc4e57d18923e0441090bd084aeb1b7dafaeb4ece58`  
		Last Modified: Wed, 14 Apr 2021 17:41:09 GMT  
		Size: 65.7 KB (65686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f5a6de061f5f5be316a0cf2d8471cf2baf8b3927a20b9d29826dc97bef2e54`  
		Last Modified: Wed, 14 Apr 2021 17:41:06 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d7ba29a03ba723c478bc9857eb2e56ee9151e8cdbffe29243a99f89b0397e8`  
		Last Modified: Mon, 26 Apr 2021 23:25:39 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2021ebedd7c90c6f8626886e4a5c36725c73a5ca464c4f4e0023d0b7698161f2`  
		Last Modified: Mon, 26 Apr 2021 23:25:58 GMT  
		Size: 181.0 MB (180968948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bec7eaaa0452e02fb354f744d09519afe8a49de6c9ecffe7a8d21b1dbc5768`  
		Last Modified: Mon, 26 Apr 2021 23:25:40 GMT  
		Size: 3.6 MB (3639408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0102b1f73d77842ed0245b118192b3de182d8073a54c48936af1dcae5958a0`  
		Last Modified: Mon, 26 Apr 2021 23:25:36 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
