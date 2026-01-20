## `openjdk:26-ea-30-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:d7cc2e6fffcc3d7864e456fadab958bfc0a2c6ed6c1e27ced1384c70e495fc25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `openjdk:26-ea-30-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull openjdk@sha256:dc0f1d317a5c460411fe7d12f9aaa570f73910442763fa517c5b746f46d5162b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.8 MB (350757171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0acea2c74cc1fe097dff7968d4bda178d7c0bea3b27ed3d2ef331f86517d3596`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Tue, 13 Jan 2026 23:37:24 GMT
SHELL [cmd /s /c]
# Tue, 13 Jan 2026 23:37:25 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 13 Jan 2026 23:37:25 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:37:27 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 13 Jan 2026 23:37:27 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:37:28 GMT
ENV JAVA_VERSION=26-ea+30
# Tue, 13 Jan 2026 23:38:14 GMT
COPY dir:e07e90760755fda5775e159516136ae7ac9e724b6c3d3e98906408d196af4b98 in C:\openjdk-26 
# Tue, 13 Jan 2026 23:38:22 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 13 Jan 2026 23:38:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:12:21 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98454f6897609d2c5809bd23acc5ca6982642201b45e7e63d94baee989cf1f4d`  
		Last Modified: Tue, 13 Jan 2026 23:38:51 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dbc5145bfeeaef4b75d626dd071370cddfd0de53084147b7c478b7edaf81a64`  
		Last Modified: Tue, 13 Jan 2026 23:38:51 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c38baea5a349f02799983d2d3c3a605358e950529c373bbf8ff1aae9a60f1f`  
		Last Modified: Tue, 13 Jan 2026 23:38:51 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8c739fc37583fcf99aa4fe8c71c059ed730e9bca70c5cad5193c485f019c59`  
		Last Modified: Tue, 13 Jan 2026 23:38:51 GMT  
		Size: 77.5 KB (77451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b6e12d342b4b568d88d62b97b754f1d3d33b3e963c36ea5e84221a6d4a4b73`  
		Last Modified: Tue, 13 Jan 2026 23:38:51 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1874d44f528cc41c245df4baedcfeb20ef54303b483b4e5629a614b6843b5a`  
		Last Modified: Tue, 13 Jan 2026 23:38:51 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1147ece7b75b221a2d0127342aeec49fb050d4b57dbf9053b821302b7f519d`  
		Last Modified: Tue, 13 Jan 2026 23:40:25 GMT  
		Size: 223.8 MB (223832917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6818e0838cdf47da76181d1e6b68572683eb132547bcee37b19301fea1a54fc5`  
		Last Modified: Tue, 13 Jan 2026 23:38:28 GMT  
		Size: 143.6 KB (143550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dceb016fbe8527a3268b30e87fe497fe6dd5de4967bd2d165e0d05d77313f698`  
		Last Modified: Tue, 13 Jan 2026 23:38:51 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
