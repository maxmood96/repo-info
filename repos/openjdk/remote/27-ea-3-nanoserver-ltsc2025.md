## `openjdk:27-ea-3-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:0d14626973702f5e4b5ac494c9764b568b498c1ade5154289e530e22a4d34ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `openjdk:27-ea-3-nanoserver-ltsc2025` - windows version 10.0.26100.7462; amd64

```console
$ docker pull openjdk@sha256:24568cf5ef694b89b4896cef12ac5cc9a3168b479ce838ca912eecc1834b9006
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.0 MB (422990870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e6e7695e1d8880e17d25a5b80c009f6fafb33296ccc11af0801d7f1957e909`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Dec 2025 21:31:34 GMT
RUN Apply image 10.0.26100.7462
# Wed, 24 Dec 2025 06:11:55 GMT
SHELL [cmd /s /c]
# Wed, 24 Dec 2025 06:13:33 GMT
ENV JAVA_HOME=C:\openjdk-27
# Wed, 24 Dec 2025 06:13:33 GMT
USER ContainerAdministrator
# Wed, 24 Dec 2025 06:13:35 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 24 Dec 2025 06:13:35 GMT
USER ContainerUser
# Wed, 24 Dec 2025 06:13:36 GMT
ENV JAVA_VERSION=27-ea+3
# Wed, 24 Dec 2025 06:13:56 GMT
COPY dir:fd5bab190d0e23cab6ba3a5710a034aa8e7b3d18ea9d8ef51c8a34f9322814a7 in C:\openjdk-27 
# Wed, 24 Dec 2025 06:14:01 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 24 Dec 2025 06:14:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a092205b76ca656d8483e99445def9f0619cb3acb2688bf9a33244c43ad44ce`  
		Last Modified: Tue, 09 Dec 2025 22:15:12 GMT  
		Size: 198.9 MB (198873947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8dca99ad75e6a24ba30d6443869285c9072c65d8b7e0398fbfd33f4ce243b75`  
		Last Modified: Wed, 24 Dec 2025 06:13:13 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290fb05b74bec4af808356dce9ffc3bbf16715a70321027492df5e7d84b4947a`  
		Last Modified: Wed, 24 Dec 2025 06:14:28 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8c5516a1aadfe41f46971e3e79fdc9c03f4f74dd3a10ab1481c26b5f22036a`  
		Last Modified: Wed, 24 Dec 2025 06:14:28 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada0aa16ceba035b61a3b792ecadee7fb25135ae7fca5c4d1f96c5a9cf24ea62`  
		Last Modified: Wed, 24 Dec 2025 06:14:28 GMT  
		Size: 72.8 KB (72810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a79af80c306572785be04ec61c47fc0b0422539c7f57aac08e78050cab4832b`  
		Last Modified: Wed, 24 Dec 2025 06:14:28 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae8c62ddc29f2dbcf7527f9f4974a104d81c6e9b2a1b32d95b727d210992453`  
		Last Modified: Wed, 24 Dec 2025 06:14:28 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e41714308e6feaa7d736c847a6ecbae2dc1f93c7bdcb61a0754a9149c7de7056`  
		Last Modified: Wed, 24 Dec 2025 06:16:16 GMT  
		Size: 223.9 MB (223925422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e6ee822846af17fc18e8860e05624396a3ed438be3194cafced52fc97f0b40`  
		Last Modified: Wed, 24 Dec 2025 06:14:28 GMT  
		Size: 112.3 KB (112320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfcac65356f7d403a48f8680c828257da1f709911a52b201de44a1ccedde815`  
		Last Modified: Wed, 24 Dec 2025 06:14:28 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
