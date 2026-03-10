## `openjdk:27-ea-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:d5939881779ff299fe515d2957967e886adf561566098679e969c35d1d278b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `openjdk:27-ea-nanoserver-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull openjdk@sha256:c52b14e2b32b9f865cff552d21364481a9250cdb856c675c12c7701731b86623
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.2 MB (351174019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a1e7360b57387aa6c02665432eabe06e555084ecf13bc0c147fb90a561d9662`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 22:36:44 GMT
SHELL [cmd /s /c]
# Tue, 10 Mar 2026 22:41:07 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 10 Mar 2026 22:41:08 GMT
USER ContainerAdministrator
# Tue, 10 Mar 2026 22:41:10 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 10 Mar 2026 22:41:10 GMT
USER ContainerUser
# Tue, 10 Mar 2026 22:41:10 GMT
ENV JAVA_VERSION=27-ea+12
# Tue, 10 Mar 2026 22:41:19 GMT
COPY dir:39bc387d6f4a82116c9105a5f2b625fb020bc268f5298b0afe5a9520fad3060e in C:\openjdk-27 
# Tue, 10 Mar 2026 22:41:24 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 10 Mar 2026 22:41:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c53f03c3b3ab65bb48a9c595259f256e55cc01d3f30eccd9d8481641d550db0`  
		Last Modified: Tue, 10 Mar 2026 22:37:40 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804894eb8d5ee55df2c493981ede1f9378a6f538b07d673c5f8b5d6d4fef1e12`  
		Last Modified: Tue, 10 Mar 2026 22:41:30 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1bca47bc1e5f47d391ac5f696f9ea8e8b1cbbb139a28f0578d16ef561753e3`  
		Last Modified: Tue, 10 Mar 2026 22:41:30 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b22cdee441f7151fa5ac0a799a5373f9342839d21e79e8557f6890f2cb2731`  
		Last Modified: Tue, 10 Mar 2026 22:41:30 GMT  
		Size: 76.6 KB (76598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00819e2b59b0a3534a67f37d911a6f582affb19555fe34313306610a537ad7c1`  
		Last Modified: Tue, 10 Mar 2026 22:41:28 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8280407515c193ed7916f06aa61f3296cee00314926687f63eed243b65d32551`  
		Last Modified: Tue, 10 Mar 2026 22:41:28 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131595f0f4cf2b694ae01fd7c7fe616ba85a84db7ac6276200a0265f0553693d`  
		Last Modified: Tue, 10 Mar 2026 22:41:44 GMT  
		Size: 224.3 MB (224333803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e91e54d91f7b4b49973aafd8a3e2e464c128bd2ca07dacfa70877951d2d2d2`  
		Last Modified: Tue, 10 Mar 2026 22:41:28 GMT  
		Size: 106.8 KB (106753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3832503e6198e131290df9083433af5cd8a167536ccb1bb3a771c4c533d55fb`  
		Last Modified: Tue, 10 Mar 2026 22:41:28 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
