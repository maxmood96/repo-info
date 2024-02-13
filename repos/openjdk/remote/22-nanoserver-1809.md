## `openjdk:22-nanoserver-1809`

```console
$ docker pull openjdk@sha256:cf5790d7875a49e642ce70b50f49ca510b65691af22ceef881a93bcf31e73f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `openjdk:22-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull openjdk@sha256:d1d5d6cd7ab41a7f30961a2842fcbc240bb0b2a51548fd4d0c63eff0d8101022
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305856792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3efce77e7512c46d7e8c8a92036d680c5c42071bd48804e048afdae93552c90`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Mon, 12 Feb 2024 22:56:00 GMT
SHELL [cmd /s /c]
# Mon, 12 Feb 2024 22:56:02 GMT
ENV JAVA_HOME=C:\openjdk-22
# Mon, 12 Feb 2024 22:56:03 GMT
USER ContainerAdministrator
# Mon, 12 Feb 2024 22:56:19 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 12 Feb 2024 22:56:20 GMT
USER ContainerUser
# Mon, 12 Feb 2024 22:56:20 GMT
ENV JAVA_VERSION=22
# Mon, 12 Feb 2024 22:56:29 GMT
COPY dir:ce7c8053267780a9233f43fd4d9a18cc1368b2bafecd86f958b1f78643bbb9b8 in C:\openjdk-22 
# Mon, 12 Feb 2024 22:56:35 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 12 Feb 2024 22:56:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f9879f6fde6b0fbbbd1d09d50cef813e06f91165865843ab1346e0cba59155`  
		Last Modified: Mon, 12 Feb 2024 22:56:40 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705c945b0e6641f7e715e77246e6933f4288bfcdc06544db6f4b2d112f355e44`  
		Last Modified: Mon, 12 Feb 2024 22:56:39 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832dfd5c5c932958b28d34c5b2342b9281535fad02cbdc80eefe21105c07fc35`  
		Last Modified: Mon, 12 Feb 2024 22:56:39 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21a36147ea038f1baecc5bf9fcbaccb127a08310e985a4a634926f36ff4d6b3`  
		Last Modified: Mon, 12 Feb 2024 22:56:39 GMT  
		Size: 67.8 KB (67781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3eb1407435535ac3651b9e2aa3b8a3b7b09ad9224d6c6beed51c0a8661bb55`  
		Last Modified: Mon, 12 Feb 2024 22:56:38 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f820dcdf301a7da30548a2155457c9999734d7c33bbcd8b2208360aa78fef39e`  
		Last Modified: Mon, 12 Feb 2024 22:56:38 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76a2d385f315b0900e376628f68a4832e3918b67634ee656096a36c0394c6c8`  
		Last Modified: Mon, 12 Feb 2024 22:56:49 GMT  
		Size: 197.4 MB (197366863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebacf58004a6ee9e75548a2ca230a015db2a7d02d9606968e48731a93dc1806c`  
		Last Modified: Mon, 12 Feb 2024 22:56:38 GMT  
		Size: 3.8 MB (3824688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2af3f00ee43683f39151dbf0e4abe1bae0b06b49ecc3ee939a99864db59d4d`  
		Last Modified: Mon, 12 Feb 2024 22:56:38 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
