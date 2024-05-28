## `clojure:temurin-21-tools-deps-1.11.3.1456-bookworm-slim`

```console
$ docker pull clojure@sha256:fce7470832dccae51398385226a2d3c060b4848abf67fe933cf87a792275dc79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-21-tools-deps-1.11.3.1456-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7c38347e2cfe80b253165e9583406c0ea8c9c54f916639b6b6b4572d3dad47c8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256716574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f8d546818917e7aa991a1de304f25359e09a352218c4e024ce2c101080c3cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 28 May 2024 21:21:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 21:38:16 GMT
COPY dir:2191d32deb04bfc59d7fcf2244f16c5ecbe60498375dcea5599e5d16a61b7305 in /opt/java/openjdk 
# Tue, 28 May 2024 21:38:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 21:40:37 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 21:40:37 GMT
WORKDIR /tmp
# Tue, 28 May 2024 21:40:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 21:40:56 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 21:40:56 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 21:40:56 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 21:40:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23c7a7173a268d2dfa0a4b24a7e486328df02bcd9c9933b9fff802cfa027875`  
		Last Modified: Tue, 28 May 2024 22:01:05 GMT  
		Size: 158.5 MB (158498320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a760f95ce3abf593ad73ebbd3aaae5b74deb403e664419bc0fc6cb46a1add37e`  
		Last Modified: Tue, 28 May 2024 22:03:08 GMT  
		Size: 69.1 MB (69066829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd6ed5efec7ebf85266f0bf75bfd4d7943ba034403a14e5b680eb0a10691088`  
		Last Modified: Tue, 28 May 2024 22:03:00 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0bf0eeea346314b1a41f06455c28730b5aedb66157a433ec08d0d887064a1e`  
		Last Modified: Tue, 28 May 2024 22:03:00 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-21-tools-deps-1.11.3.1456-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b89ae00a9cb76e1a94e557e8df653afa730f52c7f133db308db51a734398a1bb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 MB (254664535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3a2b8501185acc4198795b33c8390304fe118f0b32f9da714406415b106598`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:44:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 19:58:40 GMT
COPY dir:96a90c8e1c03defb238a6d560d8927dc81a1a58af3fce1471cbce5249ed27f38 in /opt/java/openjdk 
# Tue, 28 May 2024 19:58:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 20:00:33 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 20:00:33 GMT
WORKDIR /tmp
# Tue, 28 May 2024 20:00:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 20:00:49 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 20:00:49 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 20:00:49 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 20:00:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1920ac4105cbc22b81c26ddcaabfb2c362fe3c65503c90870b72f26ce9cc92`  
		Last Modified: Tue, 28 May 2024 20:18:30 GMT  
		Size: 156.7 MB (156665508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06828b245099f3a54f5945eb148ef3dc1cbc8a12b8995971bd1d4e4467c3ae3c`  
		Last Modified: Tue, 28 May 2024 20:20:13 GMT  
		Size: 68.8 MB (68818509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680c2b889b83acf5ca782d4d2c60cb6744e8d419d08e8e53b36d76f6221d78b1`  
		Last Modified: Tue, 28 May 2024 20:20:05 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4745fbcdf77976647496749cdd7406354e9aa339a2e0c18f71035fe538ddcf55`  
		Last Modified: Tue, 28 May 2024 20:20:06 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
