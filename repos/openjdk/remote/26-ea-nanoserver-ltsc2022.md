## `openjdk:26-ea-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:b61e1120a50273417b040eed2b6df445caa44bb7c14669d513a5ba349aebd26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `openjdk:26-ea-nanoserver-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull openjdk@sha256:c8583556a788f13fffdd8f690951c92fff0cbb752d953839c7f9decc33e123b9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.4 MB (350396857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4469ef2681da790c41426e09746ef60325260073f1b2a940ba0604dc371b0c41`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Wed, 24 Dec 2025 06:13:47 GMT
SHELL [cmd /s /c]
# Wed, 24 Dec 2025 06:13:49 GMT
ENV JAVA_HOME=C:\openjdk-26
# Wed, 24 Dec 2025 06:13:49 GMT
USER ContainerAdministrator
# Wed, 24 Dec 2025 06:14:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 24 Dec 2025 06:14:03 GMT
USER ContainerUser
# Wed, 24 Dec 2025 06:14:04 GMT
ENV JAVA_VERSION=26-ea+29
# Wed, 24 Dec 2025 06:15:06 GMT
COPY dir:aceac1af5e514f13bd2af14bc760ceecc8137160caf73722d11683e6eac7c871 in C:\openjdk-26 
# Wed, 24 Dec 2025 06:15:13 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 24 Dec 2025 06:15:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4ee1569deb7eabb78b2e56801651a6097a302b00f949609430bcb98f46824f`  
		Last Modified: Wed, 24 Dec 2025 06:15:41 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53af183b7311a0812a250e26c6f6b214da312ee9472a2a37656b35ade6190797`  
		Last Modified: Wed, 24 Dec 2025 06:15:41 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83ebfee7f83fe3e0035fcdf564cc31f9e12312cdce7ee99ca57129798c1f056`  
		Last Modified: Wed, 24 Dec 2025 06:15:41 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8a45ab0fe91662f8f14af875f07a25786e7bb4a70b73b7e845fd07ce39d0c3`  
		Last Modified: Wed, 24 Dec 2025 06:15:41 GMT  
		Size: 85.2 KB (85172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b63d49cbb5ba7fb20fdfc75588f1ea428df313e1322a53f0f8f532bf8f754e8`  
		Last Modified: Wed, 24 Dec 2025 06:15:41 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f6d43f9bdeea462d72f88a9ee08b5ae9ad83cd7652ffb5d1fd9a11e6bb4063`  
		Last Modified: Wed, 24 Dec 2025 06:15:41 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbeca8d3852d198530987f4ea6ec0a3ab665cfcba20d1d3dc16a2b8cef06e7f`  
		Last Modified: Wed, 24 Dec 2025 06:15:52 GMT  
		Size: 223.8 MB (223835628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826ea88028342821f7948c1b6fec0185336021232469462bdc4de39d9808e8ee`  
		Last Modified: Wed, 24 Dec 2025 06:15:41 GMT  
		Size: 111.3 KB (111316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f1ca98be395bc894fe9d39653e665ed808047bd08eb7f88047884119fc82c0`  
		Last Modified: Wed, 24 Dec 2025 06:15:41 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
