## `eclipse-temurin:8u432-b06-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:91f78718ce6d491c5e22d22e2d8283d1f46a4094267c8acc9eab8e2a037d4491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `eclipse-temurin:8u432-b06-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:f0c753696731e2e14168b410e5169d6bfaa42690ac773398e4e59253dccc243c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224123763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce9a581a68764c06b79529da7b3b62701e4bdbd6f264cb837b35c4780b467ff`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Thu, 24 Oct 2024 01:52:42 GMT
SHELL [cmd /s /c]
# Thu, 24 Oct 2024 01:52:42 GMT
ENV JAVA_VERSION=jdk8u432-b06
# Thu, 24 Oct 2024 01:52:43 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 24 Oct 2024 01:52:43 GMT
USER ContainerAdministrator
# Thu, 24 Oct 2024 01:53:01 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 24 Oct 2024 01:53:02 GMT
USER ContainerUser
# Thu, 24 Oct 2024 01:53:09 GMT
COPY dir:20063c61efcf25f5137b7902f122f09a78eae5d617f3f56a66aed8780998122b in C:\openjdk-8 
# Thu, 24 Oct 2024 01:53:13 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59cd071304faa8858dafe8d047619b01d15aa97c5554fdff76e91bb19a3030d6`  
		Last Modified: Thu, 24 Oct 2024 01:53:20 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c9c37944b4821e8f74352711232aebf04df82e01cab1ba4c0ad4d98a45011b`  
		Last Modified: Thu, 24 Oct 2024 01:53:20 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da2e80086a3f5dcd541d8e2aa3b85e586518538392f8e5b58b459eeca84f15f`  
		Last Modified: Thu, 24 Oct 2024 01:53:20 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e047249939d0bcdb0f964755639b53d85c6428d9407d5f4413ab65b801cdd8ad`  
		Last Modified: Thu, 24 Oct 2024 01:53:18 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b148ee602e2ef3bcd0eb20e5109b9f2e953a12fa83efcd7ed1aca9c33d651e`  
		Last Modified: Thu, 24 Oct 2024 01:53:18 GMT  
		Size: 78.5 KB (78498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448bfdede2c3604ad678650555ca4d33e2a8e598495f8e8ee907d8d64ffae96e`  
		Last Modified: Thu, 24 Oct 2024 01:53:18 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9084cc3e2ae592f23f1064080acef87eebcd5f217e113de477bebc7995a223`  
		Last Modified: Thu, 24 Oct 2024 01:53:25 GMT  
		Size: 103.4 MB (103441240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8716ade059cca0d598edb98a1f98789cc00d70ae68037f89cce81e33865fca6`  
		Last Modified: Thu, 24 Oct 2024 01:53:18 GMT  
		Size: 87.8 KB (87844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
