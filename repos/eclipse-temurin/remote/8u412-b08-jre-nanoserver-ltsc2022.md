## `eclipse-temurin:8u412-b08-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:0ef42cb97eb52458fe215e2f7b89d6e263e7f5a301452d33f1e9d53ce3dbe2b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `eclipse-temurin:8u412-b08-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull eclipse-temurin@sha256:50a5847cca6fa89f1e1594e6e231b320d1f8b79a8787e500b8a597733c856910
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160749343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86e13c75382d11afddc323eebc8b7f749b91233430df900148ad3e1c39f9862`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 09:30:07 GMT
RUN Apply image 10.0.20348.2582
# Wed, 10 Jul 2024 17:17:20 GMT
SHELL [cmd /s /c]
# Wed, 10 Jul 2024 17:17:20 GMT
ENV JAVA_VERSION=jdk8u412-b08
# Wed, 10 Jul 2024 17:17:21 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 10 Jul 2024 17:17:22 GMT
USER ContainerAdministrator
# Wed, 10 Jul 2024 17:17:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jul 2024 17:17:34 GMT
USER ContainerUser
# Wed, 10 Jul 2024 17:18:08 GMT
COPY dir:2b748c8b95a49802258ef446e3948354b660cf39e9ffa8b2cf36461ec042c5c0 in C:\openjdk-8 
# Wed, 10 Jul 2024 17:18:19 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:652774a5d82a114642848f8b0b8d486ec1b4995f9dda56e36fe4ac7563429990`  
		Last Modified: Tue, 09 Jul 2024 20:33:26 GMT  
		Size: 120.5 MB (120490378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dbb650483c31087741ccfe7cfef17abfd7465711d0851e35d39eabc775bdae`  
		Last Modified: Wed, 10 Jul 2024 17:38:52 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b07b4ab2b5c1253e760d8d609ce086416c7f607dcd785ddc10ae04fc6dcf43`  
		Last Modified: Wed, 10 Jul 2024 17:38:52 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466a2a5b4537cebbb010784b348c6d9dcd47b4f8d69d7cf47584a4b2b06a7e1e`  
		Last Modified: Wed, 10 Jul 2024 17:38:52 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349dbf14a3f3dbc38bcf98fa084b4075217e8f81a60abc6a8419f18e28409955`  
		Last Modified: Wed, 10 Jul 2024 17:38:50 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44202090d90884ecdf62a2ed28b786bc9682ca7d588cdc44d14ebe2faee6ba39`  
		Last Modified: Wed, 10 Jul 2024 17:38:50 GMT  
		Size: 76.1 KB (76072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a2df7fd32b943df2a978a5227c92cbf590367f08819a2f021c1eb239e4ef10`  
		Last Modified: Wed, 10 Jul 2024 17:38:50 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c4ba3d4dc76b4e4253ccd9ce5c0ff10f257ccb0fe6c26961e70b40505e85a2`  
		Last Modified: Wed, 10 Jul 2024 17:39:25 GMT  
		Size: 40.1 MB (40115936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533c5495b40cc5dc6f7e2bb9e14512af5c3933fcc23a6a07c0e84b98a52f3ba8`  
		Last Modified: Wed, 10 Jul 2024 17:39:18 GMT  
		Size: 61.3 KB (61253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
