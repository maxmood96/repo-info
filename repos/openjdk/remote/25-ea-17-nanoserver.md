## `openjdk:25-ea-17-nanoserver`

```console
$ docker pull openjdk@sha256:84ce749bcd4731cfd6d474d587a4841b7f1c3280f3050b3e0cffc77f936cae58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `openjdk:25-ea-17-nanoserver` - windows version 10.0.26100.3775; amd64

```console
$ docker pull openjdk@sha256:5c51639e2f3e5857a3397004e3166f666ae5c5e6164e028f1b2de2e5f7582036
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.3 MB (398267628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b0dcbdc3b77b86a167cffb9998a7b6d195727e4c082d8a42aad2ee580c98c3d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Apr 2025 07:26:08 GMT
RUN Apply image 10.0.26100.3775
# Wed, 09 Apr 2025 01:18:18 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:18:18 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 09 Apr 2025 01:18:19 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:18:21 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 09 Apr 2025 01:18:22 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:18:22 GMT
ENV JAVA_VERSION=25-ea+17
# Wed, 09 Apr 2025 01:18:29 GMT
COPY dir:31d4a08dd20e935927d81b33c56eb56ceaeead96529382a0c30c5f89fc836ee7 in C:\openjdk-25 
# Wed, 09 Apr 2025 01:18:36 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 09 Apr 2025 01:18:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:79b2ed45f890e91d23d7d22491a8fb6909c9268c668dc6a0e3b40131da02ed74`  
		Last Modified: Wed, 09 Apr 2025 00:36:30 GMT  
		Size: 190.1 MB (190113206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdfe7b8f10b04296652ae9abbb37362fdd7e3adda4ace99bec5aa59d6c19769`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2a91e8784f4d940134c228c5facff9aa28b816c718df6aa20c2500d9bf1f2c`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6e565ceb16763cf82294dbca944eaa9e87ad284f6c652c8f33d5f380c21450`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7c47343bc6d40619735349e13025407a28453f70334d136df0fd7c62eb2168`  
		Last Modified: Wed, 09 Apr 2025 01:18:42 GMT  
		Size: 76.2 KB (76170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb1948d2ea41f6f9ac5c561fab41b76ef30dadb0522badb08c9a9c2a8f8c5c8`  
		Last Modified: Wed, 09 Apr 2025 01:18:40 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4414ae27a8a5f72ca8f740f0d9f7363c8b893191c777fa93cf343135bfa259a3`  
		Last Modified: Wed, 09 Apr 2025 01:18:40 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e82fadf2ab1496c794d9e030acd85d6be33f4d586f05b47849128dcb23657e`  
		Last Modified: Wed, 09 Apr 2025 01:18:51 GMT  
		Size: 208.0 MB (207956634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062cbd056959ea3cff5fcbce17c63b6307a44935e9e960bf2b3ab041d0dda243`  
		Last Modified: Wed, 09 Apr 2025 01:18:40 GMT  
		Size: 115.3 KB (115260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881ab8f2bd5f6520d8701a1b8952da4f440d612fe1701c149c0bab09ddcc977b`  
		Last Modified: Wed, 09 Apr 2025 01:18:40 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-17-nanoserver` - windows version 10.0.20348.3453; amd64

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

### `openjdk:25-ea-17-nanoserver` - windows version 10.0.17763.7136; amd64

```console
$ docker pull openjdk@sha256:cce01d878c73a00fca956d4c2a97b05afd270a6fc53df5bf5f9245dacc808102
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.4 MB (319392725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68c2857267892b5c6688ec3ec02f9c6c82920a8e43fcc6504f75e34220930e82`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Apr 2025 01:31:28 GMT
RUN Apply image 10.0.17763.7136
# Wed, 09 Apr 2025 01:51:57 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:51:59 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 09 Apr 2025 01:52:00 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:52:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 09 Apr 2025 01:52:03 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:52:04 GMT
ENV JAVA_VERSION=25-ea+17
# Wed, 09 Apr 2025 01:52:11 GMT
COPY dir:31d4a08dd20e935927d81b33c56eb56ceaeead96529382a0c30c5f89fc836ee7 in C:\openjdk-25 
# Wed, 09 Apr 2025 01:52:17 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 09 Apr 2025 01:52:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a06e0965a0fa3715e629889bd9332aa22aadd75654cac5c9818b67c0264b3ee1`  
		Last Modified: Tue, 08 Apr 2025 20:16:02 GMT  
		Size: 106.9 MB (106922524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4649969ca3c3e4d5c4d5f747d5316968fe11da1ae6e14575ae9501414afbf22b`  
		Last Modified: Wed, 09 Apr 2025 01:52:22 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4485974b5b247c933daca6ab33b247bea2559120a3552aa087b50551530966ee`  
		Last Modified: Wed, 09 Apr 2025 01:52:21 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647044e2eae66526b8155aa7f20f679defd3402136e35b26622eb1c5de599cf7`  
		Last Modified: Wed, 09 Apr 2025 01:52:21 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdaf719fddf02a35729887893db2f262beaf98132c47aa904019b7501a2fdf9c`  
		Last Modified: Wed, 09 Apr 2025 01:52:21 GMT  
		Size: 71.0 KB (71012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777eb8ead373566fa5357484afde0be6159c11a0ad28c2076047f42f25a0c2a1`  
		Last Modified: Wed, 09 Apr 2025 01:52:20 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b014ade311506118e15e73c000215111edba25b160ed36f25996747a11f354`  
		Last Modified: Wed, 09 Apr 2025 01:52:20 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096b83ba0821b16afb90c992699094441a915fb169f2ae928ffae7b1142bb60a`  
		Last Modified: Wed, 09 Apr 2025 01:52:33 GMT  
		Size: 208.0 MB (207953398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eef4450d61dd5494a853948cad0a75cd7b53c2c7936a3ed8cad70e1a388516a`  
		Last Modified: Wed, 09 Apr 2025 01:52:21 GMT  
		Size: 4.4 MB (4439566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fcfe9e1afc3a49edeaee35f97f3227d4ae28c96a7e2b676e8fee482b636e136`  
		Last Modified: Wed, 09 Apr 2025 01:52:20 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
