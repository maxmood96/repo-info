## `eclipse-temurin:17-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:33fb8ef4cb54c4b367f9a7cf855c7dc9278810d37c0eb0a9eeb8125154a98939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `eclipse-temurin:17-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:719cfd396b27fde604f610b0b5da0ebb17c6f4755a711a1e5b82214ea685e1df
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307115481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5db89b52c23437adb8801a01866f0a47a1bd49a95cea4b8bcf878bc09bd7b0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Thu, 10 Oct 2024 00:11:44 GMT
SHELL [cmd /s /c]
# Thu, 10 Oct 2024 00:14:20 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 10 Oct 2024 00:14:21 GMT
ENV JAVA_HOME=C:\openjdk-17
# Thu, 10 Oct 2024 00:14:22 GMT
USER ContainerAdministrator
# Thu, 10 Oct 2024 00:14:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 10 Oct 2024 00:14:33 GMT
USER ContainerUser
# Thu, 10 Oct 2024 00:14:46 GMT
COPY dir:11f935f87b5561ba9de5a02e585d9b073f4114e9ab1765209f28e6005e01c91d in C:\openjdk-17 
# Thu, 10 Oct 2024 00:15:00 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 10 Oct 2024 00:15:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96818114ce85fcf68e8af61951767bf11ed374ffe6a9023b6150122fbad46d51`  
		Last Modified: Thu, 10 Oct 2024 00:32:47 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9349d39233008b4b01a5a45122a3f0ce101ac42823cce0b2c9da4e23bfdcf0`  
		Last Modified: Thu, 10 Oct 2024 00:34:16 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38a88948c573f25296e7fb9e5462b405ea1d04275036d0e9e54ff7ccc7ea550`  
		Last Modified: Thu, 10 Oct 2024 00:34:16 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5027fbf91035446eea340563bf15148e87fae0e401cbb7063f27e45ff85490ec`  
		Last Modified: Thu, 10 Oct 2024 00:34:15 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2fecaf9e2fe9c74149948522974e818e75d31e33d62bafcfcf8026b0059263`  
		Last Modified: Thu, 10 Oct 2024 00:34:14 GMT  
		Size: 76.8 KB (76805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3c15dacadb7611c3a92b206003ff3106b0e55b706fa53067ef20e9924a2906`  
		Last Modified: Thu, 10 Oct 2024 00:34:14 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21dcf35e04cad3dc5e606fdd3495261366992287168e72516f53800ac6d6389`  
		Last Modified: Thu, 10 Oct 2024 00:34:31 GMT  
		Size: 186.5 MB (186459344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc4571395f22963cd727bc997432d7c69e3def67dd8473e1b80788bc9f3c5f7`  
		Last Modified: Thu, 10 Oct 2024 00:34:14 GMT  
		Size: 61.4 KB (61421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc357d3ab8d42bcabce48924e7c24f8a5905381f3f14f3c8fc573ff61a5e1e6a`  
		Last Modified: Thu, 10 Oct 2024 00:34:14 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
