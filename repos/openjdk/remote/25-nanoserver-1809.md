## `openjdk:25-nanoserver-1809`

```console
$ docker pull openjdk@sha256:f89384ee338e9cf309431de2759f95a55f641a571f8144531c988fe3c6e8ccd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `openjdk:25-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:5efed6438831a1a670f4a4cc6d4960501696bf0ad108eb736476b13ec87eae17
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.2 MB (367224289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5b6931cebb69171b3aa12326eb423b2ef9e2842e95b94fb930d047f8fcd075`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Tue, 11 Feb 2025 01:28:06 GMT
SHELL [cmd /s /c]
# Tue, 11 Feb 2025 01:28:07 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 11 Feb 2025 01:28:08 GMT
USER ContainerAdministrator
# Tue, 11 Feb 2025 01:28:28 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 11 Feb 2025 01:28:29 GMT
USER ContainerUser
# Tue, 11 Feb 2025 01:28:29 GMT
ENV JAVA_VERSION=25-ea+9
# Tue, 11 Feb 2025 01:28:41 GMT
COPY dir:d7acfa7ae78317b124adc15f4373b266207aef9ee64c7b37ba0d0b39bb9389f0 in C:\openjdk-25 
# Tue, 11 Feb 2025 01:28:47 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 11 Feb 2025 01:28:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Wed, 15 Jan 2025 07:23:16 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0e98901daf448d7b7108791c075e7bd537617e8aa81f78703d15c858edfc9f`  
		Last Modified: Wed, 12 Feb 2025 21:50:25 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14889923c476e830c372226162661ce115791175644cfa35951e721e5c744d2`  
		Last Modified: Wed, 12 Feb 2025 21:50:26 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1591cbf85d73773982923a2a341761d819e926cfe48908e20556145960b3c6b9`  
		Last Modified: Wed, 12 Feb 2025 21:50:27 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a476cae9e0671f0de4517848c7a2520bfd704ecb583625436829bf2630378bab`  
		Last Modified: Wed, 12 Feb 2025 21:50:28 GMT  
		Size: 74.8 KB (74794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59628c56a214178e0380378505a642f218f241c8db0d9feac4fec44a659fc1a6`  
		Last Modified: Wed, 12 Feb 2025 21:50:30 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8278cf74fdbe48f0776671e711ca04c2a34a8ba2041cfa7d73b60ff6d63c4bc3`  
		Last Modified: Wed, 12 Feb 2025 21:50:30 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528a5f86ba034bb954587cb793ba29f63217644a5a47b95c8f590585b5ff5609`  
		Last Modified: Tue, 11 Feb 2025 01:29:02 GMT  
		Size: 207.5 MB (207492295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c69a57d05662ccf2bb4f9f154ab8a3ca9e1c8725c11a688d1495ff51abf627`  
		Last Modified: Wed, 12 Feb 2025 21:51:06 GMT  
		Size: 4.4 MB (4383244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594f46864ebf14deb7600287c9f7c1a9d43e724097679f8713f2f400c11b9f2f`  
		Last Modified: Wed, 12 Feb 2025 21:51:08 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
