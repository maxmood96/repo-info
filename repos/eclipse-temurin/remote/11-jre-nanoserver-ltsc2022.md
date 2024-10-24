## `eclipse-temurin:11-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:20fa4f9406ed54f3a343dd22b83bcecccc3927ede2db5dc0e5591814f5f10fba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:4c6ae90da6697f78eda1bdb2c4a88fb38ef11a03b40e29736e67971ce63808fa
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.0 MB (164984777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77c85d038f276bc46f0a7cd2c92618315c361955fc7a8cfbd9ec83b288588408`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Thu, 24 Oct 2024 01:52:51 GMT
SHELL [cmd /s /c]
# Thu, 24 Oct 2024 01:52:52 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Thu, 24 Oct 2024 01:52:52 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 24 Oct 2024 01:52:53 GMT
USER ContainerAdministrator
# Thu, 24 Oct 2024 01:53:05 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 24 Oct 2024 01:53:06 GMT
USER ContainerUser
# Thu, 24 Oct 2024 01:53:09 GMT
COPY dir:a15dacd11bbcaacf83a6b6e1490d6483ae4af68a125407fd4cb6bb7a70e4639c in C:\openjdk-11 
# Thu, 24 Oct 2024 01:53:14 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1be6268d61ae87c99d59756e3d4df28d0c9850b35dc7508ad0a377a9e500ff`  
		Last Modified: Thu, 24 Oct 2024 01:53:19 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c835aad90c3276dfeb271221a7c6c257aadd98bb3e0a9b678fee283b0fcf277`  
		Last Modified: Thu, 24 Oct 2024 01:53:19 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e3387584ffed4107e8af081754f9ecd5f8d71e97d4f3fb974723393ba62fda`  
		Last Modified: Thu, 24 Oct 2024 01:53:19 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4999cf09ae3b1c4f92c28aaeddf8231407ae1fa18808acc8b07a9233e60722`  
		Last Modified: Thu, 24 Oct 2024 01:53:17 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9872eb6e70e65b1904310fbf87269f96a112ab107f9d115f24b924bbd6c724`  
		Last Modified: Thu, 24 Oct 2024 01:53:17 GMT  
		Size: 72.6 KB (72601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f41d658b14e506caaa7f0c5441bae06c0e1f56f42fb06e309aca140f12b3919`  
		Last Modified: Thu, 24 Oct 2024 01:53:17 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5acc43a34450b3d26896ad6ba1dbd7eb59f694cf11b3caaa906662958904d824`  
		Last Modified: Thu, 24 Oct 2024 01:53:22 GMT  
		Size: 44.3 MB (44308193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9bfda603efa7292d32feea6134906997f59a29f05cf64c8fd0d53867689f25`  
		Last Modified: Thu, 24 Oct 2024 01:53:17 GMT  
		Size: 87.8 KB (87836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
