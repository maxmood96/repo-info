## `openjdk:26-ea-30-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:50f62f2954cfcede69b55b3d42e3bcd5dcb756ed5c287138eae2eb0fc6971607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `openjdk:26-ea-30-nanoserver-ltsc2025` - windows version 10.0.26100.7462; amd64

```console
$ docker pull openjdk@sha256:89104e5c918571ecfdc84636f6a08aa74d2521dda4317ffc9e3c24f8585e1a0c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.9 MB (422866476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c694535ff4ecc9a9c51dd6094672310ad3687a0c8d60c8e75ebc6a4a2518186`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Dec 2025 21:31:34 GMT
RUN Apply image 10.0.26100.7462
# Mon, 12 Jan 2026 21:12:46 GMT
SHELL [cmd /s /c]
# Mon, 12 Jan 2026 21:12:47 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 12 Jan 2026 21:12:48 GMT
USER ContainerAdministrator
# Mon, 12 Jan 2026 21:12:58 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 12 Jan 2026 21:12:58 GMT
USER ContainerUser
# Mon, 12 Jan 2026 21:12:58 GMT
ENV JAVA_VERSION=26-ea+30
# Mon, 12 Jan 2026 21:13:31 GMT
COPY dir:e07e90760755fda5775e159516136ae7ac9e724b6c3d3e98906408d196af4b98 in C:\openjdk-26 
# Mon, 12 Jan 2026 21:13:38 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 12 Jan 2026 21:13:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a092205b76ca656d8483e99445def9f0619cb3acb2688bf9a33244c43ad44ce`  
		Last Modified: Tue, 09 Dec 2025 22:15:12 GMT  
		Size: 198.9 MB (198873947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae0c30a24f290070e5783e9d1fe48a8f8ae05edd00cbb7a4d624c8138a5784a`  
		Last Modified: Mon, 12 Jan 2026 21:14:09 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6929d53888fd0885e8f79ba669ae179ba97eff97f3ae6f1110b59283e8a9ebad`  
		Last Modified: Mon, 12 Jan 2026 21:14:09 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f867fe111396f35b4b29e0306dd656f46cba10e0072a9e0a71dfeca78539b17`  
		Last Modified: Mon, 12 Jan 2026 21:14:09 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee7bec712c6daf76a8f37d627869fd5717e49d853e5fdc8cee04f1d8fe97d63`  
		Last Modified: Mon, 12 Jan 2026 21:14:11 GMT  
		Size: 70.5 KB (70494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4ae485a4d736b9d8e5f09fa047d9124472a0c6a90fa8ea2125b8370c1b26b5`  
		Last Modified: Mon, 12 Jan 2026 21:14:09 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034ea90897a477675ff72bebc78d94808b1abddf0fef825e8d69f5685cbf4a40`  
		Last Modified: Mon, 12 Jan 2026 21:14:09 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829b62a32d4c5a3ed4c491787614d94dba57d8b6e0f5ad4d5e0a2965fcf44fa8`  
		Last Modified: Mon, 12 Jan 2026 21:15:17 GMT  
		Size: 223.8 MB (223832538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0d63b3b82f9988fd81169c24a038088b7024252d676a61e9dbc5fe7274b0583`  
		Last Modified: Mon, 12 Jan 2026 21:14:09 GMT  
		Size: 83.1 KB (83096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6483a1c453db343ebddaba204e22ed604a12c4d0e8ac149f2e60611a9e64ca`  
		Last Modified: Mon, 12 Jan 2026 21:14:09 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
