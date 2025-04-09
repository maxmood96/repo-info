## `eclipse-temurin:17-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:a7338b3cd2821323d70a0c7bafa17b3579d8edc3baa2b9597b55e91097a2bc11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `eclipse-temurin:17-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull eclipse-temurin@sha256:0c18618a40c751c7f58d001ed05cef787aa9be5c4a0017ec0075958dc310c3cf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308169273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45961a6d973fd03582d8da5f7b2cec4c10dc7c55240c177c48f112904087cc9f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Apr 2025 22:57:50 GMT
RUN Apply image 10.0.20348.3453
# Wed, 09 Apr 2025 01:21:50 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:21:50 GMT
ENV JAVA_VERSION=jdk-17.0.14+7
# Wed, 09 Apr 2025 01:21:51 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 09 Apr 2025 01:21:51 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:21:53 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:21:53 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:22:00 GMT
COPY dir:5f87ec570fea10148b246e6a91d6cf8396b47b1e19a7e8d79bcea78e84a1d159 in C:\openjdk-17 
# Wed, 09 Apr 2025 01:22:04 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Apr 2025 01:22:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5caa30147a287e99992660f7f85276c53fe3299503a06c47d476387410721453`  
		Last Modified: Wed, 09 Apr 2025 01:13:36 GMT  
		Size: 120.7 MB (120736312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030e1afded150e24995ef20f54830bdcd9294733704595352867a17a77a07885`  
		Last Modified: Wed, 09 Apr 2025 01:22:10 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b2087112539514015589da1695bf277a784b3946d7955faa4dc33e2569ad3f`  
		Last Modified: Wed, 09 Apr 2025 01:22:10 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d09e3ac9e0c9f31817f9d6dbf6e841c2955bca338f7b7be651b5a198c5dff0`  
		Last Modified: Wed, 09 Apr 2025 01:22:10 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad57c38adf09d2e37beb06ff7d1d66008c5f62c22e7629fdc924bafa4b11f49`  
		Last Modified: Wed, 09 Apr 2025 01:22:10 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744ec92d5da057e6cb9e4dc3cdf51f67a3aeed4c62fb47c7917c6ef6ea9994ff`  
		Last Modified: Wed, 09 Apr 2025 01:22:09 GMT  
		Size: 75.4 KB (75431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193b0317ae8a09901d970d326d42c08f8111689e55d19d6fe25de529dcccd9c5`  
		Last Modified: Wed, 09 Apr 2025 01:22:08 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e450494f5b17c13a1dc8d00752d611f12893eb024cdbf9e5bcf113e9b2022bb`  
		Last Modified: Wed, 09 Apr 2025 01:22:19 GMT  
		Size: 187.2 MB (187233472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a5f5c7efe3aa83570b17bbfaa7cfe209517f7bb8aaf10b096457ff39f557032`  
		Last Modified: Wed, 09 Apr 2025 01:22:09 GMT  
		Size: 117.9 KB (117881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ccd6e8f8229010b42bf898bedd3e5dd568c4a0596e9fced055c4ce7dfef0cb`  
		Last Modified: Wed, 09 Apr 2025 01:22:09 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
