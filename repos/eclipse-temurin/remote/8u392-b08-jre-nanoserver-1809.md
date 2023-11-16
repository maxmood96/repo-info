## `eclipse-temurin:8u392-b08-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:c78ecbc7482ef1333f091e7a1497345285c27a8fd5277cab1442b9b62b818202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `eclipse-temurin:8u392-b08-jre-nanoserver-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull eclipse-temurin@sha256:3c9db43c48c303121ce1e8fb5ae4da593e96483e2bdaf722bc86e7b59f741f60
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144763831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9086c19972c304380212cb55ef7e2f7f636de3ff8a38eabb13209893344c2b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Nov 2023 17:21:05 GMT
RUN Apply image 10.0.17763.5122
# Thu, 16 Nov 2023 01:41:12 GMT
SHELL [cmd /s /c]
# Thu, 16 Nov 2023 01:41:13 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Thu, 16 Nov 2023 01:41:14 GMT
ENV JAVA_HOME=C:\openjdk-8
# Thu, 16 Nov 2023 01:41:15 GMT
USER ContainerAdministrator
# Thu, 16 Nov 2023 01:41:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 16 Nov 2023 01:41:27 GMT
USER ContainerUser
# Thu, 16 Nov 2023 01:46:03 GMT
COPY dir:dbdf2dd9ed9894186d74b75beac1320724c73c6994b00118f04985f0ea2b3067 in C:\openjdk-8 
# Thu, 16 Nov 2023 01:46:14 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:24e10ec0ecb89022cf68752b9f9196dcf2f423f9589b14401693fb2a1b3de37f`  
		Last Modified: Tue, 14 Nov 2023 22:06:25 GMT  
		Size: 104.5 MB (104497517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e5c133738aab79d4c21c47e77cb838e2d00166f5e3e2632177622f67488259`  
		Last Modified: Thu, 16 Nov 2023 02:28:08 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001b8d65ec89d4fd832acce6037db85dddec1200131f5e609fa4a8c74d9aa08d`  
		Last Modified: Thu, 16 Nov 2023 02:28:07 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098df4d2a628a16ff447f34741e7530283c13e252104d9e3ac749df571941064`  
		Last Modified: Thu, 16 Nov 2023 02:28:08 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79510d2c134c91689203a24e81971d573b835fdd61baedd442def46468cd6b3d`  
		Last Modified: Thu, 16 Nov 2023 02:28:06 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ee22aa6b0b0623853f8dd73c8d7db27ef87fc407914c74e6b377815e6b5441`  
		Last Modified: Thu, 16 Nov 2023 02:28:06 GMT  
		Size: 69.1 KB (69126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0405951c92e8acd1a52ba508748bbbb67cbf3f9a60ac58872953b1640d32447a`  
		Last Modified: Thu, 16 Nov 2023 02:28:06 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b532cb9a43b34a0a4fadc403700b4eb008723c1cf2c7bacc14b1bb8a1255d17`  
		Last Modified: Thu, 16 Nov 2023 02:29:19 GMT  
		Size: 40.1 MB (40110915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650b2f3620ada1b847f57d4882211af70197721a2d097185cd905d7ce250bd06`  
		Last Modified: Thu, 16 Nov 2023 02:29:14 GMT  
		Size: 81.1 KB (81069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
