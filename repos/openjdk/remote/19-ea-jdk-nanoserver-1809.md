## `openjdk:19-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:e7e3658888efbf1c7a706eb40fed49919e3490ba756d77451515997630bad9b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `openjdk:19-ea-jdk-nanoserver-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull openjdk@sha256:5147b9c5c24fca7686c5f4dc414f08d4106a3eb6f45090614965e4e997b8be6e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294533680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c06d584352608e2b47f2d5d316d66ca578e9325d2dcab46f05372ad3e0add8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Tue, 08 Mar 2022 21:56:20 GMT
SHELL [cmd /s /c]
# Wed, 09 Mar 2022 17:13:35 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 09 Mar 2022 17:13:36 GMT
USER ContainerAdministrator
# Wed, 09 Mar 2022 17:13:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 09 Mar 2022 17:13:48 GMT
USER ContainerUser
# Tue, 29 Mar 2022 00:18:49 GMT
ENV JAVA_VERSION=19-ea+15
# Tue, 29 Mar 2022 00:19:03 GMT
COPY dir:381391f2c8770c3199db33f10ea3eb7bb36ab341d2a71c6db293ae0e24f44960 in C:\openjdk-19 
# Tue, 29 Mar 2022 00:19:40 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e0065cd23a657c8f30ae5af121fd18451d2307835a1124ea57c80683eda26c94`  
		Last Modified: Tue, 08 Mar 2022 22:37:21 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab71e137ca33aa5127b0e55796dd1ffba9bdcf004bd9e37533e42daa5ebd2bf`  
		Last Modified: Wed, 09 Mar 2022 17:42:19 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b9123b1e06063521bbaeb5ac4dc7ac8960be154774560ca5c9db99a43b2d8d`  
		Last Modified: Wed, 09 Mar 2022 17:42:19 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ab23123853d0353a546935f5a1d10d91f5c5c44d79bf888ae0d353941c6938`  
		Last Modified: Wed, 09 Mar 2022 17:42:19 GMT  
		Size: 68.0 KB (68002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e219e794e6ab490d19f1491c0d2de445c430aac5eceb51f362b916de14e9250d`  
		Last Modified: Wed, 09 Mar 2022 17:42:17 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb41d4019c79695bb996a1ee1d72fa46fe33b1b085e1648eb865f8474c5defec`  
		Last Modified: Tue, 29 Mar 2022 00:29:30 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfee1bf9746ce45a9f77c98ed0e317ef1eb610f2924db257b7d9739ec3f8cd5d`  
		Last Modified: Tue, 29 Mar 2022 00:32:57 GMT  
		Size: 187.8 MB (187825462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693d37960c08c86f5b4ada874fb4bbae27b2cfb15a4a8bf4916ad1f61d97c05`  
		Last Modified: Tue, 29 Mar 2022 00:29:30 GMT  
		Size: 3.6 MB (3578825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b435ebd3d59a0045bb3a3c1ed79a94ff8f16e5c7421b2eb0aebdf7ac6b33f77`  
		Last Modified: Tue, 29 Mar 2022 00:29:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
