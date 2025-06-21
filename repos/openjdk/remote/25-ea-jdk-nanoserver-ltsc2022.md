## `openjdk:25-ea-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:a7e65dc8ddc0616aef630fd579e8de7bd86b8a142ef1ad451996f56f0d378153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `openjdk:25-ea-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull openjdk@sha256:108ac5813f97e49f76e40efb4a988af37eb0588b7c9ce389cc2278a77aae83bd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.2 MB (341180306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f30cd1e8e9d7835788dcee1113619522f2f410a2f39b9b76ef05e63026451e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Sat, 21 Jun 2025 01:08:31 GMT
SHELL [cmd /s /c]
# Sat, 21 Jun 2025 01:08:32 GMT
ENV JAVA_HOME=C:\openjdk-25
# Sat, 21 Jun 2025 01:08:33 GMT
USER ContainerAdministrator
# Sat, 21 Jun 2025 01:08:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 21 Jun 2025 01:08:52 GMT
USER ContainerUser
# Sat, 21 Jun 2025 01:08:52 GMT
ENV JAVA_VERSION=25-ea+28
# Sat, 21 Jun 2025 01:09:03 GMT
COPY dir:5401461bb1e2d6bb9fab71a6bf196682408eddda480d435a025c18a8000305e3 in C:\openjdk-25 
# Sat, 21 Jun 2025 01:09:13 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 21 Jun 2025 01:09:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7699290e6c55485b018a488cb21ba7c92d57e98574caaeea596fa1c1e80b86ca`  
		Last Modified: Sat, 21 Jun 2025 01:11:00 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8caa18e3bcc4a7af5c77de9f0a8cc2a3a9b067f6f18fe46be015bc09afb6c730`  
		Last Modified: Sat, 21 Jun 2025 01:11:01 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35df83b81c0d26fa6f7434d303685c2d4faa7f17cc69dae4e2fb0ba0daa3fb2e`  
		Last Modified: Sat, 21 Jun 2025 01:16:56 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48708de65cc314da0504e014038d646c474f48695135c1c92fd97566209b5c35`  
		Last Modified: Sat, 21 Jun 2025 01:16:59 GMT  
		Size: 87.2 KB (87155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80718010ae623b7d7dd484d3ab19a2fbd06ac8921cc26cc05bde77d9679db7d0`  
		Last Modified: Sat, 21 Jun 2025 01:17:03 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2322effcce411e414304e8f2fea2786dfedfdc5a4afba29490750c959401e8a3`  
		Last Modified: Sat, 21 Jun 2025 01:17:05 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc650fefd966461bd0c1ff89636b4f3047a219e3d0f59b9c931fb4867eae0b3`  
		Last Modified: Sat, 21 Jun 2025 03:24:13 GMT  
		Size: 218.4 MB (218448541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c723303a49be6522e317d1ea342eff8164f8aef96038bb5b823a466f6f58d866`  
		Last Modified: Sat, 21 Jun 2025 01:17:08 GMT  
		Size: 97.9 KB (97906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2cd839e5375013049122511c4d19a58d537306b4e6301ad23c49343579bb363`  
		Last Modified: Sat, 21 Jun 2025 01:17:12 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
