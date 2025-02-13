## `openjdk:25-ea-9-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:0fea8b2e7bbe88b3113927c76535a08b1261a8b7ffb08ab67887824261b43dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `openjdk:25-ea-9-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull openjdk@sha256:d761616005afa03fab1617d7bb04a91f7507830a0c709fd66100bfe06923dbdc
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328361129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0f78c798792830aefd231790a286a634568426c26f5443d278530ac3e2d6ca`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Thu, 13 Feb 2025 01:18:20 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:18:21 GMT
ENV JAVA_HOME=C:\openjdk-25
# Thu, 13 Feb 2025 01:18:22 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:18:25 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 13 Feb 2025 01:18:25 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:18:26 GMT
ENV JAVA_VERSION=25-ea+9
# Thu, 13 Feb 2025 01:18:34 GMT
COPY dir:d7acfa7ae78317b124adc15f4373b266207aef9ee64c7b37ba0d0b39bb9389f0 in C:\openjdk-25 
# Thu, 13 Feb 2025 01:18:39 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 13 Feb 2025 01:18:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:49:39 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ded16b24cbe888f5b94fb9cdee90efe89a6f8ba50ae3e689c97962a82b1fc35`  
		Last Modified: Thu, 13 Feb 2025 04:24:06 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0caf4cc603aab32900a2b432e17fd24a0d5263fdcead3fdfea1e767a06e0c3`  
		Last Modified: Thu, 13 Feb 2025 04:24:06 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc746471d97bbf8b341cb410fbb151ff426851c9b8e585305d5a9c0b1a94346`  
		Last Modified: Thu, 13 Feb 2025 04:24:06 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc7c607ba546ed30b6e366e2b1553aa18f9b95bd7d16ac4abaa2e47077304e4`  
		Last Modified: Thu, 13 Feb 2025 04:24:06 GMT  
		Size: 78.7 KB (78676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b1f4d25c5c3767495777d6c47104dc8a151d04d4ca0aa3776a306d07614399`  
		Last Modified: Thu, 13 Feb 2025 04:24:06 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee167e8f0b7b150cf8d97f1a2aecc73c1e12145b03803c9ef2423ede084e944`  
		Last Modified: Thu, 13 Feb 2025 04:24:07 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc29fde919b08a8213849d7d25191c2cbd1067311b1b0b52f495e2350af374b`  
		Last Modified: Thu, 13 Feb 2025 04:24:18 GMT  
		Size: 207.5 MB (207491611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3a4c0a49c05a84694f01e21fdfcc84b8e4ffae5c575afb4470025b89c3bd63`  
		Last Modified: Thu, 13 Feb 2025 04:24:07 GMT  
		Size: 118.0 KB (118042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95cbf379b2560231ff47db9be22a2a1750f549e7cc84ecd6ae0bb2a65721f29c`  
		Last Modified: Thu, 13 Feb 2025 04:24:07 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
