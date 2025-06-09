## `clojure:tools-deps-1.12.1.1550-trixie-slim`

```console
$ docker pull clojure@sha256:f7772711f2d252f95a4be34823f4a02f730c5ffe4ac7e0f88fd022cfa2db252a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.1.1550-trixie-slim` - linux; amd64

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

### `clojure:tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

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

### `clojure:tools-deps-1.12.1.1550-trixie-slim` - linux; arm64 variant v8

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

### `clojure:tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

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
