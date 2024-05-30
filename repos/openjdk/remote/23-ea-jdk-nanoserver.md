## `openjdk:23-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:585429ab827fcc88d68513c11ff0ed15c33feac1842764a604ad8b75d0e08863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `openjdk:23-ea-jdk-nanoserver` - windows version 10.0.17763.5820; amd64

```console
$ docker pull openjdk@sha256:c1672347ff5082cd86b5403d0f8e67802f77b9fba093e6201396c218e30598e9
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.1 MB (364132311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:addbcbbf02e540c3a14f7a9c56800b7add9658c30f0b85a15b86fefb33cedcf1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 29 May 2024 23:58:40 GMT
SHELL [cmd /s /c]
# Wed, 29 May 2024 23:58:44 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 29 May 2024 23:58:45 GMT
USER ContainerAdministrator
# Wed, 29 May 2024 23:59:06 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 29 May 2024 23:59:07 GMT
USER ContainerUser
# Wed, 29 May 2024 23:59:07 GMT
ENV JAVA_VERSION=23-ea+24
# Wed, 29 May 2024 23:59:17 GMT
COPY dir:ee26d50d1f28bbf6b9e13fd08d1d699e5f102e1f09256827aa584bef75554245 in C:\openjdk-23 
# Wed, 29 May 2024 23:59:25 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 29 May 2024 23:59:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc0ebfbcc646761a16a866cfdb68153e6ab50cdcbac9701d6ca2369269bef1ef`  
		Last Modified: Wed, 29 May 2024 23:59:32 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf16ab19c9cdcf60965a3fbbbad9d09c1298f789328b05e5021e9f9c8555c245`  
		Last Modified: Wed, 29 May 2024 23:59:32 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be043d55ec70dd171ff5779b4eb9f660e261f7801f32ad320e0f2f0d8e05f36`  
		Last Modified: Wed, 29 May 2024 23:59:32 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743927ee05e18ea48f81b48f86188472d19e134d020cc1f74613a6e2dcba0af8`  
		Last Modified: Wed, 29 May 2024 23:59:31 GMT  
		Size: 66.8 KB (66763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf079f471c7bdadc61f7b84c228b90001c4786fcf9f92fbb50256f1c68ded73f`  
		Last Modified: Wed, 29 May 2024 23:59:31 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28aaf72ad6397e29e2865cdf4558f2a42170bcd01ad508a516e59c5567bd8b3`  
		Last Modified: Wed, 29 May 2024 23:59:30 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9aa6e5d472c4b6fb0bd33f3b919cdd87a968d9bedbfe114b1be41ece0b10706`  
		Last Modified: Wed, 29 May 2024 23:59:42 GMT  
		Size: 205.3 MB (205300945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64313367f4d1ea92436757d9ced4caf4ec582c4a2f820e980372bb6810930dbc`  
		Last Modified: Wed, 29 May 2024 23:59:30 GMT  
		Size: 3.8 MB (3816855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec0593e4493210a38243cc77075a0ec533ab014af3e9922950239bda096249`  
		Last Modified: Wed, 29 May 2024 23:59:30 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
