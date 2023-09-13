## `eclipse-temurin:17-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:c4cd61dc48ecf98eea6f6941007bfbec4395929e30824993d2395d7a2f5c7363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `eclipse-temurin:17-nanoserver-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull eclipse-temurin@sha256:63c61ef27397718a0f0ea642110753ee1d78a163b7b6f0dd6634266a42bf5cde
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.0 MB (293969551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1eda4c426dd69b3c6038463aee76b1b4a4e0379abb4e0e4ba97c9805bc21864`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 02:29:44 GMT
SHELL [cmd /s /c]
# Wed, 13 Sep 2023 02:59:25 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Wed, 13 Sep 2023 02:59:26 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 13 Sep 2023 02:59:26 GMT
USER ContainerAdministrator
# Wed, 13 Sep 2023 02:59:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 Sep 2023 02:59:39 GMT
USER ContainerUser
# Wed, 13 Sep 2023 02:59:54 GMT
COPY dir:87d4868aeffb4665dc24a8514128e3f1a9351c7c90320c533fd29622fc9de6e2 in C:\openjdk-17 
# Wed, 13 Sep 2023 03:00:10 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 13 Sep 2023 03:00:11 GMT
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
	-	`sha256:46866e88a2e2203e2c828c7515efa3bcfff5ed97bc0b8ccca47b02e26762e9b2`  
		Last Modified: Wed, 13 Sep 2023 03:42:24 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3aeefc47e52f23903eb84c46ec6583cca206032acfda8978535aa5a8b794c9`  
		Last Modified: Wed, 13 Sep 2023 03:42:23 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c056dbd4fb6cae767c9dadf26bfae407d7f187c470f06a8ea3141feb8c69c2`  
		Last Modified: Wed, 13 Sep 2023 03:42:23 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b13f7c7c8506492d6fb503feac3189e00aa3646261acc986d39c00dc6fa8dcb6`  
		Last Modified: Wed, 13 Sep 2023 03:42:21 GMT  
		Size: 69.7 KB (69703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89d7acd9a610e48784f4d8d8b42c43cbde1464cb26be36c38c17cd8fecf2f7d`  
		Last Modified: Wed, 13 Sep 2023 03:42:21 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b688c6ee5555fa18081c50e93a5484539715d1043c60f94d0c91cdbae66e6b8f`  
		Last Modified: Wed, 13 Sep 2023 03:42:43 GMT  
		Size: 185.7 MB (185726127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7bb7f3a6dda5937330c7385b6550809f2ded47bfe616f48620241b873edcb48`  
		Last Modified: Wed, 13 Sep 2023 03:42:23 GMT  
		Size: 3.7 MB (3674262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc72fc32b9d8d184929f4e6d0c7b4891aeb6d5b7ec205bc82abe9a9986e32f6`  
		Last Modified: Wed, 13 Sep 2023 03:42:22 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
