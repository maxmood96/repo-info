## `openjdk:24-nanoserver`

```console
$ docker pull openjdk@sha256:adaf82c1eaaa32c029087905481f206d7bf854fd6b426f1faadd855bf18b394a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `openjdk:24-nanoserver` - windows version 10.0.17763.6189; amd64

```console
$ docker pull openjdk@sha256:90b812398e653ba6fb947d7741ebebe48ab8a3a4a61d4000bc75fd422a02cb5e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.4 MB (368393346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c4600833dcce8d1e335d04d4047904ad77d0a5979a7bd07f6d5c5ceca913de6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Fri, 23 Aug 2024 21:56:53 GMT
SHELL [cmd /s /c]
# Fri, 23 Aug 2024 21:56:54 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 23 Aug 2024 21:56:55 GMT
USER ContainerAdministrator
# Fri, 23 Aug 2024 21:57:02 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 23 Aug 2024 21:57:03 GMT
USER ContainerUser
# Fri, 23 Aug 2024 21:57:03 GMT
ENV JAVA_VERSION=24-ea+12
# Fri, 23 Aug 2024 21:57:12 GMT
COPY dir:f86baa7bff4606e03b961c0b46c7b3a9e84d3004e30a05dd50f323da0c74d9dc in C:\openjdk-24 
# Fri, 23 Aug 2024 21:57:20 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 23 Aug 2024 21:57:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f70be380cea0e657f1d1757e804746b1555f650ef88b35677ef44266636d37`  
		Last Modified: Fri, 23 Aug 2024 21:57:28 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b239cfd2496c1809bb926024e9884dcfec5f1cff0eec5c08f172b55f11c0eb`  
		Last Modified: Fri, 23 Aug 2024 21:57:27 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d800dc0b56e965bf2e422e667e0d0ff98cf9e74f87a70486d6cc4c8371297c3`  
		Last Modified: Fri, 23 Aug 2024 21:57:26 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f2544aa599cd5a3ac1fadf4c6af102ead9787e761d01eb6aaa94f867ce789e`  
		Last Modified: Fri, 23 Aug 2024 21:57:26 GMT  
		Size: 66.8 KB (66774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6befbc612b836ad2c06dcf5bdbdf85c8202a0486c29ce25b673bb9a41d994dd`  
		Last Modified: Fri, 23 Aug 2024 21:57:25 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaddc69c3631f3e3dcb96f548847a22e17fc13467d7449c647b8cc044db21b97`  
		Last Modified: Fri, 23 Aug 2024 21:57:25 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992c822653b01f700d53e2093a59ff3a47b9933404bb60292150c0063f136074`  
		Last Modified: Fri, 23 Aug 2024 21:57:36 GMT  
		Size: 207.6 MB (207622429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9666d6ab54c407d2c1c05f053c316d1bdd4143deecf622d97bdf3884e2b89df1`  
		Last Modified: Fri, 23 Aug 2024 21:57:26 GMT  
		Size: 5.6 MB (5614787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81bffc4b2ddc7665b2ac489c286312f24e6dbb22c490e265a134c57e361604c`  
		Last Modified: Fri, 23 Aug 2024 21:57:25 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
