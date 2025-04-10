## `eclipse-temurin:21-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:c5349867874c06279f6403ceeecc88c6ba3de2816697ee19f56a571b40970b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `eclipse-temurin:21-jre-nanoserver-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull eclipse-temurin@sha256:8ddc39fc6d5de2a10fa09cea63c637bee55fd0ec9f8b41cb242ca7b8da3e6133
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159305009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b40df849f8c460a52c1812f6e9604f0b9c305f72ffe819eb5ec53c5e8ef1f76`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Apr 2025 01:31:28 GMT
RUN Apply image 10.0.17763.7136
# Wed, 09 Apr 2025 02:48:34 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 02:48:36 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Wed, 09 Apr 2025 02:48:37 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 09 Apr 2025 02:48:37 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 02:48:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 02:48:40 GMT
USER ContainerUser
# Wed, 09 Apr 2025 02:48:44 GMT
COPY dir:c0b7c132c85049081486a93cd76fe016c559b0b921796f63592a768b082ae9e2 in C:\openjdk-21 
# Wed, 09 Apr 2025 02:48:48 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:a06e0965a0fa3715e629889bd9332aa22aadd75654cac5c9818b67c0264b3ee1`  
		Last Modified: Tue, 08 Apr 2025 20:16:02 GMT  
		Size: 106.9 MB (106922524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae59fc3d956527eb385790dd6757c2506944546c5fd7b1f844b253b0677907a3`  
		Last Modified: Wed, 09 Apr 2025 02:48:52 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a60c465d39daa356fe1ff52c6fc848caa3a9cfeb8369ef2b573dd057afc8a1b`  
		Last Modified: Wed, 09 Apr 2025 02:48:52 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c938cb4b933193118295a11996328ac1633cf05a9711ed7de139d6d274fe2a3`  
		Last Modified: Wed, 09 Apr 2025 02:48:52 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b63e86600b2dfb7a27186010e1339a699e256e783a7695c347c037c195e13e`  
		Last Modified: Wed, 09 Apr 2025 02:48:51 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0dae61f3582cf7a520911ddfc21c039b34b2abc5618f0745274a11da66df536`  
		Last Modified: Wed, 09 Apr 2025 02:48:51 GMT  
		Size: 71.4 KB (71447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628e8c2df97e98be5b729aad1b85e8b08bdf6d04a76a0425a2efcd08b9d5dee9`  
		Last Modified: Wed, 09 Apr 2025 02:48:51 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93bd191a34d864c7030cad792d38739dda38b0ad7d1f6e9df3b8d570f9b33ad7`  
		Last Modified: Wed, 09 Apr 2025 02:48:57 GMT  
		Size: 48.9 MB (48941122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f858c3db20c1296e5f6a402fe2ff42363b0c7c53764209dbc13d0658589ce17`  
		Last Modified: Wed, 09 Apr 2025 02:48:52 GMT  
		Size: 3.4 MB (3364697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
