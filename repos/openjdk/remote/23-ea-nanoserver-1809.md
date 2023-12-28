## `openjdk:23-ea-nanoserver-1809`

```console
$ docker pull openjdk@sha256:bfb732fa571ac4770da6094c71145c53782186e3311ab3fe085ec47127195c47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5206; amd64

### `openjdk:23-ea-nanoserver-1809` - windows version 10.0.17763.5206; amd64

```console
$ docker pull openjdk@sha256:94da3cdceee33ecd98d5be7ac63ebdeae86b55f97d55ea0ac1770715dceb242c
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.8 MB (305835301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80300598b458fb46c4be5145101d7841bcd25f4bbf9cf99898e8ccea6a8f1e86`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Dec 2023 10:54:04 GMT
RUN Apply image 10.0.17763.5206
# Thu, 28 Dec 2023 02:50:03 GMT
SHELL [cmd /s /c]
# Thu, 28 Dec 2023 02:50:04 GMT
ENV JAVA_HOME=C:\openjdk-23
# Thu, 28 Dec 2023 02:50:05 GMT
USER ContainerAdministrator
# Thu, 28 Dec 2023 02:50:18 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 28 Dec 2023 02:50:19 GMT
USER ContainerUser
# Thu, 28 Dec 2023 02:50:19 GMT
ENV JAVA_VERSION=23-ea+3
# Thu, 28 Dec 2023 02:50:29 GMT
COPY dir:37394bbcd2615f0c554fabbb20d661cbccb2f0a255d9c7ec71329b2f03204f32 in C:\openjdk-23 
# Thu, 28 Dec 2023 02:50:35 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 28 Dec 2023 02:50:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:424f13a93a185a5defe848e7d270655e05233555f51328c0af24b9e70677d037`  
		Last Modified: Tue, 12 Dec 2023 20:02:40 GMT  
		Size: 104.5 MB (104510104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2066ee41b3b8819509896643efc9cfdc778a0ba846b58202de419743029deb67`  
		Last Modified: Thu, 28 Dec 2023 02:50:43 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4baed411cb824b649583af1aa81d49456f67e20668122f1ec9c6548312a2d822`  
		Last Modified: Thu, 28 Dec 2023 02:50:42 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff550e9df43ad6007a13f9d8bebffabd637445548bad26b29bbfef5d3793737a`  
		Last Modified: Thu, 28 Dec 2023 02:50:42 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a11ddf1527c97e82283656740f6d51ab086ac5ae37b98b235a7153a81fed5c6`  
		Last Modified: Thu, 28 Dec 2023 02:50:42 GMT  
		Size: 66.5 KB (66527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691aa33f2af74a28e5ad7588b6c06fef05ab812abf3004baa895d2d67af86d5d`  
		Last Modified: Thu, 28 Dec 2023 02:50:40 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd957e4ebe6461fe01f6ce2b9a3a4967779286f7fd7de84544819641b0389469`  
		Last Modified: Thu, 28 Dec 2023 02:50:40 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d27628516639bb1ee64e0d890bc1fe3a8232d87ebbf89c18acbeaf6756f7441`  
		Last Modified: Thu, 28 Dec 2023 02:50:51 GMT  
		Size: 197.4 MB (197421296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a62d71a5378a32a88de7503ad4faa65f35b6a4d7f73fea85a6cc5574cc35d6`  
		Last Modified: Thu, 28 Dec 2023 02:50:41 GMT  
		Size: 3.8 MB (3831079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c41cd4d216cc36ed427eaa2488b9b91c98602dcb553775e8692f0ee8dfc8a5d`  
		Last Modified: Thu, 28 Dec 2023 02:50:40 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
