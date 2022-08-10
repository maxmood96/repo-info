## `eclipse-temurin:11-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:84a94b2b98988e643e1eb58fdc6ad57e801b412d30f478313b191536dfd028e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.887; amd64

### `eclipse-temurin:11-nanoserver-ltsc2022` - windows version 10.0.20348.887; amd64

```console
$ docker pull eclipse-temurin@sha256:a2b58ca80a853fb4387fac5292494a956e41b83852d092499c664a7be6d0a981
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 MB (310652895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49db5a80d91b2000a0f0707ea9f4232072dd899b818529d94e4f937284b84ca3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Aug 2022 18:05:23 GMT
RUN Apply image 10.0.20348.887
# Wed, 10 Aug 2022 16:28:17 GMT
SHELL [cmd /s /c]
# Wed, 10 Aug 2022 16:29:53 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Wed, 10 Aug 2022 16:29:54 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 10 Aug 2022 16:29:55 GMT
USER ContainerAdministrator
# Wed, 10 Aug 2022 16:30:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Aug 2022 16:30:18 GMT
USER ContainerUser
# Wed, 10 Aug 2022 16:30:35 GMT
COPY dir:311b50e59d3b0be0ca838f3cd712deaf9388198aeb821aea34d4de0537bd9b6e in C:\openjdk-11 
# Wed, 10 Aug 2022 16:30:55 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Aug 2022 16:30:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ebf439f800cd4c1fccaf4a0545e6bff60caa5141295c8ab81f6c525073c423d`  
		Size: 118.1 MB (118088450 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5f1e06146ab0490d235fe89786637467a4b71853ee428e8740ea6efbc536c47c`  
		Last Modified: Wed, 10 Aug 2022 16:48:40 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4f00e89b19d1ce99daab79ba1bcca3e29ad052342fc52687679c6a9e6bdec0`  
		Last Modified: Wed, 10 Aug 2022 16:49:19 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2afc3c37badc7edc01952be676e9530d9ec3492ccf678d80c67b9548b96bee`  
		Last Modified: Wed, 10 Aug 2022 16:49:19 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6a0937662bedc3cabcdb61a1381d73205583cc8305c01e7a454d9d497173d8`  
		Last Modified: Wed, 10 Aug 2022 16:49:19 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0950a807fee1581948edb4112ce7ac3456a011f5420c15f19c5a429ecac0ac3e`  
		Last Modified: Wed, 10 Aug 2022 16:49:17 GMT  
		Size: 87.6 KB (87631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c5c928d9674ef57d0d85aa68dbff73f5992d86b39e5bc4f23d6db42329416c4`  
		Last Modified: Wed, 10 Aug 2022 16:49:17 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57743c30113de140ed6253db93e7b17fe173a490009f309d1d5c46cfacca0fea`  
		Last Modified: Wed, 10 Aug 2022 16:49:35 GMT  
		Size: 192.4 MB (192370328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb4db824b42bc00c2d20d3fe424f0f123f098592d44c5be9b190d98c954b2a3`  
		Last Modified: Wed, 10 Aug 2022 16:49:17 GMT  
		Size: 99.6 KB (99586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b4ebd7b6108c093033d28af8d577e0327ce4d137cfd41589b22c68087287863`  
		Last Modified: Wed, 10 Aug 2022 16:49:17 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
