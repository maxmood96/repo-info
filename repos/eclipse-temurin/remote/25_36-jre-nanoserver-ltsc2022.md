## `eclipse-temurin:25_36-jre-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:a52affa7d54a1fb4b7977f64d0c54ce2f255a49e68fe44ffa997ac9daf98ac73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:25_36-jre-nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull eclipse-temurin@sha256:0d405d21056d5973c8aadbfe794375702718abc31cee4a3df62da66f09b4817a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181424635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3086d3da677e99ac5a3a5c34c96ce0953e52b259aae943b625244db7d44ba94f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Fri, 24 Oct 2025 19:21:14 GMT
SHELL [cmd /s /c]
# Fri, 24 Oct 2025 19:22:51 GMT
ENV JAVA_VERSION=jdk-25+36
# Fri, 24 Oct 2025 19:22:52 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 24 Oct 2025 19:22:52 GMT
USER ContainerAdministrator
# Fri, 24 Oct 2025 19:22:54 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 24 Oct 2025 19:22:55 GMT
USER ContainerUser
# Fri, 24 Oct 2025 19:23:15 GMT
COPY dir:8aa8ce0e84e7e6f80be28438d765894541d9d2eadfccff43ebe7257923223c3b in C:\openjdk-25 
# Fri, 24 Oct 2025 19:23:19 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9adff1d5bd5f0331cd06d179e8f7838493a03ac53a23db6febaf0765bbfe2607`  
		Last Modified: Fri, 24 Oct 2025 19:22:34 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661abc182d843efa44ef1a9a47214a159d3c39a367609d2192ad760b6b001ee2`  
		Last Modified: Fri, 24 Oct 2025 19:23:37 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb2246685c2bc0213a3cd3f048e0fd9e0d28e23448ae2eff4e57e1985aa5260`  
		Last Modified: Fri, 24 Oct 2025 19:23:37 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df591df749668abd00a8a3996d4e7f3a474cb3b97cc887c633463450e7709e16`  
		Last Modified: Fri, 24 Oct 2025 19:23:37 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce98ba75604e33d567213c7587bb15cc547f24c556c0813ab0cc4e0ec59bb73`  
		Last Modified: Fri, 24 Oct 2025 19:23:37 GMT  
		Size: 76.4 KB (76435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16604b593d1cd32479b06c8aacd53ee2bd771e68c67b9ba6a2142ea4f2126fea`  
		Last Modified: Fri, 24 Oct 2025 19:23:37 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ef5d535ef5d512aa1a26704dde568b0fe7ba22adf7c5ce337929232842207d`  
		Last Modified: Fri, 24 Oct 2025 19:23:42 GMT  
		Size: 58.6 MB (58551043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1afdfcf44f3a7ca0c3f1771a3f47b6dd169879d19f4520ff73618d255c1f4c`  
		Last Modified: Fri, 24 Oct 2025 19:23:37 GMT  
		Size: 107.8 KB (107774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
