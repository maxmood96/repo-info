## `openjdk:25-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:69904c98ce4dddde389a4dcd8ccf2271a75eec41ffa68ea73d49343beaa01285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `openjdk:25-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull openjdk@sha256:ee65e72bc4f9e80b3c7ae13e4aaab9763c0fa32f849c7fc172302f9dc522f2ec
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.8 MB (410787550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6241377a5ae8c00634d418c6d158d87f0f901be1beb94d93fddad0472f24e4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 07 Jun 2025 15:19:59 GMT
RUN Apply image 10.0.26100.4349
# Mon, 30 Jun 2025 18:14:42 GMT
SHELL [cmd /s /c]
# Mon, 30 Jun 2025 18:14:43 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 30 Jun 2025 18:14:44 GMT
USER ContainerAdministrator
# Mon, 30 Jun 2025 18:14:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 30 Jun 2025 18:14:48 GMT
USER ContainerUser
# Mon, 30 Jun 2025 18:14:49 GMT
ENV JAVA_VERSION=25-ea+29
# Mon, 30 Jun 2025 18:14:58 GMT
COPY dir:42ea662c144d042c5c993e4ad460b12969ac9552d3e3695a34b691e1b9c80eac in C:\openjdk-25 
# Mon, 30 Jun 2025 18:15:05 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 30 Jun 2025 18:15:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:709fa8bff22087ae5c45c65a3b0777eb6ee12afd1b773aece2a322e84b66b1d1`  
		Last Modified: Tue, 10 Jun 2025 22:41:49 GMT  
		Size: 192.1 MB (192082516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b936cb450ccc6032edd1a3cb44bebaa8c2fe0ee2bfe559522089f6acd549b0`  
		Last Modified: Mon, 30 Jun 2025 18:15:53 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7235d886459d0899149f553e67fd5e8d18b35a1bf8692cfd3f0e1e9714a545e`  
		Last Modified: Mon, 30 Jun 2025 18:15:53 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808ce20c38dee62b31cc080104de2f77db83a557c43a457b200e0b2df5e0a9d7`  
		Last Modified: Mon, 30 Jun 2025 18:15:53 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c90f05de2fa9bd84b7d77bd5991e95e35d4200c7605bf8c91990110c2d54030`  
		Last Modified: Mon, 30 Jun 2025 18:15:53 GMT  
		Size: 76.3 KB (76305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1feb3a5a2c169a31b5a7a186fa827267b8e87a67b8287962baf5fd74360955cb`  
		Last Modified: Mon, 30 Jun 2025 18:15:53 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9922fa774122a0d802916432f4cc260e226b408e87574f800090a452747dc1`  
		Last Modified: Mon, 30 Jun 2025 18:15:53 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3bb01ba9adb42180d3130bbf86da4bf5d67f9ee7a0daf7047d9fd0c8a998bc`  
		Last Modified: Mon, 30 Jun 2025 21:24:19 GMT  
		Size: 218.5 MB (218496851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f19e1cadeec5505e20e75c69a8ec510be900b2aaacaa4f61d8e6e179c8bc35`  
		Last Modified: Mon, 30 Jun 2025 18:15:53 GMT  
		Size: 125.6 KB (125565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef48cf7ec026adacb3d1700b30b3c0edb897d371ba274f78cf476479f313a28a`  
		Last Modified: Mon, 30 Jun 2025 18:15:53 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
