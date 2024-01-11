## `openjdk:22-ea-30-nanoserver`

```console
$ docker pull openjdk@sha256:119372af4040aa40df9d780911a8e2277e914a896cf0f9b968fce57c4c930ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `openjdk:22-ea-30-nanoserver` - windows version 10.0.17763.5329; amd64

```console
$ docker pull openjdk@sha256:9d77d6948738af2768bd8208afdb0f0d572bafb886eb67301d7a76244b8ecdd8
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.9 MB (305852589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9660cbc28823366af85260ebf70acf95009b58bebbe468dbede1d35c6b12ad`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 02 Jan 2024 22:32:22 GMT
RUN Apply image 10.0.17763.5329
# Thu, 11 Jan 2024 00:58:01 GMT
SHELL [cmd /s /c]
# Thu, 11 Jan 2024 00:58:02 GMT
ENV JAVA_HOME=C:\openjdk-22
# Thu, 11 Jan 2024 00:58:03 GMT
USER ContainerAdministrator
# Thu, 11 Jan 2024 00:58:05 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 11 Jan 2024 00:58:06 GMT
USER ContainerUser
# Thu, 11 Jan 2024 00:58:07 GMT
ENV JAVA_VERSION=22-ea+30
# Thu, 11 Jan 2024 00:58:16 GMT
COPY dir:5f6175456bd75036441df77ae70a347d5f61c8c5d6826fd50ec6962633347072 in C:\openjdk-22 
# Thu, 11 Jan 2024 00:58:20 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 11 Jan 2024 00:58:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:37cbb0a6bd5a9996acd9e9f7cddbafa117bd273617c56bfa07424416ef58d236`  
		Last Modified: Tue, 09 Jan 2024 22:20:25 GMT  
		Size: 104.6 MB (104591228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9ff65523edad2704f30d79e3167357f046cb217c05b82b4dfab6be99e3c4c4`  
		Last Modified: Thu, 11 Jan 2024 00:58:28 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2af26a04d10777e3c8c9c4e4bc534d073301cdd2a7530559926b85feb0a28a4`  
		Last Modified: Thu, 11 Jan 2024 00:58:27 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d53c5de826336047d0b465344e2a4679246098023f808dfddc07af7750c183`  
		Last Modified: Thu, 11 Jan 2024 00:58:27 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5c19ac526f09d9eb1c3e8250a10cf7292034e42933c8ddf20ab04f66b6bbd4`  
		Last Modified: Thu, 11 Jan 2024 00:58:27 GMT  
		Size: 73.8 KB (73832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0afb8fc340db9bb7dad3ccdd3c7540280718548beb36cabeeebb5aff1d27b69`  
		Last Modified: Thu, 11 Jan 2024 00:58:25 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1399fa6e78101c7ef7827541b764a3ed580cc90431e717718b4444aadecd3efe`  
		Last Modified: Thu, 11 Jan 2024 00:58:25 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3920e96ed9625298ec3311ea9282dcbcb6227eefd0374e6c4bad80fe5b561e`  
		Last Modified: Thu, 11 Jan 2024 00:58:36 GMT  
		Size: 197.3 MB (197334154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe2a623f596566f858c773b84b6558aab4d32f524647515710cf2b5e82067c32`  
		Last Modified: Thu, 11 Jan 2024 00:58:26 GMT  
		Size: 3.8 MB (3847132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21efc67a9f87cffb1dfed64d4e930966366283133ef6e162ea588cc5f1adc865`  
		Last Modified: Thu, 11 Jan 2024 00:58:25 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
