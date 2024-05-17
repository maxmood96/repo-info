## `openjdk:23-ea-23-nanoserver`

```console
$ docker pull openjdk@sha256:ebf1bfae9e72d8e93712874e2da1127e55936b554a0864f2fd0336f89ec867e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `openjdk:23-ea-23-nanoserver` - windows version 10.0.17763.5820; amd64

```console
$ docker pull openjdk@sha256:06b6b06c69e4529c6ff62285bb0f3be1e053e112f5b91bd3ce9cdaeac01ccb94
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.6 MB (364555126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c9a9b6365293881be53a721b903004e433ed5b5f5b05ec9ea36e03c6551f45`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Fri, 17 May 2024 19:49:18 GMT
SHELL [cmd /s /c]
# Fri, 17 May 2024 19:49:19 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 17 May 2024 19:49:20 GMT
USER ContainerAdministrator
# Fri, 17 May 2024 19:49:23 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 17 May 2024 19:49:23 GMT
USER ContainerUser
# Fri, 17 May 2024 19:49:24 GMT
ENV JAVA_VERSION=23-ea+23
# Fri, 17 May 2024 19:49:32 GMT
COPY dir:712d4903b6703505dfd33b77fe5c34559bb1f3dcc1f72135fc48036755475a3b in C:\openjdk-23 
# Fri, 17 May 2024 19:49:40 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 17 May 2024 19:49:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceafbe027946b88ee57dfc12ac88ead231fafca4227e4e7ca886c73dcb753ad8`  
		Last Modified: Fri, 17 May 2024 19:49:48 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4497804a02c7b30c0d214bfbe1bd9003af816b7885ff63911269b8befdc022f`  
		Last Modified: Fri, 17 May 2024 19:49:47 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc73335e17b6ffdc9b19f63b2202568cbcd761c7d00dba74e023e0e5272eb5a`  
		Last Modified: Fri, 17 May 2024 19:49:46 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a634df5edd6eeb939f1f910235f1c9f965af0f0fadeb6026fa52287884b167a3`  
		Last Modified: Fri, 17 May 2024 19:49:47 GMT  
		Size: 65.9 KB (65925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eba7919348a5fb017556e8fb9b6e86355f9e294b98d23f07bf456b43fda5bd3`  
		Last Modified: Fri, 17 May 2024 19:49:45 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5a834c4e7ec5c27cf3a1985e73e661b3ab2d2199d305a095366fcc9f5c3b33`  
		Last Modified: Fri, 17 May 2024 19:49:45 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac03b9db642f0bf21d7159d7175f8082b7dfd654e946c490e5635757abaa00c8`  
		Last Modified: Fri, 17 May 2024 19:49:56 GMT  
		Size: 204.6 MB (204562764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fb202352c5acff2dbc42fce88b1f8a20ba59919d7397f712dc105eac831b91`  
		Last Modified: Fri, 17 May 2024 19:49:46 GMT  
		Size: 5.0 MB (4978767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77191f8c74d8f827a5b3f067ed84cf517976b34f7f1f7ac3fe0fc7f6cfbf91de`  
		Last Modified: Fri, 17 May 2024 19:49:44 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
