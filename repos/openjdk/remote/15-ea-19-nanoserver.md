## `openjdk:15-ea-19-nanoserver`

```console
$ docker pull openjdk@sha256:7d51cc4a67541221c89700bb54a0e25aa24dcc44c7f41ef5115c9d85b1375288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `openjdk:15-ea-19-nanoserver` - windows version 10.0.17763.1158; amd64

```console
$ docker pull openjdk@sha256:67c40c30e6fa3e214087e4fbcb8a3fcf0b05c3cf3ee49e4c64b8ebb737118db1
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.7 MB (296735312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715a5f6992e6c38bd4deb406d9a9ee35f93c27fd5222147104f2e47479688e2d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 12 Apr 2020 11:41:03 GMT
RUN Apply image 1809-amd64
# Tue, 14 Apr 2020 21:42:38 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2020 21:42:39 GMT
ENV JAVA_HOME=C:\openjdk-15
# Tue, 14 Apr 2020 21:42:39 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2020 21:42:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Tue, 14 Apr 2020 21:42:54 GMT
USER ContainerUser
# Mon, 20 Apr 2020 19:26:15 GMT
ENV JAVA_VERSION=15-ea+19
# Mon, 20 Apr 2020 19:27:07 GMT
COPY dir:1a87f54ae5c36ed2b5e95a32a622e15b0d9d1344aee856b4ef28c63f882d4608 in C:\openjdk-15 
# Mon, 20 Apr 2020 19:27:31 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Mon, 20 Apr 2020 19:27:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0fe89239909ba300aeb9b977458b61ae3fbbcd2d9591086ed05ca023209d3122`  
		Size: 101.1 MB (101118377 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:895ca47ba9cf1a5b61a0721217cfcc038bbe9a4987c7536321c3ac51ef8e5e0c`  
		Last Modified: Tue, 14 Apr 2020 22:17:22 GMT  
		Size: 836.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bcf297e34b7d011805160436d6acaba77887d05e2acd81e88acd84ad22cdff1`  
		Last Modified: Tue, 14 Apr 2020 22:17:22 GMT  
		Size: 830.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9641626825020cd19b05bbf1f20b92df3d267d2aade5a84deef0163b791a895b`  
		Last Modified: Tue, 14 Apr 2020 22:17:22 GMT  
		Size: 819.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062e1c072d6c921a1b4e4db61fa592b7f9ccbc231f6c5cc8dfd4417fc317438c`  
		Last Modified: Tue, 14 Apr 2020 22:17:21 GMT  
		Size: 67.0 KB (67045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe221d18f1e3ca2b86519debf76a76b4ba0e95f42490a1a161bffea2d3306309`  
		Last Modified: Tue, 14 Apr 2020 22:17:19 GMT  
		Size: 824.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e661cb99d3d5e14d4985fd82d83d376d215f1cc58792e91a25ecb7500e4c12`  
		Last Modified: Mon, 20 Apr 2020 19:32:35 GMT  
		Size: 864.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c473fff8a5e2d7333812692c79ed99f754359fb80b17dbf87ee8889a6a6859ff`  
		Last Modified: Mon, 20 Apr 2020 19:35:52 GMT  
		Size: 192.1 MB (192080276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5619d2e14edf14a2cd86b122c577f013dc28f25178544927bda03c421d0092`  
		Last Modified: Mon, 20 Apr 2020 19:32:36 GMT  
		Size: 3.5 MB (3464554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217d4fedbc2421cb3bac159a9e8ab79dc50815ca3ff6092bbaa172bf2ca16f0f`  
		Last Modified: Mon, 20 Apr 2020 19:32:36 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
