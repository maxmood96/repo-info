## `eclipse-temurin:17-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:6ba9ea00704aef6277365ddc422caf36983baf403e92fe0fe565f3efda772b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `eclipse-temurin:17-jre-nanoserver-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:1f66656b6736864c07016e2d8f17471a020c487822342b30666a6e6afcef884c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166466585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf9f3b7566f3b85b10631ad1467b008f3c8daa84e0d9765319e82e4cf7e6a19`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Wed, 23 Apr 2025 17:21:22 GMT
SHELL [cmd /s /c]
# Wed, 23 Apr 2025 17:21:22 GMT
ENV JAVA_VERSION=jdk-17.0.15+6
# Wed, 23 Apr 2025 17:21:23 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 23 Apr 2025 17:21:24 GMT
USER ContainerAdministrator
# Wed, 23 Apr 2025 17:21:27 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 23 Apr 2025 17:21:28 GMT
USER ContainerUser
# Wed, 23 Apr 2025 17:21:33 GMT
COPY dir:6f6fcea1890c098492beafa1d6f550d144651035b2d4a098a7658e545737cf82 in C:\openjdk-17 
# Wed, 23 Apr 2025 17:21:39 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842ba3953cf193e46295f9e657b20a6b72c09454521fa752839cdf4c00c8bbc3`  
		Last Modified: Fri, 09 May 2025 07:50:47 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bfe20174336a2177bc1d38e76bd1e7e3cf8cdf3436a6f7ea832e0387dbb640`  
		Last Modified: Fri, 09 May 2025 07:50:47 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc893157ad6c767725f969abdc87121efa7ef67672c8f8df53880a9e5ef0479`  
		Last Modified: Fri, 09 May 2025 07:50:47 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc28c18cbaa15aed1e5e7b8f49006472b16107cbfa522b26bc24aa8590cc2aa5`  
		Last Modified: Fri, 09 May 2025 07:50:47 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6884c8eadbed4f7940f2a54915c3ec25b79aa0d766e20f3315c4bdf1dd4d3281`  
		Last Modified: Fri, 09 May 2025 07:50:47 GMT  
		Size: 76.6 KB (76590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff06a9d3f3172b1b5b1bca019e3e717650d87bc8bb466a0ff0dde7b693ead37`  
		Last Modified: Fri, 09 May 2025 07:50:48 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3ac00c80a20cdfc7f3e0afe764b67aa6d666245b638ac1686790717397669b`  
		Last Modified: Wed, 23 Apr 2025 17:21:46 GMT  
		Size: 43.7 MB (43736900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3ec9a785a29dfac332dd3c4815f7a5a0ff299946bb0e0ed7249b661f62ff4f`  
		Last Modified: Fri, 09 May 2025 07:50:48 GMT  
		Size: 108.7 KB (108724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
