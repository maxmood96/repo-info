## `openjdk:22-nanoserver-1809`

```console
$ docker pull openjdk@sha256:43de10415da7b7fcb5bfe5ef56c38c12a10d29d4b5e2b263e0f7b7492bfd5b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `openjdk:22-nanoserver-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull openjdk@sha256:27c02b5112d0c0d9d1177f7663c76ead56637ce2b907e27431422f94123482be
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.3 MB (307279779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502756293ff4612447b3990dc39e26c1e5943f1adc90bc126b4bc034fa9038d1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:04:01 GMT
SHELL [cmd /s /c]
# Wed, 13 Mar 2024 02:04:02 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 13 Mar 2024 02:04:03 GMT
USER ContainerAdministrator
# Wed, 13 Mar 2024 02:04:05 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 13 Mar 2024 02:04:05 GMT
USER ContainerUser
# Wed, 13 Mar 2024 02:04:06 GMT
ENV JAVA_VERSION=22
# Wed, 13 Mar 2024 02:04:14 GMT
COPY dir:0ef6a7becb679ad3edc5c96eb7b0f5b5893989ee8e0051f559b592b4b972c479 in C:\openjdk-22 
# Wed, 13 Mar 2024 02:04:22 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 13 Mar 2024 02:04:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb049a7377525d529c82214d94a32b8b48415eff1fcdccfdc78b1a8b1fc56cc`  
		Last Modified: Wed, 13 Mar 2024 02:04:29 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd789ee02068583deb9afb9814a75cd95634e9e62d150acd559274029dda6d57`  
		Last Modified: Wed, 13 Mar 2024 02:04:28 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcc426cdba25cb12f205913c2dccb88621974f53801ca2c32de6ca319395e4b`  
		Last Modified: Wed, 13 Mar 2024 02:04:28 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7242f986ae99041dbcade53056c3b1209560dec2b3a62579be54a6c6a8f527e0`  
		Last Modified: Wed, 13 Mar 2024 02:04:28 GMT  
		Size: 73.4 KB (73373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:525582c40468e61b6cc42a7bf96a41c672faaa211908c7dace063ae94eb5be77`  
		Last Modified: Wed, 13 Mar 2024 02:04:26 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f859c8d8dd77c9782601486dc3cf363c4a3add96977b2221ae5c6659fa3e8788`  
		Last Modified: Wed, 13 Mar 2024 02:04:26 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7a67925459deece9e70037c6a31623b1fd136b438cfaec8fb9b10ac6f2d09b`  
		Last Modified: Wed, 13 Mar 2024 02:04:38 GMT  
		Size: 197.4 MB (197368367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639999f161cc7c28dc4979822ccf1593ea4265d323fff2a613f1448188a6881a`  
		Last Modified: Wed, 13 Mar 2024 02:04:27 GMT  
		Size: 5.2 MB (5211710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54aac61e5a200dece99097e689b7fee2b82066bd4751a6809e9f49d034c62766`  
		Last Modified: Wed, 13 Mar 2024 02:04:26 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
