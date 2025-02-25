## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:24f8422071a0ba09260b8f8d5c2732ce2404ed4a9f324a6114b9d6d1af5e407e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:642a09eeb5bc21dd4783eb55a6026346fe48ee19053a4a19d42c5e10c4635498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (274037845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9dae22d65fdd2873790e162ab42c6f6763867b7039b1b826cf7310d9f5e70c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70d8f0d47dff0ce19b8d433830013cbb65165ac9cf7731cd27c9d558068358a`  
		Last Modified: Tue, 25 Feb 2025 02:33:16 GMT  
		Size: 144.6 MB (144566545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a775a1814762f04bc70ddc5a75f7feb59ddeb821c443c10df130e84ff581eb`  
		Last Modified: Tue, 25 Feb 2025 02:33:17 GMT  
		Size: 81.0 MB (80994156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68519367c62445d7019b8e784560c6f928c66d8f042b01ab0fa068ea7f554ab`  
		Last Modified: Tue, 25 Feb 2025 02:33:15 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b7008f44cf4624da881fcec684d05f2cb41bd1637ed9628b8eb3860dbe76da`  
		Last Modified: Tue, 25 Feb 2025 02:33:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:70fc9e2e943100222e0fcaeaee3f32746e84f968ccae39b1e97a76d55fcce19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7186916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5818d1ead06acf0f208bb7a242977cfe2c2ef6078a437c0a7d4a82111be172`

```dockerfile
```

-	Layers:
	-	`sha256:f019d1dbe63990252dce60154af6e8c5c431e088a1a800d068e60ecab54d636f`  
		Last Modified: Tue, 25 Feb 2025 02:33:15 GMT  
		Size: 7.2 MB (7171096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b45d6ea11116c4711230ca47a5f707542d7e3927efa11180090d677be6dae57b`  
		Last Modified: Tue, 25 Feb 2025 02:33:15 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bfa4f72cd6747afcb74905e27bef66f5646f4a484dd94e2f485ff30462ad181f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272606540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ade5ddbb2b80350b5e747c112dd84bcb899e42cfd2bff6970dd5f1491422c91`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df762dda615cd0ea3bb492e0a356dc38d0e9557cc2a49308361196d4a1b3619`  
		Last Modified: Tue, 25 Feb 2025 11:02:42 GMT  
		Size: 143.5 MB (143454699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3723142033041ec4abb49ab10d79a3a10bc1b2f5ab4c442414302c3db89db7ff`  
		Last Modified: Tue, 25 Feb 2025 11:06:05 GMT  
		Size: 80.8 MB (80842789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6a3c163e4682a3a077e22578ee6b77763d13a348ab234c70f5c0474d3f195e`  
		Last Modified: Tue, 25 Feb 2025 11:06:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422adbe9efcd24f0b717065fb272c1f35a7ccacd166bfadce110a29eec440fa1`  
		Last Modified: Tue, 25 Feb 2025 11:06:02 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:47113ad3ae666c3a680ae930820f0cd15e2c3eb3047e8d42e28121ccf5ca916b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7192798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac76886ddb9a751586ffb878386ef14d3a4926b732edc1d2c3b75daa18338fc`

```dockerfile
```

-	Layers:
	-	`sha256:a0e5466b11a121ad477c3343b0eb62de91644be5c77746aec7e4e28ffdf3ee88`  
		Last Modified: Tue, 25 Feb 2025 11:06:03 GMT  
		Size: 7.2 MB (7176859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffa149ef8986fab5649b444788e07a0a6818169f11df5fd04449f7c1db3f4b74`  
		Last Modified: Tue, 25 Feb 2025 11:06:02 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
