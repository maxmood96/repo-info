## `openjdk:24-ea-32-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:c701de8abf2622fb940cf8dc1f53a72833f1d9a7cebd4609747eef68d19777d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `openjdk:24-ea-32-jdk-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:9a994ed0a0c3d917ba2acae8711fc107b101ee1b50221bf74ee259b9a03c4b23
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368211611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5344b4ecf411967ecad16234e5e752c34b145483cef6c9581d3eec11a60402`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Thu, 23 Jan 2025 23:08:34 GMT
SHELL [cmd /s /c]
# Thu, 23 Jan 2025 23:08:36 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 23 Jan 2025 23:08:36 GMT
USER ContainerAdministrator
# Thu, 23 Jan 2025 23:08:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 23 Jan 2025 23:08:49 GMT
USER ContainerUser
# Thu, 23 Jan 2025 23:08:50 GMT
ENV JAVA_VERSION=24-ea+32
# Thu, 23 Jan 2025 23:09:02 GMT
COPY dir:86d923ef445b254beb0a3a098fc78a6b4825f40d8c18f13f837cc4a7df771680 in C:\openjdk-24 
# Thu, 23 Jan 2025 23:09:08 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 23 Jan 2025 23:09:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a11d492babc456466e49db70691893af70094fce4d149e8d5bf2ef3139d81b`  
		Last Modified: Thu, 23 Jan 2025 23:09:13 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef6e76956e5a4dd35013202ee2ab433bc6b189195c47892aa1d80f3b249e965`  
		Last Modified: Thu, 23 Jan 2025 23:09:13 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1664734d9b7983054a8f1b17bc021db9026effd3d02fcedf97e64d9e2747b5`  
		Last Modified: Thu, 23 Jan 2025 23:09:12 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a1b683df1eb5a4f08686db506e2a57ec4c54367c9c20b7cf1bac9cb4a92004`  
		Last Modified: Thu, 23 Jan 2025 23:09:12 GMT  
		Size: 66.7 KB (66716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cb45d0564755af2f5bfa0a3c287e1c6d87c5bb3f26ad8473b46ade25bfd912`  
		Last Modified: Thu, 23 Jan 2025 23:09:11 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef1deae82c8f9f2fd34a71d28fb8ccb27571e65358380b305b0bc385a96b81d1`  
		Last Modified: Thu, 23 Jan 2025 23:09:11 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ba9f04b4fb03757682bffbcb6ada1d507768f47224e375c5e54e9b30dca647`  
		Last Modified: Thu, 23 Jan 2025 23:09:23 GMT  
		Size: 208.5 MB (208488764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d186c6900bc0f7a7d5818a445b7de1a1a00c5e43a7217d4abc7700d0254ffa`  
		Last Modified: Thu, 23 Jan 2025 23:09:12 GMT  
		Size: 4.4 MB (4382323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83dfacd4be28ea0a4de16d4db0a90aa88c41e0da0cc5eb0066227881928f1d5`  
		Last Modified: Thu, 23 Jan 2025 23:09:11 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
