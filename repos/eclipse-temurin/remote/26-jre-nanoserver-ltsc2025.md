## `eclipse-temurin:26-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:a8e1e47bed0decaf179ee788908c1d541f07f3d4ae5fb22c0c84320978a6f2a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `eclipse-temurin:26-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull eclipse-temurin@sha256:1cfa648eff449a36d9dd924d1a9c06ed87f7e3eb5de5cdd17adc62ca49b8d387
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.2 MB (260169235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db853150e371aa70038a24478dc7730202ea2ef178348c76c24a61e0cb32e05f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 May 2026 09:46:02 GMT
RUN Apply image 10.0.26100.32860
# Wed, 13 May 2026 00:28:41 GMT
SHELL [cmd /s /c]
# Wed, 13 May 2026 00:29:53 GMT
ENV JAVA_VERSION=jdk-26+35
# Wed, 13 May 2026 00:29:54 GMT
ENV JAVA_HOME=C:\openjdk-26
# Wed, 13 May 2026 00:29:54 GMT
USER ContainerAdministrator
# Wed, 13 May 2026 00:29:56 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 13 May 2026 00:29:56 GMT
USER ContainerUser
# Wed, 13 May 2026 00:30:01 GMT
COPY dir:45edd54e05e2fb7ffc611e6ef0c2df37aa13ac9c3c9a476003fc542e9ad17481 in C:\openjdk-26 
# Wed, 13 May 2026 00:30:04 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:34ab6476d71f2d23d05a00ac439000ba4c19d17e5c66f15efbe329ed79bba2bf`  
		Last Modified: Tue, 12 May 2026 22:29:47 GMT  
		Size: 199.7 MB (199739001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c6a8908648c0dfbf8d32abc71669debdbb0d446292f14c2e6abe1a34f4ed93`  
		Last Modified: Wed, 13 May 2026 00:28:59 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2430676335d3e201cbef0a1a063645fc4d7a82440656e8b3285588bbfc6026`  
		Last Modified: Wed, 13 May 2026 00:30:09 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342117a011a369bc6f86ef26773c48abb1e4ec53ebf8d904e8691e2e9c66f802`  
		Last Modified: Wed, 13 May 2026 00:30:09 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c9ae66edd08dce3f6f4b7aed94dd5dbea7f67e3b7d18dfcafd7375645a37ac`  
		Last Modified: Wed, 13 May 2026 00:30:08 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ed3c86ee90ce85d21422b9bb5001baabd76c3a90d029b3379c688c367f9d5e`  
		Last Modified: Wed, 13 May 2026 00:30:08 GMT  
		Size: 72.1 KB (72093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd957938c8462a70c7892d04a81114985a09d59dae4f4d908d46e36f81828ab9`  
		Last Modified: Wed, 13 May 2026 00:30:08 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d076c2fcd8dd89d6e5052e54e1a2dc0e094e70b4817cdba078b921d9076e54d`  
		Last Modified: Wed, 13 May 2026 00:30:15 GMT  
		Size: 60.3 MB (60266435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:608b2ccd48b9141c0970e7c007f0aa6ab0cab6206e700545a7bc9acfa2d5a24e`  
		Last Modified: Wed, 13 May 2026 00:30:08 GMT  
		Size: 86.4 KB (86399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
