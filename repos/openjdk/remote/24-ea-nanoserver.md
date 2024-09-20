## `openjdk:24-ea-nanoserver`

```console
$ docker pull openjdk@sha256:bb065accf3abd3a3b0803cfd95f7cffa88d70d0172610033da7b2df7d49b6b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `openjdk:24-ea-nanoserver` - windows version 10.0.17763.6293; amd64

```console
$ docker pull openjdk@sha256:b4a7f354c8a5324955cbae47e8196e5bc24d924387eb5ff5902d61659ec059bf
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.3 MB (367302645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a772760c6f118777da26a0b6f9db6bebf69f86d7cd7f8894f1402f9e36943a18`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Fri, 20 Sep 2024 18:49:57 GMT
SHELL [cmd /s /c]
# Fri, 20 Sep 2024 18:49:59 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 20 Sep 2024 18:50:00 GMT
USER ContainerAdministrator
# Fri, 20 Sep 2024 18:50:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 20 Sep 2024 18:50:13 GMT
USER ContainerUser
# Fri, 20 Sep 2024 18:50:13 GMT
ENV JAVA_VERSION=24-ea+16
# Fri, 20 Sep 2024 18:50:22 GMT
COPY dir:57b8deb20b6280d804fec4507fa48f4d16ae437ff9b34f9497291d0f001cd213 in C:\openjdk-24 
# Fri, 20 Sep 2024 18:50:28 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 20 Sep 2024 18:50:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f797423a0d1c84bf7059bb78be6fd32bd4ac12766a49ce8105d887ba258c8b`  
		Last Modified: Fri, 20 Sep 2024 18:50:33 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa84a7f759136c205eebbf90843b76b2a1dee9755af8f48bb40238807bc8d3c`  
		Last Modified: Fri, 20 Sep 2024 18:50:32 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3610e4df3b2c840ac76d201288da266b995b4b07077bb74e9541f6e92c07b74`  
		Last Modified: Fri, 20 Sep 2024 18:50:32 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe63b337c3eb42721c14e20b107ca521c3ae3ff654a64708f2a5f49f46d1a27`  
		Last Modified: Fri, 20 Sep 2024 18:50:32 GMT  
		Size: 67.6 KB (67574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02ee1bb021307b69208adac962ff9a6c656597447d778f5ec1f0e295bbdaa70`  
		Last Modified: Fri, 20 Sep 2024 18:50:31 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae63002e7e20f727a191e33c6955ab6daa5ae4ca53824adf244fb05bc2fe0ed`  
		Last Modified: Fri, 20 Sep 2024 18:50:31 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c3fdeab355bead7066efd15ab2ad2e359cebc6758672c092288d92ec6b2403`  
		Last Modified: Fri, 20 Sep 2024 18:50:42 GMT  
		Size: 207.7 MB (207675430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c9bd1b5d380d9f64686c1a51349a862886b6b8c9657c162b37446a30cffafa`  
		Last Modified: Fri, 20 Sep 2024 18:50:32 GMT  
		Size: 4.5 MB (4472394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10aa0cb382ace9eb4b46e3c943e8fe0a9a03ecc20a55ac0cec5fe49e70c3e74e`  
		Last Modified: Fri, 20 Sep 2024 18:50:31 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
