## `eclipse-temurin:17-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:eec964b2108a37b4d8f2eb2530018d7131a74fe3c1216a117b163372439ce8ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `eclipse-temurin:17-nanoserver-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull eclipse-temurin@sha256:cc3f10b9d090495ef9fba8debb657df8992cd01de56e5e23f52ee1f3a81f3041
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.9 MB (378910849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d112168e6c27a6f2659963aa1ef26a8b9a811d2ee59e14b3a2314da057bc3f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 10 May 2025 00:58:48 GMT
RUN Apply image 10.0.26100.4061
# Wed, 14 May 2025 21:14:00 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 21:14:02 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 14 May 2025 21:14:04 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 14 May 2025 21:14:05 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:14:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 14 May 2025 21:14:11 GMT
USER ContainerUser
# Wed, 14 May 2025 21:14:20 GMT
COPY dir:642284f27aa03ba1e21a689edd99e2d493ba3e3290e848ff1bdf623fc783a5e1 in C:\openjdk-17 
# Wed, 14 May 2025 21:14:29 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 14 May 2025 21:14:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9824510349be04d2eb26f9aaba1d016eddcbed10bdcd6681f4636c948766f3d1`  
		Last Modified: Thu, 15 May 2025 20:15:30 GMT  
		Size: 191.4 MB (191412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d6b9a96e5ff7cc0cf5b965e710a2c82df56be17a5dc508db8dd1d1bd6d38e9`  
		Last Modified: Fri, 16 May 2025 17:06:28 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0d044b65fab6b1efc0f6f0d8f58f8b765d70f50ae8e65182b8c456d5acea2d`  
		Last Modified: Fri, 16 May 2025 17:06:28 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc659115d4b46d8c49d5c3e0ad86c424ec3b7462753cbf8b5a7856fbd596cb1`  
		Last Modified: Fri, 16 May 2025 17:06:29 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98d18067d3bac9f8c29ba7847697208cdcc925fce4475a5206c653e42f784a4`  
		Last Modified: Fri, 16 May 2025 17:06:28 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79dc294f09b66f0e7c4d0d161159a76381ec6d28769a39885a6291c27a3e351`  
		Last Modified: Fri, 16 May 2025 17:06:28 GMT  
		Size: 77.9 KB (77917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49caae00fd568c3b4738ee75c61b23666f3265ae3cfa7caa85b82594c2e92f07`  
		Last Modified: Fri, 16 May 2025 17:06:28 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d318d339a5f098692f576fbe37cb646baef072ef05ea962809645e914ac14c46`  
		Last Modified: Sun, 18 May 2025 20:20:24 GMT  
		Size: 187.3 MB (187310232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b843262cb961ccdad232f7f858b78601e87e0719b7d616ec3b9358fb51af1e93`  
		Last Modified: Fri, 16 May 2025 17:06:28 GMT  
		Size: 104.4 KB (104444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524e56621313becf168498234dfa18d36e46c83dfab902ea14dedd90c553c3ed`  
		Last Modified: Fri, 16 May 2025 17:06:28 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
