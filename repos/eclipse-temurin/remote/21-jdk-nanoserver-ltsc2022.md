## `eclipse-temurin:21-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:aaf4c50ec12789df5f37aae62611a8bb5d6db9e22463554ad66dc02f077e210b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `eclipse-temurin:21-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:af6fcb322380fc8557dc8cd915ca97abe04b214b18147848ff29b82fcb7fef68
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.3 MB (323255097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05bc099b2820ea3000d57f2119a016a048de3dcc447064ffb38ec8b48051e05d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Thu, 24 Oct 2024 01:52:51 GMT
SHELL [cmd /s /c]
# Thu, 24 Oct 2024 01:52:51 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Thu, 24 Oct 2024 01:52:52 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 24 Oct 2024 01:52:53 GMT
USER ContainerAdministrator
# Thu, 24 Oct 2024 01:53:05 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 24 Oct 2024 01:53:06 GMT
USER ContainerUser
# Thu, 24 Oct 2024 01:53:14 GMT
COPY dir:cc909cc6d9328a16dd1468618a073abc368d41e200a32534756819e3433a0b04 in C:\openjdk-21 
# Thu, 24 Oct 2024 01:53:19 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 24 Oct 2024 01:53:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab6983d85d5ea82e0f3f95a6fb89ec05dcea3e0480946795c60f76949024b9d`  
		Last Modified: Thu, 24 Oct 2024 01:53:26 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20830494b10e35d7612dcdd0657cf0b3cc03d5d57e256964268e2ba92f64fa67`  
		Last Modified: Thu, 24 Oct 2024 01:53:26 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1c79963351d8d886970a5c50bd7a19243fbe34198fdbb321751bf837473050`  
		Last Modified: Thu, 24 Oct 2024 01:53:26 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174534683c421f0dfbd426778dae85f094a9d20eff07f5c059fc3845a5aa72f8`  
		Last Modified: Thu, 24 Oct 2024 01:53:26 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f8c84a2ab49bec260ca6f0b60ef60f5113b61abddcecf55570db7c08beca40`  
		Last Modified: Thu, 24 Oct 2024 01:53:24 GMT  
		Size: 73.1 KB (73124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7fab5dee104872c358c88a56736cd301b03ff4241b2413ad8acc820faab63d`  
		Last Modified: Thu, 24 Oct 2024 01:53:24 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:836530ca906d0804aefa42da4e3123e592b85eb0fb12a777dd5166469f0f0857`  
		Last Modified: Thu, 24 Oct 2024 01:53:35 GMT  
		Size: 202.6 MB (202576126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2438b34b7bff2a34faeed61604914e761824e255c9478849b7ced60f61779de1`  
		Last Modified: Thu, 24 Oct 2024 01:53:24 GMT  
		Size: 88.5 KB (88513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42179192d764910b44acf271742f54c8ad65a63e965b3c9df3ebb988b51d8d7b`  
		Last Modified: Thu, 24 Oct 2024 01:53:24 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
