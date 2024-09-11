## `eclipse-temurin:11-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:80827f43ba1a42586f8b912b9a041955a663acab6f88c72031806a4bb3c53dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull eclipse-temurin@sha256:fa9a65e230c8b0fae95c42ca9be441e03050c9994d2dcdfe44e9230f2b9b9485
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.9 MB (163917010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f6160128d3061b674adf09bb49c1be34d47e03876ef56e603ad71c11d6dc18`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 05 Sep 2024 23:48:03 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 01:05:47 GMT
SHELL [cmd /s /c]
# Wed, 11 Sep 2024 01:06:51 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Wed, 11 Sep 2024 01:06:52 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 11 Sep 2024 01:06:53 GMT
USER ContainerAdministrator
# Wed, 11 Sep 2024 01:07:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 11 Sep 2024 01:07:01 GMT
USER ContainerUser
# Wed, 11 Sep 2024 01:07:41 GMT
COPY dir:d312cd25f7717f1c23a729ceda7f0a5b69cc56184795f5759819b3fb155af4e0 in C:\openjdk-11 
# Wed, 11 Sep 2024 01:07:52 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:a447243899be39b01c34fc7e1bcecb47ce42b14668876fdd121f8b5e2d4d4a86`  
		Last Modified: Tue, 10 Sep 2024 22:28:02 GMT  
		Size: 120.5 MB (120509521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015f530aeae2fa9f5c34641a19099e9949880479ad7319678bd0506ba1927a95`  
		Last Modified: Wed, 11 Sep 2024 01:33:11 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb8fc165231f0ac01f3f49e3863537debb756f545e24faa797835d7a82c1104`  
		Last Modified: Wed, 11 Sep 2024 01:33:55 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226153802201755c536f792f8f86b0e0cf059c6b64f38dfd260dbc2ed394bc4e`  
		Last Modified: Wed, 11 Sep 2024 01:33:55 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea66e9d0f05f631f1b33df4a821d35938474f945ee3d182336e4de260af21e6`  
		Last Modified: Wed, 11 Sep 2024 01:33:55 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f03e4d90b49299418c82a3f1c052d100ba3199ec9d7ce399b989d5a1ddd8a0`  
		Last Modified: Wed, 11 Sep 2024 01:33:53 GMT  
		Size: 77.3 KB (77308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0ed8186a4fc8838840ef3a2662b606b337a503db11f07a8e4cd97620cc9c0d`  
		Last Modified: Wed, 11 Sep 2024 01:33:53 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10fa2fa5da60671fef107c1654493ba529f13b6edd19a816342348f783e28d86`  
		Last Modified: Wed, 11 Sep 2024 01:34:27 GMT  
		Size: 43.3 MB (43263149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:630e83084e1f44e490861baba0767a99e2ec55f7ba3cbc1fd973ca85148a8bc6`  
		Last Modified: Wed, 11 Sep 2024 01:34:20 GMT  
		Size: 61.3 KB (61333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
