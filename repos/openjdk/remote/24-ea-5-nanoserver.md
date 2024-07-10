## `openjdk:24-ea-5-nanoserver`

```console
$ docker pull openjdk@sha256:eb158e17a974e4e645c53dfa83683f3a45388e7848b81b279eb3a39a2e6e9318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `openjdk:24-ea-5-nanoserver` - windows version 10.0.17763.6054; amd64

```console
$ docker pull openjdk@sha256:cbce8ee6a87876182cff96ea3ddbd9e5f53d0d8945a14983b7ff3a283bb9a4f3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.5 MB (366507335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ed6368436922ff4c62b090f3c947ec1a6342783a6436f9d1bb0db467b3f8ac`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 18:12:58 GMT
SHELL [cmd /s /c]
# Wed, 10 Jul 2024 18:12:59 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 10 Jul 2024 18:12:59 GMT
USER ContainerAdministrator
# Wed, 10 Jul 2024 18:13:01 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Jul 2024 18:13:01 GMT
USER ContainerUser
# Wed, 10 Jul 2024 18:13:02 GMT
ENV JAVA_VERSION=24-ea+5
# Wed, 10 Jul 2024 18:13:09 GMT
COPY dir:42629391e472e10c3a5c0e61498da2606abe04ae5ffbc2871bee3fab2500b46f in C:\openjdk-24 
# Wed, 10 Jul 2024 18:13:15 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 10 Jul 2024 18:13:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a14c10008e58bc21e48b45ce9d7b4685deedbda75c14dbb0c38503ab32b5634`  
		Last Modified: Wed, 10 Jul 2024 18:13:22 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70eb920170aae3c52c3032252cf36d44223508049fdb6ea8b33f7cf5a2ea1393`  
		Last Modified: Wed, 10 Jul 2024 18:13:21 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef84f0b33917886cc20e5eb21098f956158491baee0b860e9215fb9684883852`  
		Last Modified: Wed, 10 Jul 2024 18:13:21 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e468d65ccd7942e72e9beaaa869065daa447e1ec74034cfb414d19dd86e49dfa`  
		Last Modified: Wed, 10 Jul 2024 18:13:21 GMT  
		Size: 70.2 KB (70214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c387912576850326fe094eac894562676aa0c1a90edfd3272275b9ba94a607`  
		Last Modified: Wed, 10 Jul 2024 18:13:19 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20acbc50b6371068aaa8eae60f8d14d931cd9a0269f0d6b4067069e6a35cbfd`  
		Last Modified: Wed, 10 Jul 2024 18:13:19 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2971d772092a6b9299b5705c3e9edeead1d71224b30a803a5f42f88af459794`  
		Last Modified: Wed, 10 Jul 2024 18:13:32 GMT  
		Size: 206.2 MB (206202881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b43e080fcceb7bf2f82e4167e0ac75fe601b9536a8d8346b5d3b64cf09fc75`  
		Last Modified: Wed, 10 Jul 2024 18:13:20 GMT  
		Size: 5.1 MB (5146620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8673f70d3309a37572037039dc9c6b524c2eec68a52791c6e0ef27cbd0c04deb`  
		Last Modified: Wed, 10 Jul 2024 18:13:19 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
