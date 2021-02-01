## `openjdk:16-ea-nanoserver-1809`

```console
$ docker pull openjdk@sha256:b755b94b06cc0bfb78ccffd4db17939fe3b75fcc6573c83658e2c2b4e6dc48cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `openjdk:16-ea-nanoserver-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull openjdk@sha256:d5f6018cd112ac65716d8a7d061372c6719b5d977d396f166e305e20d16a2e13
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285109982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e58ba6caae49d75bb74904bcec4dbe9ab2b8f4e0ded2c08231ce08bc9c71603`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 19:56:48 GMT
SHELL [cmd /s /c]
# Wed, 13 Jan 2021 20:35:00 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 13 Jan 2021 20:35:01 GMT
USER ContainerAdministrator
# Mon, 01 Feb 2021 19:27:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 01 Feb 2021 19:27:44 GMT
USER ContainerUser
# Mon, 01 Feb 2021 19:27:44 GMT
ENV JAVA_VERSION=16-ea+34
# Mon, 01 Feb 2021 19:27:57 GMT
COPY dir:34bc02a77dc0d5a69f6521a3b8c624d3b0f5e8152f303aed7418e38f16cc8d09 in C:\openjdk-16 
# Mon, 01 Feb 2021 19:28:08 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 01 Feb 2021 19:28:08 GMT
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
	-	`sha256:f22f53d1f631e14bb9677766dc089ce4caf4dae9627d1513773cfff289e94f42`  
		Last Modified: Wed, 13 Jan 2021 21:19:22 GMT  
		Size: 920.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43af010a68e2978961a3d63887efbc1230811009f66bd683e9fc4174f4185177`  
		Last Modified: Wed, 13 Jan 2021 21:19:20 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc21fd6a90ecf4bad3b3c8e7bb04983c6f83066e69902b8ca81fa59689840b66`  
		Last Modified: Mon, 01 Feb 2021 19:59:49 GMT  
		Size: 64.4 KB (64370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31594dace4b4fb71f33733dfe040fcaa15873767a452b1cd4fc5f9c40298a9a3`  
		Last Modified: Mon, 01 Feb 2021 19:59:46 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8415e3a91c6a76142af554400622dea7e11db5349635a92561f693b71da27f`  
		Last Modified: Mon, 01 Feb 2021 19:59:46 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6459329dabdd9ac4494d480f052bc577eda65b370eeac7c1c5c08325505f51`  
		Last Modified: Mon, 01 Feb 2021 20:00:06 GMT  
		Size: 180.0 MB (180029687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1282d44da2e9d7bbc4aa7ec6a2450814913aae6787fc9754040b76509e386b84`  
		Last Modified: Mon, 01 Feb 2021 19:59:47 GMT  
		Size: 3.7 MB (3669744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371e9dcec2788d8ca3bcfce19a61734142672c15d1e9a4e3b034fe6f885b74c1`  
		Last Modified: Mon, 01 Feb 2021 19:59:46 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
