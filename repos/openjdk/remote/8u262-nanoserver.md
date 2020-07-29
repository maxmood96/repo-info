## `openjdk:8u262-nanoserver`

```console
$ docker pull openjdk@sha256:a7597fbdc90e95ba1b63e9636b419db3c1209ac8e812f75cbe9cd146b386a9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `openjdk:8u262-nanoserver` - windows version 10.0.17763.1339; amd64

```console
$ docker pull openjdk@sha256:7bde18c10d7d9c8b77ec6eaf74e9b2680e3d84a9091a46ca0c98fcbec25fade0
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.1 MB (201142870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e719f8d30f2d914283759165335003f64d157ebadc3922a583924f1794fafd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 07 Jul 2020 13:50:07 GMT
RUN Apply image 1809-amd64
# Wed, 15 Jul 2020 01:54:43 GMT
SHELL [cmd /s /c]
# Wed, 15 Jul 2020 02:34:08 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 15 Jul 2020 02:34:09 GMT
USER ContainerAdministrator
# Wed, 29 Jul 2020 01:38:31 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 29 Jul 2020 01:38:32 GMT
USER ContainerUser
# Wed, 29 Jul 2020 01:38:33 GMT
ENV JAVA_VERSION=8u262
# Wed, 29 Jul 2020 01:38:59 GMT
COPY dir:bba4d92d93095aa974aa8ae4e9c21aa857106fb3a7cda2c1ce2b7787f65f8201 in C:\openjdk-8 
# Wed, 29 Jul 2020 01:39:22 GMT
RUN echo Verifying install ... 	&& echo   javac -version && javac -version 	&& echo   java -version && java -version
```

-	Layers:
	-	`sha256:dc95608099543221ef539391bfece5c1ce37b97af9da457f5990349cab028a12`  
		Size: 100.9 MB (100895619 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9f6486e4debac36806ed3527d9b1baea75c1a807e26baccdd0a2f521c814273f`  
		Last Modified: Wed, 15 Jul 2020 02:43:55 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635f616413e2ffeb2b698529474f16b802473016d0380fd29b21f12527e7006d`  
		Last Modified: Wed, 15 Jul 2020 02:54:29 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a9bf2169040f2fa44109296c3dc79cd3e81ec224a0a19ae4d74f3866e4bac3`  
		Last Modified: Wed, 15 Jul 2020 02:54:29 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12919e4a3f7690ed0c169e50a54145f9ad295248806072f541b2753c617e25c7`  
		Last Modified: Wed, 29 Jul 2020 01:55:54 GMT  
		Size: 66.4 KB (66363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a3ba49404160f0c5b7fe7e56cc630dc53340e9e3ce7327144589c193f51427`  
		Last Modified: Wed, 29 Jul 2020 01:55:53 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d958a1c92873cb903a6771ee4c7b07969f3585c9163f927bb001aa92a6bc7c6`  
		Last Modified: Wed, 29 Jul 2020 01:55:53 GMT  
		Size: 891.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120c8bad1bf9310a96fa267d8e5caf8be7b1201fbf4c496503b66188f203019d`  
		Last Modified: Wed, 29 Jul 2020 01:56:05 GMT  
		Size: 100.1 MB (100110232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ebfe9d889cb5bbdfb788cb6d1dae2f599c4f4aa37c9f8ff3bfc934b9c85afb`  
		Last Modified: Wed, 29 Jul 2020 01:55:54 GMT  
		Size: 66.2 KB (66211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
