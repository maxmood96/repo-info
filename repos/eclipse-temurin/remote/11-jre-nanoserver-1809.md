## `eclipse-temurin:11-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:f1a83756920e258f81b79b1e290a7b80e14b16f5f755bac4c00d038f9f7dbb30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:11-jre-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:aa0e56b632fa8bbeaf39acbfdd549e0f656dd9306c69f4a055124f5207bb7510
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199066743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f0f3818a91a8221d01180db72866dcaae02a6b37aeb6808a623ba97193c54f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Fri, 31 Jan 2025 03:11:50 GMT
SHELL [cmd /s /c]
# Fri, 31 Jan 2025 03:11:51 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Fri, 31 Jan 2025 03:11:51 GMT
ENV JAVA_HOME=C:\openjdk-11
# Fri, 31 Jan 2025 03:11:52 GMT
USER ContainerAdministrator
# Fri, 31 Jan 2025 03:11:58 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 31 Jan 2025 03:11:58 GMT
USER ContainerUser
# Fri, 31 Jan 2025 03:12:03 GMT
COPY dir:e7319a06d2b9171c954fc18de0614fa7d0eb408950b795be61492806db04a6ea in C:\openjdk-11 
# Fri, 31 Jan 2025 03:12:06 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Wed, 15 Jan 2025 07:23:16 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca7086926f493ad2a6ede9e3319b925ec28b99d058d68a4081b62c96ac13138`  
		Last Modified: Fri, 31 Jan 2025 03:12:12 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28197d935e34282bed8a0d1b5a0e82033931980697a186696abfab36853842d0`  
		Last Modified: Fri, 31 Jan 2025 03:12:12 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f593f1be8e1799dccc0a794177ed739e2ab5aaa7d4b497c19be7e5a08e17ee`  
		Last Modified: Fri, 31 Jan 2025 03:12:12 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76afdfaa508b86bcb2c0a9797badf093381bbd1e156bced1c87c1a112ba2060f`  
		Last Modified: Fri, 31 Jan 2025 03:12:10 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2810864b89b5f5c2354c07eb9824355075b3c0be475b0e5f06acc941edf528e`  
		Last Modified: Fri, 31 Jan 2025 03:12:10 GMT  
		Size: 68.0 KB (68027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84178d01dd8413e9a7b495c7544e274d918013a6a3f1a959db6f7852c1bbf375`  
		Last Modified: Fri, 31 Jan 2025 03:12:10 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3e4799f58112b1f496e941d62072cd76d2461b8975b4d249b4fa2315f16d23`  
		Last Modified: Fri, 31 Jan 2025 03:12:15 GMT  
		Size: 43.7 MB (43656864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49563bdb3d17f5cd27ccb84ec1ab2c3e6fe6130d157b498024f89ca9b663c03`  
		Last Modified: Fri, 31 Jan 2025 03:12:10 GMT  
		Size: 68.8 KB (68773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
