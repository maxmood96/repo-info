## `eclipse-temurin:21-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:426d6072163b797ae93a14c47ed95d9b3205e1d6dd166a21382ba33b216eb63e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.20348.2849; amd64

```console
$ docker pull eclipse-temurin@sha256:6fc17671f50ab627fa6e6897bcfaad702a5792d8ced385eeb4f6a6d768c65aca
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170371748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a3f23da1eb17ba3b2345c08d4c329d72d88032596443b5070b498e2abc04d8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 02 Nov 2024 23:34:35 GMT
RUN Apply image 10.0.20348.2849
# Thu, 14 Nov 2024 21:21:03 GMT
SHELL [cmd /s /c]
# Thu, 14 Nov 2024 21:21:04 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Thu, 14 Nov 2024 21:21:04 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 14 Nov 2024 21:21:05 GMT
USER ContainerAdministrator
# Thu, 14 Nov 2024 21:21:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 14 Nov 2024 21:21:08 GMT
USER ContainerUser
# Thu, 14 Nov 2024 21:21:11 GMT
COPY dir:d301f311784d572cc6cc0a5ee90712dcade9d3f8b4a48a0f2df4274582f5072e in C:\openjdk-21 
# Thu, 14 Nov 2024 21:21:15 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:815d6b7f925aef8327c34c34073ae54cc1c82120f1058682eac4c8c14ca21c70`  
		Last Modified: Tue, 12 Nov 2024 22:44:32 GMT  
		Size: 120.6 MB (120604951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc939bb5b42fc3c66067baa0bef316f1b2b9fb00eac9a5d13f607782bedaeb41`  
		Last Modified: Thu, 14 Nov 2024 21:21:20 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e9a4e1c17d9a0c2506d8bc6b8752cb3b1178606e1f456777d6021678cfa9c6`  
		Last Modified: Thu, 14 Nov 2024 21:21:20 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604d2de4a9851b34b40511eba523885be0899e7c3878e79c91d1afe81aa7744b`  
		Last Modified: Thu, 14 Nov 2024 21:21:20 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5361ebd738cabf191fd3d9ca125e8f659bb72bd44c0161ad7d87907762635604`  
		Last Modified: Thu, 14 Nov 2024 21:21:19 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950d5eb8960edd4ab4de5bf17b8b13e2ed702f53439d0dfdb1f135a2702a19b4`  
		Last Modified: Thu, 14 Nov 2024 21:21:19 GMT  
		Size: 75.5 KB (75478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ff20dd828e4c007e0a8de9a1f48ff7b7946e296d8ac9d4e3479eefa35fa0f2`  
		Last Modified: Thu, 14 Nov 2024 21:21:18 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc313c0a253f9c1684fc99dbd7b6238ae389d685105d97d325dc031d809632a4`  
		Last Modified: Thu, 14 Nov 2024 21:21:24 GMT  
		Size: 49.6 MB (49585934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fada55ff0fdcf9296075e31acca5d7d632532716c4b7d06a7ff4182b22a088d3`  
		Last Modified: Thu, 14 Nov 2024 21:21:19 GMT  
		Size: 100.2 KB (100233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.17763.6532; amd64

```console
$ docker pull eclipse-temurin@sha256:af23357222b84c704cc64dc7df74a5bad031dc8c09b857109c439ce922a62ae4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208264390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d074dc9ca580913e81a4c7f59ce2a3c1bff28e6c6be117e8252bc4fb0bd633b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Thu, 14 Nov 2024 21:21:59 GMT
SHELL [cmd /s /c]
# Thu, 14 Nov 2024 21:22:00 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Thu, 14 Nov 2024 21:22:01 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 14 Nov 2024 21:22:01 GMT
USER ContainerAdministrator
# Thu, 14 Nov 2024 21:22:04 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 14 Nov 2024 21:22:04 GMT
USER ContainerUser
# Thu, 14 Nov 2024 21:22:08 GMT
COPY dir:d301f311784d572cc6cc0a5ee90712dcade9d3f8b4a48a0f2df4274582f5072e in C:\openjdk-21 
# Thu, 14 Nov 2024 21:22:13 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895aadcfe2dd8971cec2c2bfe0bcf03d779c992349d4fa7053d3783c6d3b4253`  
		Last Modified: Thu, 14 Nov 2024 21:22:17 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8bfb8815705b9dcdee2a440ca35214c554dba15b0b10e2cf2e52f3253f0d4b`  
		Last Modified: Thu, 14 Nov 2024 21:22:17 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a299b4a94ee1feb3081299fb8656a1a4dfb07d186e945fabff2b9dfdfa5b626`  
		Last Modified: Thu, 14 Nov 2024 21:22:17 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1307a61c2dad2d2d84e9df7431929df0691ca2a53b773828d67f2c7ce2c0069`  
		Last Modified: Thu, 14 Nov 2024 21:22:16 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab93d1a73a923451407a762880f22d9589a5215ff6f3a04e6ce972843f8b0ae`  
		Last Modified: Thu, 14 Nov 2024 21:22:16 GMT  
		Size: 83.9 KB (83910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b9ddfd31046680876b9a96dd9f15a98a38eca74ca99f953f6d572d85f2060f`  
		Last Modified: Thu, 14 Nov 2024 21:22:16 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55824cc37b9999ba5de44e41ef395ec152ed2b60fc8e77ca719e66cba427e8c6`  
		Last Modified: Thu, 14 Nov 2024 21:22:22 GMT  
		Size: 49.6 MB (49588030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4e2bb361526c19f2241f8488ed70fcc32e725692e9c22e7431a59cce4bf673`  
		Last Modified: Thu, 14 Nov 2024 21:22:17 GMT  
		Size: 3.4 MB (3372656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
