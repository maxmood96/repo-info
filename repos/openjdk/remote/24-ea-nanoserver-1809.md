## `openjdk:24-ea-nanoserver-1809`

```console
$ docker pull openjdk@sha256:e6582327f7e9a58b57ce6df1d69fe7da6d17c3da59fe0c34c4ee4b6f43018740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `openjdk:24-ea-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:69464fe0d6aec1374c7591dacc3e10b67a425b9f52a4d153895db5c166ba3cc5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368215579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cc27a7c1ad6073b506e0708feb0e209ea3eef82a72d60183c25f37bf59f30c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 29 Jan 2025 01:28:28 GMT
SHELL [cmd /s /c]
# Wed, 29 Jan 2025 01:28:30 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 29 Jan 2025 01:28:31 GMT
USER ContainerAdministrator
# Wed, 29 Jan 2025 01:28:48 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 29 Jan 2025 01:28:49 GMT
USER ContainerUser
# Wed, 29 Jan 2025 01:28:49 GMT
ENV JAVA_VERSION=24-ea+33
# Wed, 29 Jan 2025 01:29:03 GMT
COPY dir:0501e586ce21e14cfb645b0134706225edb213a038c5d5da062ef05b40a90877 in C:\openjdk-24 
# Wed, 29 Jan 2025 01:29:09 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 29 Jan 2025 01:29:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47f657c1b441b831e252022f38eb928e1b466db37be2bec78c6ce54f9889a49`  
		Last Modified: Wed, 29 Jan 2025 01:29:14 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67de9982c926acf1ab99924b9e2630194cc4b2a4bd8b75d082db836dac0bd48`  
		Last Modified: Wed, 29 Jan 2025 01:29:14 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0565120c5e75b8617ce753dde25f7c5b2529b3c8b1d455e760d12990567ae4b0`  
		Last Modified: Wed, 29 Jan 2025 01:29:14 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139ceae1f7599d8e2aa14635d0dc5b6a5204b61ff77c888402a5896336d08709`  
		Last Modified: Wed, 29 Jan 2025 01:29:14 GMT  
		Size: 67.8 KB (67770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d7d32ef6426bb73f8aeb780e1e71d74bdf0032d11a6625534fe443ac6c255b`  
		Last Modified: Wed, 29 Jan 2025 01:29:13 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b24efd1519f763869319b98c0d7af54d4a2bfbbc65b66cf868a237ef7bbe77`  
		Last Modified: Wed, 29 Jan 2025 01:29:13 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151ffc6437a9734cd20fb9ad869447c73cdc2c746ce51b5c723945af93e6dcca`  
		Last Modified: Wed, 29 Jan 2025 01:29:24 GMT  
		Size: 208.5 MB (208491130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3e63e334bb48d10a63aac04ea32a4a8a35252592999edde3e7f7ccc8c9bc9c`  
		Last Modified: Wed, 29 Jan 2025 01:29:13 GMT  
		Size: 4.4 MB (4382728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d0e4eee5840a3caaf03774d430b2f7d090c8f09575b19cc1f0a56967ae7b3a`  
		Last Modified: Wed, 29 Jan 2025 01:29:13 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
