## `eclipse-temurin:25-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:e1a5bde94c373a7f449d7780ed62f7233c3263c99f69d0016a0c75e826ec6039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:25-jre-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:670e2f1d38f524faa958cb4ea191603d93d71019312aea6663f527c89ccdcb56
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.5 MB (185460788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de6950bd0546be8f038da7fa6912b125534cd9a4830d276a60ada95b0624ade`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Thu, 05 Feb 2026 22:39:17 GMT
SHELL [cmd /s /c]
# Thu, 05 Feb 2026 22:40:19 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:40:19 GMT
ENV JAVA_HOME=C:\openjdk-25
# Thu, 05 Feb 2026 22:40:20 GMT
USER ContainerAdministrator
# Thu, 05 Feb 2026 22:40:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 05 Feb 2026 22:40:22 GMT
USER ContainerUser
# Thu, 05 Feb 2026 22:40:30 GMT
COPY dir:15db28d5461f0a5f42074eb42e42a8535b9576d6847f4e637cb0dcfe9abfaabd in C:\openjdk-25 
# Thu, 05 Feb 2026 22:40:34 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81eeb53037f4a6db66b71a97aead342992cc6906094403bd195c8563fb7f71a4`  
		Last Modified: Thu, 05 Feb 2026 22:39:51 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f9c0fe3e290675e39e4f472f37c8dc3ca9dc46b849b30d640ce726600db489`  
		Last Modified: Thu, 05 Feb 2026 22:40:39 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b7f9b07e0e888518997242d4d3395b9b441c357d94bec123d2950a8effe170`  
		Last Modified: Thu, 05 Feb 2026 22:40:39 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a45c142afbda79236ab49491a98289e19d913b81e84985110f1dc4e0d711f6`  
		Last Modified: Thu, 05 Feb 2026 22:40:38 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab5bf67986acdf30a41e00b257f914bd32d2c13c694bebdd79047999bb42056`  
		Last Modified: Thu, 05 Feb 2026 22:40:38 GMT  
		Size: 76.5 KB (76503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603a96ead04de1f3a21d63f1da39d8cdae827937ae049a22991dd8e9f9080699`  
		Last Modified: Thu, 05 Feb 2026 22:40:38 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a612e5c94ee71a86b3d7873e0b6d3447e7fd28313954ab9dc7236f764774ca54`  
		Last Modified: Thu, 05 Feb 2026 22:40:45 GMT  
		Size: 58.6 MB (58582891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa9820d1cd6a9b18f5185aad327ae7d258de34cb8bce647db9a0902d9cf7f76`  
		Last Modified: Thu, 05 Feb 2026 22:40:38 GMT  
		Size: 99.3 KB (99261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
