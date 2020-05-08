## `openjdk:15-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:c8bc4d4cc484b36d34eb129f6c827d84947ea248e3003bf8ad5ba8fedfef8ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1158; amd64

### `openjdk:15-ea-jdk-nanoserver-1809` - windows version 10.0.17763.1158; amd64

```console
$ docker pull openjdk@sha256:927c852a3cf4ee76528674168afbdd92c74f8ff18f868f4d7c5a7759cacbef2e
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.2 MB (292224988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c45365f5d291d5a9c3897adb2af1bccf8b142fadf24b83015a81f006b04543`
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
# Thu, 07 May 2020 21:21:29 GMT
ENV JAVA_VERSION=15-ea+22
# Thu, 07 May 2020 21:22:16 GMT
COPY dir:2f3367520b3c419024b6707c817295e284534707809e0e97170d6114ec04ea5f in C:\openjdk-15 
# Thu, 07 May 2020 21:22:32 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Thu, 07 May 2020 21:22:34 GMT
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
	-	`sha256:45f3c7a80fab450cf93b78642ce27a0a06173c7ed5fbaa15171b1e9ca5b04704`  
		Last Modified: Thu, 07 May 2020 21:27:46 GMT  
		Size: 932.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a85d62828541abb63bad337c2af33710be095d9e962941c41c12170a5d316507`  
		Last Modified: Thu, 07 May 2020 21:31:05 GMT  
		Size: 187.6 MB (187559723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2d2404c065bddfabdb009e6e398ce3d79b50a558bc1dbc478db7939dfb3401`  
		Last Modified: Thu, 07 May 2020 21:27:47 GMT  
		Size: 3.5 MB (3474693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea7bc68ab848dd48511e61d8f74d4677c6a52cbdad3e00504d1eab0f5130eb1`  
		Last Modified: Thu, 07 May 2020 21:27:46 GMT  
		Size: 909.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
