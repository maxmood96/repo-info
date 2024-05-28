## `clojure:temurin-21-bookworm-slim`

```console
$ docker pull clojure@sha256:128c5aa944cda4942e89bface7b5ef0ef36816b32247392e0c953faa240dfa95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-21-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:543875f92156398ba82c2191eae8e4adc79ed7c9e413ce6b40cf3e557b6e3344
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256716340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ebc2397efdb6da10925e155031d27c9a91148e717fcd0afeea4cc38ff949ca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:16:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 May 2024 02:26:47 GMT
COPY dir:2191d32deb04bfc59d7fcf2244f16c5ecbe60498375dcea5599e5d16a61b7305 in /opt/java/openjdk 
# Tue, 14 May 2024 02:26:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 02:28:41 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 14 May 2024 02:28:41 GMT
WORKDIR /tmp
# Tue, 14 May 2024 02:28:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 14 May 2024 02:29:00 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 14 May 2024 02:29:00 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 14 May 2024 02:29:00 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 14 May 2024 02:29:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4c4fae2d7be70250ec8504a05324e67af7721d2c8193f8d83f2d4d5fd88fc5`  
		Last Modified: Tue, 14 May 2024 02:43:57 GMT  
		Size: 158.5 MB (158498262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb873f00af90a8170f13b2274474ab81e1b00e3335ea3c9a3950d0384427c9db`  
		Last Modified: Tue, 14 May 2024 02:45:43 GMT  
		Size: 69.1 MB (69066653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbfcf80a31cf52a56e6df7385a49b63f3006016e35b551702e9599515979f6f`  
		Last Modified: Tue, 14 May 2024 02:45:35 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526f3679c49805459f81ddd500b655b05d20827ccf7bd1a3244167e9caf11a20`  
		Last Modified: Tue, 14 May 2024 02:45:35 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-21-bookworm-slim` - linux; arm64 variant v8

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
