## `openjdk:24-rc-nanoserver`

```console
$ docker pull openjdk@sha256:53e8570b581da2cce2c1cd168e2fade2f38aaa8b07b67bba6e77ba71a89dd1e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `openjdk:24-rc-nanoserver` - windows version 10.0.26100.2894; amd64

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

### `openjdk:24-rc-nanoserver` - windows version 10.0.20348.3207; amd64

```console
$ docker pull openjdk@sha256:5d99fd40a56e2dc97df07817613073c7d8394315d89e14f725181c13eb7079ce
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.4 MB (329398030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffde4c639f0d9bddad0571c1d4c4e2e1eff1cf7ad7a7799db1fa685a799b503e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Thu, 13 Feb 2025 01:18:46 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:18:47 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 13 Feb 2025 01:18:48 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:18:51 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 13 Feb 2025 01:18:51 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:18:52 GMT
ENV JAVA_VERSION=24
# Thu, 13 Feb 2025 01:18:59 GMT
COPY dir:cf5ecdf170ed29d5224593d2b3a510464d2e7297517065c397a2229de8b2a139 in C:\openjdk-24 
# Thu, 13 Feb 2025 01:19:04 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 13 Feb 2025 01:19:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:49:39 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca32c5ed90f22b0929449a457d80c4c4d488d229a00de61f4ad4c2ad992ab6e`  
		Last Modified: Thu, 13 Feb 2025 04:23:28 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ec97e98e193c39e1ba87bf34b37ab27327cb58abd4c444ae089417a4d397e6`  
		Last Modified: Thu, 13 Feb 2025 04:23:28 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea151a55ec5a5402d2ed66d67168550cebb72bdae88962cdf056147110d30be9`  
		Last Modified: Thu, 13 Feb 2025 04:23:28 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e40df6a94263acbe1e3457fdc53e1d0c32c3475686f1ce81ac7813cf4416ae1`  
		Last Modified: Thu, 13 Feb 2025 04:23:28 GMT  
		Size: 79.3 KB (79336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26011d2ade6cdbbed31766f3d18cbb3a2f2320e8516c6857d724cfe3b4671366`  
		Last Modified: Thu, 13 Feb 2025 04:23:28 GMT  
		Size: 1.0 KB (1010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbb293beea64d907a749bea6cf0b9ba20cd3d8ed46e88b46ef3ae1ab16b8833`  
		Last Modified: Thu, 13 Feb 2025 04:23:28 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046171047dce804264d3cea1587ddf75710e1a88d40de818a7185426f6dd27b3`  
		Last Modified: Thu, 13 Feb 2025 04:23:44 GMT  
		Size: 208.5 MB (208527578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f03e65ece69044afe2727d8b07a82891ad8efedfc7596ff820e5f1bf387992`  
		Last Modified: Thu, 13 Feb 2025 04:23:28 GMT  
		Size: 118.3 KB (118277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75301350ffd85a4c54218762a009c59e3a7d0afd1ba168dc281b51f2361f394`  
		Last Modified: Thu, 13 Feb 2025 04:23:28 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-rc-nanoserver` - windows version 10.0.17763.6893; amd64

```console
$ docker pull openjdk@sha256:296396df4bb3a27df6f57305a46c036bc95239f9b067da25109484c9e141b9e1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.9 MB (319947495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe27c8d69bd53797c7cba7c49cee2885338a2b2f99ddfc43ef7123ce20e75d6b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Thu, 13 Feb 2025 01:15:32 GMT
SHELL [cmd /s /c]
# Thu, 13 Feb 2025 01:15:33 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 13 Feb 2025 01:15:34 GMT
USER ContainerAdministrator
# Thu, 13 Feb 2025 01:15:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 13 Feb 2025 01:15:36 GMT
USER ContainerUser
# Thu, 13 Feb 2025 01:15:37 GMT
ENV JAVA_VERSION=24
# Thu, 13 Feb 2025 01:15:44 GMT
COPY dir:cf5ecdf170ed29d5224593d2b3a510464d2e7297517065c397a2229de8b2a139 in C:\openjdk-24 
# Thu, 13 Feb 2025 01:15:49 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 13 Feb 2025 01:15:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Wed, 12 Feb 2025 21:38:54 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d693e20229b4584d695af0ea22ff9983a8de5c2580d824746662df0d098f502`  
		Last Modified: Thu, 13 Feb 2025 04:23:28 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048de90e4af2eabd8e88300d174a6eaf8d1affb9595bcb44a910aa550b022535`  
		Last Modified: Thu, 13 Feb 2025 04:23:28 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19bb4302440864df2605567730ccb6b95ebc4b08573d103a940c53acf995219`  
		Last Modified: Thu, 13 Feb 2025 04:23:28 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d6b5ce27eeb5fe93f3581fa080e78a5b7323e2324ad9d7d06be329180949cb`  
		Last Modified: Thu, 13 Feb 2025 04:23:28 GMT  
		Size: 71.8 KB (71844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f236e3498e94674c64603c786bf6df9aaf5094fb7432f19754a7f1bc615b010`  
		Last Modified: Thu, 13 Feb 2025 04:23:28 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555c2989c1b53c407da6d9802d5c6defa5d3e1792cafc3729a6ff5708bca5633`  
		Last Modified: Thu, 13 Feb 2025 04:23:28 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f41e9c89e8697db60ccd4b7fc32bf2e9f9dd03475e4dd99beddffd626920a5d`  
		Last Modified: Thu, 13 Feb 2025 04:23:45 GMT  
		Size: 208.5 MB (208527262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42030d586c0ee7286f1ab46a1f0682b98fb2b2935a3e2769b0c20ba5b22d66b`  
		Last Modified: Thu, 13 Feb 2025 04:23:29 GMT  
		Size: 4.4 MB (4426662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf7b48f254b4096babf9224902bad9fc075703ed90c1c0e1864722b25ee4867`  
		Last Modified: Thu, 13 Feb 2025 04:23:29 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
