## `eclipse-temurin:23-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:f9d379705756b16cc458a218bb6306d8a70849eb65a8720e40809a3a5a1a20d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:23-nanoserver` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:62638293d16643ceed239c0c8251e64474423a545bc4ff7f1253541b680b31f4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.3 MB (409336052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ddc8d5cd794313834f79e6bb0625d00d90dc14bc9db4932ab8389ae3fcffe7b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Wed, 22 Jan 2025 19:34:52 GMT
SHELL [cmd /s /c]
# Wed, 22 Jan 2025 19:34:52 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 22 Jan 2025 19:34:53 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 22 Jan 2025 19:34:53 GMT
USER ContainerAdministrator
# Wed, 22 Jan 2025 19:34:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 22 Jan 2025 19:34:56 GMT
USER ContainerUser
# Wed, 22 Jan 2025 19:35:03 GMT
COPY dir:997f391ddfc9feaa4d1b725e1babc077a76dd78201dd489cc8f03fe767c19cd0 in C:\openjdk-23 
# Wed, 22 Jan 2025 19:35:10 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 22 Jan 2025 19:35:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d22ecd46f907c71487b358f1e7d6fdb118b99254fff2017c48e61923db7c43`  
		Last Modified: Wed, 22 Jan 2025 19:35:16 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5959b8753e08fefc422949e00dd50b69f12c7afc4f060e21d7cb328ef830c498`  
		Last Modified: Wed, 22 Jan 2025 19:35:16 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9959b6a28f6e9c73a01ee70d1ee9b0e7ed9ad79708632222bcbbbac0d2f93f08`  
		Last Modified: Wed, 22 Jan 2025 19:35:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d36961fb2b2a4da0b87e5c0cbb97c32776539d2bfe4f28f22747b73bb7c57d1`  
		Last Modified: Wed, 22 Jan 2025 19:35:16 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5693ce293f450a7ba0fbeb3c56865d93923063a156bbf7f64174ad43a505a4c5`  
		Last Modified: Wed, 22 Jan 2025 19:35:14 GMT  
		Size: 76.2 KB (76154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60977d3727568d8efd30a6a9de0c8bcd64d32fc03f8ef85f71dbba7d26af278a`  
		Last Modified: Wed, 22 Jan 2025 19:35:14 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cfc20225b7c5f4a37236ec25a8157146b0cd17334e538f7465fc712cb40d3d`  
		Last Modified: Wed, 22 Jan 2025 19:35:27 GMT  
		Size: 210.1 MB (210105881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5d455da88e3829365d95908eb5ee60f8e23d9f46ae39133bb281580db5cbaf`  
		Last Modified: Wed, 22 Jan 2025 19:35:14 GMT  
		Size: 93.5 KB (93476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5840a3d7243ce114e16b8cc74811d09ca9a1843792f8028b06e6ab1b5c57402`  
		Last Modified: Wed, 22 Jan 2025 19:35:14 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-nanoserver` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:b1c6b1dec4a557a83177dfd3cf22137ccc042b17018f87d0b181dda70b3de72f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.0 MB (330956998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e87831c021afa214df535e1726b53588820674f8044a709f1d69d93919f576`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Wed, 15 Jan 2025 18:04:45 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2025 18:04:46 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 15 Jan 2025 18:04:46 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 15 Jan 2025 18:04:47 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 18:04:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jan 2025 18:04:50 GMT
USER ContainerUser
# Wed, 15 Jan 2025 18:04:56 GMT
COPY dir:997f391ddfc9feaa4d1b725e1babc077a76dd78201dd489cc8f03fe767c19cd0 in C:\openjdk-23 
# Wed, 15 Jan 2025 18:05:02 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 15 Jan 2025 18:05:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ffecce690777f0472281a7f5b9295c2c4683edc03aeb9ff32a54d48f65e660`  
		Last Modified: Wed, 15 Jan 2025 18:05:06 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff130bfce978d49a05b3ab66ff0fbc27a1740683bc562a0569248797e65017a`  
		Last Modified: Wed, 15 Jan 2025 18:05:06 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5df21e3a8956a9325000ebb45e7b53df0fe80bbe2da3fe3e8ea26dc28a9409`  
		Last Modified: Wed, 15 Jan 2025 18:05:06 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23362ce95183b58f31ecb7b6514f05c5ec9fdebad93ad9d3824fbd968c488afd`  
		Last Modified: Wed, 15 Jan 2025 18:05:06 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7962b3b1a3a828e6c63f05583d707458e99920f80dce216511cec71f046923`  
		Last Modified: Wed, 15 Jan 2025 18:05:05 GMT  
		Size: 76.2 KB (76208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e43e89e40d9ab94c31a368ee9a722f3af179f1b9928e90decab1c4a9cb00cd5`  
		Last Modified: Wed, 15 Jan 2025 18:05:05 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a35cb80f9f2bb533dde6bb63913a483404eb9d0209d2789feeb4ffe45bbd4a3`  
		Last Modified: Wed, 15 Jan 2025 18:05:16 GMT  
		Size: 210.1 MB (210105816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb94dd9038f9dd2c02a0b728a0c7b3678c2bd51dd418361ab7f6d42f162a482c`  
		Last Modified: Wed, 15 Jan 2025 18:05:05 GMT  
		Size: 107.2 KB (107237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2179edc90888ab3d33db146b39e74709c3571451bca9990b1e6cfac21822c1bd`  
		Last Modified: Wed, 15 Jan 2025 18:05:05 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:23-nanoserver` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:5e4cda68849976d1c040120d8ff2dc3feaf33a0a27ea993341ed1ea85b19a006
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.6 MB (369605336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdaba62bf2f5b42831c34b3f9393d76fc54c1e84a365a29b43d8b0846bd5b49a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 18:01:14 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2025 18:01:16 GMT
ENV JAVA_VERSION=jdk-23.0.1+11
# Wed, 15 Jan 2025 18:01:16 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 15 Jan 2025 18:01:17 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 18:01:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jan 2025 18:01:20 GMT
USER ContainerUser
# Wed, 15 Jan 2025 18:01:29 GMT
COPY dir:997f391ddfc9feaa4d1b725e1babc077a76dd78201dd489cc8f03fe767c19cd0 in C:\openjdk-23 
# Wed, 15 Jan 2025 18:01:34 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 15 Jan 2025 18:01:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830c6182fadf16f749358d2a2343828611c30059fac7b1bc230972450a304dc9`  
		Last Modified: Wed, 15 Jan 2025 18:01:39 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b1ddc3f230807da1b8af3776ecc744cc3911d8e0861c8cdf3500c77352d7f6`  
		Last Modified: Wed, 15 Jan 2025 18:01:39 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37c03863d7a681f9515e0443158c2dc5606a18d3da2b09e2908349463379b4f`  
		Last Modified: Wed, 15 Jan 2025 18:01:38 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cdcf2952a2f034607d21e99bc7a7b7f5a78ee8403d7b5e4e618c112de8b74ec`  
		Last Modified: Wed, 15 Jan 2025 18:01:39 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3af3219d0ea4734b1db0427fd6c5bf14bf4e3fb143b285052ba26622f9eec9c`  
		Last Modified: Wed, 15 Jan 2025 18:01:38 GMT  
		Size: 74.9 KB (74906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ad7f8bd7b1ecf548f12710ac3ba9e573a33fdba6a087cb2c826e070c12cac1`  
		Last Modified: Wed, 15 Jan 2025 18:01:38 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8569ac4d25604d7fe0ebaf067ab442b99abd8bc527af470c8465ae9248b9a89a`  
		Last Modified: Wed, 15 Jan 2025 18:01:51 GMT  
		Size: 210.1 MB (210105693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e26390405cb47cb98cb58d04c557a684e844966364c680d71d20be58c65ef51`  
		Last Modified: Wed, 15 Jan 2025 18:01:38 GMT  
		Size: 4.2 MB (4150922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e905aa290d0d39e173ceeca1db9883855075c414e98cb686f8add69d25b8a47`  
		Last Modified: Wed, 15 Jan 2025 18:01:37 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
