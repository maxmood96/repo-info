## `openjdk:16-ea-11-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:ff660b8a12da6a404fe7924d7be53e8cb544f67c7aec2331bc6d51ad71c5a46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `openjdk:16-ea-11-jdk-nanoserver-1809` - windows version 10.0.17763.1397; amd64

```console
$ docker pull openjdk@sha256:e2bca3c16db40a175cbea09419391f45c8760f1fb9c907f79298d4d82e7cee2d
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.8 MB (296778018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41fbda602b610816718e2e2d00e35bba396b8f6a716529581ac9c4690b5de7a2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Aug 2020 01:28:42 GMT
RUN Apply image 1809-amd64
# Wed, 12 Aug 2020 15:28:05 GMT
SHELL [cmd /s /c]
# Wed, 12 Aug 2020 15:28:06 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 12 Aug 2020 15:28:06 GMT
USER ContainerAdministrator
# Wed, 12 Aug 2020 15:28:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 12 Aug 2020 15:28:22 GMT
USER ContainerUser
# Fri, 14 Aug 2020 21:19:04 GMT
ENV JAVA_VERSION=16-ea+11
# Fri, 14 Aug 2020 21:19:43 GMT
COPY dir:722997efe0adc41119b1256a64d17f5a912c52ff04afdf07393fa7ede34133ad in C:\openjdk-16 
# Fri, 14 Aug 2020 21:20:10 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Fri, 14 Aug 2020 21:20:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ce1c649a3e5b5b5449776d4afce631c673cade12336ccb5a38a0aac7c9d8b2bc`  
		Size: 101.0 MB (100984944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1c7c341c7a3d0c7b6e849b6faec560815682d07ce87df2e4d1e83f928aab306b`  
		Last Modified: Wed, 12 Aug 2020 16:10:21 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4ff90b84cb0e951da0f399342768862ac8c294fbe71e80d787a60d9cc2c7b5`  
		Last Modified: Wed, 12 Aug 2020 16:10:20 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f566429948e6233b746b6d219e57703486a6f2f00910b8e1842ff9920d1834e1`  
		Last Modified: Wed, 12 Aug 2020 16:10:20 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4bcc2b175dfe1adf68a872a4fa40033320f09b67b59f3dbf35cae4783189d4`  
		Last Modified: Wed, 12 Aug 2020 16:10:20 GMT  
		Size: 65.9 KB (65918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca4105c8d6a5159a2ffd6904f118076cb11506891820a04656978435fd29bad`  
		Last Modified: Wed, 12 Aug 2020 16:10:17 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731d30b22c7588cff68f32e8e5f8de5a21861cc913795d3bb17c77950db2b3c8`  
		Last Modified: Fri, 14 Aug 2020 21:32:19 GMT  
		Size: 863.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267bbeea1a81015a82c8deacc8780f3aaa72d9b8b265b9c2e524af1b7cc43b75`  
		Last Modified: Fri, 14 Aug 2020 21:32:39 GMT  
		Size: 192.2 MB (192202753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de90d114aa5f4771cf025ad74c71a9c82cdae50b17d129fca9787a298da30b3`  
		Last Modified: Fri, 14 Aug 2020 21:32:21 GMT  
		Size: 3.5 MB (3519137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db82edf589bf2a78a7d8c300cc1bb1550eea74724bbe617f44eae47a424cd7a8`  
		Last Modified: Fri, 14 Aug 2020 21:32:19 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
