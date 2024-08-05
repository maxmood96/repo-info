## `openjdk:23-ea-35-nanoserver`

```console
$ docker pull openjdk@sha256:e20fdd49ec5b9433a9f02aa053a87d2cbd19452c8faa381ea13865ffcc0d44fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `openjdk:23-ea-35-nanoserver` - windows version 10.0.17763.6054; amd64

```console
$ docker pull openjdk@sha256:75e4216beb64fd63bdcf8e2da6d9fcf76faa6a67a37c43016d6d76b33b27f745
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.3 MB (365283645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7c5faf21369e8631a42b2e59213455462204342a5ad8a0e30811a9f6394069`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Mon, 05 Aug 2024 19:53:05 GMT
SHELL [cmd /s /c]
# Mon, 05 Aug 2024 19:53:07 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 05 Aug 2024 19:53:08 GMT
USER ContainerAdministrator
# Mon, 05 Aug 2024 19:53:25 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 05 Aug 2024 19:53:26 GMT
USER ContainerUser
# Mon, 05 Aug 2024 19:53:26 GMT
ENV JAVA_VERSION=23-ea+35
# Mon, 05 Aug 2024 19:53:34 GMT
COPY dir:457e41fda330755bbd51bbb9967b4ac09f441b735938b6e1816791c55fb3047c in C:\openjdk-23 
# Mon, 05 Aug 2024 19:53:40 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 05 Aug 2024 19:53:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c14e109da2609c3d47383b027e26b6b0d28d7beb071ea3c51943b68fd8bfc08`  
		Last Modified: Mon, 05 Aug 2024 19:53:45 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df38f0babcd971ab1de06226e14fab4f61e43afe6548d09f283b759ba1d708d5`  
		Last Modified: Mon, 05 Aug 2024 19:53:44 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a96f394ff2d8f3a33f9fb9c120d95d1f322512ffa5d825f9ba30f0d2790bbc`  
		Last Modified: Mon, 05 Aug 2024 19:53:44 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542138f5f6044d3cd8e80e4cd7f07958489a7694ecb84f193cd44310c7b41185`  
		Last Modified: Mon, 05 Aug 2024 19:53:44 GMT  
		Size: 67.8 KB (67836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7744ae3b5682b0a3099bbf4f61665d1b4f4c86cd2c4ab709e5a86beed000326e`  
		Last Modified: Mon, 05 Aug 2024 19:53:43 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df3814388334038c66eb55ae5f694d098e19de65705f4924e32ef7cd9ed49ec`  
		Last Modified: Mon, 05 Aug 2024 19:53:43 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137b3f8703cd5e5b0fe04815ec1fb27fff7298ab74a9d55f74fddef8e0b30c3a`  
		Last Modified: Mon, 05 Aug 2024 19:53:54 GMT  
		Size: 206.0 MB (206048046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8951a44716f08b46ee46f8f0040f637db12314746ee54c9aa19001ecffebf3`  
		Last Modified: Mon, 05 Aug 2024 19:53:44 GMT  
		Size: 4.1 MB (4080089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85e84496b71ab43b04c3de24ef06bdb390da9acb5b56575d02464bf3fbddb16`  
		Last Modified: Mon, 05 Aug 2024 19:53:43 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
