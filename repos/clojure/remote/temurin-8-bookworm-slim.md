## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:9e858e56ee25f416e6fbbec2960245b15b9886361a1cc330b701b22fc53eeb17
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e399c821c1d5ce20e45f3b368003f7df165d0bdbe17c890841ddba596f78916a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152629998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f50bd8c1aee0c8f375e7d7f780e8a98f0e7289c36967041a07747d41993a9e2a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296af1712f9a90d92c2c615d393b8efff75a977df78c6d607bf884ce68fd76aa`  
		Last Modified: Mon, 08 Sep 2025 21:41:49 GMT  
		Size: 54.7 MB (54731283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f77eeb65eadc3cc7a8c8e6f0128bd1bf71416040558e1e4a4afd2984c3a3ff`  
		Last Modified: Mon, 08 Sep 2025 21:41:49 GMT  
		Size: 69.7 MB (69669724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a58149d1042d0789bb38912d5d5ecb16ebcd7988a610095e0cd6da077f468c0`  
		Last Modified: Mon, 08 Sep 2025 23:03:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fa857dacd66b8d93388ed79a94fe9e0746e67c832ba1f02a1c2299be09a8286e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac63faf3674dc021f6a529d7772b317b8c3a65d6cd510099e0d05103f408e26`

```dockerfile
```

-	Layers:
	-	`sha256:63027a93500e70add40c9c12ba5358854466f4cc54aebf6372049165c07269bc`  
		Last Modified: Tue, 09 Sep 2025 00:45:33 GMT  
		Size: 5.2 MB (5234998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5acf7b3f591d6950ea95fc2d2e3661fc89dd95ec796e86eca72e1120cbd95b5`  
		Last Modified: Tue, 09 Sep 2025 00:45:34 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:72ca5be489764c7a7286936a120721b7089cf961d3c0362211482063a25d3e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151497476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c408952a1364a6a00273c4d5b84220e133e3fe9facb82915cb7d413e527cf091`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65336dd5f6e45f82a2b0174215ee2ba29b496af36c69df875d049e24078afc7e`  
		Last Modified: Tue, 09 Sep 2025 00:34:42 GMT  
		Size: 53.8 MB (53835606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b4c701df29e55551edcf923780a99a613d9b566bd429cace992faa1e8a6cb0`  
		Last Modified: Tue, 09 Sep 2025 00:34:42 GMT  
		Size: 69.6 MB (69559124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7162c71f7d5aad79c1ad2226d22b2baa12ae6ad43a1b8fd88199a103a680e1ae`  
		Last Modified: Tue, 09 Sep 2025 01:12:45 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8a8e671a99ddd08ceba7c56146d22f35bf6de4dcbaf18c8393cbc797aa972174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e1b3623027ba573e277d9802da9397a54f1b26219e29b32495f558764116d8`

```dockerfile
```

-	Layers:
	-	`sha256:f48de715f04810acd26b95bdc54e787bb3e12b0091a1ba942c9fdf13c8ccf0a2`  
		Last Modified: Tue, 09 Sep 2025 03:43:37 GMT  
		Size: 5.2 MB (5241457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ce5e0e28210ecf35f0b1588a09a401cc21d44199c290b01adb4a60b571d078f`  
		Last Modified: Tue, 09 Sep 2025 03:43:38 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d138bfc5b2a74eaf56f9181ab841713b07b20577efe4d3d9a288b97fbae0947d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159743420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bee5c8ddb352bf49598aceac2d3d09c398761ef755963da19863c9d9fdc03c0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970d5ed7e7cca3514b30899e1c6f9a7db1fea89aa6aaacfd6066cb2d0b3fa613`  
		Last Modified: Tue, 02 Sep 2025 07:52:08 GMT  
		Size: 52.2 MB (52165399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632796a6ee3a0bf26faaa49916e010f9979543cc4af1e8db59c098acbac6c228`  
		Last Modified: Tue, 02 Sep 2025 08:02:10 GMT  
		Size: 75.5 MB (75503957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41e77d968c04a18609cd2be4308a2f9e36faeda6caec494da945ea3d8bcf3a1`  
		Last Modified: Tue, 02 Sep 2025 08:01:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:94cf53785b6c683cf8f9c5bafd796d2526973e72cfa58c7f5672bbf12583fca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee9efd48e06efcc3cecc0d0ba90d3c71723d3be64a36ec9e0e0cfa849c7c5af`

```dockerfile
```

-	Layers:
	-	`sha256:b07292343f6ffe4d7a0c7d0dca47e0f3f5d89ac3d8379f7475b4d5f863457219`  
		Last Modified: Tue, 02 Sep 2025 09:44:28 GMT  
		Size: 5.2 MB (5238634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ebc2936db5dcd63dcf91c86c62c953a94adf9d25bd403d209a75e2a97f373f1`  
		Last Modified: Tue, 02 Sep 2025 09:44:29 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json
