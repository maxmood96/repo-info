## `openjdk:24-ea-27-nanoserver-1809`

```console
$ docker pull openjdk@sha256:806400f5ca980670c94588ea93ef2e4c2b44f29d78623dcfe35bc146a34e5afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `openjdk:24-ea-27-nanoserver-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull openjdk@sha256:c8e4e721c106f7e1bb0fd0385b1aa93b2676f4ae83e2178304ac523dc29ae865
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.1 MB (368095789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15fb2d077240c0b6f109a04a8ab613e2d09be3cc74ac731f804b3915645461b2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Tue, 10 Dec 2024 00:08:52 GMT
SHELL [cmd /s /c]
# Tue, 10 Dec 2024 00:08:53 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 10 Dec 2024 00:08:54 GMT
USER ContainerAdministrator
# Tue, 10 Dec 2024 00:09:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 10 Dec 2024 00:09:10 GMT
USER ContainerUser
# Tue, 10 Dec 2024 00:09:10 GMT
ENV JAVA_VERSION=24-ea+27
# Tue, 10 Dec 2024 00:09:21 GMT
COPY dir:742091ed6dd70bfaf8aa0c105e548ba4349e24f3ab2840414b5a569350576e65 in C:\openjdk-24 
# Tue, 10 Dec 2024 00:09:27 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 10 Dec 2024 00:09:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4b7697a1da682cc10f04d72f83a97c53b01cf1d0d8dbd3c955428856124992`  
		Last Modified: Tue, 10 Dec 2024 00:09:34 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd771578072ce11d12735517cdf31071f592717a857d43158847ff912daae38`  
		Last Modified: Tue, 10 Dec 2024 00:09:33 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206bd1aefa3d0df202b076cf45a8b6c0b476f5c5d4f4b360b1891c6c0bdbecc2`  
		Last Modified: Tue, 10 Dec 2024 00:09:33 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87708cd9624080b60673a4d03a3359479cfd5c00f23683b3735e14b9fd768d32`  
		Last Modified: Tue, 10 Dec 2024 00:09:33 GMT  
		Size: 67.0 KB (66958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b154b1ad8a6e8110a862c2a8c0ac052643c03355b4f60278ab9103693d32b5`  
		Last Modified: Tue, 10 Dec 2024 00:09:32 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9ce759a33780cc07d9b43936c65df06e60bc245742a79bf729b32746ca01c3`  
		Last Modified: Tue, 10 Dec 2024 00:09:32 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4df2f71994dfdc5b6a102bfa9ab03206b00cf93db8607f60eca139bee1c955`  
		Last Modified: Tue, 10 Dec 2024 00:09:43 GMT  
		Size: 208.4 MB (208436016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d1fe692cb009e035ef1ef1205e5c2d44c0a7fcfad22125c3b70c229f44926c`  
		Last Modified: Tue, 10 Dec 2024 00:09:32 GMT  
		Size: 4.4 MB (4372235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac8407ca8f60b5600c43cd75a241a4c40dad00f66a5d322e0e60e713f8edf1e`  
		Last Modified: Tue, 10 Dec 2024 00:09:32 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
