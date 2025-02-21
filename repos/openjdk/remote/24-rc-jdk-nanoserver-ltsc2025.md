## `openjdk:24-rc-jdk-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:4f74531d9fe654a90f1c0d282fff10cbc8d89940970b2b5d7413d0ca904a46ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `openjdk:24-rc-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.2894; amd64

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
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd40d472f727a57dd2e47b8b30281956e438e2cc97f89242eb30406c2302529`  
		Last Modified: Tue, 11 Feb 2025 01:32:26 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7113580be8b532a47b85045a1b5665e24099327b639aa9033899ca85700941`  
		Last Modified: Tue, 11 Feb 2025 01:32:26 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f2cbc61f9873334e8bc96ebb3f1ecf35d1e92f1f25b2b28c11b8185ce67acc`  
		Last Modified: Tue, 11 Feb 2025 01:32:26 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2f578bbe811a2b404f30a722c549c4c3b2227dc04a144240664b3509f10252`  
		Last Modified: Tue, 11 Feb 2025 01:32:26 GMT  
		Size: 76.0 KB (76016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067cafe440e70408d25db457f5aefb91005daa220248d649cac7a84a02c2ff45`  
		Last Modified: Tue, 11 Feb 2025 01:32:25 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db21a00e5b4882e23ec84d02d746f806ee6623138743414df9d7a586c89cea6`  
		Last Modified: Tue, 11 Feb 2025 01:32:25 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ba459dba219f0bab14db0e23816b8726d5a79c484f803388052f2a2c800b51`  
		Last Modified: Tue, 11 Feb 2025 01:32:39 GMT  
		Size: 208.5 MB (208526354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd9c570ae5320e8f504f6918e2c61fa80fe0eba6c736fae85659453df0c147f`  
		Last Modified: Tue, 11 Feb 2025 01:32:25 GMT  
		Size: 92.8 KB (92792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56798443389ccce21a0b04df9c98cd5ffe48f0ea82150eed031906839bccf6c`  
		Last Modified: Tue, 11 Feb 2025 01:32:25 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
