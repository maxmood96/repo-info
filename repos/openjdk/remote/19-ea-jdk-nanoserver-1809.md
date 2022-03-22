## `openjdk:19-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:0f31670300ecb3597eeed70edd6e8d3c121cbdafd09d54fee9df11c581bf1cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `openjdk:19-ea-jdk-nanoserver-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull openjdk@sha256:f2e9229124a8d65cc26cdeea15aca6b278b3fc9ccad69dbc0c32ad00defaa096
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294547201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2868feb8f52f8a91a0ee81ecef32dc7839fe3cb6e7da9176df844e8306a174bc`
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
# Tue, 22 Mar 2022 01:17:41 GMT
ENV JAVA_VERSION=19-ea+14
# Tue, 22 Mar 2022 01:17:54 GMT
COPY dir:09fc921b37a439732cc1ddf6087f22000a16e23f3b717bfedea6b7945d654428 in C:\openjdk-19 
# Tue, 22 Mar 2022 01:18:18 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 22 Mar 2022 01:18:19 GMT
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
	-	`sha256:5985d99dca3d61750f6475540572848645adc376c8a7fe4d9620eff321e7c71b`  
		Last Modified: Tue, 22 Mar 2022 03:26:59 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9bddbbb1c3ac049e0173b65de443f50c0cae32356451e9b604e9986b9e3b05`  
		Last Modified: Tue, 22 Mar 2022 03:30:12 GMT  
		Size: 187.8 MB (187805248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573e9d0846e12a6efeb2bbae26d9e5a824d377afae3b124c7f0aeda2033d1bd8`  
		Last Modified: Tue, 22 Mar 2022 03:27:00 GMT  
		Size: 3.6 MB (3612526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787df96d21a5f07908aa86ecc3536880a488ac125176b8721dbe1bb3eb218b6`  
		Last Modified: Tue, 22 Mar 2022 03:26:59 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
