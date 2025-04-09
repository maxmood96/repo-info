## `eclipse-temurin:8u442-b06-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:ba3d0e13de7aeef4fcefcee32ef36baf9333326e61121f996809f42b642f8847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `eclipse-temurin:8u442-b06-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3453; amd64

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
