## `openjdk:24-ea-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:e438c787c840f03003c228ad5c371c74f02caf377c93fcea4819512ee3cbe0ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `openjdk:24-ea-nanoserver-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:22dbcd150da908fa2046bf69b4c1c9b874cbb30b37ab552b2e194a556dd5b89f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.4 MB (329382456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:790120bd65638fca7cb59a633f96b37d8c9bae6e321eeebf7529ee75707bd36a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Wed, 05 Feb 2025 00:10:19 GMT
SHELL [cmd /s /c]
# Wed, 05 Feb 2025 00:10:19 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 05 Feb 2025 00:10:20 GMT
USER ContainerAdministrator
# Wed, 05 Feb 2025 00:10:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 05 Feb 2025 00:10:43 GMT
USER ContainerUser
# Wed, 05 Feb 2025 00:10:44 GMT
ENV JAVA_VERSION=24-ea+35
# Wed, 05 Feb 2025 00:10:52 GMT
COPY dir:8f8aac6961c71e892e6587cdd6058441c6f263293987c0242380c839d9a86912 in C:\openjdk-24 
# Wed, 05 Feb 2025 00:10:59 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 05 Feb 2025 00:10:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0ddb5ee07b0f40d5a387b47ac5c7d1f5cee3ab894851431cb8300f7b767e13`  
		Last Modified: Wed, 05 Feb 2025 00:11:03 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff33d38bd3905004e335b47e5a8d1d9f8f7aee84cd402bf91d9007cab491e94`  
		Last Modified: Wed, 05 Feb 2025 00:11:03 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2094754633c776c3f8ec6ba01b957858b81e0bdfc4633abd6db125341982e86e`  
		Last Modified: Wed, 05 Feb 2025 00:11:03 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0670eedf40c7fda8e15f9a6079ae34d71db4f5960db0bb6442746668b304be`  
		Last Modified: Wed, 05 Feb 2025 00:11:03 GMT  
		Size: 85.2 KB (85250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101056cceb797f5da16b0adac709a2063a2f88fcdb3a0fdec4a7b25209ef41e1`  
		Last Modified: Wed, 05 Feb 2025 00:11:02 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7928282fce0d74428716e46516676b4ff19c5ad60061c3169a9a906cdb20f2`  
		Last Modified: Wed, 05 Feb 2025 00:11:02 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:629ca0f598a0cc0162cef8957cc8b3ab236d5d98e8b321e32f9f5fd4d727f4a7`  
		Last Modified: Wed, 05 Feb 2025 00:11:14 GMT  
		Size: 208.5 MB (208531980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0496a77d0be821da49b160621120f788a233b733a0c237e6045a3f7b50828ab`  
		Last Modified: Wed, 05 Feb 2025 00:11:02 GMT  
		Size: 97.5 KB (97458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1376eec32258737d0e53a225f0f2255abeaa1082e4d305f576e5479375ad09ce`  
		Last Modified: Wed, 05 Feb 2025 00:11:02 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
