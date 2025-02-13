## `openjdk:24-rc-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:969aacff319cf49eb14933504f163a36a66fc383fadc8b0f76be4f2d6fd4c728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `openjdk:24-rc-jdk-nanoserver` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:d9c64d930ad759f1ad0db2b45ff3f0e21b80bb6c8e7164621e99638e5d0900ed
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.8 MB (407755927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9cf90574303fb15c57ce6441e64bb07a5cc4d9f85c68816a54cb71dd5eeae36`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Tue, 11 Feb 2025 01:31:58 GMT
SHELL [cmd /s /c]
# Tue, 11 Feb 2025 01:31:58 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 11 Feb 2025 01:31:59 GMT
USER ContainerAdministrator
# Tue, 11 Feb 2025 01:32:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 11 Feb 2025 01:32:02 GMT
USER ContainerUser
# Tue, 11 Feb 2025 01:32:03 GMT
ENV JAVA_VERSION=24
# Tue, 11 Feb 2025 01:32:15 GMT
COPY dir:cf5ecdf170ed29d5224593d2b3a510464d2e7297517065c397a2229de8b2a139 in C:\openjdk-24 
# Tue, 11 Feb 2025 01:32:22 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 11 Feb 2025 01:32:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Wed, 22 Jan 2025 08:02:27 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd40d472f727a57dd2e47b8b30281956e438e2cc97f89242eb30406c2302529`  
		Last Modified: Wed, 12 Feb 2025 21:51:29 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7113580be8b532a47b85045a1b5665e24099327b639aa9033899ca85700941`  
		Last Modified: Wed, 12 Feb 2025 21:51:30 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f2cbc61f9873334e8bc96ebb3f1ecf35d1e92f1f25b2b28c11b8185ce67acc`  
		Last Modified: Wed, 12 Feb 2025 21:51:31 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2f578bbe811a2b404f30a722c549c4c3b2227dc04a144240664b3509f10252`  
		Last Modified: Wed, 12 Feb 2025 21:51:31 GMT  
		Size: 76.0 KB (76016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067cafe440e70408d25db457f5aefb91005daa220248d649cac7a84a02c2ff45`  
		Last Modified: Wed, 12 Feb 2025 21:51:33 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db21a00e5b4882e23ec84d02d746f806ee6623138743414df9d7a586c89cea6`  
		Last Modified: Wed, 12 Feb 2025 21:51:34 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ba459dba219f0bab14db0e23816b8726d5a79c484f803388052f2a2c800b51`  
		Last Modified: Wed, 12 Feb 2025 21:51:53 GMT  
		Size: 208.5 MB (208526354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd9c570ae5320e8f504f6918e2c61fa80fe0eba6c736fae85659453df0c147f`  
		Last Modified: Wed, 12 Feb 2025 21:51:55 GMT  
		Size: 92.8 KB (92792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56798443389ccce21a0b04df9c98cd5ffe48f0ea82150eed031906839bccf6c`  
		Last Modified: Wed, 12 Feb 2025 21:51:56 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-rc-jdk-nanoserver` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:72a7c54ee9c084003b3ca5a192c13d03a4b8265737fe95ff11d81eafaabbafb4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.4 MB (329378275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f77d90ecb675039c97581a24bf6dd31cebb0a8e1ee464139a7c6dca367916b5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Tue, 11 Feb 2025 02:08:14 GMT
SHELL [cmd /s /c]
# Tue, 11 Feb 2025 02:08:14 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 11 Feb 2025 02:08:15 GMT
USER ContainerAdministrator
# Tue, 11 Feb 2025 02:08:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 11 Feb 2025 02:08:34 GMT
USER ContainerUser
# Tue, 11 Feb 2025 02:08:34 GMT
ENV JAVA_VERSION=24
# Tue, 11 Feb 2025 02:08:43 GMT
COPY dir:cf5ecdf170ed29d5224593d2b3a510464d2e7297517065c397a2229de8b2a139 in C:\openjdk-24 
# Tue, 11 Feb 2025 02:08:49 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 11 Feb 2025 02:08:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Wed, 15 Jan 2025 01:24:28 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c9b14e7c383b9d19a004e99387b95147ffca114fe022436f0f01f5c2450d0e`  
		Last Modified: Wed, 12 Feb 2025 21:51:30 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b879f70c688ca76849d42862ac84f6057b864d2f9751f121ce35f12557c0b0`  
		Last Modified: Wed, 12 Feb 2025 21:51:31 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d7a2a44f1c27541b8be59ceba6ce678f61b858880423e6659f55bda975b297`  
		Last Modified: Tue, 11 Feb 2025 02:10:10 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a0fb31da926939b82c71af07d4ef64bc190b6a7e9af56a1babc354a5bb4bb9`  
		Last Modified: Tue, 11 Feb 2025 02:10:10 GMT  
		Size: 86.0 KB (85972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd7bd8de31312bfb56146a89f6ce369091156ecc6a51f7ed458f535c1e3f9e7`  
		Last Modified: Tue, 11 Feb 2025 02:10:10 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20a8e44714436e92e3812641c66f1f6ce020bdce1d271426df520f23a4f648c`  
		Last Modified: Tue, 11 Feb 2025 02:10:10 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa417497cea233dc4190668c0fcbe4f3da0d3ac44dc047782daadbfea3042ba`  
		Last Modified: Tue, 11 Feb 2025 02:09:03 GMT  
		Size: 208.5 MB (208527408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4215867c0b68ce8e0ea2c9acba05aeb607adef319c6dc25553b182c5653648e`  
		Last Modified: Tue, 11 Feb 2025 02:10:11 GMT  
		Size: 97.1 KB (97142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63d8cc246cbdb21e17e49bbe132e3b94e62b52bd2968b436146b9974a38403c`  
		Last Modified: Wed, 12 Feb 2025 21:52:07 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-rc-jdk-nanoserver` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:63c784d1c9cceefc7bbdd2d4839e01162ba0e84c26c5b399c486830166ecade3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368244466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e270a5da9a491497a4ee5269ffde61d98ad8918f6a78f573f8b347a2913b9288`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Tue, 11 Feb 2025 02:08:32 GMT
SHELL [cmd /s /c]
# Tue, 11 Feb 2025 02:08:34 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 11 Feb 2025 02:08:35 GMT
USER ContainerAdministrator
# Tue, 11 Feb 2025 02:08:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 11 Feb 2025 02:08:54 GMT
USER ContainerUser
# Tue, 11 Feb 2025 02:08:55 GMT
ENV JAVA_VERSION=24
# Tue, 11 Feb 2025 02:09:10 GMT
COPY dir:cf5ecdf170ed29d5224593d2b3a510464d2e7297517065c397a2229de8b2a139 in C:\openjdk-24 
# Tue, 11 Feb 2025 02:09:16 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 11 Feb 2025 02:09:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Wed, 15 Jan 2025 07:23:16 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48998653beafd11420a55fc0354d945e0c558381d8516b68032d995bb16ef644`  
		Last Modified: Wed, 12 Feb 2025 21:52:15 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcd6fd09e15e797aa235dc19f6f408d3cd2325905e7743fd538c66b87e3d13a`  
		Last Modified: Wed, 12 Feb 2025 21:52:16 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49121cbe4ebb8f43191f829e05c4a52b994641d2053ed0bd6ad5c01e6daf8491`  
		Last Modified: Wed, 12 Feb 2025 21:52:17 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a4dabc869167399a65490e0004e0b2bdd93ec9f8993e791caf68276905906d5`  
		Last Modified: Wed, 12 Feb 2025 21:52:18 GMT  
		Size: 67.5 KB (67454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f673638d6fff94a86f19c9334b7dd3816cf81bc5785c62d4cf512121ef5826e`  
		Last Modified: Wed, 12 Feb 2025 21:52:19 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3922e157442242e5683bb927c813e9ce65d21c20c687847f6c81e57d719f7c3e`  
		Last Modified: Wed, 12 Feb 2025 21:52:20 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b426371be59ade1110a0ee5d6704592c5414334309a02905958852245ec47bfc`  
		Last Modified: Wed, 12 Feb 2025 21:52:49 GMT  
		Size: 208.5 MB (208527384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb999fac7b86565850559cdcbca24d6bd5c34827d7d40eb1aa2024236eec8975`  
		Last Modified: Wed, 12 Feb 2025 21:52:51 GMT  
		Size: 4.4 MB (4375775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:090584256921484d56cdd2abe00cbb9bb7bce131cb975b0796a769f2b85e13fe`  
		Last Modified: Wed, 12 Feb 2025 21:52:53 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
