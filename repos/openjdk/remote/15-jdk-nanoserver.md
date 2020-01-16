## `openjdk:15-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:74920734b5287ae16e37d4db9bd028427c3e0a81ee9d1aece783cf5a9ac5f844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `openjdk:15-jdk-nanoserver` - windows version 10.0.17763.973; amd64

```console
$ docker pull openjdk@sha256:a1492fd3af8c0c155387d5d25af0d6e1f15ba87917354f11bca02843d2343050
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298513700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42006a0ee8186b0c51d44943526ff1517e0c65cce4f596cab690a419c2237961`
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
# Wed, 15 Jan 2020 23:16:37 GMT
ENV JAVA_VERSION=15-ea+5
# Wed, 15 Jan 2020 23:17:45 GMT
COPY dir:f8bfc4b6f83af8c4b67f8b320cbe7344d894f9a7a96e85d4285e5f15df437cee in C:\openjdk-15 
# Wed, 15 Jan 2020 23:18:11 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Wed, 15 Jan 2020 23:18:12 GMT
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
	-	`sha256:3ed3bd53863b69ec1aa9c5ac9453f04c1f40b973688fc70a1b679bfb3752dbe5`  
		Last Modified: Thu, 16 Jan 2020 00:14:11 GMT  
		Size: 924.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae7e06ab14263fd44115bdb85ee39a445c9e51c8011b1b141f6e0572a9f1b8d`  
		Last Modified: Thu, 16 Jan 2020 00:14:42 GMT  
		Size: 193.9 MB (193937128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdba6d8e8e00b8cc81119344ef930c4a23910e43188ca43adf6c10fa9a8eab3`  
		Last Modified: Thu, 16 Jan 2020 00:14:13 GMT  
		Size: 3.4 MB (3446740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a7a8c8ded190db77e416d504c7afe9d169525ab991abdffe78358d25122c71`  
		Last Modified: Thu, 16 Jan 2020 00:14:11 GMT  
		Size: 917.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
