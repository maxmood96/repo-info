## `eclipse-temurin:11-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:bea5d5cc0ff1537865095ddc4c434f0bafab5ca2988efb6c63fe9cc643ba9fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:11-jre-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:4dd93d3da467ff9b8fd4411a86741cf9b55d3453730983c5f3ba7b85bd22ca3f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.8 MB (199758377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ebbad44bb850d67ec467cb7c0d8c4125ca7540ec358a9958541fc64581c42d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 18:01:39 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2025 18:01:42 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 15 Jan 2025 18:01:42 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 15 Jan 2025 18:01:43 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 18:01:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jan 2025 18:01:47 GMT
USER ContainerUser
# Wed, 15 Jan 2025 18:01:51 GMT
COPY dir:a15dacd11bbcaacf83a6b6e1490d6483ae4af68a125407fd4cb6bb7a70e4639c in C:\openjdk-11 
# Wed, 15 Jan 2025 18:01:55 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2633738020979a24781eac52c3878ca3851781649096629e977a5c179e7d315`  
		Last Modified: Wed, 15 Jan 2025 18:02:01 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158b0f44fa58139d48f270f3a44393f52086715436bfd4f78d53eadfc0bcfc6c`  
		Last Modified: Wed, 15 Jan 2025 18:02:01 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4aba1d89090852d3a7f330d7caf72e23dc4928d2af5d6efdc7d9f49d143aef`  
		Last Modified: Wed, 15 Jan 2025 18:02:00 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1780d2ba9b27b83c74f0434287dd7a015dbff7ac1bfff9cb37deefd97459fa`  
		Last Modified: Wed, 15 Jan 2025 18:01:59 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04c026d67aa285f980f581d9b2f5ee2f860bfcbde8ae19dec08cfbc9fc2048c`  
		Last Modified: Wed, 15 Jan 2025 18:01:59 GMT  
		Size: 83.8 KB (83815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8adc09902c4c89667f29f72148c44b7fe74c8d4c6fa9a5653f714d9773e1057f`  
		Last Modified: Wed, 15 Jan 2025 18:01:59 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f215ed3bd8e6a97f4fc45c65f053ce15cb6f3406796165de91fb4d00997276a`  
		Last Modified: Wed, 15 Jan 2025 18:02:03 GMT  
		Size: 44.3 MB (44308624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49f0caf374bd20fe99f95cf4697e6483e7e30e14cc4f2d1e69256f7b96b5412`  
		Last Modified: Wed, 15 Jan 2025 18:01:59 GMT  
		Size: 93.2 KB (93186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
