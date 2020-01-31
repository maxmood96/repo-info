## `openjdk:15-ea-nanoserver-1809`

```console
$ docker pull openjdk@sha256:11d9055836355a527dd981deb896b175974c2666bba0ca7d72f60a31a937f173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `openjdk:15-ea-nanoserver-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull openjdk@sha256:606a39c428373225be9182efcb14a8df78062c3d3cce512f637f07c2409a5e04
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298519784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07dd8aad17ac2838ad3f728db1b7f2b3e904b3bafeda0f8f9e02a0b0f040f90`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 04 Jan 2020 07:17:17 GMT
RUN Apply image 1809-amd64
# Tue, 14 Jan 2020 23:56:11 GMT
SHELL [cmd /s /c]
# Tue, 14 Jan 2020 23:56:12 GMT
ENV JAVA_HOME=C:\openjdk-15
# Tue, 14 Jan 2020 23:56:13 GMT
USER ContainerAdministrator
# Tue, 14 Jan 2020 23:56:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Tue, 14 Jan 2020 23:56:31 GMT
USER ContainerUser
# Fri, 31 Jan 2020 17:53:22 GMT
ENV JAVA_VERSION=15-ea+8
# Fri, 31 Jan 2020 17:54:28 GMT
COPY dir:89f0cf6360f6b771ecac550a12fd8546f5de33d8908e4e96652d583ab81d9869 in C:\openjdk-15 
# Fri, 31 Jan 2020 17:54:50 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Fri, 31 Jan 2020 17:54:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ee446884f7bef76f8275c2f16add1c4fb598bea2ba861e72bce8fb4aac9b55ef`  
		Size: 101.1 MB (101054324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:764e25aa4e95684bd69a4d130dc1c729bfaef95293d9c76c4d2a12ced9e3a9ac`  
		Last Modified: Wed, 15 Jan 2020 01:51:06 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f193e511d66e393e8623d9efd86f48f82cc15ceb19ee3a6ac9da7343da044ad`  
		Last Modified: Wed, 15 Jan 2020 01:51:04 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01fab357b0406f3be040eca20b497e3bdd7e731b95865fbfbe83acf826248583`  
		Last Modified: Wed, 15 Jan 2020 01:51:03 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fed5c1fef1ff77da19cbdb310981f89c791b7c4206a8b99d9a1f114b6a5a107`  
		Last Modified: Wed, 15 Jan 2020 01:51:03 GMT  
		Size: 70.0 KB (69974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dae8d73c31bd6bb443dd054e2ff7514c3f89f2252ad8f45b02d272a63de3194`  
		Last Modified: Wed, 15 Jan 2020 01:51:01 GMT  
		Size: 922.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8d0280dd236664af1b05a2ecaae933f7235ef8164e6a454a57790b89ee04c1`  
		Last Modified: Fri, 31 Jan 2020 18:08:54 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0710ae5ea4232f4fb12350bbb948ac4972e132824e546be3eea8c703c277d5`  
		Last Modified: Fri, 31 Jan 2020 18:09:16 GMT  
		Size: 194.0 MB (193952613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38d5093e10150c5e6e7b978403e14bd5cef4718b0aa4d1d4d46e7f1370f22c4`  
		Last Modified: Fri, 31 Jan 2020 18:08:55 GMT  
		Size: 3.4 MB (3437344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2de61da85e796082a7c67233ab6100a46dc6feab92bff4ef26ea8baf7ccf09`  
		Last Modified: Fri, 31 Jan 2020 18:08:54 GMT  
		Size: 894.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
