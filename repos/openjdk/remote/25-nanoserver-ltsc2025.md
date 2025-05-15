## `openjdk:25-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:004f3d9776c69589f0cd23f8e77f3904d11e6a5813929dbbf41e0eb58f9b3a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `openjdk:25-nanoserver-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull openjdk@sha256:359658374fbdd9dff095d33634b17e68fa158b0be47f2a5d41d7916de2853cf5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.0 MB (399956726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a60e3e1f946e9b9e932cd67191337dc93cf1015985f60c44dc022c33edc0c59`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 10 May 2025 00:58:48 GMT
RUN Apply image 10.0.26100.4061
# Wed, 14 May 2025 21:14:08 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 21:14:09 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 14 May 2025 21:14:10 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:14:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 May 2025 21:14:14 GMT
USER ContainerUser
# Wed, 14 May 2025 21:14:15 GMT
ENV JAVA_VERSION=25-ea+22
# Wed, 14 May 2025 21:14:25 GMT
COPY dir:d2aeeab016ce5cfb722c90fbb6527341de5d03dac18528814b93fc4084ba77f8 in C:\openjdk-25 
# Wed, 14 May 2025 21:14:32 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 14 May 2025 21:14:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9824510349be04d2eb26f9aaba1d016eddcbed10bdcd6681f4636c948766f3d1`  
		Last Modified: Tue, 13 May 2025 23:02:56 GMT  
		Size: 191.4 MB (191412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7be936c5bae6798509722388fef548775f98172c3002406e3f616451819ffb`  
		Last Modified: Wed, 14 May 2025 21:14:39 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d42a68adf4a5f6273fca0894b3d91aa66344ed1e320efb65a8c1b5934418e7e`  
		Last Modified: Wed, 14 May 2025 21:14:39 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e989cec3f93ca5db5e12f8da959e0532603b12334895fc26576b88b75ff11a`  
		Last Modified: Wed, 14 May 2025 21:14:39 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9032652dc193211ca8c52af5623b82241e86b3d502aacaf96f2715e490720ab5`  
		Last Modified: Wed, 14 May 2025 21:14:39 GMT  
		Size: 76.2 KB (76162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22bdd871400fdba24a02da3436188164a1fde98908334edc8184f56351c786d`  
		Last Modified: Wed, 14 May 2025 21:14:37 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4075a8e58c5bc386f4c10da47d63bfce27c2285ea5246545da02c370f11116d6`  
		Last Modified: Wed, 14 May 2025 21:14:37 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594e03a12128dc8b7b4c982a8932bab39bf29e25a7641c511c8f8124099d703e`  
		Last Modified: Wed, 14 May 2025 21:14:48 GMT  
		Size: 208.4 MB (208367631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827dde15c6082ca3083f4c1d23714a2a8d7392944dbb2c80da4503454ba8bcb7`  
		Last Modified: Wed, 14 May 2025 21:14:37 GMT  
		Size: 94.6 KB (94617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1ea0fc678634ee0a5d6bb4bb36e14518eed40f3e131519c01dc3be921c38f4`  
		Last Modified: Wed, 14 May 2025 21:14:37 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
