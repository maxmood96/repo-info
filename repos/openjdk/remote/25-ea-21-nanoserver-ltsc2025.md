## `openjdk:25-ea-21-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:26cada59005fa5421e88c440277c571b615e0196de85139f683b6c53200fcbed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `openjdk:25-ea-21-nanoserver-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull openjdk@sha256:d2ac3ed03eb4c2a6845ea4e5fac232104336ba160fd27b985029f89a934b03e0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.2 MB (399188981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3dd09bf09998e6fc2d599f0b681321d0188f863fb3e0994141727ca932670e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Mon, 05 May 2025 18:15:43 GMT
SHELL [cmd /s /c]
# Mon, 05 May 2025 18:15:45 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 05 May 2025 18:15:48 GMT
USER ContainerAdministrator
# Mon, 05 May 2025 18:15:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 05 May 2025 18:15:59 GMT
USER ContainerUser
# Mon, 05 May 2025 18:16:01 GMT
ENV JAVA_VERSION=25-ea+21
# Mon, 05 May 2025 18:16:11 GMT
COPY dir:38c9db30a8dff81edae6bd00112f30e7c6eed8d0f73c59888875d8c30a4a8de1 in C:\openjdk-25 
# Mon, 05 May 2025 18:16:20 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 05 May 2025 18:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 08 May 2025 17:04:55 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafb9f71f8d35a779092d3a9cd50121413cafc540a91ec3fc00148f688304858`  
		Last Modified: Mon, 05 May 2025 18:16:26 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7999c4994c4285bc63ecebaa9b077168bbf2ec0f487f6b4540a2a4226be894ea`  
		Last Modified: Mon, 05 May 2025 18:16:25 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a8c685ac339a5531ee6d2f559b1835c04ef20206e852c574d89df6cbf5af75`  
		Last Modified: Mon, 05 May 2025 18:16:25 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60085c4619c552efa7c80216a91deeabb5eb45f0783bf9af3d5167a36ead87d`  
		Last Modified: Mon, 05 May 2025 18:16:25 GMT  
		Size: 76.5 KB (76510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4c805ea3329b4deecfbeedfd7ca02e146318d7df630fa83e3f6b02c03790d0`  
		Last Modified: Mon, 05 May 2025 18:16:24 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f299a69fc1175bc39bc4a219bdaf17134399dcdf28c1d1386cdb683d0b1e77e8`  
		Last Modified: Mon, 05 May 2025 18:16:24 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94757bc67637d3787e05740f11f27a50138bc32a7539e578af682e49d4a303c4`  
		Last Modified: Mon, 05 May 2025 18:16:38 GMT  
		Size: 208.8 MB (208849514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a0d1f558df9705d1b0cf98a1e627e44ec506764db15d97c080e1fa397b18d2`  
		Last Modified: Mon, 05 May 2025 18:16:24 GMT  
		Size: 114.5 KB (114542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99deacf4608d0f6ffd2a1af961e4b43a7da719e196f999911d2faeee1f06ff9e`  
		Last Modified: Mon, 05 May 2025 18:16:24 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
