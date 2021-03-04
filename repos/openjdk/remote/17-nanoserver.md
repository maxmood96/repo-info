## `openjdk:17-nanoserver`

```console
$ docker pull openjdk@sha256:906fc8f65541bce517a69e50b8b5ea2870f9b603311c064155dd1d5ea08a58e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64

### `openjdk:17-nanoserver` - windows version 10.0.17763.1757; amd64

```console
$ docker pull openjdk@sha256:96c9c328744bfb2b21561306f5595f9640fa7c6db6a36173c00f05631189914e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286261462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4152a9f24d813cbf2d394154086e84fd087fd3f5ed7c5068a2c34b7efe63d2e1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 02 Feb 2021 13:06:30 GMT
RUN Apply image 1809-amd64
# Wed, 10 Feb 2021 16:45:48 GMT
SHELL [cmd /s /c]
# Wed, 10 Feb 2021 16:45:49 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 10 Feb 2021 16:45:49 GMT
USER ContainerAdministrator
# Wed, 10 Feb 2021 16:46:03 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Feb 2021 16:46:04 GMT
USER ContainerUser
# Wed, 03 Mar 2021 23:19:34 GMT
ENV JAVA_VERSION=17-ea+12
# Wed, 03 Mar 2021 23:19:52 GMT
COPY dir:e90aa80169589c57ed7bec5bf70db5d188379b2ffb181f82a330953778f3c3dd in C:\openjdk-17 
# Wed, 03 Mar 2021 23:20:16 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 03 Mar 2021 23:20:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ba17af31b9276ee11fdf859681b442db50979a39eff4cea2a559a5755cedbe01`  
		Size: 101.4 MB (101406193 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:89effbaeeb74323a670701c3b9dac248927e603ffb2d7efed14d993d32f7c183`  
		Last Modified: Wed, 10 Feb 2021 17:17:35 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba245c3ca8dc95a5fefadb2d7b2366434552cc96ad3951f7028404924978fe3`  
		Last Modified: Wed, 10 Feb 2021 17:17:35 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1331b1edc6cf93ddcbfd0ea0179ca55d1bc1fd44fee36a6d4260248d6207a6`  
		Last Modified: Wed, 10 Feb 2021 17:17:35 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ea90039b4b8e858352f401598e9a3aab5416bb5c88d71cc86d8cd325fe8586`  
		Last Modified: Wed, 10 Feb 2021 17:17:34 GMT  
		Size: 68.2 KB (68240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612927d1022d536248e669e8c4abbee53b84db28247493cf7238816707bc0e1e`  
		Last Modified: Wed, 10 Feb 2021 17:17:32 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79219a10daa7bc3eb955bd8388e557e7a5917f598d757a65076445eccad9edc7`  
		Last Modified: Wed, 03 Mar 2021 23:28:07 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1553964c9a12be991495d195290e1bda9efa6e2124410c68ef0083cdfaa28a0`  
		Last Modified: Wed, 03 Mar 2021 23:28:27 GMT  
		Size: 181.1 MB (181089231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20dbfae85f20fb91023e8e1ea9170529450b34f637455e4c68583c64d57d64d`  
		Last Modified: Wed, 03 Mar 2021 23:28:08 GMT  
		Size: 3.7 MB (3691047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1adc83222d0512ad75157aa478cb051711fad53c2cf87c29e97569d8878d4349`  
		Last Modified: Wed, 03 Mar 2021 23:28:07 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
