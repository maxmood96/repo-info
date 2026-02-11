## `openjdk:27-ea-7-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:536bdd8fb481fef90189cdea933255b60c5c516e1c3ca4760bcce5ee2b68e77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `openjdk:27-ea-7-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull openjdk@sha256:f56914a828349fd085e77100df4ad6c4eefdfdfc08f50cbd3f869a6648eb70bc
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351079821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c11a027d4c029be35e909688b494bb9e0a534aad3c237ff13bca1b168b680e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Wed, 11 Feb 2026 00:15:08 GMT
SHELL [cmd /s /c]
# Wed, 11 Feb 2026 00:15:08 GMT
ENV JAVA_HOME=C:\openjdk-27
# Wed, 11 Feb 2026 00:15:09 GMT
USER ContainerAdministrator
# Wed, 11 Feb 2026 00:15:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 11 Feb 2026 00:15:15 GMT
USER ContainerUser
# Wed, 11 Feb 2026 00:15:16 GMT
ENV JAVA_VERSION=27-ea+7
# Wed, 11 Feb 2026 00:15:54 GMT
COPY dir:76eebc3ec90e26d61797b94158298a9f6d9a357a62ce831433f35d5314564117 in C:\openjdk-27 
# Wed, 11 Feb 2026 00:15:59 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 11 Feb 2026 00:16:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736f9492bdd80947d1b97be5dc0bcb20e7116d1d2515e6c63a79e064c7cbc782`  
		Last Modified: Wed, 11 Feb 2026 00:16:08 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f210103d7ca5cb369e73b1e78396ce34b139520647b0f26d5025019e578ce5f`  
		Last Modified: Wed, 11 Feb 2026 00:16:08 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f541c74ba4fd86762b88de32a40a662c20dc6f14c943e0ed2044472601597e5`  
		Last Modified: Wed, 11 Feb 2026 00:16:08 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e6923cc10aa371ab4bb57e31936e8d69b096f5dcf479df56906275efb2c7014`  
		Last Modified: Wed, 11 Feb 2026 00:16:08 GMT  
		Size: 85.9 KB (85875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b95644a7d904df9d3b876162791fe84d2da62b3b76144d1068d8a6829e70b28`  
		Last Modified: Wed, 11 Feb 2026 00:16:07 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b05bf3d3ac9a52529ba5fb3b00386f2bb6a04060c2ddf12b556c7cbdc3dfe0f`  
		Last Modified: Wed, 11 Feb 2026 00:16:07 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8a64a75ed5aab6a85b05bd5ab6441967584a6fe41b5e9cb8cf4bcafd05dc3a`  
		Last Modified: Wed, 11 Feb 2026 00:16:22 GMT  
		Size: 224.2 MB (224232815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2211e51e3ca716f2d30825ccd86ac05f9bb02439dd8d0d6194dba1b2d7420a4c`  
		Last Modified: Wed, 11 Feb 2026 00:16:07 GMT  
		Size: 108.9 KB (108895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a05540358aa37dc36b8d04702c5ddcd744aa1d28b8140b5b19e4d1d7bda1b7`  
		Last Modified: Wed, 11 Feb 2026 00:16:06 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
