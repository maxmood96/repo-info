## `openjdk:25-ea-nanoserver-1809`

```console
$ docker pull openjdk@sha256:1c1feaac44d32a8e31d2f5353e5a90b2c2f4864bd9d83fab30226bd555c5b497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `openjdk:25-ea-nanoserver-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull openjdk@sha256:f876170154d52ad898aaebc0d7a667ee24ba1e60d3073dbe01da50facb73410e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.3 MB (319304762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d23a17ebafb62735fd6236dcecc48d12b5740b0c5d67ac8e98022db721a134d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Thu, 27 Mar 2025 21:13:27 GMT
SHELL [cmd /s /c]
# Thu, 27 Mar 2025 21:13:29 GMT
ENV JAVA_HOME=C:\openjdk-25
# Thu, 27 Mar 2025 21:13:29 GMT
USER ContainerAdministrator
# Thu, 27 Mar 2025 21:13:31 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 27 Mar 2025 21:13:32 GMT
USER ContainerUser
# Thu, 27 Mar 2025 21:13:32 GMT
ENV JAVA_VERSION=25-ea+16
# Thu, 27 Mar 2025 21:13:40 GMT
COPY dir:19cd448448f63399f0cc00bb4ac8df0759f681650f72cc2b82002a92d2bbe677 in C:\openjdk-25 
# Thu, 27 Mar 2025 21:13:45 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 27 Mar 2025 21:13:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8267004f1f0fc028dab165f507d228139ea336a7126e7fdd4a32d3cd40c3a5`  
		Last Modified: Thu, 27 Mar 2025 21:13:53 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b045c5fbfc0c0c8703b001d0de7e35808a52618cebcb8eae83632f6733ff889`  
		Last Modified: Thu, 27 Mar 2025 21:13:52 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f00d6f09164f9df6b47e9d73f135296d9e439d45f9f77051e55391ee25eed48b`  
		Last Modified: Thu, 27 Mar 2025 21:13:52 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13c3c62d3e6bad637efd34daeec58629329572b8a94fc84cb14d4860944e511`  
		Last Modified: Thu, 27 Mar 2025 21:13:52 GMT  
		Size: 69.2 KB (69174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2726c956a4676ac3fe218dcfd8f548859b54cd3bfe8df9b6c35b41a84d45547b`  
		Last Modified: Thu, 27 Mar 2025 21:13:50 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5802690e9a3fb7a4b757cd3e7a21b9eb089868580906322ae92de8c9a9d4916`  
		Last Modified: Thu, 27 Mar 2025 21:13:50 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04fef1de62a23dd9ed7ace5d0e45e3802004ec5d4177a74241a640b2c0569a1`  
		Last Modified: Thu, 27 Mar 2025 21:14:02 GMT  
		Size: 207.9 MB (207899682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f464a7383390ddb6bd81d17fe53be77a418b68ffb2100568610a52d2699f23c`  
		Last Modified: Thu, 27 Mar 2025 21:13:51 GMT  
		Size: 4.4 MB (4421996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1f36273f92f85b35507d67a19e5f0690bb5b90bb06f777b1955b465980ce04`  
		Last Modified: Thu, 27 Mar 2025 21:13:50 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
