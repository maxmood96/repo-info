## `openjdk:26-ea-nanoserver`

```console
$ docker pull openjdk@sha256:21a32b770ba4fc590b81cb9abbf806a56e071825006448650567e66f028188a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `openjdk:26-ea-nanoserver` - windows version 10.0.26100.7462; amd64

```console
$ docker pull openjdk@sha256:89104e5c918571ecfdc84636f6a08aa74d2521dda4317ffc9e3c24f8585e1a0c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.9 MB (422866476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c694535ff4ecc9a9c51dd6094672310ad3687a0c8d60c8e75ebc6a4a2518186`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Dec 2025 21:31:34 GMT
RUN Apply image 10.0.26100.7462
# Mon, 12 Jan 2026 21:12:46 GMT
SHELL [cmd /s /c]
# Mon, 12 Jan 2026 21:12:47 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 12 Jan 2026 21:12:48 GMT
USER ContainerAdministrator
# Mon, 12 Jan 2026 21:12:58 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 12 Jan 2026 21:12:58 GMT
USER ContainerUser
# Mon, 12 Jan 2026 21:12:58 GMT
ENV JAVA_VERSION=26-ea+30
# Mon, 12 Jan 2026 21:13:31 GMT
COPY dir:e07e90760755fda5775e159516136ae7ac9e724b6c3d3e98906408d196af4b98 in C:\openjdk-26 
# Mon, 12 Jan 2026 21:13:38 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 12 Jan 2026 21:13:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a092205b76ca656d8483e99445def9f0619cb3acb2688bf9a33244c43ad44ce`  
		Last Modified: Tue, 09 Dec 2025 22:15:12 GMT  
		Size: 198.9 MB (198873947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae0c30a24f290070e5783e9d1fe48a8f8ae05edd00cbb7a4d624c8138a5784a`  
		Last Modified: Mon, 12 Jan 2026 21:14:09 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6929d53888fd0885e8f79ba669ae179ba97eff97f3ae6f1110b59283e8a9ebad`  
		Last Modified: Mon, 12 Jan 2026 21:14:09 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f867fe111396f35b4b29e0306dd656f46cba10e0072a9e0a71dfeca78539b17`  
		Last Modified: Mon, 12 Jan 2026 21:14:09 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee7bec712c6daf76a8f37d627869fd5717e49d853e5fdc8cee04f1d8fe97d63`  
		Last Modified: Mon, 12 Jan 2026 21:14:11 GMT  
		Size: 70.5 KB (70494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4ae485a4d736b9d8e5f09fa047d9124472a0c6a90fa8ea2125b8370c1b26b5`  
		Last Modified: Mon, 12 Jan 2026 21:14:09 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034ea90897a477675ff72bebc78d94808b1abddf0fef825e8d69f5685cbf4a40`  
		Last Modified: Mon, 12 Jan 2026 21:14:09 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829b62a32d4c5a3ed4c491787614d94dba57d8b6e0f5ad4d5e0a2965fcf44fa8`  
		Last Modified: Mon, 12 Jan 2026 21:15:17 GMT  
		Size: 223.8 MB (223832538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d63b3b82f9988fd81169c24a038088b7024252d676a61e9dbc5fe7274b0583`  
		Last Modified: Mon, 12 Jan 2026 21:14:09 GMT  
		Size: 83.1 KB (83096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6483a1c453db343ebddaba204e22ed604a12c4d0e8ac149f2e60611a9e64ca`  
		Last Modified: Mon, 12 Jan 2026 21:14:09 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-nanoserver` - windows version 10.0.20348.4529; amd64

```console
$ docker pull openjdk@sha256:f120b801be4a61850dfa37845fad34748476256d08239a099389360ec023594c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.4 MB (350402581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cbb256422cfdf5ac1d26b0d586fafceead3a28e35f76d8711fa770714e91897`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Dec 2025 18:00:04 GMT
RUN Apply image 10.0.20348.4529
# Mon, 12 Jan 2026 21:36:06 GMT
SHELL [cmd /s /c]
# Mon, 12 Jan 2026 21:36:08 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 12 Jan 2026 21:36:09 GMT
USER ContainerAdministrator
# Mon, 12 Jan 2026 21:36:23 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 12 Jan 2026 21:36:23 GMT
USER ContainerUser
# Mon, 12 Jan 2026 21:36:24 GMT
ENV JAVA_VERSION=26-ea+30
# Mon, 12 Jan 2026 21:37:27 GMT
COPY dir:e07e90760755fda5775e159516136ae7ac9e724b6c3d3e98906408d196af4b98 in C:\openjdk-26 
# Mon, 12 Jan 2026 21:37:36 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 12 Jan 2026 21:37:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ea9d570ff70f4580675afb6f622bfb47ce08fdd6d018d58c20d1f3539bd2ada`  
		Last Modified: Tue, 09 Dec 2025 22:32:21 GMT  
		Size: 126.4 MB (126358310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b3f59c2a2a510228fd4f8632a9f997a8da7163939246e89711c940e6054c8b`  
		Last Modified: Mon, 12 Jan 2026 21:38:08 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2077698b91079f1c136b3baccb5751c73e0c6e8940f26c3a2dd3757db1fc9fcb`  
		Last Modified: Mon, 12 Jan 2026 21:38:08 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff38e3c650075d7999cfd6022cfad8c8b8b41df69c9001d053d0d3a6ac7a8b1`  
		Last Modified: Mon, 12 Jan 2026 21:38:10 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa5a117d6815a1e4c8791b2cbe1867b1d2517df12d699c81bef049b5443acf6`  
		Last Modified: Mon, 12 Jan 2026 21:38:08 GMT  
		Size: 71.1 KB (71095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35df635b1056acf1a1e4c16f7eafe00bbb02478a0e7e426868ec3c64a459951c`  
		Last Modified: Mon, 12 Jan 2026 21:38:09 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f6ab9b3e39dae853f4310890b927adb83ef85674aff5b7a66ad9fc978f61ed`  
		Last Modified: Mon, 12 Jan 2026 21:38:08 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7883a53ddc0ccdf6fea5c0f22236738a7735ce79636942668d4ecea34d8378ed`  
		Last Modified: Mon, 12 Jan 2026 21:39:38 GMT  
		Size: 223.8 MB (223832878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82ee099a382de562e21bf7bc8ceeec27094ecbc56c3c910b0f4f838c8027810`  
		Last Modified: Mon, 12 Jan 2026 21:38:08 GMT  
		Size: 133.8 KB (133846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677964cdad8e8e71adc24ec0c10a7c05dce21a626830499eb7c67797945a9872`  
		Last Modified: Mon, 12 Jan 2026 21:38:08 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
