## `openjdk:27-ea-nanoserver`

```console
$ docker pull openjdk@sha256:c170624928db8e3cd30a466937768942837f53497d8d7b86c2794396acb800f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `openjdk:27-ea-nanoserver` - windows version 10.0.26100.32370; amd64

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

### `openjdk:27-ea-nanoserver` - windows version 10.0.20348.4773; amd64

```console
$ docker pull openjdk@sha256:5d49f47b138e8bf5a20a279df8ed94bc2d81a45faf7d91257f750626da9d9de8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351141434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a341006d8b064831d9134cfece918693c1a3bd4d4a59170b0e4492b7ca756207`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Fri, 13 Feb 2026 01:11:50 GMT
SHELL [cmd /s /c]
# Fri, 13 Feb 2026 01:14:51 GMT
ENV JAVA_HOME=C:\openjdk-27
# Fri, 13 Feb 2026 01:14:52 GMT
USER ContainerAdministrator
# Fri, 13 Feb 2026 01:14:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 13 Feb 2026 01:14:54 GMT
USER ContainerUser
# Fri, 13 Feb 2026 01:14:54 GMT
ENV JAVA_VERSION=27-ea+8
# Fri, 13 Feb 2026 01:15:39 GMT
COPY dir:b6c1882cd38fa8bcaed3eaff150c211b52c7be8cc1588db9cefe115dd4b4e6b6 in C:\openjdk-27 
# Fri, 13 Feb 2026 01:15:44 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 13 Feb 2026 01:15:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9cc2da1daea54f1cf84245cd706060bed9755e4a888051af1fdd2840e00426c`  
		Last Modified: Fri, 13 Feb 2026 01:13:53 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df00c0e0eccfec9b223dec64d9c9e353cc5eeebf47966c075e19a48ca3d9b93`  
		Last Modified: Fri, 13 Feb 2026 01:15:50 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176f12f32be63d4f1fbfdd52baca840f8ba2c69e86d9950392d2ff94a13f1c5f`  
		Last Modified: Fri, 13 Feb 2026 01:15:50 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264b8a2eac80d91459f1551e2ebcfad267c9873c3915178eb5e65e819e717183`  
		Last Modified: Fri, 13 Feb 2026 01:15:50 GMT  
		Size: 77.1 KB (77072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5854911d7a40c35af1f9c5517ce40c528efb6238be7585f7b83848ca86ceefa`  
		Last Modified: Fri, 13 Feb 2026 01:15:48 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9c676ebd3888f17abbe68ff1f17283c4e863c263af4753d594579d70a9dc83`  
		Last Modified: Fri, 13 Feb 2026 01:15:48 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b928b456cbc24738d8b6f78aa5a574e338429e9ab2f0bc485fd0001317bee48`  
		Last Modified: Fri, 13 Feb 2026 01:16:09 GMT  
		Size: 224.3 MB (224305082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d691b318bbf43a2266c6de263c4db3dd1d83ab4dcf56532911ae9cba8d1badf0`  
		Last Modified: Fri, 13 Feb 2026 01:15:48 GMT  
		Size: 107.0 KB (107020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6efc59978ecf395ab11d6795013e262daa7a40bc0bfaeaa70318194484bca3`  
		Last Modified: Fri, 13 Feb 2026 01:15:48 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
