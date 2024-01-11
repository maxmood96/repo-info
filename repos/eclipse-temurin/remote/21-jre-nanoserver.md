## `eclipse-temurin:21-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:96eefc044bba901581aa12e072c8063022e0ffb8abcf5b7ad17484d952569bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.20348.2227; amd64

```console
$ docker pull eclipse-temurin@sha256:0a59c7ef83a40d30c20ef992a3835292164f5c0e1cba5c8ba4af02c2a5823608
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.6 MB (169603284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e422e58a686d99017e827438bb3882cc2862654d097dee9920c61673986cd089`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 04 Jan 2024 03:13:36 GMT
RUN Apply image 10.0.20348.2227
# Wed, 10 Jan 2024 23:17:03 GMT
SHELL [cmd /s /c]
# Wed, 10 Jan 2024 23:21:04 GMT
ENV JAVA_VERSION=jdk-21.0.1+12
# Wed, 10 Jan 2024 23:21:05 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 10 Jan 2024 23:21:06 GMT
USER ContainerAdministrator
# Wed, 10 Jan 2024 23:21:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 10 Jan 2024 23:21:16 GMT
USER ContainerUser
# Wed, 10 Jan 2024 23:22:04 GMT
COPY dir:a5a397b00294543a7015e10bed54514e1c5f8af5ed3eff5933ba2b604ae103c1 in C:\openjdk-21 
# Wed, 10 Jan 2024 23:22:15 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:11d5cdc5eaac7bace3ae1ecd3c0df2a27ef5005ab296c56b7f83e24bf25c236c`  
		Last Modified: Tue, 09 Jan 2024 20:57:18 GMT  
		Size: 120.8 MB (120769267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a5f2601f3a3b05b34c1f8683e3c9ea81ea63dbe1b04c37b85d09170f020fc0`  
		Last Modified: Thu, 11 Jan 2024 04:18:57 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb0820211400dec4e153c1886927282ab505977cf5c264b923c75db3505330c`  
		Last Modified: Thu, 11 Jan 2024 04:21:15 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95aff2991b8667c66d40974dc6bf32c04ed96d6225e5cb7759c418f68a6edb37`  
		Last Modified: Thu, 11 Jan 2024 04:21:15 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf3bc46f30940d81e38a97c0cb0383d2a82784e1543bf5e8febf0d5903d5505`  
		Last Modified: Thu, 11 Jan 2024 04:21:15 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a532a318c9949ef279ad340461a67508a00b13ee829f7d49d80a2b2c68cef80`  
		Last Modified: Thu, 11 Jan 2024 04:21:13 GMT  
		Size: 83.9 KB (83908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5936bd13281cecf6165dbc08623caec1e1a756b44deb81a196b0c87713de4310`  
		Last Modified: Thu, 11 Jan 2024 04:21:13 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db4bbfd26b2fbbe7e5b55aeb43215d9e410661f96eaba35588c9fd888db8a9b`  
		Last Modified: Thu, 11 Jan 2024 04:21:55 GMT  
		Size: 48.7 MB (48689656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1328db2b3fb8eb4e0ee1e9e69993fc5fe3f3c86560bdd6b6aab54205bd89578`  
		Last Modified: Thu, 11 Jan 2024 04:21:45 GMT  
		Size: 54.7 KB (54651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-jre-nanoserver` - windows version 10.0.17763.5329; amd64

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
