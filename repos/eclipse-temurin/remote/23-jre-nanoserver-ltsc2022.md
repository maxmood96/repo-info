## `eclipse-temurin:23-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:c8b8c9eb508d400d0fe71dc835d49a6b18c39ddfdc192a8c7df51d15d09318f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `eclipse-temurin:23-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:2fe7a00f9835d80c088abca54eeb401a90e1bc81e4c1d4affa07664f1e9b5686
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170285149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9acc40286f00309594db2242e50c805035a63489975c21b5810846efbf5e8467`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Thu, 24 Oct 2024 01:52:56 GMT
SHELL [cmd /s /c]
# Thu, 24 Oct 2024 01:52:57 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Thu, 24 Oct 2024 01:52:57 GMT
ENV JAVA_HOME=C:\openjdk-23
# Thu, 24 Oct 2024 01:52:58 GMT
USER ContainerAdministrator
# Thu, 24 Oct 2024 01:53:28 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 24 Oct 2024 01:53:28 GMT
USER ContainerUser
# Thu, 24 Oct 2024 01:53:32 GMT
COPY dir:d9adc234ed2c06cd6b72c0beb8933c6d824941dbd1cece41e4fd2578b0632fbd in C:\openjdk-23 
# Thu, 24 Oct 2024 01:53:38 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b490a44387cac3724ada15de137e68c75e0619f2822bef8c3f16c7dee27a47`  
		Last Modified: Thu, 24 Oct 2024 01:53:42 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b9f7f55f6d18d03ed0cce67da4c0c98f775dda38cf0639d3b1598eee1f3d4f`  
		Last Modified: Thu, 24 Oct 2024 01:53:42 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03d0b8fee81e9453a35da52e24d25eaf9414a4fc31f7c4fb9654b0db0f8aac8`  
		Last Modified: Thu, 24 Oct 2024 01:53:42 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95796fdeb9081b0b0a7383909bed5c7dde366efdbed6a5ad1ed13e72b7078bea`  
		Last Modified: Thu, 24 Oct 2024 01:53:41 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191a29860ee7ce68cb30916e0b508ef1ab71760da33f8f7a65d8b197d96fb542`  
		Last Modified: Thu, 24 Oct 2024 01:53:41 GMT  
		Size: 72.2 KB (72179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2664bc9526d71f53fe8941e0959e53eab6a787b8e9b2b77ec7a20ed3b338ab8f`  
		Last Modified: Thu, 24 Oct 2024 01:53:41 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84488b7499a6dc1957cad7a63f6d3a038b8af068f158ce01927c0ce11054d46c`  
		Last Modified: Thu, 24 Oct 2024 01:53:46 GMT  
		Size: 49.6 MB (49608105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd42f3b50ef27304e13ac2896789c2a7475b06b9dd9ac508c597136e0645ce48`  
		Last Modified: Thu, 24 Oct 2024 01:53:41 GMT  
		Size: 88.4 KB (88410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
