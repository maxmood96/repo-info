## `eclipse-temurin:21-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:325796eed2521fd47629a99c08fa371f0d61bb28789c34725a55e6b728000fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:21-jre-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:45378b02251842ae36cb5ba4e75163085bdc2124b1c5fb9efc7699414b809fc0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208319598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2054e90a28e996395634f51229b1300ba9b6ccc65603f2106ecca3113982b30`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 18:02:19 GMT
SHELL [cmd /s /c]
# Wed, 15 Jan 2025 18:02:21 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Wed, 15 Jan 2025 18:02:23 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 15 Jan 2025 18:02:24 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 18:02:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jan 2025 18:02:32 GMT
USER ContainerUser
# Wed, 15 Jan 2025 18:02:38 GMT
COPY dir:d301f311784d572cc6cc0a5ee90712dcade9d3f8b4a48a0f2df4274582f5072e in C:\openjdk-21 
# Wed, 15 Jan 2025 18:02:45 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0518f764b368beeb0ed8d1056aa8db1e4b1fe4f690798804807eb350a5f5d3da`  
		Last Modified: Wed, 15 Jan 2025 18:02:48 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5e283466aa6f32907338c83f064c1e50b563769c2df10f260c62cca851892e`  
		Last Modified: Wed, 15 Jan 2025 18:02:48 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788c8a5c347b2e3d83c5cf603efa2e4b05e7245e1e6de59df22968583b3fe7f6`  
		Last Modified: Wed, 15 Jan 2025 18:02:48 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2fab20c26fb09d362d85b32417f24a64fd92e407cd070768d41d19d9ae6cce`  
		Last Modified: Wed, 15 Jan 2025 18:02:47 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a1ef81838dfda8b6fc71df98c6c9a4e1d47d4c5d1e1e7b427deb6e085a8e17`  
		Last Modified: Wed, 15 Jan 2025 18:02:47 GMT  
		Size: 83.9 KB (83935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67db9790bf56abe4b0f4f1c1156a9515be166463443df69799c80024870da70f`  
		Last Modified: Wed, 15 Jan 2025 18:02:47 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da00196971ed0eda5f42c9d6b27eb64943fe418571546db44e8b4d5efa601349`  
		Last Modified: Wed, 15 Jan 2025 18:02:52 GMT  
		Size: 49.6 MB (49585735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3199da1cc4f3437f0abb53bf947e99dcf04e34be63a3acae6717fdad3354725f`  
		Last Modified: Wed, 15 Jan 2025 18:02:47 GMT  
		Size: 3.4 MB (3377191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
