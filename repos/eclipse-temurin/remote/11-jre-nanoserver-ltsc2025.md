## `eclipse-temurin:11-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:b4e27c2f3241493de9fde2925c23541016e5e497e5261598e6af93b49cb9ba88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6899; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2025` - windows version 10.0.26100.6899; amd64

```console
$ docker pull eclipse-temurin@sha256:f504013cc7bfd1422417859dfd0d06f54cf17385875f7c767359bc9555442547
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.9 MB (237884019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b78a0a6506537c07eab87ad2954c93d99d27c0e3db517fd84c4cf7f5e1d4014`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 11 Oct 2025 15:58:41 GMT
RUN Apply image 10.0.26100.6899
# Tue, 14 Oct 2025 21:12:55 GMT
SHELL [cmd /s /c]
# Tue, 14 Oct 2025 21:12:56 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Tue, 14 Oct 2025 21:12:57 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 14 Oct 2025 21:12:57 GMT
USER ContainerAdministrator
# Tue, 14 Oct 2025 21:13:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Oct 2025 21:13:00 GMT
USER ContainerUser
# Tue, 14 Oct 2025 21:13:09 GMT
COPY dir:58dfc6149e1020fd4be2dce5848817d79ad79993fb8b5211b36f6f0e332ab65c in C:\openjdk-11 
# Tue, 14 Oct 2025 21:13:12 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:463edd10ad50b00cf92c69fc3eaa85e1fa40aad1b7938fa232899405bd80f001`  
		Last Modified: Tue, 14 Oct 2025 22:41:48 GMT  
		Size: 194.0 MB (194026741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404aa613cfca5d724308cd1b3bbb1a1f1635dfe7d84be6029d2db7f9ca9a73c8`  
		Last Modified: Tue, 14 Oct 2025 21:13:30 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b230df4c7f0a4ad79584452e8f85ef1477710434984d211a8f0c1d0b04d1a725`  
		Last Modified: Tue, 14 Oct 2025 21:13:29 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03a720ff639ae4dbc5674d886fc91f1bea0c658bcba70789717354c67b2d1af`  
		Last Modified: Tue, 14 Oct 2025 21:13:31 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e9ac073299c1135df90c0ce384afd1a2ccfbab40f240e2bf05934c64c77f1d`  
		Last Modified: Tue, 14 Oct 2025 21:13:30 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d70e7474976473cfdf6d61bec9ac869d264b436af68356c21a470c99a8f24b4`  
		Last Modified: Tue, 14 Oct 2025 21:13:29 GMT  
		Size: 72.6 KB (72578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2fec796cc33c2ba355b89e036a29561d4a59d31a8261f07b25d45fd9c9efb6`  
		Last Modified: Tue, 14 Oct 2025 21:13:29 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:586155e552efb47945e55e914b22fbba869bb6c930bf3a5683c63cffcd835389`  
		Last Modified: Tue, 14 Oct 2025 21:13:34 GMT  
		Size: 43.7 MB (43666817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30731a2ed485cc8d9028af76ef4c0c2a3095259572dd4fc349b77ff743f5a753`  
		Last Modified: Tue, 14 Oct 2025 21:13:30 GMT  
		Size: 112.5 KB (112490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
