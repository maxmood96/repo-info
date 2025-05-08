## `openjdk:25-ea-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:3f964d3b975f18df961ba083bc096a9bd9ded5bca0b3624edf8938206021b519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `openjdk:25-ea-nanoserver-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull openjdk@sha256:4b81b26d90899edb00590749c155e35ef662f6b96826dc1328598a5bf7fea821
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.6 MB (331576073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8e912a07fe069e89dde27d8d1aa4df1b4db358355c7bd6e3c791f2bb2302a4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Mon, 05 May 2025 17:36:19 GMT
SHELL [cmd /s /c]
# Mon, 05 May 2025 17:36:20 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 05 May 2025 17:36:21 GMT
USER ContainerAdministrator
# Mon, 05 May 2025 17:36:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 05 May 2025 17:36:37 GMT
USER ContainerUser
# Mon, 05 May 2025 17:36:38 GMT
ENV JAVA_VERSION=25-ea+21
# Mon, 05 May 2025 17:36:46 GMT
COPY dir:38c9db30a8dff81edae6bd00112f30e7c6eed8d0f73c59888875d8c30a4a8de1 in C:\openjdk-25 
# Mon, 05 May 2025 17:36:51 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 05 May 2025 17:36:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9635bc147a7cf7815d9348f116cacd975415a199d02d61357d967a665154dd40`  
		Last Modified: Mon, 05 May 2025 17:36:56 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492d96f02510e216edec6dc2cc936db9a94b20c98468d0bb61af77f9a6866b82`  
		Last Modified: Mon, 05 May 2025 17:36:56 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446d06add54d27d68692b4da073d387ba52f04f092e6fc195152bf54da5fc5f2`  
		Last Modified: Mon, 05 May 2025 17:36:56 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cc3c2f9a2b8240ca8f309ef15b11efd398db669e95a6840e37bd5c84dc0f95`  
		Last Modified: Mon, 05 May 2025 17:36:55 GMT  
		Size: 84.3 KB (84260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17dbe5c39933bf7bd887ef0a24be24f912bb099b3d81395ede1291930883be8d`  
		Last Modified: Mon, 05 May 2025 17:36:54 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e76599aad8b709c1e5b59d8de38b9b1c688472f471a62ce14453b0e77acc661`  
		Last Modified: Mon, 05 May 2025 17:36:54 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807ebeebeece88b9d681369be31fdb24fc92ab8749b19d2b34c74daf192ab1b5`  
		Last Modified: Mon, 05 May 2025 17:37:06 GMT  
		Size: 208.8 MB (208848902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1117ba3ba20ecb79eb47c1bfab4edba1a492a50ff9404b1a1221b5c9f5b9f652`  
		Last Modified: Mon, 05 May 2025 17:36:55 GMT  
		Size: 97.6 KB (97641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2696902c14fdd3f554fc8dd9981eddc64aa74ad2363f53d74f9b22cab80842c9`  
		Last Modified: Mon, 05 May 2025 17:36:55 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
