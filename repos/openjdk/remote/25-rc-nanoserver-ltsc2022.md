## `openjdk:25-rc-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:b5d60a84ab55102ccba2db3e77e3b2708a408f11ef6a2b5fdabb54ecbe000334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `openjdk:25-rc-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull openjdk@sha256:ea8b86a0d00926c41786823df97517922916cb6af2af0d7be66522aa7e3712c7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.5 MB (341463920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:874808e3719934d6d8b3a4530a3caab7c85464d389e28c17b8e5bdb918457e84`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Wed, 10 Sep 2025 22:18:34 GMT
SHELL [cmd /s /c]
# Wed, 10 Sep 2025 22:22:01 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 10 Sep 2025 22:22:01 GMT
USER ContainerAdministrator
# Wed, 10 Sep 2025 22:22:03 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Sep 2025 22:22:03 GMT
USER ContainerUser
# Wed, 10 Sep 2025 22:22:04 GMT
ENV JAVA_VERSION=25
# Wed, 10 Sep 2025 22:22:16 GMT
COPY dir:af1d593aa380a5189ac7ad7e58ca0fcfe62de322216fccee65cb868225e0c49a in C:\openjdk-25 
# Wed, 10 Sep 2025 22:22:21 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 10 Sep 2025 22:22:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e0ce028103081865bc14b1610899edd5f6a839fc9d1f091fb2e07888198fc6`  
		Last Modified: Wed, 10 Sep 2025 22:19:41 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e7f218dc540942717bc97a22410742171bf34f93acca0512dfa35a64d72f91`  
		Last Modified: Wed, 10 Sep 2025 22:22:49 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a1bebc36fb69171ca3184a4e0206a7247285f6819ecf5562d74fd7a7c378f3`  
		Last Modified: Wed, 10 Sep 2025 22:22:49 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4bc60d39386a24c31b43dddab75d40435a339a89eb7ee44d56cd187ee53573`  
		Last Modified: Wed, 10 Sep 2025 22:22:49 GMT  
		Size: 77.1 KB (77146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5d8dd9bb69d8a239e06ce48bd4cee4c9bc072b3f77d9597ef0871018ff2281`  
		Last Modified: Wed, 10 Sep 2025 22:22:49 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:467f0d899205758adf1f02d40f5f52f5e494693d57d2c363104ab4179c45baa4`  
		Last Modified: Wed, 10 Sep 2025 22:22:49 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b44abe59b0467a4947c68cbf85b2d1a355c9809f3e1879d8edbf69e735e432e`  
		Last Modified: Thu, 11 Sep 2025 00:23:55 GMT  
		Size: 218.6 MB (218552956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60499523164b28844fb7330109569ee3848e7a68e363c8ec76455dba24aa49b6`  
		Last Modified: Wed, 10 Sep 2025 22:22:49 GMT  
		Size: 107.5 KB (107471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e44f5d18b5e26fc8f55686a8ebcd843fc43520be5d8755b4417bb69239f5954`  
		Last Modified: Wed, 10 Sep 2025 22:22:49 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
