## `eclipse-temurin:21-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:62c805d0eab35566468eb726f209605e4c0795d219f78d65b5ca535c1b01cb5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `eclipse-temurin:21-jre-nanoserver-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull eclipse-temurin@sha256:7f96910d10d3073e6bf54e3be3152691c29e8014ee9a3cca505e16750d054320
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.7 MB (156716641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21749eb1d18a932645af867ddea465f56aafa353a33945e2b69106cbe73b554f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Wed, 10 Jan 2024 22:41:06 GMT
SHELL [cmd /s /c]
# Wed, 10 Jan 2024 23:10:51 GMT
ENV JAVA_VERSION=jdk-21.0.1+12
# Wed, 10 Jan 2024 23:10:51 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 10 Jan 2024 23:10:52 GMT
USER ContainerAdministrator
# Wed, 10 Jan 2024 23:11:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jan 2024 23:11:01 GMT
USER ContainerUser
# Wed, 10 Jan 2024 23:16:42 GMT
COPY dir:a5a397b00294543a7015e10bed54514e1c5f8af5ed3eff5933ba2b604ae103c1 in C:\openjdk-21 
# Wed, 10 Jan 2024 23:16:53 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec88c6fd1d0cd14082069642ccb3b0dd5a7538a4b8b0c2d430549f345d8fd53`  
		Last Modified: Thu, 11 Jan 2024 04:09:21 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f947371f94db731a429f4924c1019dfb90d38824515c071ae72e2702280e1346`  
		Last Modified: Thu, 11 Jan 2024 04:17:24 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d892e630c4c0f35f6788ffb8a704125d58c321345db1b7c8791c9ebed5059732`  
		Last Modified: Thu, 11 Jan 2024 04:17:25 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8b04b0717e07a5207a948e72f23afeb6ff8181055323dccf5d42cc5384b003`  
		Last Modified: Thu, 11 Jan 2024 04:17:24 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90639508c1f7fda55369ef3c64d705b2b78a1e6432b3388792c64439b2e7ace1`  
		Last Modified: Thu, 11 Jan 2024 04:17:22 GMT  
		Size: 68.1 KB (68146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d684573824819ca2de63a1a5e404e5a3f1aeb486e8a4388ef7963668da307a88`  
		Last Modified: Thu, 11 Jan 2024 04:17:23 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3314b2c948a45eecd44501a97c31325c99e8fef3c3a0d00c8ad34fd15b2c7274`  
		Last Modified: Thu, 11 Jan 2024 04:18:46 GMT  
		Size: 48.7 MB (48689551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972f06b7758d548e2d23a5cd96150c99cfc90ca7753481887aa70733caf6d296`  
		Last Modified: Thu, 11 Jan 2024 04:18:37 GMT  
		Size: 3.4 MB (3362324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
