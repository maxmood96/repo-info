## `openjdk:15-ea-20-nanoserver`

```console
$ docker pull openjdk@sha256:fe0a42a677bd309767a7812f9ec59ef450372868bd51246ad96cd12d656e97d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `openjdk:15-ea-20-nanoserver` - windows version 10.0.17763.1158; amd64

```console
$ docker pull openjdk@sha256:eb490a956041c71f5cb567abfd1f1b0236b6d350ebf920e6a4eca2e5dc3acd05
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.6 MB (291612828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547ee38d1b0ea1bda503d926dc69f43a42a7defae637c51a9bf5410324ce3b9a`
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
# Fri, 24 Apr 2020 23:19:16 GMT
ENV JAVA_VERSION=15-ea+20
# Fri, 24 Apr 2020 23:20:01 GMT
COPY dir:6dc0f3305f5ecdab4f98f005b781c57ca513e198bfa201b009b4f91916a799a4 in C:\openjdk-15 
# Fri, 24 Apr 2020 23:20:22 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Fri, 24 Apr 2020 23:20:23 GMT
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
	-	`sha256:89c25cbe2a0514611e7342d386a909d4994c961335d58d8995594b25b3bf062c`  
		Last Modified: Fri, 24 Apr 2020 23:25:20 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f863eab20d24bbac9d33a03b3d4b5ba762291be0e54dc73d2918998226b5a2`  
		Last Modified: Fri, 24 Apr 2020 23:25:40 GMT  
		Size: 186.9 MB (186926675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ba1a11d0b27c6cfeae5c75ab563bd6c1ae63abc7ffff8c4b61c877110c8c0c`  
		Last Modified: Fri, 24 Apr 2020 23:25:21 GMT  
		Size: 3.5 MB (3495672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40401f94f3dbbf78b99df60ec7090c46fe67bf1751d97aefd8d72a9c5c48d37`  
		Last Modified: Fri, 24 Apr 2020 23:25:20 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
