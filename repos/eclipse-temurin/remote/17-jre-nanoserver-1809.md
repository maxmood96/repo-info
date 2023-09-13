## `eclipse-temurin:17-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:e60e832de05427dab92b08360433ecc92d6f1644881743212e971adf214cc7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `eclipse-temurin:17-jre-nanoserver-1809` - windows version 10.0.17763.4851; amd64

```console
$ docker pull eclipse-temurin@sha256:6b91201d463dce7af0d284ee1ab51cec203247fd56191d3faf87d5629d17522b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150998126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b14f1759f9e39fc29e53f0aa2f8077916f20c78568e75f0dd5af57d9a6c853cc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Wed, 13 Sep 2023 03:05:32 GMT
COPY dir:a0385e93ace109911eb3f9b447c778bc50121e83afa8a78ec38a5f32b2b463cb in C:\openjdk-17 
# Wed, 13 Sep 2023 03:05:51 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:57e0fc4c072431085857636a7b1f4050ade03daae580c96969f3cf06938e2fc4`  
		Last Modified: Wed, 13 Sep 2023 03:43:47 GMT  
		Size: 43.4 MB (43385316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc228632b0cf3fd2139c0d8a9eaece1996155f733a84961effe61a01a918b49`  
		Last Modified: Wed, 13 Sep 2023 03:43:39 GMT  
		Size: 3.0 MB (3044812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
