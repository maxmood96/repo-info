## `eclipse-temurin:24-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:cca438cf96c7e00d4b1d7dd68a8c50e19e5ed6db71df7a5ebb123676fa5298fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64

### `eclipse-temurin:24-jdk-nanoserver` - windows version 10.0.26100.3781; amd64

```console
$ docker pull eclipse-temurin@sha256:096e750ee3a3e058f12aab3ad5d996cc50b21f29504007a0bb2328da0b6b5e44
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.7 MB (327683796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb80260a830de24398f302feac627f74633280163d33c7c84a08419bbba760bb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Wed, 23 Apr 2025 17:16:47 GMT
SHELL [cmd /s /c]
# Wed, 23 Apr 2025 17:16:49 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 23 Apr 2025 17:16:50 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 23 Apr 2025 17:16:52 GMT
USER ContainerAdministrator
# Wed, 23 Apr 2025 17:16:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 23 Apr 2025 17:16:58 GMT
USER ContainerUser
# Wed, 23 Apr 2025 17:17:08 GMT
COPY dir:ab006ab9903f5de6ad6a158af78f8d39737a3dacdd719a53420635ed01783e4e in C:\openjdk-24 
# Wed, 23 Apr 2025 17:17:17 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 23 Apr 2025 17:17:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 08 May 2025 17:04:55 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780e003820430a52bf2d6eb421ec7291b9bc42aacc50a8e944e2c9b1b19a0adc`  
		Last Modified: Wed, 23 Apr 2025 17:17:25 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b8612bb6455dd3792d9319afb0174c546496f2ca5c7e57d40223f031a692d9`  
		Last Modified: Wed, 23 Apr 2025 17:17:25 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a7497f161786f6a03db41440e02c531965a8f4c4013375befecb78c860aafeb`  
		Last Modified: Wed, 23 Apr 2025 17:17:25 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e50455ce00e39b5e05c6e4921c03348762941ef028ff785728a273627a667d4`  
		Last Modified: Wed, 23 Apr 2025 17:17:25 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9350d79baf9db4ca60fd1c305345b8a55110de01d44b32cca0e41e52045d2669`  
		Last Modified: Wed, 23 Apr 2025 17:17:23 GMT  
		Size: 78.9 KB (78903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2372aba2485e73fe4bbc0cdb85feb5a2b78f98d360e3cc1eb1af4a2fb5e216`  
		Last Modified: Wed, 23 Apr 2025 17:17:23 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a244a10902bc99928296215367bedad9b274f7900ec6e09df0e2f5db54cc5c5`  
		Last Modified: Wed, 23 Apr 2025 17:17:34 GMT  
		Size: 137.4 MB (137364228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120227b18dfc8f8edd6056fcf41388659ae9f0416cedfb3b039a8ddd1ebf498a`  
		Last Modified: Wed, 23 Apr 2025 17:17:23 GMT  
		Size: 92.3 KB (92279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fc3c9cadce2a26db6f497e658255c55d5bc483f22adc8f7103b1a734171261`  
		Last Modified: Wed, 23 Apr 2025 17:17:23 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:24-jdk-nanoserver` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:b9e3acc10c60bc5f2c16fdd64f700b7e712db763a62a130bce2ecd3466201878
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260080172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6fe12b8da29729370a633c734194c3a3655f6f8e59aa3099d5a2d1e5e4f8bf5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Wed, 23 Apr 2025 17:16:00 GMT
SHELL [cmd /s /c]
# Wed, 23 Apr 2025 17:16:01 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 23 Apr 2025 17:16:02 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 23 Apr 2025 17:16:03 GMT
USER ContainerAdministrator
# Wed, 23 Apr 2025 17:16:17 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 23 Apr 2025 17:16:18 GMT
USER ContainerUser
# Wed, 23 Apr 2025 17:16:24 GMT
COPY dir:ab006ab9903f5de6ad6a158af78f8d39737a3dacdd719a53420635ed01783e4e in C:\openjdk-24 
# Wed, 23 Apr 2025 17:16:31 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 23 Apr 2025 17:16:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1170aa6c028d2c2d24b2a8d5abf6644e51aad9460c14b565e165ca51a5f7f8e1`  
		Last Modified: Wed, 23 Apr 2025 17:16:39 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072bcc5edd61e9778eb345dd111bee04fff52d7125f638be4ddd11b293dab858`  
		Last Modified: Wed, 23 Apr 2025 17:16:39 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a872c0c6a7ab1b6a9ac3c1fa2c3817d29fe87569b4a86b9916efe139e85a5a76`  
		Last Modified: Wed, 23 Apr 2025 17:16:39 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1373d900308e582ef196da3b0059ef509ef55ce6d7833623ac74c139c4940db6`  
		Last Modified: Wed, 23 Apr 2025 17:16:39 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c87717a3afee9caa3e6b917b56190a6dfb83d4a85b969b9f8083c036fad94f`  
		Last Modified: Wed, 23 Apr 2025 17:16:37 GMT  
		Size: 72.3 KB (72329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbe2e58d1e86e142c0e7c52350cc471b53d64c95198e632d2d746ddb1942642`  
		Last Modified: Wed, 23 Apr 2025 17:16:37 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a8cb8a9af09212966cae62158f7258d8b24f3602c812301e8cceda6cc458d8`  
		Last Modified: Wed, 23 Apr 2025 17:16:48 GMT  
		Size: 137.4 MB (137364774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d01cc8d8dba9338061acc6b5b13dfec41ffbc38ceaa2d3dd852c4d203b162b`  
		Last Modified: Wed, 23 Apr 2025 17:16:37 GMT  
		Size: 97.7 KB (97660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98dd68b3e80d73f9694c060d6273b4cf86c1cd3a07810d065cfecb7ceaebbdd0`  
		Last Modified: Wed, 23 Apr 2025 17:16:37 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
