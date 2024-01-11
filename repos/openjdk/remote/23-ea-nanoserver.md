## `openjdk:23-ea-nanoserver`

```console
$ docker pull openjdk@sha256:60aefcca263e64ac5b4bd7d5f5eb9a1d1af52f23afacf9f647d130cb7f555f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `openjdk:23-ea-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull openjdk@sha256:56c94e7faaa243624b32780bb58bc16fcf4dba0efa5e25be87177727961c14c4
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.0 MB (305993837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20c0fe7e405f9d2371dfd6c4f2f12d9c1bc74c395f42c3c83b15a4d1eb4dab86`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:52:23 GMT
SHELL [cmd /s /c]
# Thu, 11 Jan 2024 00:52:24 GMT
ENV JAVA_HOME=C:\openjdk-23
# Thu, 11 Jan 2024 00:52:25 GMT
USER ContainerAdministrator
# Thu, 11 Jan 2024 00:52:27 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 11 Jan 2024 00:52:28 GMT
USER ContainerUser
# Thu, 11 Jan 2024 00:52:28 GMT
ENV JAVA_VERSION=23-ea+4
# Thu, 11 Jan 2024 00:52:36 GMT
COPY dir:b1dbdc77fa994774cb71fa9af312b9dd09b92bbbdd1998ea80c5705205a8768a in C:\openjdk-23 
# Thu, 11 Jan 2024 00:52:41 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 11 Jan 2024 00:52:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b393576aa40ede497d5cc8cdfb9fe8ab67c2cb984698428634bb828739e30d`  
		Last Modified: Thu, 11 Jan 2024 00:52:49 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329cfa3d3600efc862d315e0d064ab4ecd54f7bd8576f0382b1eb532764366eb`  
		Last Modified: Thu, 11 Jan 2024 00:52:48 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25827d312a94b1f42892d69adefd0fc9014d56cc44340b43c0f3040da764aaab`  
		Last Modified: Thu, 11 Jan 2024 00:52:48 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607748ae1f3bf48b82962b28023d4f5ecd1fede747b6b1a719114b7b2b61fbdb`  
		Last Modified: Thu, 11 Jan 2024 00:52:48 GMT  
		Size: 73.2 KB (73246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020f1a4c9044f91944a80d3552e86425721cded0b58f0397ff3431f5476577b2`  
		Last Modified: Thu, 11 Jan 2024 00:52:46 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c2242738af534667b6d22e931d4b5614ced58bc55d6281bc670371eaadaed1`  
		Last Modified: Thu, 11 Jan 2024 00:52:46 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1900441d14dd95ad47589e9c99ef2ca0b6c6410e10e62fb072e82d75b7eda17c`  
		Last Modified: Thu, 11 Jan 2024 00:52:58 GMT  
		Size: 197.4 MB (197424840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc9820177606a7403152a74e580f293aa9efd24be6b943e7ecc74e672a3e6d7`  
		Last Modified: Thu, 11 Jan 2024 00:52:47 GMT  
		Size: 3.9 MB (3898291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214cca88d497df4073b43d88e7aff92647427ea7ba69b811f930369fd0ed990e`  
		Last Modified: Thu, 11 Jan 2024 00:52:46 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
