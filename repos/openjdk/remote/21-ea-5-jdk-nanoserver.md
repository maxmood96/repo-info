## `openjdk:21-ea-5-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:210d29873de64fbd1f5943d7526bb8cb1262b879c5ff0d89bd4fa94b28ab2358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3887; amd64

### `openjdk:21-ea-5-jdk-nanoserver` - windows version 10.0.17763.3887; amd64

```console
$ docker pull openjdk@sha256:190edaac050a1c6f44792e7d91d7420d8b56af67e0590d6b521ee70806c8a16f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.5 MB (304476757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff75a47c0a529252061163790f8e15bca54ad7511cdb359df4ad0ce699912a48`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jan 2023 05:17:01 GMT
RUN Apply image 10.0.17763.3887
# Thu, 12 Jan 2023 01:45:31 GMT
SHELL [cmd /s /c]
# Thu, 12 Jan 2023 05:11:18 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 12 Jan 2023 05:11:19 GMT
USER ContainerAdministrator
# Thu, 12 Jan 2023 05:11:34 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 12 Jan 2023 05:11:35 GMT
USER ContainerUser
# Fri, 13 Jan 2023 00:18:26 GMT
ENV JAVA_VERSION=21-ea+5
# Fri, 13 Jan 2023 00:18:41 GMT
COPY dir:2f2fdb9dbe8d086cf120c146a57f0b2459bca8999858ecd01d846f3de07dda8d in C:\openjdk-21 
# Fri, 13 Jan 2023 00:19:22 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 13 Jan 2023 00:19:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e58f9ad3b15a2a4882ab0a845e8e619cc8c3c411ddbe8b50046c1618a95c1397`  
		Last Modified: Thu, 12 Jan 2023 02:40:44 GMT  
		Size: 106.7 MB (106666138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea67a6bd980bdee35399883e5abcc31c738b338ad384b2f92d91a15cf09d9df`  
		Last Modified: Thu, 12 Jan 2023 02:40:16 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c10d054b2ffa414ee6a75be646bd3ee1ea6bd5a11e2400c757afeb68d8c6d4`  
		Last Modified: Thu, 12 Jan 2023 05:23:44 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e99b18c6e5f683aa5e6fa7ad7ce124fabae3b048287a183a71a7dc15df8ef6a`  
		Last Modified: Thu, 12 Jan 2023 05:23:44 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6700bb1c6480ee456d21843fdd01e9a05b05ea2d8ac6f54cbd75acbaafe6ab52`  
		Last Modified: Thu, 12 Jan 2023 05:23:44 GMT  
		Size: 69.3 KB (69271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9fc3250a046295f3386717ccc0548a5954c2c32fb3c4bbbc83dc8fdd13e1c27`  
		Last Modified: Thu, 12 Jan 2023 05:23:42 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce8499b6f2aaa46904230ee45d6bb8d23bd6dec02c446c3c416913d1852bc91`  
		Last Modified: Fri, 13 Jan 2023 03:20:15 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa2a4d2bfe097a31bda00e566240776fa6d4191c2ef09e5dd762c92869e2bdf`  
		Last Modified: Fri, 13 Jan 2023 03:20:38 GMT  
		Size: 194.0 MB (193957488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3d9a50d82fb8e990d8f9061b1eaceeb46aa91af5860bf8a7432405f24a54bef`  
		Last Modified: Fri, 13 Jan 2023 03:20:16 GMT  
		Size: 3.8 MB (3776981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da018cca7b7fbebced16385ccdd438d87988223873ea1cf4b820afeef6784bdc`  
		Last Modified: Fri, 13 Jan 2023 03:20:15 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
