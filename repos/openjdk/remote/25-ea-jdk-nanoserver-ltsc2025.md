## `openjdk:25-ea-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:d7cf14a45bf53f6a65f26f12f9e4787cca249d2c39b7f30d4cbbbb3654fec3f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `openjdk:25-ea-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull openjdk@sha256:601d70bf5f747be83a35f776652bb7d94d051e4631757e20b18fd5d0b710c816
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.0 MB (413979123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355f8734c3c75bd9128834cf07da7ac1b0f6608a21313fe260dcdefb0f7e7e9e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Mon, 17 Mar 2025 22:22:13 GMT
SHELL [cmd /s /c]
# Mon, 17 Mar 2025 22:22:14 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 17 Mar 2025 22:22:15 GMT
USER ContainerAdministrator
# Mon, 17 Mar 2025 22:22:18 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 17 Mar 2025 22:22:18 GMT
USER ContainerUser
# Mon, 17 Mar 2025 22:22:19 GMT
ENV JAVA_VERSION=25-ea+14
# Mon, 17 Mar 2025 22:22:27 GMT
COPY dir:3bbdecdaf44fd794a45fa39cf7b31efe4cc2d91c5e3e7c4c5333407317959149 in C:\openjdk-25 
# Mon, 17 Mar 2025 22:22:34 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 17 Mar 2025 22:22:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010ae974e71c7ed6ed32b3b9148a32449b4e9e025d7ee33295e7bd082f8f79e3`  
		Last Modified: Mon, 17 Mar 2025 22:22:39 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11303ce1488b9b0ac7ce4243b34267067f6a0a545dfbab43128e6aa576ff908d`  
		Last Modified: Mon, 17 Mar 2025 22:22:39 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63523ba142d168932523fc2a23dae1145b3c1e6709d3a54db5f4ea9bed14d98b`  
		Last Modified: Mon, 17 Mar 2025 22:22:39 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aca364136771e9524c8408279d4de4514fa0cfde1e0b5cbc00e778d04dfd9a1`  
		Last Modified: Mon, 17 Mar 2025 22:22:39 GMT  
		Size: 76.1 KB (76098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a78a8e6e2549ac32bae8276a7c43a8fed69851a985659ef4c0bbda471d7a917`  
		Last Modified: Mon, 17 Mar 2025 22:22:38 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f71c25076f272f3bd6008f431f9d5125320e3d8fa1572cfd74e194a3b1d98f`  
		Last Modified: Mon, 17 Mar 2025 22:22:38 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ccb08a91ea6e6944f12190b891774cada5bad79ce67bbc52ec570f381a94d2`  
		Last Modified: Mon, 17 Mar 2025 22:22:51 GMT  
		Size: 207.5 MB (207470546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1954fff5b0ba549a590d4de6007f14311a0b9b27c5eb6db7ee021a4ee22f4efe`  
		Last Modified: Mon, 17 Mar 2025 22:22:38 GMT  
		Size: 123.9 KB (123886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9d2ce3bc1bda95aeabf9b1221a3f21f99d6231221cad8e644e2659f1432457`  
		Last Modified: Mon, 17 Mar 2025 22:22:38 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
