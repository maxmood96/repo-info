## `eclipse-temurin:20-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:b0980aba5a3cf26d1bdcfd04266fe03be03d1d9842843a3f90f360ffd5dfc004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `eclipse-temurin:20-jdk-nanoserver-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull eclipse-temurin@sha256:e53b5e04488c0d8c3981af8573365b56c4c3896a921f5b474c51498baf64c027
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303819952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5a62fb33b773d57f4d9913a2f56a22ea876fe912282de027fb36b2e678d4d3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 02:29:44 GMT
SHELL [cmd /s /c]
# Wed, 13 Sep 2023 03:11:56 GMT
ENV JAVA_VERSION=jdk-20.0.2+9
# Wed, 13 Sep 2023 03:11:57 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 13 Sep 2023 03:11:58 GMT
USER ContainerAdministrator
# Wed, 13 Sep 2023 03:12:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Sep 2023 03:12:10 GMT
USER ContainerUser
# Wed, 13 Sep 2023 03:12:25 GMT
COPY dir:4ed074865171ba014f3c2f68f57ad2bb21a4dd6e4cf7ff9654ee6c4c6e5176c0 in C:\openjdk-20 
# Wed, 13 Sep 2023 03:12:42 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 Sep 2023 03:12:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a5bcbc9b0f0398bf8f14c235b24ba85d9acacf855518119cd1ce338a235a15`  
		Last Modified: Wed, 13 Sep 2023 03:36:33 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e8f8b6a865f909378039e86ae667b406118a25b3a153bfc989219634e11931`  
		Last Modified: Wed, 13 Sep 2023 03:45:27 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a9140c6a0cfd95053c573337fe186e7c914e2cddc4ded5396d633f8168d811`  
		Last Modified: Wed, 13 Sep 2023 03:45:27 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ad06a8f04950c85d8c4f1f0bf2976f8279ad5bddaa2eeb25ac627a5322ee4f`  
		Last Modified: Wed, 13 Sep 2023 03:45:27 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d27824264e82d62f11110ce00b426e3404ff58b09ac8981602874b9d0f4518a`  
		Last Modified: Wed, 13 Sep 2023 03:45:25 GMT  
		Size: 68.8 KB (68806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03cb3c15586ae832292360f56f1ac78eaf96af2d83bcb41622737199018f5d2`  
		Last Modified: Wed, 13 Sep 2023 03:45:25 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d644afcd2e63d379fd16cf7a9b319e78f9b27f9aa0b6602b6a5d2892a90674d`  
		Last Modified: Wed, 13 Sep 2023 03:45:48 GMT  
		Size: 195.5 MB (195461576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924647b3486ebb2a95e164b84a6afe90a8ad6594b4f5d12438d658b56253d834`  
		Last Modified: Wed, 13 Sep 2023 03:45:26 GMT  
		Size: 3.8 MB (3790191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49d2cd495f776642bdc3ef9e3ce4d400e4a5c005477d03075a38ba748dcadda`  
		Last Modified: Wed, 13 Sep 2023 03:45:25 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
