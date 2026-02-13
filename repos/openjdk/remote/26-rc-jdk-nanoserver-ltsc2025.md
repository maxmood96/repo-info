## `openjdk:26-rc-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:920d40361493c7f41122e714c8051a0e163355eae33096eb8dd0bf745499c502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `openjdk:26-rc-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull openjdk@sha256:df9a94c80fa5ec1900b22073c14c9c209c783d5d642fa5dbef2afa40544835c5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.3 MB (423319308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bfec8d7aa40ec3154ebaa02057a023a038e0942fbb3fe74b41bc7d585ddbf18`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 22:06:41 GMT
RUN Apply image 10.0.26100.32370
# Fri, 13 Feb 2026 00:18:36 GMT
SHELL [cmd /s /c]
# Fri, 13 Feb 2026 00:18:36 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 13 Feb 2026 00:18:37 GMT
USER ContainerAdministrator
# Fri, 13 Feb 2026 00:18:41 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 13 Feb 2026 00:18:42 GMT
USER ContainerUser
# Fri, 13 Feb 2026 00:18:42 GMT
ENV JAVA_VERSION=26
# Fri, 13 Feb 2026 00:18:54 GMT
COPY dir:d694f138ae93de163149df5684967cf6e6d03015ac3abc206becddb178db66e4 in C:\openjdk-26 
# Fri, 13 Feb 2026 00:18:59 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 13 Feb 2026 00:19:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:77321bd03612cfa46920e790ae0c3b142758a5803ad759fdb406c98b6f2e4ed0`  
		Last Modified: Tue, 10 Feb 2026 22:50:26 GMT  
		Size: 199.3 MB (199251619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb470eb34f65f777fd8ee09f627cd5c11bd26a26db6e87a0cabf1fe379821ab5`  
		Last Modified: Fri, 13 Feb 2026 00:19:05 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9472f47bec11fd58c6e9d2897554b2e3648b1064bb4c4ce713b5190b804ed24`  
		Last Modified: Fri, 13 Feb 2026 00:19:05 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47bd77b5c3672ced065fa28efb8a7cec4e237940f2a09c090685add72d099909`  
		Last Modified: Fri, 13 Feb 2026 00:19:05 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0ac10e7819c914cd9bdafca58bba1937f68412102e80e923f3420a5823fa1b`  
		Last Modified: Fri, 13 Feb 2026 00:19:05 GMT  
		Size: 72.1 KB (72142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c1d39a1a47d3aaf72aeb8152bdb61730444b4ae8b4c1f1bb50d92c6c5cc6e6c`  
		Last Modified: Fri, 13 Feb 2026 00:19:03 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd2c800f0bac7a1655f9dc64a43427c354875f216f9a43e37985e165c2142ea`  
		Last Modified: Fri, 13 Feb 2026 00:19:03 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e783f2f8d195cf41dbeb1d9eda95aebf1f5f68cd8dc4e610cc5ad547067a0c1`  
		Last Modified: Fri, 13 Feb 2026 00:19:19 GMT  
		Size: 223.9 MB (223876578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49f2df0767ddb65518ded8c57ee5c6795f4a612db936ffd9e5378311dea7052`  
		Last Modified: Fri, 13 Feb 2026 00:19:03 GMT  
		Size: 112.5 KB (112527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cd65051d7395ab0323e59a851c7b1eac34865ec34461469ad8b036a816f540`  
		Last Modified: Fri, 13 Feb 2026 00:19:03 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
