## `eclipse-temurin:11-jdk-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:df48df624a672a5d1621438333f0a381f50284b37d16ec961398fae562ba9b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `eclipse-temurin:11-jdk-nanoserver-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull eclipse-temurin@sha256:f5dfc975fd2433073becbc9427f88b5756431c710f6a121b87fcdd2e9da74854
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.1 MB (299132824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f79fd1705c45b8bbb9934cd9f6102d6248745a0370da177aeb12d240ab17d9ad`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Tue, 09 Apr 2024 23:42:55 GMT
SHELL [cmd /s /c]
# Wed, 24 Apr 2024 18:41:40 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Wed, 24 Apr 2024 18:41:41 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 24 Apr 2024 18:41:41 GMT
USER ContainerAdministrator
# Wed, 24 Apr 2024 18:41:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 24 Apr 2024 18:41:52 GMT
USER ContainerUser
# Wed, 24 Apr 2024 18:42:09 GMT
COPY dir:8aa740e08efd9dadfa2fb1fd54d653720c8e2097106a2d2f0f8f1f0b127bcc3e in C:\openjdk-11 
# Wed, 24 Apr 2024 18:42:24 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Apr 2024 18:42:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b591b5f81c02344da39dc8a9084b5791cbf552c1eb85e79db1f38dfc715a681`  
		Last Modified: Wed, 10 Apr 2024 00:47:46 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73dd9de1f4ee2da0931c1efc7e007a79d522de315970bd4907f8c25164b4031`  
		Last Modified: Wed, 24 Apr 2024 19:36:04 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e7f2c5227d7bceac1a1244abe9f29e1b98f10b958eb2e11d13368d8d4a1015`  
		Last Modified: Wed, 24 Apr 2024 19:36:04 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc4b0d14ed0bfa53e3fc8ed4b1fcd11a8044f1787b20c50741d17b5f8b62ca8`  
		Last Modified: Wed, 24 Apr 2024 19:36:04 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8591bed2b34e6566a4509056ef1b7ce711037fd180b7805c456d83705454a6`  
		Last Modified: Wed, 24 Apr 2024 19:36:02 GMT  
		Size: 66.9 KB (66856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5127635c315d87e10a1285051f1aac1cb26539824ae9224bcb54a542a1e1faa`  
		Last Modified: Wed, 24 Apr 2024 19:36:02 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6e0670c91bff7268ee61dd4cc4f8bc88a79a8cb7b8b10d095f8b445eb10eb3`  
		Last Modified: Wed, 24 Apr 2024 19:36:20 GMT  
		Size: 194.1 MB (194084434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e577d90cbcf65ce6e9f87955d46e7c08cc81c277e126f9618ebb49c1fd2d70`  
		Last Modified: Wed, 24 Apr 2024 19:36:02 GMT  
		Size: 85.5 KB (85477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9eb4157d4521d11f623e392ef3498109d9504a5c4b5039910f2d4d9f1741ee6`  
		Last Modified: Wed, 24 Apr 2024 19:36:02 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
