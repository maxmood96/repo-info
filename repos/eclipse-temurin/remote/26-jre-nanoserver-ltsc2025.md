## `eclipse-temurin:26-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:8a09e202f16df62a29cb48da2dc2f1925a36ba76a14501990f9b7a95b1007f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `eclipse-temurin:26-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull eclipse-temurin@sha256:c03c8ffb90c38a87f80f7bc76d6c85c7bfad898a21bb168dc0d2be38e4cc8b78
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.2 MB (260181186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26671da10f02b891b69305425b2017cea782902097b97e9f9fc098b793c7f205`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 06:39:57 GMT
RUN Apply image 10.0.26100.32690
# Tue, 14 Apr 2026 22:14:17 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2026 22:14:17 GMT
ENV JAVA_VERSION=jdk-26+35
# Tue, 14 Apr 2026 22:14:17 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 14 Apr 2026 22:14:18 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 22:14:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Apr 2026 22:14:20 GMT
USER ContainerUser
# Tue, 14 Apr 2026 22:14:38 GMT
COPY dir:45edd54e05e2fb7ffc611e6ef0c2df37aa13ac9c3c9a476003fc542e9ad17481 in C:\openjdk-26 
# Tue, 14 Apr 2026 22:14:42 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:8af320c3b6d19296bcc7947e3beb8bc0c69cb12143db52efe988dc998ac088dc`  
		Last Modified: Tue, 14 Apr 2026 21:00:37 GMT  
		Size: 199.7 MB (199717094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84021931477dfb29a332bf69444c211840756a55c1d55f1809f8ad7a1591778`  
		Last Modified: Tue, 14 Apr 2026 22:14:47 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d33c223c93c957f49300deee7db0ba7b7710e794405aff175a77479556d39fe`  
		Last Modified: Tue, 14 Apr 2026 22:14:47 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a1124d7a3400317727471500e409a23986e9c11717c46725d759cdbc7bf9f1`  
		Last Modified: Tue, 14 Apr 2026 22:14:47 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0393b6619508a52c853d491fa26c59e13e2b2a6e7a0f1700090dcbd12481bf`  
		Last Modified: Tue, 14 Apr 2026 22:14:46 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b95475246f912d5e73b52e1113972ffdf5add1cf9fa63962485aff0469d37f`  
		Last Modified: Tue, 14 Apr 2026 22:14:46 GMT  
		Size: 72.3 KB (72298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b332faecae5aa3bee35579017f0c06867e44de92ec500c29697a07fdc381fc`  
		Last Modified: Tue, 14 Apr 2026 22:14:46 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7d87942a63ec79cdadad141ecfc559b84c2e9075eedc163878ea90ff5c5540`  
		Last Modified: Tue, 14 Apr 2026 22:14:54 GMT  
		Size: 60.3 MB (60266534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd880099ff90171b6c82c50f47f2e8c8ed1a2011464e70c6ced49fe1c42e2f9`  
		Last Modified: Tue, 14 Apr 2026 22:14:46 GMT  
		Size: 119.9 KB (119948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
