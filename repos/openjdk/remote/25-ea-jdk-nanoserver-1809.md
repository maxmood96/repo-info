## `openjdk:25-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:419bc37b0c488a63f91bebd1a1f9241a46866bd77f073f8ac7c0bcb148542b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `openjdk:25-ea-jdk-nanoserver-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull openjdk@sha256:199e70742777497f982da71f50bb112a0a74f18dae94611f6ad5112302c279dd
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.9 MB (318910803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7476a504d2d8eb605c73897878da0c1fe5633a4925d2247e67b4ce0d2cee8e5b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:18:39 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:18:41 GMT
ENV JAVA_HOME=C:\openjdk-25
# Thu, 13 Feb 2025 01:18:42 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:18:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 13 Feb 2025 01:18:45 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:18:46 GMT
ENV JAVA_VERSION=25-ea+9
# Thu, 13 Feb 2025 01:18:53 GMT
COPY dir:d7acfa7ae78317b124adc15f4373b266207aef9ee64c7b37ba0d0b39bb9389f0 in C:\openjdk-25 
# Thu, 13 Feb 2025 01:18:59 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 13 Feb 2025 01:18:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Wed, 12 Feb 2025 21:38:54 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde751c4bc53b6c604b5c8a99be5897187126d9e793ae873e57ee25fbf7eb519`  
		Last Modified: Thu, 13 Feb 2025 04:24:10 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91205a8bdb894e0e58e1d0b036d4991b214aef422a3303ed05c70f8ce76d2497`  
		Last Modified: Thu, 13 Feb 2025 04:24:10 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e96511b9b02efbbae1dcbd361681213436e54fe19463647e53a29225319f68`  
		Last Modified: Thu, 13 Feb 2025 04:24:10 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc9724db27288929ffe00fba733a5efde62eb4a214e7e35df99cea26c958111`  
		Last Modified: Thu, 13 Feb 2025 04:24:10 GMT  
		Size: 80.0 KB (80036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ac56568fc42802a538facfd762a3ecc719d6d8d820299e81bba715c77a0b96`  
		Last Modified: Thu, 13 Feb 2025 04:24:10 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a561e6b74538464c5ec9b6f01cc375b65c00df3ef569d69fdddc44e17abc2bad`  
		Last Modified: Thu, 13 Feb 2025 04:24:10 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6145d4c146b68baf20bf50e2f84817c912e061e986b494d0fe4cfc5882055a`  
		Last Modified: Thu, 13 Feb 2025 04:24:28 GMT  
		Size: 207.5 MB (207491688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efa93d1f6b21fddd6955ae38f3c18e1f7802bc7f136c51940e160342e7a98e5`  
		Last Modified: Thu, 13 Feb 2025 04:24:10 GMT  
		Size: 4.4 MB (4417374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a9587f6560d67a2a7d0c5aac0ddf81b03f86ee14e9f10b5e178be9148c7976`  
		Last Modified: Thu, 13 Feb 2025 04:24:10 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
