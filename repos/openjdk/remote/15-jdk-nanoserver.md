## `openjdk:15-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:d8f133459aba893325191a8bd27b0092f8b3fedc20d3d368e3dd9a1811b926e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `openjdk:15-jdk-nanoserver` - windows version 10.0.17763.1339; amd64

```console
$ docker pull openjdk@sha256:806b22d09b248e062f99f75a756d97ab8e414ee96f773f24027ce5cee1b57f43
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 MB (295836482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f9f6e0cc9574e68e2389ee136b732a5d137f7586e2c34a0e1269af369d748f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 07 Jul 2020 13:50:07 GMT
RUN Apply image 1809-amd64
# Wed, 15 Jul 2020 01:54:43 GMT
SHELL [cmd /s /c]
# Wed, 15 Jul 2020 02:03:33 GMT
ENV JAVA_HOME=C:\openjdk-15
# Wed, 15 Jul 2020 02:03:34 GMT
USER ContainerAdministrator
# Fri, 24 Jul 2020 18:27:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Fri, 24 Jul 2020 18:27:58 GMT
USER ContainerUser
# Fri, 07 Aug 2020 23:41:36 GMT
ENV JAVA_VERSION=15
# Fri, 07 Aug 2020 23:42:16 GMT
COPY dir:4c7563c7b2e040444227132d1a1c3dae3372f0cf26f8929954f8261ead9f7656 in C:\openjdk-15 
# Fri, 07 Aug 2020 23:42:36 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Fri, 07 Aug 2020 23:42:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dc95608099543221ef539391bfece5c1ce37b97af9da457f5990349cab028a12`  
		Size: 100.9 MB (100895619 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9f6486e4debac36806ed3527d9b1baea75c1a807e26baccdd0a2f521c814273f`  
		Last Modified: Wed, 15 Jul 2020 02:43:55 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c17195adca743b283e9fdf01c1670d33e88c1b7f8ad0ff6a19afa11f90abbdaa`  
		Last Modified: Wed, 15 Jul 2020 02:46:29 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4978cbb8680255360d757c7d46e5a1c7c246047f93257964335958cd1b1307`  
		Last Modified: Wed, 15 Jul 2020 02:46:30 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0cf1f70e8582e4556e8be6e96025ad2d6e372cf6fdaaffb1cda64b76d8150f`  
		Last Modified: Fri, 24 Jul 2020 18:36:57 GMT  
		Size: 69.4 KB (69424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60b2e2d468204c429e90685f0b28fc4a0bcb8c1b50ce01d726ca37b23d8a576`  
		Last Modified: Fri, 24 Jul 2020 18:36:54 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95efa77edf97fe40d654cb03ccf3865eb00e3ebb6fd34d16054c936fafa54dd3`  
		Last Modified: Fri, 07 Aug 2020 23:53:32 GMT  
		Size: 909.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941d206a46673db16fdd97eb16c8ead91c6848220e6c5f1f7ebc2a5b0efa89f5`  
		Last Modified: Fri, 07 Aug 2020 23:53:52 GMT  
		Size: 191.4 MB (191357335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40a601f344277d2dd7808cb84c346757d6076a1b8a9b227d042fb187fccdfb4`  
		Last Modified: Fri, 07 Aug 2020 23:53:34 GMT  
		Size: 3.5 MB (3508794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b60a9899cf7e85d32a299479950eb5354616d49ee8d52c6a79942549c0c93d0`  
		Last Modified: Fri, 07 Aug 2020 23:53:32 GMT  
		Size: 869.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
