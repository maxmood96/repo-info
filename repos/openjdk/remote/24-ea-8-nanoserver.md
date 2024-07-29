## `openjdk:24-ea-8-nanoserver`

```console
$ docker pull openjdk@sha256:9d2f56f0355a00c6deeed564849172549587f17f344c98861259b94e53cf4590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `openjdk:24-ea-8-nanoserver` - windows version 10.0.17763.6054; amd64

```console
$ docker pull openjdk@sha256:9acba8b2ade7103337c34bdb2e512dce6a6fe1c169e395e4883202e8fcd6d918
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.7 MB (365738385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee665681d55758c8199680300a07c386c559743bd95ef438a08efb3e380c46a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Mon, 29 Jul 2024 18:57:14 GMT
SHELL [cmd /s /c]
# Mon, 29 Jul 2024 18:57:15 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 29 Jul 2024 18:57:16 GMT
USER ContainerAdministrator
# Mon, 29 Jul 2024 18:57:28 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 29 Jul 2024 18:57:29 GMT
USER ContainerUser
# Mon, 29 Jul 2024 18:57:29 GMT
ENV JAVA_VERSION=24-ea+8
# Mon, 29 Jul 2024 18:57:37 GMT
COPY dir:c1967bfd4392c46491d2e5d9e59f7ca398a787c2a674096b632e5e99ff564f24 in C:\openjdk-24 
# Mon, 29 Jul 2024 18:57:43 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 29 Jul 2024 18:57:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e14e30479bffacfb385b422d4fa6854e4c941488b4f021fbce4c3c123c103a79`  
		Last Modified: Mon, 29 Jul 2024 18:57:51 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:744f52637ecf51eb0a8358fb0d5672bd467206492de4ef60e09d303b615cce49`  
		Last Modified: Mon, 29 Jul 2024 18:57:50 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062fee9181f6aebbef6a6dd907d009e99d80277f0af69f39067f1279cafd6633`  
		Last Modified: Mon, 29 Jul 2024 18:57:50 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68bcac40547e10e2391f33f5189f658dbc98552953df87623230d70dd9ca6b9f`  
		Last Modified: Mon, 29 Jul 2024 18:57:50 GMT  
		Size: 66.4 KB (66373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70b0a31ab340ca05546ffb1c927af816540b5e2e0e42c59836d20e889cb6061`  
		Last Modified: Mon, 29 Jul 2024 18:57:48 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3549d2a5ade7194e9d4de7671402701f2dc6b9bc9251a5219266dbc590620be`  
		Last Modified: Mon, 29 Jul 2024 18:57:48 GMT  
		Size: 1.0 KB (1049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b56eef085f71bb308b5716cb43f5412f9a1b07bc3720b68ede7156334a50f113`  
		Last Modified: Mon, 29 Jul 2024 18:57:59 GMT  
		Size: 206.5 MB (206535126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da0282e7fce32726d415d5771b2b13c7df34f366439d4a9661f03f12d026e5b`  
		Last Modified: Mon, 29 Jul 2024 18:57:49 GMT  
		Size: 4.0 MB (4049160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432c1b016344d173d16a146a907cbbe0028041000913b84ed034c795c50900ab`  
		Last Modified: Mon, 29 Jul 2024 18:57:48 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
