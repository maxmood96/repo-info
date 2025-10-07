## `openjdk:26-ea-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:b7fca2b968f8b37b000efc6cfd711fe2942ca27311c2dd6cd022814bd60d2b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `openjdk:26-ea-nanoserver-ltsc2022` - windows version 10.0.20348.4171; amd64

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
