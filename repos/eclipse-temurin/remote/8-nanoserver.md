## `eclipse-temurin:8-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:6d0104300bb60bdde8aca37749355c4bde69915b32e30919c54945547705942f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `eclipse-temurin:8-nanoserver` - windows version 10.0.26100.3775; amd64

```console
$ docker pull eclipse-temurin@sha256:fafbc38e6689e5edb6df3f2bb443b54d967d78e2008b4c4f6376888503fe0605
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292746098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b797dd15b560b4ccc98736d246d01a5a1b2e837e83ab7dca7b3994364a14c7d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Apr 2025 07:26:08 GMT
RUN Apply image 10.0.26100.3775
# Wed, 09 Apr 2025 01:17:46 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:17:47 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 09 Apr 2025 01:17:49 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 09 Apr 2025 01:17:50 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:17:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:17:55 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:18:03 GMT
COPY dir:bdaea23e3e57be9dfb95abf135786259c631aa0db2125cb7a86f299ac37b3921 in C:\openjdk-8 
# Wed, 09 Apr 2025 01:18:12 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:79b2ed45f890e91d23d7d22491a8fb6909c9268c668dc6a0e3b40131da02ed74`  
		Last Modified: Wed, 09 Apr 2025 00:36:30 GMT  
		Size: 190.1 MB (190113206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07fc009319f48c85cb127de3610b7a59f9b45f9d8512290eef0e8cec1525a0f3`  
		Last Modified: Wed, 09 Apr 2025 01:18:16 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdfdf016b75ab466d2219b5ab7d022b17dd5246979f93b8b050202b7af0a032`  
		Last Modified: Wed, 09 Apr 2025 01:18:16 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be9bcd4d09eb2acedf5ef13a2b7dae962d2bc56ddfa1d2ccac47bcf884edc82`  
		Last Modified: Wed, 09 Apr 2025 01:18:16 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12cc880161c0b61e1a3bfdf6aa052b959155ce28a3c01d8cb803859563710dd`  
		Last Modified: Wed, 09 Apr 2025 01:18:15 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc4b8040355ed6a1d9c3bbd169252ba241d58f9cbacebf3565ec2baf995b3b7`  
		Last Modified: Wed, 09 Apr 2025 01:18:15 GMT  
		Size: 78.8 KB (78816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d25234e63b9661c60d019da6c2c0279f7dd0263679f78f880fd4d520149a471`  
		Last Modified: Wed, 09 Apr 2025 01:18:15 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45197970a707ae43a4e27d088c8b3f3fa7d6a4cbc914f20a3a212d7f8045a4c7`  
		Last Modified: Wed, 09 Apr 2025 01:18:22 GMT  
		Size: 102.4 MB (102434201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d79cd86a2dc89700968337a2fdb8d74a5fe2636cecc0614cdd982c1f477aa0f`  
		Last Modified: Wed, 09 Apr 2025 01:18:15 GMT  
		Size: 114.6 KB (114586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-nanoserver` - windows version 10.0.20348.3453; amd64

```console
$ docker pull eclipse-temurin@sha256:5fcf12308687472d73b594179016d15fbcd7c72e50ac51053dfab47c26e1f2a2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223368813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064afc07121ef00c9af7aa7d1d43e8f9563f79fe7e28d62d09e7d63420d7ef4d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Apr 2025 22:57:50 GMT
RUN Apply image 10.0.20348.3453
# Wed, 09 Apr 2025 01:21:17 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:21:18 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 09 Apr 2025 01:21:19 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 09 Apr 2025 01:21:19 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:21:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:21:22 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:21:27 GMT
COPY dir:bdaea23e3e57be9dfb95abf135786259c631aa0db2125cb7a86f299ac37b3921 in C:\openjdk-8 
# Wed, 09 Apr 2025 01:21:32 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:5caa30147a287e99992660f7f85276c53fe3299503a06c47d476387410721453`  
		Last Modified: Wed, 09 Apr 2025 01:13:36 GMT  
		Size: 120.7 MB (120736312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9eb4128fa0aa2bcb03af9cbff4389847bc6ce3d8bfbfab7266531ba07678149`  
		Last Modified: Wed, 09 Apr 2025 01:21:36 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7a175276c636d597b35064a56fee9f4523a63ab813cb8eb5a3d0a6d82d13c3`  
		Last Modified: Wed, 09 Apr 2025 01:21:36 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e184a006828b8885edb13a6a40ce4d9898516ad514926282ad4b775e072aacb`  
		Last Modified: Wed, 09 Apr 2025 01:21:36 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03312b843f81ac39e3d52beb7064159dd017bb7f3550b43317e142c87a0af56`  
		Last Modified: Wed, 09 Apr 2025 01:21:35 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fcbdb5f2c43c657c5c19bd3f53aac8b2001ca331246eea93ecf5179d968e116`  
		Last Modified: Wed, 09 Apr 2025 01:21:35 GMT  
		Size: 77.4 KB (77410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7e5783724dae464d5e643b51b4036bf8ccd7d126b7d05cae949d6497329122`  
		Last Modified: Wed, 09 Apr 2025 01:21:35 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:622a3dd8e418525855648c1847e6ed95fdab1dd8deda4d3f76b6ad9255da2381`  
		Last Modified: Wed, 09 Apr 2025 01:21:41 GMT  
		Size: 102.4 MB (102431672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bd12743741c7e2a4e92f0e0b5222bc8938d9219f0c051319bdf9fe9a453749`  
		Last Modified: Wed, 09 Apr 2025 01:21:35 GMT  
		Size: 118.2 KB (118238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8-nanoserver` - windows version 10.0.17763.7136; amd64

```console
$ docker pull eclipse-temurin@sha256:952e30695b95afff16a5afad598765d413892c204ee55ed6d541a5f10883f43f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.5 MB (209532851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6745856c183982f9f16aaa17ca1ca79f240eff626b05a78a9c31ba3d3a7988`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Apr 2025 01:31:28 GMT
RUN Apply image 10.0.17763.7136
# Wed, 09 Apr 2025 01:17:04 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:17:05 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 09 Apr 2025 01:17:06 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 09 Apr 2025 01:17:07 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:17:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:17:10 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:17:17 GMT
COPY dir:bdaea23e3e57be9dfb95abf135786259c631aa0db2125cb7a86f299ac37b3921 in C:\openjdk-8 
# Wed, 09 Apr 2025 01:17:21 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:a06e0965a0fa3715e629889bd9332aa22aadd75654cac5c9818b67c0264b3ee1`  
		Last Modified: Tue, 08 Apr 2025 20:16:02 GMT  
		Size: 106.9 MB (106922524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a4a9cf2fc7af908b726e9ebe0ef9df28c4fe20326597b3ba269fdc98b858625`  
		Last Modified: Wed, 09 Apr 2025 01:17:25 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149d27841e1abbbbaa820d10d6543425c4c83558346120934de52632fbb7b494`  
		Last Modified: Wed, 09 Apr 2025 01:17:25 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ed874f3a5edb38d19a33a6ff360388a7953b8ee1d064bea592b4f00a5039ec`  
		Last Modified: Wed, 09 Apr 2025 01:17:24 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25df916e9c16032a143304f10f185fd2eabcd6261125e0f0f56591db8d3c28c1`  
		Last Modified: Wed, 09 Apr 2025 01:17:24 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc4146513325951684e20a940e2c9f04d64bededd8cc01f4c4e10ac5a88779f`  
		Last Modified: Wed, 09 Apr 2025 01:17:24 GMT  
		Size: 71.9 KB (71943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7abc1fff11455d5351c0ea445beddc1976b10b5948d7991a9e711ab366840d3`  
		Last Modified: Wed, 09 Apr 2025 01:17:23 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881a36420c941eccb94e2ec17f566162f1742852fcfd2640e5d0973a5eb1f5ca`  
		Last Modified: Wed, 09 Apr 2025 01:17:30 GMT  
		Size: 102.4 MB (102433306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b3272a80b37d1ab4680c99a01ae4cbb982eb4b923b7a87c7cca62fa434d5a0`  
		Last Modified: Wed, 09 Apr 2025 01:17:23 GMT  
		Size: 99.9 KB (99930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
