## `openjdk:26-rc-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:0c2f9b741ca431d2853bdcb2b74529524c6f50d4e7eef469e312af813cd14686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `openjdk:26-rc-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull openjdk@sha256:5957d8e27b4f96680f29becace5f56e29021f0bf76a081512291d37b64f1d23f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.7 MB (350728116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00d3fedfc96199a6659ee220e8c6c25e89c32d51df9a88782ce834cbd864caf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Fri, 13 Feb 2026 01:11:50 GMT
SHELL [cmd /s /c]
# Fri, 13 Feb 2026 01:11:52 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 13 Feb 2026 01:11:54 GMT
USER ContainerAdministrator
# Fri, 13 Feb 2026 01:12:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 13 Feb 2026 01:12:09 GMT
USER ContainerUser
# Fri, 13 Feb 2026 01:12:11 GMT
ENV JAVA_VERSION=26
# Fri, 13 Feb 2026 01:13:33 GMT
COPY dir:d694f138ae93de163149df5684967cf6e6d03015ac3abc206becddb178db66e4 in C:\openjdk-26 
# Fri, 13 Feb 2026 01:13:39 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 13 Feb 2026 01:13:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9cc2da1daea54f1cf84245cd706060bed9755e4a888051af1fdd2840e00426c`  
		Last Modified: Fri, 13 Feb 2026 01:13:53 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19702178b80b6ffe3cc7ebc84a93b9d17121b2241396187a3c552868d7fddd1`  
		Last Modified: Fri, 13 Feb 2026 01:13:53 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbf1ff75dee3261f7c0d13fa9f5ecc7538f5a70f66304717e0c50af1ec4ed51`  
		Last Modified: Fri, 13 Feb 2026 01:13:53 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1430add21289bf82333903797557dcfcd40f8cb5e41aba95da77950549543ef`  
		Last Modified: Fri, 13 Feb 2026 01:13:53 GMT  
		Size: 71.4 KB (71406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1eca5096b6b11e94398611d955b90b12bd1881e9bb40ed1cb41d5bef7ecedf7`  
		Last Modified: Fri, 13 Feb 2026 01:13:52 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dbadf51d8e22bcfa66da84a0df4419be9bab578cb006523585d639b45a18de4`  
		Last Modified: Fri, 13 Feb 2026 01:13:51 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34a2918b53af1e3ed358e62afbcd555077d0e333bdcc02642952c2e106bef7f`  
		Last Modified: Fri, 13 Feb 2026 01:14:07 GMT  
		Size: 223.9 MB (223876643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a2b0dacb5fa151bc07feaf37d662dd093feb9817db53a33b6370de9e900f8f0`  
		Last Modified: Fri, 13 Feb 2026 01:13:51 GMT  
		Size: 127.9 KB (127932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505c8ccc5e72fd59a11c8269c6b6efddb0bc0c57ed27d169dba3b411b2d3c924`  
		Last Modified: Fri, 13 Feb 2026 01:13:52 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
