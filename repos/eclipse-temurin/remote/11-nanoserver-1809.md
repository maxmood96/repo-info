## `eclipse-temurin:11-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:ed083e8d8315eb4e68035d8dc2ef9177e8d4fd33116b7a81169ac73569982064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `eclipse-temurin:11-nanoserver-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull eclipse-temurin@sha256:f9d4d5220b4ad3dc4fedfde49848e71e770493499cdae8f0e2d3a242da4c356c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301648456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5526874000f840fc8708e0617520a1f369fec717c5e41e4138cdd76e9baaae0f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:11:53 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:11:53 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Thu, 13 Feb 2025 01:11:54 GMT
ENV JAVA_HOME=C:\openjdk-11
# Thu, 13 Feb 2025 01:11:54 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:11:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 13 Feb 2025 01:11:56 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:12:03 GMT
COPY dir:9a97e9a1ce762bb8542962ee0a2b0ca6fa379668e092b80acfc01b297b3b57a6 in C:\openjdk-11 
# Thu, 13 Feb 2025 01:12:07 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 13 Feb 2025 01:12:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee5e44cb2688ba9714bcd16871834fa8451602470e350aa40d00e945513aba6`  
		Last Modified: Thu, 13 Feb 2025 01:12:14 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0282a74c64f75268f379c718c068cd2307c2c2a3aca9b6bc30af8d8a38b68e2a`  
		Last Modified: Thu, 13 Feb 2025 01:12:14 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0bb9eb067940e945e2d2de8ddbadf5d82a6bc72f52cc4ae2f9d0d9f2d39421`  
		Last Modified: Thu, 13 Feb 2025 01:12:14 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0e2e7fb0809c379887c08c14d15b51d61d402d917d83a8ac35cf937d5c0893`  
		Last Modified: Thu, 13 Feb 2025 01:12:14 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6953294570ba3d03408c4f789af998f871679df0146736eb54019bf700eb71`  
		Last Modified: Thu, 13 Feb 2025 01:12:12 GMT  
		Size: 71.0 KB (71022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb932f4e49331dc4cb2df20eb9fa2075498a2d69a5efb9c646ea4fced90fb17`  
		Last Modified: Thu, 13 Feb 2025 01:12:12 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3af8a0e08082525f0805dd2643e73c92931a3df8cbb6ab2fb0b3d1600b2f1b`  
		Last Modified: Thu, 13 Feb 2025 01:12:22 GMT  
		Size: 194.6 MB (194555902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9dc7fbcb9d50edd7186dc23b7262c7cc82955bb980eb6386a36055152edb75c`  
		Last Modified: Thu, 13 Feb 2025 01:12:12 GMT  
		Size: 99.8 KB (99840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3889e6eb9cafca8240e2d15981c0480627d0eb7fca0e39a975ec06166e36a259`  
		Last Modified: Thu, 13 Feb 2025 01:12:12 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
