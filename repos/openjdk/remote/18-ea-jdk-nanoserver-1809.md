## `openjdk:18-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:46502f345e9398d2aa37f555c8c312137c87042f8c2c8c49eb641b3675640fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2300; amd64

### `openjdk:18-ea-jdk-nanoserver-1809` - windows version 10.0.17763.2300; amd64

```console
$ docker pull openjdk@sha256:16621e6c8f887cdc4051d51ec9804da8cde346b27c0149760c8839fc69530a18
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290171943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06801270526c19e99bb208f438608c109f466f60263db688c1234e4cecb7226`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 04 Nov 2021 00:06:50 GMT
RUN Apply image 1809-amd64
# Wed, 10 Nov 2021 17:13:20 GMT
SHELL [cmd /s /c]
# Wed, 10 Nov 2021 20:31:55 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 10 Nov 2021 20:31:55 GMT
USER ContainerAdministrator
# Wed, 10 Nov 2021 20:32:07 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Nov 2021 20:32:07 GMT
USER ContainerUser
# Tue, 30 Nov 2021 01:23:01 GMT
ENV JAVA_VERSION=18-ea+25
# Tue, 30 Nov 2021 01:23:16 GMT
COPY dir:9c143a28a4dbe238bb5bea772a8df411ed8432e415524d95882af5eea67538a2 in C:\openjdk-18 
# Tue, 30 Nov 2021 01:23:41 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 30 Nov 2021 01:23:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b9dc943b4e8df8f472d444248152fa0920172ec630a60ada316e1603600dd1c7`  
		Size: 102.8 MB (102782944 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e60ec86b90e1492e0e0ed2cbebcf624990a34862e24207343fd85b84b3544c8e`  
		Last Modified: Wed, 10 Nov 2021 18:01:59 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d97d878bac5dd9dcbe1bb5f45ade2111fc77e8d4a5a348163bd9c3ddddbaf0`  
		Last Modified: Wed, 10 Nov 2021 21:11:37 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5a46fd95d3a8e8b5949c49cc0d70b858bddbe38c8c33e0a6a3e0f157d7795a`  
		Last Modified: Wed, 10 Nov 2021 21:11:37 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88539ad3f1fb0ea6957da9a7298c1f6546afbb52b2deb7199763195fca993d98`  
		Last Modified: Wed, 10 Nov 2021 21:11:37 GMT  
		Size: 74.2 KB (74205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d133fe2173015750539b2d0a8fb86dbdbe0c6b44c8d75ddeb714a82814f98e00`  
		Last Modified: Wed, 10 Nov 2021 21:11:33 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3dfac1169043776f30a445c08eb6c57bba5064f83609f9505aff2ef31f6ea3`  
		Last Modified: Tue, 30 Nov 2021 01:33:49 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddaec307e11a83538b928f396ac872b34dc9d2f992ce3e0882d12e78a10549ef`  
		Last Modified: Tue, 30 Nov 2021 01:34:08 GMT  
		Size: 183.8 MB (183791114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104aaae87f2802992f3ac772e2c45d1e9777a822ca3e16b7b2ff16f4d96425cc`  
		Last Modified: Tue, 30 Nov 2021 01:33:52 GMT  
		Size: 3.5 MB (3516828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a8b3f662989bdff5c6e36f45a0c552cfb61dccc185533b557b6b881b7eebbe`  
		Last Modified: Tue, 30 Nov 2021 01:33:49 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
