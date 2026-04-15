## `openjdk:27-ea-17-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:ce750ac8d76a602ff58a2903c44b3792bf8f3f010d307dd2832122459e772722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `openjdk:27-ea-17-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull openjdk@sha256:2ce06361119fa8a5ab2f2fe945d605d33b91a0dc74c342ce4c24dbbacd2cfd53
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.0 MB (352002872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bdc345ae9d9cce5ab5d4cbb4f61daa3ed79b7444eb5f75b351f7b29ed331d4b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 22:11:19 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2026 22:15:21 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 14 Apr 2026 22:15:22 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 22:15:24 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 14 Apr 2026 22:15:25 GMT
USER ContainerUser
# Tue, 14 Apr 2026 22:15:27 GMT
ENV JAVA_VERSION=27-ea+17
# Tue, 14 Apr 2026 22:15:57 GMT
COPY dir:0691f65abcad9aa5e8b70bfb251a5fc900e0d4cf82de17dca757301a739d34d1 in C:\openjdk-27 
# Tue, 14 Apr 2026 22:16:04 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 14 Apr 2026 22:16:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a92e0e44c72d10bf75d0edaa06ddcc97f14d6c2afb302cffe065c90d3dee37`  
		Last Modified: Tue, 14 Apr 2026 22:11:56 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3766390d50944426798a56c14603210869c055d2a1d5a05eedfd6f066fc3b609`  
		Last Modified: Tue, 14 Apr 2026 22:16:10 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76091565f49863a6bccb0e404eba432f03fcd8a77cc27b96d7c1ec8a0bab9c4e`  
		Last Modified: Tue, 14 Apr 2026 22:16:10 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee7044106cf59d26f234a2c7c6708d2e270fe82d09df2480f307888facbbe20`  
		Last Modified: Tue, 14 Apr 2026 22:16:10 GMT  
		Size: 76.4 KB (76449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24944b8b2118691d166efcd8a784c9145239cb3e31b4c36522cdfec18101a1ee`  
		Last Modified: Tue, 14 Apr 2026 22:16:09 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176211b85a36785dc9a7f9a93a802c836934b908c797bdd618ce1846c597961f`  
		Last Modified: Tue, 14 Apr 2026 22:16:09 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e540bb065c65b9a958891ae9aadcf63cf280c78a471cc8ad269ac2630ccd7ae3`  
		Last Modified: Tue, 14 Apr 2026 22:16:24 GMT  
		Size: 224.8 MB (224811347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fce8067ec9a787d2149e28365a5d4bf101f701dcd4cca198f97c177f2d2bf1c`  
		Last Modified: Tue, 14 Apr 2026 22:16:09 GMT  
		Size: 152.7 KB (152664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303e6651e5cdf4aaefabda17debfc4a04d0ebd392ed5851484ba035af4084e91`  
		Last Modified: Tue, 14 Apr 2026 22:16:09 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
