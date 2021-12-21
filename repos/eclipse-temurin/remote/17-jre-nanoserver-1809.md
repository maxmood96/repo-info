## `eclipse-temurin:17-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:47812b3b71e3bfe6dc9dfe461293297a1c425b05863c02f07bcbef8f63e54e90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `eclipse-temurin:17-jre-nanoserver-1809` - windows version 10.0.17763.2366; amd64

```console
$ docker pull eclipse-temurin@sha256:8e7958f2fa4b3ff7a4dd062c35749c773e402dc15ca0e0444c06d142a1fe9957
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149069869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32db7a644f23aac9b509ba9143fd3329c9f27fd2723e997e53b44f69ac48935`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 07 Dec 2021 04:37:11 GMT
RUN Apply image 1809-amd64
# Sat, 18 Dec 2021 05:18:44 GMT
SHELL [cmd /s /c]
# Sat, 18 Dec 2021 05:58:50 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Sat, 18 Dec 2021 05:58:50 GMT
ENV JAVA_HOME=C:\openjdk-17
# Sat, 18 Dec 2021 05:58:51 GMT
USER ContainerAdministrator
# Sat, 18 Dec 2021 05:59:05 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 18 Dec 2021 05:59:05 GMT
USER ContainerUser
# Tue, 21 Dec 2021 18:22:44 GMT
COPY dir:38eebe4e3a4da98e178f49482de333d171d427f5886e68b2b67715641b9694d5 in C:\openjdk-17 
# Tue, 21 Dec 2021 18:23:02 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:034b2f457cdf6a0d3f7024523d40fd6eeb8568e6c76d9fa56f4053fcf3a21d63`  
		Size: 102.9 MB (102904001 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4c557aac927613dd487d7c04b01a8eeb8ad174693f61b14c8f4285f1db6afdd2`  
		Last Modified: Sat, 18 Dec 2021 06:13:05 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26306f8e8a4f4dfe20500528de7aa39df4e7dee0979f58489a2ded09004ffbd`  
		Last Modified: Sat, 18 Dec 2021 06:40:15 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9362cfac01213205fa1c339e140a340bb1905cb5e0a78c93e0c6a0e5bbfef6d0`  
		Last Modified: Sat, 18 Dec 2021 06:40:14 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec169fd6feabc29f6922c4666746164f5167e3d65707e55174b9a8f12cabf094`  
		Last Modified: Sat, 18 Dec 2021 06:40:14 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0099d82d3944a044d664e71f334526a8d7d2ed1bd7096d3acb142c80c2ea7bb7`  
		Last Modified: Sat, 18 Dec 2021 06:40:12 GMT  
		Size: 66.9 KB (66924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0ed6216ade0a806a34dbf8eed2a100bee72f70e7f01a8403826a5a189e8e6b`  
		Last Modified: Sat, 18 Dec 2021 06:40:12 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd46bfa6b024452cf4983a58884281a3eb2ebfd699c45830629da9acd5c9262a`  
		Last Modified: Tue, 21 Dec 2021 18:31:19 GMT  
		Size: 43.1 MB (43072404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122c9ccdc8d62f2bfc14782e1395317a7926221c18b675ec48ff0fb83239a319`  
		Last Modified: Tue, 21 Dec 2021 18:31:11 GMT  
		Size: 3.0 MB (3020728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
