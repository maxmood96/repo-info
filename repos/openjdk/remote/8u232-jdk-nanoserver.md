## `openjdk:8u232-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:061fadfe6bc95299726932e449173d1d81475f5a4f617841adeb79096dfc9a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `openjdk:8u232-jdk-nanoserver` - windows version 10.0.17763.973; amd64

```console
$ docker pull openjdk@sha256:79b955f773599345bf42ec1a2af0a3823e7bb2f04775421b0da6feb283df9f88
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.6 MB (200619192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7179171b6d027588bb9f00bde06f32ee0574b7c8a5502e7ac36956a89f4c5ac2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 04 Jan 2020 07:17:17 GMT
RUN Apply image 1809-amd64
# Tue, 14 Jan 2020 23:56:11 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2020 01:37:11 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 15 Jan 2020 01:37:12 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2020 01:37:25 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 15 Jan 2020 01:37:26 GMT
USER ContainerUser
# Wed, 15 Jan 2020 01:37:27 GMT
ENV JAVA_VERSION=8u232
# Wed, 15 Jan 2020 01:38:18 GMT
COPY dir:423f1b6bc7bd2d846b13aab5eb2a97e2d8834390209ac9e4daad889695778323 in C:\openjdk-8 
# Wed, 15 Jan 2020 01:38:37 GMT
RUN echo Verifying install ... 	&& echo   javac -version && javac -version 	&& echo   java -version && java -version
```

-	Layers:
	-	`sha256:ee446884f7bef76f8275c2f16add1c4fb598bea2ba861e72bce8fb4aac9b55ef`  
		Size: 101.1 MB (101054324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:764e25aa4e95684bd69a4d130dc1c729bfaef95293d9c76c4d2a12ced9e3a9ac`  
		Last Modified: Wed, 15 Jan 2020 01:51:06 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b207e8571875b5c57f6bec51eea1e0fc14627b12fe76121e7a220c2870ec6c`  
		Last Modified: Wed, 15 Jan 2020 02:16:26 GMT  
		Size: 919.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb4e324b3232465d20aa50722eb8ddd36076bba06d7903391ea8b65d41fc3d1`  
		Last Modified: Wed, 15 Jan 2020 02:16:25 GMT  
		Size: 930.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb46126f2f094e1347e791f19d060913b307a75f7732fe94aeabf500c9ef057a`  
		Last Modified: Wed, 15 Jan 2020 02:16:24 GMT  
		Size: 72.1 KB (72068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0327ebcd1fd4b5d11809f5351b664cd79050fa966f08e3777e8b25082e3036`  
		Last Modified: Wed, 15 Jan 2020 02:16:23 GMT  
		Size: 936.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae264c9cdfce3393d4308e927d928aa21ad2995f63b1afa24b07c1a23089bd8`  
		Last Modified: Wed, 15 Jan 2020 02:16:23 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa2efed451ac93d37f65a7fc20bdf5e7fd384e4137dfb97e8d70500d1f8fa56`  
		Last Modified: Wed, 15 Jan 2020 02:18:03 GMT  
		Size: 99.4 MB (99436545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11d682beb16e3b2ab7750b65dace6c1446234ad5901404fab8803536cd035c0`  
		Last Modified: Wed, 15 Jan 2020 02:16:23 GMT  
		Size: 51.6 KB (51599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
