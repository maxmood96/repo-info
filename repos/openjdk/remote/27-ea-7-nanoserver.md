## `openjdk:27-ea-7-nanoserver`

```console
$ docker pull openjdk@sha256:3b7cd5ed2dd374b3179cd75e6899438bc03ea2442ea29bc0a4c4c1d498bd20b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `openjdk:27-ea-7-nanoserver` - windows version 10.0.26100.32370; amd64

```console
$ docker pull openjdk@sha256:4261731c76a926d316e1a433b3e81ffacc7210569849139296c6d192c72c7408
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.7 MB (423681940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603b4b7340332ab549394456916c82f6ffb8a16a7452a9280631a82a6655df8b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 22:06:41 GMT
RUN Apply image 10.0.26100.32370
# Tue, 10 Feb 2026 23:36:33 GMT
SHELL [cmd /s /c]
# Tue, 10 Feb 2026 23:38:15 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 10 Feb 2026 23:38:16 GMT
USER ContainerAdministrator
# Tue, 10 Feb 2026 23:38:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 10 Feb 2026 23:38:17 GMT
USER ContainerUser
# Tue, 10 Feb 2026 23:38:18 GMT
ENV JAVA_VERSION=27-ea+7
# Tue, 10 Feb 2026 23:38:29 GMT
COPY dir:76eebc3ec90e26d61797b94158298a9f6d9a357a62ce831433f35d5314564117 in C:\openjdk-27 
# Tue, 10 Feb 2026 23:38:34 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 10 Feb 2026 23:38:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:77321bd03612cfa46920e790ae0c3b142758a5803ad759fdb406c98b6f2e4ed0`  
		Last Modified: Tue, 10 Feb 2026 22:50:26 GMT  
		Size: 199.3 MB (199251619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ee029b14f013ec4b8c026aa2261c04a1fbb3f25373d8d88ab30292a6f287c6`  
		Last Modified: Tue, 10 Feb 2026 23:37:01 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e1b3bc007ecf03f96505e9a70cc222568b9487359da9d60d3cc8494cff2c8d`  
		Last Modified: Tue, 10 Feb 2026 23:38:40 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b935f7b45a95f2812922f2d625bda9892e94138408b3327975894e4244b5aedb`  
		Last Modified: Tue, 10 Feb 2026 23:38:40 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001d1f95ae6342229b893a900c616178fd7bf3e24fa2daf1922473a7efb3cf6d`  
		Last Modified: Tue, 10 Feb 2026 23:38:40 GMT  
		Size: 73.2 KB (73156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935967275aaa0d5422abd80af24366a799ac1ff2e4d438d7e367dcc2d76348da`  
		Last Modified: Tue, 10 Feb 2026 23:38:38 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e93b3b0f5be119ef20b08ae049734250a01eea3795dcbbfcd07ad3f99e430bb`  
		Last Modified: Tue, 10 Feb 2026 23:38:38 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf1b47df84fddf03bcdf50d4164ee8af7ef4755abd1983d9275ed11840c55e1`  
		Last Modified: Tue, 10 Feb 2026 23:38:55 GMT  
		Size: 224.2 MB (224232733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d788dafd63b0e76248d0dc4eade65c6448b7eb917abbded2ec814d819fff2d04`  
		Last Modified: Tue, 10 Feb 2026 23:38:38 GMT  
		Size: 118.0 KB (117964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7452684d00bfa62d2fba4a825bea16bd39a73133115fdb7dcb80c1193a3820`  
		Last Modified: Tue, 10 Feb 2026 23:38:38 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-7-nanoserver` - windows version 10.0.20348.4773; amd64

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
