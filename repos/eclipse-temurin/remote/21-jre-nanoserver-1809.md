## `eclipse-temurin:21-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:d0da9b2d97e13aa0a65687191214228c91c5175d7584283764080910455725cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `eclipse-temurin:21-jre-nanoserver-1809` - windows version 10.0.17763.6532; amd64

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
