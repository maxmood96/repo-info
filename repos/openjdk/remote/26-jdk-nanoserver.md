## `openjdk:26-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:1b41624c4d9f63fff47d85d5d8cec1397a8d5174eb1107c9c8685455fb39f56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `openjdk:26-jdk-nanoserver` - windows version 10.0.26100.6584; amd64

```console
$ docker pull openjdk@sha256:0dfadb33f067ecb510f208b3e31e33734350e47748071f96416bf2086ec202c1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.9 MB (414900440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8580453fb6911287339ffd17ed807cedc699877a9750b9afd63881cd83d09c0a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 06 Sep 2025 02:12:39 GMT
RUN Apply image 10.0.26100.6584
# Mon, 06 Oct 2025 22:13:31 GMT
SHELL [cmd /s /c]
# Mon, 06 Oct 2025 22:13:33 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 06 Oct 2025 22:13:34 GMT
USER ContainerAdministrator
# Mon, 06 Oct 2025 22:13:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 06 Oct 2025 22:13:46 GMT
USER ContainerUser
# Mon, 06 Oct 2025 22:13:46 GMT
ENV JAVA_VERSION=26-ea+18
# Mon, 06 Oct 2025 22:14:42 GMT
COPY dir:e6c654e75731597f0435b40aeddf616b12e3e120e9e2343d833678b37f3598da in C:\openjdk-26 
# Mon, 06 Oct 2025 22:14:51 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 06 Oct 2025 22:14:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a75a4ab04983f989d9a1442633d6c3952b863719a00dd77cf160f7055beaded9`  
		Last Modified: Tue, 09 Sep 2025 22:28:08 GMT  
		Size: 193.6 MB (193550846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44b57cc4b440522859eb6ee57d0e0e1c8bd281b3354e9c16746f105992f1aa6`  
		Last Modified: Mon, 06 Oct 2025 22:15:22 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d467f2af8b135dc163bcd5d44e13c95e78b57b43ab26e1d2fa1c84b0ffcada3`  
		Last Modified: Mon, 06 Oct 2025 22:15:22 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d32c6ebd099e1619d23e924a5d3863ccf100474840190bfdda37c59e3786cb`  
		Last Modified: Mon, 06 Oct 2025 22:15:22 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8369d25322d7a357989c85b19f508c36821c227b16db38629776c1ac8ee16fa7`  
		Last Modified: Mon, 06 Oct 2025 22:15:21 GMT  
		Size: 69.4 KB (69354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef84c6d5ef33ad386269b17c5581869260f70e7054870491c013c1d39e8ded4`  
		Last Modified: Mon, 06 Oct 2025 22:15:21 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699045ff0f9205dd933b7ac608f280aeff8323b05b5c45d08cff720f014a6c83`  
		Last Modified: Mon, 06 Oct 2025 22:15:22 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1736b1809dea5973410ba96c301a05f0124029a8a9f9646f0a6d513b101366bd`  
		Last Modified: Tue, 07 Oct 2025 00:24:08 GMT  
		Size: 221.2 MB (221170238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e02b5c49f7786c3978a145c6b7e994a6e3f62430efe2d9c292bf3721609eeba`  
		Last Modified: Mon, 06 Oct 2025 22:15:22 GMT  
		Size: 103.6 KB (103588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bab902ec39106d0ea83345e48beb60e1a73c8e225c5a00528175809f291d11`  
		Last Modified: Mon, 06 Oct 2025 22:15:21 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-jdk-nanoserver` - windows version 10.0.20348.4171; amd64

```console
$ docker pull openjdk@sha256:b6b92892fe43a3a755974a8b39de29d6611ab8afa1116703edd59a94ced06c7e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.1 MB (344106003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4c96e4feb62bd689f89dfb32008352666d8891787931fd0fdd53b5028d791c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 05 Sep 2025 12:57:47 GMT
RUN Apply image 10.0.20348.4171
# Mon, 06 Oct 2025 22:13:58 GMT
SHELL [cmd /s /c]
# Mon, 06 Oct 2025 22:14:00 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 06 Oct 2025 22:14:01 GMT
USER ContainerAdministrator
# Mon, 06 Oct 2025 22:14:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 06 Oct 2025 22:14:16 GMT
USER ContainerUser
# Mon, 06 Oct 2025 22:14:17 GMT
ENV JAVA_VERSION=26-ea+18
# Mon, 06 Oct 2025 22:15:30 GMT
COPY dir:e6c654e75731597f0435b40aeddf616b12e3e120e9e2343d833678b37f3598da in C:\openjdk-26 
# Mon, 06 Oct 2025 22:15:39 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 06 Oct 2025 22:15:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4d91bcff7058a4e51844e56c699b1d7293eed6bf0647068b736e15bccbb8e8ed`  
		Last Modified: Tue, 09 Sep 2025 17:40:59 GMT  
		Size: 122.7 MB (122719927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de08159d436ace9541eaa74781d58acdeaa1d39bf123f57332021430176e6fa6`  
		Last Modified: Mon, 06 Oct 2025 22:16:09 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9e40086ab4eb72d936cb5b65de9c1d2053ad5ab61388e2c1877476ab07eab7`  
		Last Modified: Mon, 06 Oct 2025 22:16:09 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bd7e3168c6a216352e27edf185377b6542931855326746a279338095ce7f11`  
		Last Modified: Mon, 06 Oct 2025 22:16:09 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152c49ae4fd448fa51c2f5db73f6f84f21c1c7513b5bc21cd0edb7bd8c04c283`  
		Last Modified: Mon, 06 Oct 2025 22:16:09 GMT  
		Size: 87.3 KB (87290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029ae25c1f14603318c621afaf7be7426b0fa526a46874b9dc8aea418818585a`  
		Last Modified: Mon, 06 Oct 2025 22:16:08 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b30ec0b5dc116a58a78b631b500a51bbeecbd09733ceba4caaa77a2383012c`  
		Last Modified: Mon, 06 Oct 2025 22:16:09 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafec6a68df84ec8db2ad4425812ede548e245f7b514d31d509356043da290a7`  
		Last Modified: Tue, 07 Oct 2025 00:24:34 GMT  
		Size: 221.2 MB (221170187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61076314fb57b8dfcdbb9e24fba9957799bcb6b580a5b2eba11d757c630ba4ae`  
		Last Modified: Mon, 06 Oct 2025 22:16:08 GMT  
		Size: 122.3 KB (122257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b08698cc986dc9ef31e717c435654041f3e7b116b253c24b38c6353e475ff6`  
		Last Modified: Mon, 06 Oct 2025 22:16:08 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
