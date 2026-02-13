## `openjdk:27-ea-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:ebe7bf5544f0eb3e427d624863095d4ec1884a91bc4a5327a979868925bd3d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `openjdk:27-ea-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull openjdk@sha256:89467bbfac5b84683f0018ffbc7246c4fb86daa8607d0b92ab7869ab04078c4d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.7 MB (423737767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd9b8d79e927a8f873c6ac289f50ef26173e4e5b9c4262be31bf4fe138979caa`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 22:06:41 GMT
RUN Apply image 10.0.26100.32370
# Fri, 13 Feb 2026 01:14:06 GMT
SHELL [cmd /s /c]
# Fri, 13 Feb 2026 01:14:06 GMT
ENV JAVA_HOME=C:\openjdk-27
# Fri, 13 Feb 2026 01:14:07 GMT
USER ContainerAdministrator
# Fri, 13 Feb 2026 01:14:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 13 Feb 2026 01:14:13 GMT
USER ContainerUser
# Fri, 13 Feb 2026 01:14:13 GMT
ENV JAVA_VERSION=27-ea+8
# Fri, 13 Feb 2026 01:14:27 GMT
COPY dir:b6c1882cd38fa8bcaed3eaff150c211b52c7be8cc1588db9cefe115dd4b4e6b6 in C:\openjdk-27 
# Fri, 13 Feb 2026 01:14:32 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 13 Feb 2026 01:14:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:77321bd03612cfa46920e790ae0c3b142758a5803ad759fdb406c98b6f2e4ed0`  
		Last Modified: Tue, 10 Feb 2026 22:50:26 GMT  
		Size: 199.3 MB (199251619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae09911a549fb934d0c9eb05ca8810332229a787f3db2a4a1fe53c9fcccb74`  
		Last Modified: Fri, 13 Feb 2026 01:14:38 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef57cb9c08da3f6eab9e66c22196b189252f41cda48c8f40beb443444cd7fa6`  
		Last Modified: Fri, 13 Feb 2026 01:14:38 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5664764b323399d4b7adae00cc122913bde390662091775f8741a28f71bfc2e`  
		Last Modified: Fri, 13 Feb 2026 01:14:38 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ef5a7cf3dfeebca13fd2014252a1bece0c9801e5a623ce0433363c951079d9`  
		Last Modified: Fri, 13 Feb 2026 01:14:38 GMT  
		Size: 72.8 KB (72813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56dbf4da7001ec0dbde26548b59db29108ded920b7c0971352b66bd7de297b55`  
		Last Modified: Fri, 13 Feb 2026 01:14:37 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7906f748957a79afb343e3914925400b9a0fba84aa2955771e597ca552da9e5`  
		Last Modified: Fri, 13 Feb 2026 01:14:37 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2948ed41749b016378c67d67e32aefe3dffe1beb52f0c8056d3ef3c057e81e0e`  
		Last Modified: Fri, 13 Feb 2026 01:14:53 GMT  
		Size: 224.3 MB (224304216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1a00b67a1c6fb34db7ed0769ca3522894548f6b0c69b13e975391ed03abb03`  
		Last Modified: Fri, 13 Feb 2026 01:14:37 GMT  
		Size: 102.6 KB (102642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285489ce5d61c17fcde5e6ff3bb81890c68929847d382cc4bb5bf7d3930665a5`  
		Last Modified: Fri, 13 Feb 2026 01:14:37 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
