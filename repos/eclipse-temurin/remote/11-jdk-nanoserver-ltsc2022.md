## `eclipse-temurin:11-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:4cfeef9bd5c267bc651ddfe8cd027dc89df624b24702b555646eebeb1949220c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `eclipse-temurin:11-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:7bc5729955f05e4abb72375b65760bf76cfb1c3457b099bcc6604ff1a95fa271
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314331288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffb933a9ce2292ae798ef7dcec9d11c19097eb6e44939a88243f6e6418b55e7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Sat, 19 Oct 2024 02:13:01 GMT
SHELL [cmd /s /c]
# Sat, 19 Oct 2024 02:13:02 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Sat, 19 Oct 2024 02:13:03 GMT
ENV JAVA_HOME=C:\openjdk-11
# Sat, 19 Oct 2024 02:13:03 GMT
USER ContainerAdministrator
# Sat, 19 Oct 2024 02:13:05 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 19 Oct 2024 02:13:06 GMT
USER ContainerUser
# Sat, 19 Oct 2024 02:13:13 GMT
COPY dir:9f246ebe37fca80f181c5fdb0fda2dac7a959f1509a5d6ecc970014a33d6198a in C:\openjdk-11 
# Sat, 19 Oct 2024 02:13:18 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 19 Oct 2024 02:13:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a5f35edd970f0dbf5fc624d4d2b28c5048b2f7530d2815c851719a6e042a5c`  
		Last Modified: Sat, 19 Oct 2024 02:13:24 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42059add2677af6fb832b14e31b52bc1a516ae0032e933a2d297835157e67929`  
		Last Modified: Sat, 19 Oct 2024 02:13:24 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d920254d6a2918a7ca1874e07524b703d704704f2b9013e483d6358a9982316`  
		Last Modified: Sat, 19 Oct 2024 02:13:24 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f530171a1053ecad0e5fb27311ea8c500dd5befbb7581e3d7bf0af96dccb4f`  
		Last Modified: Sat, 19 Oct 2024 02:13:24 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44aad60d4bf3914f454c55c7e9272af8f5e09ec4584f597a8c9e512e84e9d7dc`  
		Last Modified: Sat, 19 Oct 2024 02:13:22 GMT  
		Size: 76.3 KB (76292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5458f71070ccf22ea756344f9cf2f55fd0750c61bd2ec2a3d9af9f6f1f4d3e`  
		Last Modified: Sat, 19 Oct 2024 02:13:22 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e16adb69879f22c358c35230d6647211016c3b2aff2f4924257d3342a5dac8c`  
		Last Modified: Sat, 19 Oct 2024 02:13:32 GMT  
		Size: 193.6 MB (193630343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8fe06797654718bcb15908d201d4a55b59a99f8b9376caa8db3578389c19e4`  
		Last Modified: Sat, 19 Oct 2024 02:13:22 GMT  
		Size: 107.5 KB (107481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50575522ed08f42f049c35899a8b2b5b279625cb5df14f2bbfc1ad806c5aeb44`  
		Last Modified: Sat, 19 Oct 2024 02:13:22 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
