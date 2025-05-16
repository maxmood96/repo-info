## `openjdk:25-ea-22-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:e2673afb4c8646a78eb35397b58971285f35971886b59a51d66d6c575e61b93a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `openjdk:25-ea-22-nanoserver-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull openjdk@sha256:c4afbf1e2b4362b8ff37363840c395543109570d1942914ebe6f4bcdb4555e44
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.1 MB (331132219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a63403ebbe9b09622baa4cea8e89855d756bddd0f8f9d9a2f5b8a014a15f48c6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 May 2025 19:22:57 GMT
RUN Apply image 10.0.20348.3692
# Wed, 14 May 2025 21:22:24 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 21:22:25 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 14 May 2025 21:22:25 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:22:28 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 May 2025 21:22:28 GMT
USER ContainerUser
# Wed, 14 May 2025 21:22:29 GMT
ENV JAVA_VERSION=25-ea+22
# Wed, 14 May 2025 21:22:36 GMT
COPY dir:d2aeeab016ce5cfb722c90fbb6527341de5d03dac18528814b93fc4084ba77f8 in C:\openjdk-25 
# Wed, 14 May 2025 21:22:42 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 14 May 2025 21:22:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46eb56853bf7d519201d6623d174cec4d04bea0e9d1426f76cc99e437f341f3a`  
		Last Modified: Thu, 15 May 2025 19:27:55 GMT  
		Size: 122.6 MB (122576639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c00bca83a11cc4fa60fed30864e3bd8e5fb69758dd2bc115394605fcc52daa6`  
		Last Modified: Wed, 14 May 2025 21:22:46 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a8e5b93aa2ae84cc35ff4e577e3de900fa198f4884a5f895f6afaed8a85660`  
		Last Modified: Wed, 14 May 2025 21:22:46 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed2148a31003cb6b6c9d5bb636caaddcf5f1d5b66180e1dd7cc394e5888a55e`  
		Last Modified: Wed, 14 May 2025 21:22:46 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e326816d6d7726d85bf1c8a00b56f26fccfd3cf6c448712a4f993493be3e7811`  
		Last Modified: Wed, 14 May 2025 21:22:46 GMT  
		Size: 76.9 KB (76867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd54da081518263083ddb39736f4cb12e829232c5738f35925507a3573e571f`  
		Last Modified: Wed, 14 May 2025 21:22:45 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f374a6b5fd8754590d22c9df7a9f55ecb9f2c1d393143c2433d3a4ec77ba521c`  
		Last Modified: Wed, 14 May 2025 21:22:45 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21b12a7250f27ee5c3674aa7328b9381b36e6d37caeffcad3bb746386cc93f69`  
		Last Modified: Wed, 14 May 2025 21:22:56 GMT  
		Size: 208.4 MB (208365835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e3735577fbc70fc11c9315a371764af552afc9e8cf02bc6225ab2727e13c3a`  
		Last Modified: Wed, 14 May 2025 21:22:45 GMT  
		Size: 106.7 KB (106717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b269613484078069fccfdab448eba3b61cbd6798de13d6d6e6ba35a9459576`  
		Last Modified: Wed, 14 May 2025 21:22:45 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
