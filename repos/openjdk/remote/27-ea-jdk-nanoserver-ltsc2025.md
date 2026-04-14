## `openjdk:27-ea-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:26fd5611bfc69a75fd3b210a7d3069c3ec2105a9c39a7676a138ed61af088653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `openjdk:27-ea-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull openjdk@sha256:7b7f4768fe38503bfcebbc32595197496d8bc545504119090a0a4872e3f870a9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.4 MB (424402210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a268790e18a74e85cf34da17e8f18ebdeb3c52c1b3b5b8c99323aa7c9d2a244c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Mar 2026 01:45:55 GMT
RUN Apply image 10.0.26100.32522
# Tue, 14 Apr 2026 01:49:59 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2026 01:50:01 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 14 Apr 2026 01:50:03 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 01:50:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 14 Apr 2026 01:50:21 GMT
USER ContainerUser
# Tue, 14 Apr 2026 01:50:22 GMT
ENV JAVA_VERSION=27-ea+17
# Tue, 14 Apr 2026 01:51:34 GMT
COPY dir:0691f65abcad9aa5e8b70bfb251a5fc900e0d4cf82de17dca757301a739d34d1 in C:\openjdk-27 
# Tue, 14 Apr 2026 01:51:44 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 14 Apr 2026 01:51:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:06fab7822816d5f43d6835d07ac8db280fdf81384187f36d8dc43bbb7064a76d`  
		Last Modified: Tue, 10 Mar 2026 20:41:46 GMT  
		Size: 199.4 MB (199409325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91da1d89d7b84e207bc76ccd6265075c393fdd33fa2042b7897589954a7f8fb8`  
		Last Modified: Tue, 14 Apr 2026 01:51:51 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd0d830657bf28567229111aab08bb039012ca2d87dc3457601a3f589c100aa`  
		Last Modified: Tue, 14 Apr 2026 01:51:51 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a00f6f26fa3782083d24decc9799751f5b757f98701131781abe576b9323a295`  
		Last Modified: Tue, 14 Apr 2026 01:51:51 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b5416ea89c24d9ffcd369bdc3c2637d22a99597800ba6e32041aead7e5352e`  
		Last Modified: Tue, 14 Apr 2026 01:51:51 GMT  
		Size: 70.6 KB (70597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338778a3ca711138a21148b61d4e98691119f9c4c074b6b3c95a659a72848614`  
		Last Modified: Tue, 14 Apr 2026 01:51:49 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f299641552201f88c0d230353fc890c283b1a3aebb31d297c911b3470db2e7ea`  
		Last Modified: Tue, 14 Apr 2026 01:51:49 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea10634e93c23a7adf15fdd55735300424e06e1c20bd1666a35064788aaacfb2`  
		Last Modified: Tue, 14 Apr 2026 01:52:04 GMT  
		Size: 224.8 MB (224811669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d39e094fbe3051da7bf59e8a5915b1e6b623bf7214481c02bf23495d388d088`  
		Last Modified: Tue, 14 Apr 2026 01:51:49 GMT  
		Size: 104.3 KB (104269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef9cd8ee3d254ba37a982360f1c2859142ae26776d244d5748d0ff93b923d66`  
		Last Modified: Tue, 14 Apr 2026 01:51:49 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
