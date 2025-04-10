## `eclipse-temurin:24-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:1a3fff49c8b817b9877cb15e4ad850b758afbd5a78381c0da94c439cd49f520c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `eclipse-temurin:24-nanoserver-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull eclipse-temurin@sha256:d340a1e7bedd694c710d2893e2801d51955514936dd996e708761f942117300f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.8 MB (248773980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc7f1893867049f3bf9d72c70d6f3ba95a711db6b276eb32e857556bdb459fe`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Apr 2025 01:31:28 GMT
RUN Apply image 10.0.17763.7136
# Wed, 09 Apr 2025 01:50:05 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:50:06 GMT
ENV JAVA_VERSION=jdk-24+36
# Wed, 09 Apr 2025 01:50:07 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 09 Apr 2025 01:50:07 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:50:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:50:10 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:50:17 GMT
COPY dir:82098476e422c0fd1b27846be91131b5a5073542830e51603132b80cd94d4318 in C:\openjdk-24 
# Wed, 09 Apr 2025 01:50:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Apr 2025 01:50:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a06e0965a0fa3715e629889bd9332aa22aadd75654cac5c9818b67c0264b3ee1`  
		Last Modified: Tue, 08 Apr 2025 20:16:02 GMT  
		Size: 106.9 MB (106922524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70586b86c0ac1b1d73d626bc586c4857b2f083b38eff7cc2d41ca91a9eaa418`  
		Last Modified: Wed, 09 Apr 2025 01:50:31 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7050f5a661edda42cd766ce92d5f8f1473c4cc4c8547ebbff8a4df276d087216`  
		Last Modified: Wed, 09 Apr 2025 01:50:30 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589cf869f284c6e4ba012867eff822a5887d46b2a9c8895a9f39606a62ee2a28`  
		Last Modified: Wed, 09 Apr 2025 01:50:30 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d45a6b5a0adb575292668d32689538205665cbfa55632ec1dee0999c7d9c1b`  
		Last Modified: Wed, 09 Apr 2025 01:50:30 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7293695835d3070bf66e066c722138780a18b8734c51d575ff9790313ab3a4f6`  
		Last Modified: Wed, 09 Apr 2025 01:50:28 GMT  
		Size: 71.9 KB (71864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f33f604b936b2c11355a6eceb14b8675155a94a0db085f7d99daaa696cc5ac6`  
		Last Modified: Wed, 09 Apr 2025 01:50:28 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d06ed132b8eb0cff2c74b80df97f44d762a0428017aa22c37495300a876b62`  
		Last Modified: Wed, 09 Apr 2025 01:50:39 GMT  
		Size: 137.4 MB (137355657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f339d9945f24dd9927c0674c75d6fa9b9e2d9740b78f45cf9e52bf61314ebab0`  
		Last Modified: Wed, 09 Apr 2025 01:50:29 GMT  
		Size: 4.4 MB (4417674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2465182f3139b66e15f619b7038187a055d12ba1346e9d632548fbaa5786c3c2`  
		Last Modified: Wed, 09 Apr 2025 01:50:28 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
