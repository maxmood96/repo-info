## `clojure:temurin-21-trixie-slim`

```console
$ docker pull clojure@sha256:63ca37cd053767a3948be1f17efda8178feae034b9aa49e61a5a5fe7c6cabb1a
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

### `clojure:temurin-21-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:47d8cb942a199f15c019b891cee6872aa6f4ce6c68f39aad16106810fa3d6bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.1 MB (262054764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e354993699268469cd40ed1d208493bf5cfc693c49738028c011e36d04cc4c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ced038dea045df288fe9bdbe03117ca66fe2a071217e196ac86ed07f965fe688`  
		Last Modified: Tue, 03 Jun 2025 13:30:48 GMT  
		Size: 29.8 MB (29755384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a70a99e924b2fec02e6bfc5f50a3e99637c2e4b87a16e06ae4e3c9a3ac0e7e`  
		Last Modified: Mon, 09 Jun 2025 18:55:51 GMT  
		Size: 157.6 MB (157634498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3350620d10974556953ccf3c64843bd64d2e703b0078539ff8820d04abb6314c`  
		Last Modified: Mon, 09 Jun 2025 17:19:18 GMT  
		Size: 74.7 MB (74663841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7e38a876a1e7c83d72cbea27b41b0419fb9c1a77fc4ceefe2e470f97abac86`  
		Last Modified: Mon, 09 Jun 2025 17:19:08 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b4c10d01430c0552eebad3748c65331c3059921cab5de2c33c2f067bbd67a8`  
		Last Modified: Mon, 09 Jun 2025 17:19:07 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4288f512526a24e26c3fec99654ec8abab1ed545e6553775abaf59a05219a4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e3d096ffa7412fc7b704245c3857379a1dfed7bd3c6631d35b6d610e74e0c4`

```dockerfile
```

-	Layers:
	-	`sha256:45e9e6ddefd0ddb9208d48c524da1b57074ac49125cc92db02fc7a16622824c9`  
		Last Modified: Mon, 09 Jun 2025 18:40:16 GMT  
		Size: 5.3 MB (5256074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aff097d1966f6fe61eb77cd86b934649d970426e4eeea57eed9d02296781c1d4`  
		Last Modified: Mon, 09 Jun 2025 18:40:17 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6952a271664ab8f1211290d023467c5850150bc90e427bec12c3cea2c0c98683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (261016629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42561060a84ec991ca7b8aca70628f617ebc98f9162383783137db923b71c5ea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
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
	-	`sha256:146e6b6e5dbd4729806832b5086c3047d2d28c9f0dd88d4eae933846e9623243`  
		Last Modified: Mon, 09 Jun 2025 18:56:14 GMT  
		Size: 75.0 MB (74967318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3988f5ec252379bf8759ea2289d82107e481b6cc57b3e6dced1f0be41f3c7c`  
		Last Modified: Mon, 09 Jun 2025 17:57:17 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca32fa3546becf83f7e0d31f8a33ec53f0cd71097a801feb89cab25d6f83109`  
		Last Modified: Mon, 09 Jun 2025 17:57:17 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ba22ac0304e81904153d00e965b215bd3e3db87a3b8b3bfdf5b2f159c719a2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5278552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b2d343523c01b008914ec368e9f4fc7482947a24aa4f2aad0ceac60ad16d22`

```dockerfile
```

-	Layers:
	-	`sha256:0d73dfb6103deaeba89e15ca51d7d77a14a5182fba2b847406ff7092b089b03c`  
		Last Modified: Mon, 09 Jun 2025 18:40:22 GMT  
		Size: 5.3 MB (5261867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29b7c04927f4f11d777dc56c8fa588362a1e95668d0a7e45287f88ef82842344`  
		Last Modified: Mon, 09 Jun 2025 18:40:23 GMT  
		Size: 16.7 KB (16685 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; ppc64le

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

### `clojure:temurin-21-trixie-slim` - unknown; unknown

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

### `clojure:temurin-21-trixie-slim` - linux; riscv64

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

### `clojure:temurin-21-trixie-slim` - unknown; unknown

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

### `clojure:temurin-21-trixie-slim` - linux; s390x

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

### `clojure:temurin-21-trixie-slim` - unknown; unknown

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
