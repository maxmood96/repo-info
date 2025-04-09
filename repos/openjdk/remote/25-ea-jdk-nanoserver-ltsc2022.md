## `openjdk:25-ea-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:fa60f4fe1a433854e4989b9cb4d93de9c608395ae8c8c8a0c17ba9b93f37c972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `openjdk:25-ea-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull openjdk@sha256:61016fe37abd6e30dcb9115fc0527dbbb04318faa208eca7ad5c6aa6773fdd01
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.9 MB (328890142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d8747fba9c975eb86ac9eb2cc75a49577390263e06ffc043086ef4726ffd30`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Apr 2025 22:57:50 GMT
RUN Apply image 10.0.20348.3453
# Wed, 09 Apr 2025 02:18:54 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 02:18:55 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 09 Apr 2025 02:18:56 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 02:18:58 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 09 Apr 2025 02:18:58 GMT
USER ContainerUser
# Wed, 09 Apr 2025 02:18:59 GMT
ENV JAVA_VERSION=25-ea+17
# Wed, 09 Apr 2025 02:19:06 GMT
COPY dir:31d4a08dd20e935927d81b33c56eb56ceaeead96529382a0c30c5f89fc836ee7 in C:\openjdk-25 
# Wed, 09 Apr 2025 02:19:11 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 09 Apr 2025 02:19:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5caa30147a287e99992660f7f85276c53fe3299503a06c47d476387410721453`  
		Last Modified: Wed, 09 Apr 2025 01:13:36 GMT  
		Size: 120.7 MB (120736312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df9b03ae6e2a08778ef655a3dcf972aba94eed9ab524b6f52b03abcc7f002e7`  
		Last Modified: Wed, 09 Apr 2025 02:19:18 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47cb72baa9dc61dad7e274f15bed055771a75a7af8aeede8be5d0ee5397ad726`  
		Last Modified: Wed, 09 Apr 2025 02:19:18 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c913432bbe18394e4c87496c4c67e35a7287ec84c71deb8c51ec5b4c4a877fa6`  
		Last Modified: Wed, 09 Apr 2025 02:19:17 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af5a4dbc89709592b12dce074f95da6d4e252f0eca6e5a8c2cb158e1ceb9c70`  
		Last Modified: Wed, 09 Apr 2025 02:19:17 GMT  
		Size: 75.6 KB (75633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba95de726f7b7689b7019e904ad2014ba1272304d44a47a4990eaced30a9a916`  
		Last Modified: Wed, 09 Apr 2025 02:19:15 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51228ba257a088ce9286f933c1af2e34275557ade6bc7204e8b32c966915eee`  
		Last Modified: Wed, 09 Apr 2025 02:19:15 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3a4221b088f2dbbd02e6b59f009b733495b2af6c818343ba3724f883a85458`  
		Last Modified: Wed, 09 Apr 2025 02:19:27 GMT  
		Size: 208.0 MB (207954191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab7fc4b960aa5112fbb0e8f4c936b96d67f4dea339bdc1067ab9741ddc5a6ee`  
		Last Modified: Wed, 09 Apr 2025 02:19:16 GMT  
		Size: 117.8 KB (117830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ec581b8b9077c29e173d470b14c1741c084a59aa370dbd3624bd034312a3fb`  
		Last Modified: Wed, 09 Apr 2025 02:19:15 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
