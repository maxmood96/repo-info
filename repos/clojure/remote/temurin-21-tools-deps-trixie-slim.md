## `clojure:temurin-21-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:3244f0fda47e3363ce0dcdfcf44e1e495ea8ca901803a531d32753ac17e25ba6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b175d41bc344108151e6600dc9ed5d109ab5d4a7893805a33df1e0eb2ae42c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.1 MB (262056321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa42b6417dd1ba70009fad80b6fd3b75babccc7beee246d931956c5a444dd3c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ced038dea045df288fe9bdbe03117ca66fe2a071217e196ac86ed07f965fe688`  
		Last Modified: Tue, 03 Jun 2025 13:30:48 GMT  
		Size: 29.8 MB (29755384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d381b01eb8a80d0a69cb9011ba33dcb59c98ed8503af0ab673a07c1df65c0fae`  
		Last Modified: Tue, 03 Jun 2025 19:17:11 GMT  
		Size: 157.6 MB (157634512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26d8c69150e8fc803f3b9e060db8bd84d8ec57f553a19d059407329c483f371`  
		Last Modified: Tue, 03 Jun 2025 18:25:06 GMT  
		Size: 74.7 MB (74665382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0959d92050d685b48443d6d0899f27091edaaabfa98210c40953ab49654c264b`  
		Last Modified: Tue, 03 Jun 2025 18:25:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd39c2ea3e53e926ce4e55b52c9deb3bacba822b93744e80e070a5c97d4d795`  
		Last Modified: Tue, 03 Jun 2025 18:25:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1d77dd29f854c4973072de8d4175cedbc2f36af44883ba2c729af7a131f84977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d912de538cad3eeb975a632128b941643406aec23ed27c2122e4e21a0da5e27`

```dockerfile
```

-	Layers:
	-	`sha256:b0052a07ff48db55ff52d41ca3a85be1e3b9fa7e2ccdb7ae206b8a622c66cc87`  
		Last Modified: Tue, 03 Jun 2025 18:38:47 GMT  
		Size: 5.1 MB (5115855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:457c6e0236610f3938d5d0f1913da93d8d402faee5a1b4e58f6bb68a80953b00`  
		Last Modified: Tue, 03 Jun 2025 18:38:48 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c78d85682eeb31d16aa0bde6965517df1fa76862165aecbd9296e4e7b55de4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (261016903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9184c7f95a08b2978170ba41bfc189f5950b78e0dee74c98ec142bc9108ec0a8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6098c2c9fa277c00ab580ce12bf64a9e1edf9e9139ba18ad85f3cc3063834aa6`  
		Last Modified: Tue, 03 Jun 2025 13:33:56 GMT  
		Size: 30.1 MB (30119455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4a1faf17299c1f04638ddc5d736ac61ac6707116abce4ce0b018d30b88ee49`  
		Last Modified: Fri, 06 Jun 2025 11:55:14 GMT  
		Size: 155.9 MB (155928817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0d4b4cd0e7e8c631e70a2b23030e93236323f26f67234d83e6f6f7f7e1174a`  
		Last Modified: Tue, 03 Jun 2025 18:51:36 GMT  
		Size: 75.0 MB (74967589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f64b1514312da0592a4b73d2ca8fa3aaf231f07ecbb4b30c781cdf20fe19b88`  
		Last Modified: Tue, 03 Jun 2025 18:51:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3601f3220e280b18cf17b1d5e8fa8c9ac44c7ff5ab6ad76041a65563b1009f39`  
		Last Modified: Tue, 03 Jun 2025 18:51:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f2bccc9216b7c5855d78571761f5b338d0ac4375c0005c1aa155986449ec7f46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d39e2151c57a6ae760bef87d11ea7ce8269a2e427b59e94f0d1440b6a777c1`

```dockerfile
```

-	Layers:
	-	`sha256:6ad54471938c159f301dc5133d334fb4b40b4400c651ad7d0ac4a9d836fe8db9`  
		Last Modified: Tue, 03 Jun 2025 21:41:42 GMT  
		Size: 5.1 MB (5121648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:709f07fee8a8665c720244a1dc6f395051c25cd8e7001f9afc12144ca0fb5e2c`  
		Last Modified: Tue, 03 Jun 2025 21:41:42 GMT  
		Size: 16.7 KB (16684 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:0aad3268de5d3b205e44c269989d777a3f5ec58bb99504e50f98a8f6185d0188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271788131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae1f9229851f384a25dc9f6c1aa694ffa4df83ca138569cd54c5550b2d25210e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:62eecea9deba6eaccef3e829ddec51f2c540dbbb668a68816c8ce3c4b8023d93`  
		Last Modified: Tue, 03 Jun 2025 14:07:09 GMT  
		Size: 33.6 MB (33580565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2ab9d4ac6bb74fed4f1c45b064cd14cdabf6a0b701738b0c7f33fe7866ad1a`  
		Last Modified: Tue, 03 Jun 2025 09:13:13 GMT  
		Size: 157.8 MB (157804907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db25bc1c008d11755dbc6eec06fc5ce5b5fcd99ee1e25a4afb81d52b08ee08e0`  
		Last Modified: Tue, 03 Jun 2025 19:09:07 GMT  
		Size: 80.4 MB (80401614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e48a4272c3ff8c8f474f181489db1f342d6fb854ae2b4a9f6ce67f70b82f781`  
		Last Modified: Tue, 03 Jun 2025 19:08:58 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb5b80ffd5d73d279d2954ff8ae9f52ce75f3cf9d8541c478adcbf926846175`  
		Last Modified: Tue, 03 Jun 2025 19:08:59 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2878bf506d106f5a7b6b2360b5f8193f83e1f0bf05a80c775a1d27eb7df882c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5136840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e2b808008e1aa1664941ec678a932d3b3292d88834e5d6b97e632b1524fa3c`

```dockerfile
```

-	Layers:
	-	`sha256:bde84f0bae72871baad4e349a3342cafba5a85cf74aac4386ff0972076460f1c`  
		Last Modified: Tue, 03 Jun 2025 21:41:47 GMT  
		Size: 5.1 MB (5120238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f68221c42541a5627c67b26c7a66d6214cf64bc97e1e6f9bd546899c86bcfb73`  
		Last Modified: Tue, 03 Jun 2025 21:41:48 GMT  
		Size: 16.6 KB (16602 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:4eea38c6f3f62bddf76ddbea4718342d97ab4d601234ba2960b93f67684a616b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (255004223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add8ca6c86a639301a251c24c33f12d348af77b90d1e3a528697675b75fe4444`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f092cb6a76bde9a7b3c337ea49e8a7adec71062dc5df097be99d3975e92bc53a`  
		Last Modified: Tue, 03 Jun 2025 14:07:17 GMT  
		Size: 28.2 MB (28245354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5009b64f50fb13ff55ef1af62e2fe1e6a6ee386115f6dc3a0f39a750f60310`  
		Last Modified: Tue, 03 Jun 2025 09:46:36 GMT  
		Size: 153.4 MB (153449629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420262cff85e153aafb17a5361664e3f8deb41b205a9395783de981e6b660680`  
		Last Modified: Tue, 03 Jun 2025 19:08:17 GMT  
		Size: 73.3 MB (73308202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed4b7269c82382974c9b9864a1a712c8f7fd2e5945e6140fa84ce37af67dd73`  
		Last Modified: Tue, 03 Jun 2025 19:08:08 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2dd2ae363ffdfde54e2132a94707bce78e53faf9a84fe37f081b6728cfb1b7`  
		Last Modified: Tue, 03 Jun 2025 19:08:08 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0a4cbc8479639e0f716d818ee795310cc806d826c830dc570898c95900f26009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5121933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0885e23ccd980ad59fc992705aeefac779e576538a18aa4c08e0f7f627878126`

```dockerfile
```

-	Layers:
	-	`sha256:b2c876127209e8a8b6224e33f864d0a6cb37bb6f6d5dc057bc4d5f856df3bde0`  
		Last Modified: Tue, 03 Jun 2025 21:41:52 GMT  
		Size: 5.1 MB (5105331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63a4f681961efb5405a3fefabcb4d7609af347206c0b84873912a1165eeaf816`  
		Last Modified: Tue, 03 Jun 2025 21:41:53 GMT  
		Size: 16.6 KB (16602 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:2004b3504915521c8045962daeb13e5f5eb8a4b40a629573d57a268d8a81d4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252147674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0090166e5748da136c97a24645e8aed4f4fc407e52ee2096883b1bd99bf9ae6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7cbda353d6047374e3da60bdf79ae89f8047840010f0964c87a8f2714e146106`  
		Last Modified: Tue, 03 Jun 2025 13:43:57 GMT  
		Size: 29.8 MB (29829620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce31050e492004a774304e4a6a039f15374ef94ca4f31b4d1ea37f80078b58a`  
		Last Modified: Tue, 03 Jun 2025 06:29:06 GMT  
		Size: 146.9 MB (146910974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d58315c607b4aff51fb78d64ae4d5ebb6bd079fff0187ac751a32fd9ebba70`  
		Last Modified: Tue, 03 Jun 2025 18:43:02 GMT  
		Size: 75.4 MB (75406039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97da64958e3c8f247a8c2a030244ba9e6cca1d8777ffbef1978b0771fb79f83`  
		Last Modified: Tue, 03 Jun 2025 18:42:55 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9758a926855c7e6932421ba985a86bd81194aaa567eb8931f9a6ccca89b680`  
		Last Modified: Tue, 03 Jun 2025 18:42:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4c38207965ec58471b9801f4f12b28e611576b8ca528f4b83bbe881a54b219b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5128322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a47144e3abb899737d653fd94e567f3f5879c301e5174ce13a16d27a27bba5`

```dockerfile
```

-	Layers:
	-	`sha256:20bdee4e1224c933636a08542bde6a4312c52992dd7caf890b9168216fa18fe4`  
		Last Modified: Tue, 03 Jun 2025 21:41:59 GMT  
		Size: 5.1 MB (5111779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e058c61b244ee18fdfbc449247bef234b3f3bfa70d7d87e9762a30bd887d0ef`  
		Last Modified: Tue, 03 Jun 2025 21:41:59 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json
