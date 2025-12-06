## `openjdk:26-ea-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:7f9c8a6b0587a28c88ed4f178cb6c351d972eaa1532c3ecaf487ff407d8c9a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `openjdk:26-ea-nanoserver-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull openjdk@sha256:b132018305aa7a11199029d77582d6608cba6cf484b08e4fa92f9be484e383c1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.7 MB (351726150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a453b79cee9860d61b6c58a02948f3860374a1eecf604896567f4bb9804ecb52`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Nov 2025 05:29:25 GMT
RUN Apply image 10.0.20348.4405
# Sat, 06 Dec 2025 01:12:46 GMT
SHELL [cmd /s /c]
# Sat, 06 Dec 2025 01:12:47 GMT
ENV JAVA_HOME=C:\openjdk-26
# Sat, 06 Dec 2025 01:12:48 GMT
USER ContainerAdministrator
# Sat, 06 Dec 2025 01:13:01 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 06 Dec 2025 01:13:01 GMT
USER ContainerUser
# Sat, 06 Dec 2025 01:13:02 GMT
ENV JAVA_VERSION=26-ea+27
# Sat, 06 Dec 2025 01:14:00 GMT
COPY dir:babad47417a0162dfe31675fb569b90c77d833ec4f406c1de246f79f46496cd3 in C:\openjdk-26 
# Sat, 06 Dec 2025 01:14:08 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 06 Dec 2025 01:14:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f1a2bf860779d298b0b94004e0d2d04a95d761e823b0c7184234535c0d000ef5`  
		Last Modified: Tue, 11 Nov 2025 19:13:45 GMT  
		Size: 126.3 MB (126349074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16dde89ce2f2f82227aa34b5f2850d12d5d12d6cc2260a6de54d26204813bd51`  
		Last Modified: Sat, 06 Dec 2025 01:14:39 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb8917965ccf581d202e99bde5e8bf97651bc3575ba153cfdf04620088937e0`  
		Last Modified: Sat, 06 Dec 2025 01:14:39 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c44db55c78af8da14fc0286ee9e321b1126036b92a30d800bc8f0f57f462e12`  
		Last Modified: Sat, 06 Dec 2025 01:14:39 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4bb74ca0f574a76469d152777feaa1dbd1655712768bb6524463223d4da813e`  
		Last Modified: Sat, 06 Dec 2025 01:14:39 GMT  
		Size: 82.6 KB (82606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b969a263b5b487e123554be3a5321f33a4d0c8b1d19b194a17b849da9a8ca657`  
		Last Modified: Sat, 06 Dec 2025 01:14:39 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2777d100be2889eb6e5bfcaa4dacc9cb7f859ae3c3f8b80a94a1d41bcdd604ac`  
		Last Modified: Sat, 06 Dec 2025 01:14:39 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a06391b52608979821cc80789c2295010ed01b12fb52ae34bcc065e5f0af483`  
		Last Modified: Sat, 06 Dec 2025 01:14:45 GMT  
		Size: 225.2 MB (225175492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c785c21407064eb8199ef35e71040c5b5f0bcb85d0676ce4141c9912978c7d25`  
		Last Modified: Sat, 06 Dec 2025 01:14:40 GMT  
		Size: 112.6 KB (112581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9449c7b1396fb9f7ab086730c67c8ddbac3a453a3553145a812444dfac83f102`  
		Last Modified: Sat, 06 Dec 2025 01:14:40 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
