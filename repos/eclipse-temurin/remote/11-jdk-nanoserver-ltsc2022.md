## `eclipse-temurin:11-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:830cb84137e52046133eb31edb264eff3b7340a5c5de01b597fa70460e21958d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `eclipse-temurin:11-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:3ddf6d0aefde93989628a0bb608826530be2387a86191d7e5c491fd21157509b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314314003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8d1904510ad92ac1029ef3872fdc9a5ad69ee04ea16ac39f4927ccac71de9b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Thu, 10 Oct 2024 00:11:44 GMT
SHELL [cmd /s /c]
# Thu, 10 Oct 2024 00:13:03 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Thu, 10 Oct 2024 00:13:04 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 10 Oct 2024 00:13:05 GMT
USER ContainerAdministrator
# Thu, 10 Oct 2024 00:13:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 10 Oct 2024 00:13:15 GMT
USER ContainerUser
# Thu, 10 Oct 2024 00:13:29 GMT
COPY dir:b5e9d6d7234e205f01359f52140171f1743cc309a4dc5e4224755ced7d18fbfc in C:\openjdk-11 
# Thu, 10 Oct 2024 00:13:43 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 10 Oct 2024 00:13:44 GMT
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
	-	`sha256:856b368fb541d849e5317a5831eab8d943e1b7fa8416571b86fd0c2376e6c290`  
		Last Modified: Thu, 10 Oct 2024 00:33:33 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079f8ffd694f4a9dc0514d9d4d76c5729b89b2255074199442038e5afbcf4673`  
		Last Modified: Thu, 10 Oct 2024 00:33:33 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fdfc2447d8d01c594e2f5cef2b41abeb158b6a7c5fa72119601042c47c46fef`  
		Last Modified: Thu, 10 Oct 2024 00:33:33 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8fff03a5e1045d0c1eb23777d6d1c7703c9ed990aa903f9f4debd43a6b29138`  
		Last Modified: Thu, 10 Oct 2024 00:33:31 GMT  
		Size: 75.9 KB (75944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571c7b704f6cf19cfc0ad633ad27b62025d67372b663f6776bc0fd0a861e02f4`  
		Last Modified: Thu, 10 Oct 2024 00:33:31 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0de1d1bb385199944deeb00638c1c2537bf2a1154ba30ab64d38041af5bb6c`  
		Last Modified: Thu, 10 Oct 2024 00:33:48 GMT  
		Size: 193.7 MB (193658738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06ed975896faa6d8b62e4373804fd07c52abef4c222dac71dc304425e7b8e34`  
		Last Modified: Thu, 10 Oct 2024 00:33:31 GMT  
		Size: 61.4 KB (61419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2946e5f12743e276c475c5880566a8350c4b9bbd196e1899d22c22fa052f7f`  
		Last Modified: Thu, 10 Oct 2024 00:33:31 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
