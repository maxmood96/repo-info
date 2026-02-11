## `eclipse-temurin:21-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:f86e8385fe38bd04dcf0aaab6f86d2cc2d1fcb5135427fec871e6a75ef7d6f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.26100.32370; amd64

```console
$ docker pull eclipse-temurin@sha256:e0db168ed63caa19cdbbdb4a13b4a7e69221df1f6da96769539f82dc6a5d3ad1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.5 MB (248457219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0769dbcf86334b25bc4359b8679c506f6c7354986600c2109dcff6f505e633`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 22:06:41 GMT
RUN Apply image 10.0.26100.32370
# Tue, 10 Feb 2026 23:37:24 GMT
SHELL [cmd /s /c]
# Tue, 10 Feb 2026 23:37:25 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 10 Feb 2026 23:37:25 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 10 Feb 2026 23:37:26 GMT
USER ContainerAdministrator
# Tue, 10 Feb 2026 23:37:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Feb 2026 23:37:30 GMT
USER ContainerUser
# Tue, 10 Feb 2026 23:37:35 GMT
COPY dir:60f2977da675e9d6a11be1282de5c19d751a1b21ff04571f86a073fb3e930423 in C:\openjdk-21 
# Tue, 10 Feb 2026 23:37:38 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:77321bd03612cfa46920e790ae0c3b142758a5803ad759fdb406c98b6f2e4ed0`  
		Last Modified: Tue, 10 Feb 2026 22:50:26 GMT  
		Size: 199.3 MB (199251619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f20b830f979c2d672ecad222e50d5724054a4743c8560e6449fd369ce38bb8`  
		Last Modified: Tue, 10 Feb 2026 23:37:44 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0d61055d81ac73c097da3196ae0af3c3f844d1eb8c8454536333a0b9939688`  
		Last Modified: Tue, 10 Feb 2026 23:37:44 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fadb397a76ccab20a2e260a802de8ca8068401b4ed9ff975fae4128ccf5441b`  
		Last Modified: Tue, 10 Feb 2026 23:37:44 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095141cfdb0ef4964718122470efad4f46c00f047df346d48a1a7fb0bf6b00cc`  
		Last Modified: Tue, 10 Feb 2026 23:37:43 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc798744ea461b843a8c3120009fc0194b4195bd4765d2e1420c58900b02b7eb`  
		Last Modified: Tue, 10 Feb 2026 23:37:43 GMT  
		Size: 73.7 KB (73686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4721ec92578744b1760424fd996c01d3f81e856ed8a28ab4dd09411c01fec87`  
		Last Modified: Tue, 10 Feb 2026 23:37:42 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c2219fce121aafb2b87d8e21ce1980745b1e7cbc4307d8ff99379b5e7cb917`  
		Last Modified: Tue, 10 Feb 2026 23:37:49 GMT  
		Size: 49.0 MB (49040227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c52cc79a0a7cb415882931dc80d6095a52ebe6142a1339f8d585356425b7731`  
		Last Modified: Tue, 10 Feb 2026 23:37:42 GMT  
		Size: 86.3 KB (86288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.20348.4773; amd64

```console
$ docker pull eclipse-temurin@sha256:828b206ea14f939d248aff023e7667f2cf011e65bbb1ba7b8cfcdd23694685d2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.9 MB (175867045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff1eb27f8645ca4aeb10bbddb46a785afca9c8431e047e5db8d8e2855ced2ee`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Tue, 10 Feb 2026 23:30:19 GMT
SHELL [cmd /s /c]
# Tue, 10 Feb 2026 23:31:02 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Tue, 10 Feb 2026 23:31:03 GMT
ENV JAVA_HOME=C:\openjdk-21
# Tue, 10 Feb 2026 23:31:03 GMT
USER ContainerAdministrator
# Tue, 10 Feb 2026 23:31:05 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Feb 2026 23:31:05 GMT
USER ContainerUser
# Tue, 10 Feb 2026 23:31:10 GMT
COPY dir:60f2977da675e9d6a11be1282de5c19d751a1b21ff04571f86a073fb3e930423 in C:\openjdk-21 
# Tue, 10 Feb 2026 23:31:13 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197769c1803e408434ab708492fd6b579050a976074dbaed3739b29b6199a8ee`  
		Last Modified: Tue, 10 Feb 2026 23:30:37 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1672463a54dce099b1d0b79e2e460ed7ff4e508c0197c23547f156c5b10b03ad`  
		Last Modified: Tue, 10 Feb 2026 23:31:19 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe10137add74fe555852e1ba1a34d6778a76a11e24c1e5cd9550eef04168cd40`  
		Last Modified: Tue, 10 Feb 2026 23:31:19 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf91d7da9f869f35009a9489bd9e80cf07f243b2f203e10f6b055175be044cc`  
		Last Modified: Tue, 10 Feb 2026 23:31:17 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b892f2a52316eb78a9cbb3c1f1950bceb21426008306ab125f4ef00216e9f79`  
		Last Modified: Tue, 10 Feb 2026 23:31:17 GMT  
		Size: 76.6 KB (76559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5d294e430e88e9036d59c5be080b3582a4f4ee7a654a450314b8e25a40bad8`  
		Last Modified: Tue, 10 Feb 2026 23:31:17 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45ec6fbe9d3bad4d9ccaba6dc1c6937a0d5f628bd124f6847f782af0a605712`  
		Last Modified: Tue, 10 Feb 2026 23:31:24 GMT  
		Size: 49.0 MB (49039698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3108fa9d27b88fbac3329ad90ec7907d7ca5100a5caf2eca22132c66ee279f7d`  
		Last Modified: Tue, 10 Feb 2026 23:31:17 GMT  
		Size: 99.6 KB (99581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
