## `eclipse-temurin:8-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:3cefb55db49f47af52ecb0a24b0a0c13796f8497ea3843fd8609222d5a41ea36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1249; amd64

### `eclipse-temurin:8-jre-nanoserver-ltsc2022` - windows version 10.0.20348.1249; amd64

```console
$ docker pull eclipse-temurin@sha256:88e8d7951d9d056297d42882d220776f9d022cae9fb50ac8d4b8f113269b6f43
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161561731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12aa74b3a82cb7fda8e947ea2ebbfe00994c8c4219a392469ff43bda1a79068`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Nov 2022 07:21:30 GMT
RUN Apply image 10.0.20348.1249
# Tue, 08 Nov 2022 19:27:23 GMT
SHELL [cmd /s /c]
# Tue, 08 Nov 2022 19:27:24 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Tue, 08 Nov 2022 19:27:25 GMT
ENV JAVA_HOME=C:\openjdk-8
# Tue, 08 Nov 2022 19:27:25 GMT
USER ContainerAdministrator
# Tue, 08 Nov 2022 19:27:42 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 08 Nov 2022 19:27:43 GMT
USER ContainerUser
# Tue, 08 Nov 2022 19:28:56 GMT
COPY dir:4e862dd3e9e3173048336ba652726d009cc7bbbadd67bc711cdb421cf611c5ab in C:\openjdk-8 
# Tue, 08 Nov 2022 19:29:14 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:72e5d750fe8c1a32d4a26ef3b4a4e1f6124ac079b142f12724af2abfcba1c8b3`  
		Last Modified: Tue, 08 Nov 2022 19:57:58 GMT  
		Size: 122.1 MB (122092167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd83067a7e6c6d9dab3ac0265a21919de95a0bf4e737e647fbf3e43c9874b0`  
		Last Modified: Tue, 08 Nov 2022 19:57:27 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c220e123f23808745fc630305de0ce242cb9a6c565cf4f700e22655ecf005687`  
		Last Modified: Tue, 08 Nov 2022 19:57:27 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c25f1362ec097d0956355257914a48a3b53f55e8671e01cef2b0e3c09c2da4`  
		Last Modified: Tue, 08 Nov 2022 19:57:27 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3937de06541d6c6a90657c15b73a603495a8d9f762eef4c868205c91c8dbb15c`  
		Last Modified: Tue, 08 Nov 2022 19:57:25 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d7087dd3a321a3aacf542b973f32ba8201f01dbb83c2cb89d350df169b7628`  
		Last Modified: Tue, 08 Nov 2022 19:57:25 GMT  
		Size: 79.6 KB (79630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375446a6e44c1ad04d6728e1b203b940f5a24bcbc2be35a789b03c1d5dabfabd`  
		Last Modified: Tue, 08 Nov 2022 19:57:25 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af3c709bff60353147d6e9c332379e40024474c5d04dab7dfba3e38e593542e`  
		Last Modified: Tue, 08 Nov 2022 19:58:19 GMT  
		Size: 39.3 MB (39322855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ea56bbc5a8e328f634f0d485688e970fbb5a9cbe262e725d625bc1e0775acb`  
		Last Modified: Tue, 08 Nov 2022 19:58:13 GMT  
		Size: 61.4 KB (61369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
