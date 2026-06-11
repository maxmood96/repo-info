## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:1fdc0313e80a2ed6e0af45a450823f729c954649e2469910dbeecda8ceea022d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a84bf17764c349af08b9864c55c380574500da30f53fced5cde22da4c93a27cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232267050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc3d5081a4045a8122513718d27d63f0290ca1cd94a0bafeaf222e62df6583c9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:18:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:18:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:18:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:18:52 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:18:52 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:19:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:19:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:19:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:19:04 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:19:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da84f642af1d50a798cd9795b30ffbe13b00dcbc48118571eed114ed5d6f54c2`  
		Last Modified: Thu, 11 Jun 2026 01:19:25 GMT  
		Size: 145.9 MB (145905445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0413456f8a600a3ffff3ea3910dbc8c5912d98a0be606b33f631111afc5851`  
		Last Modified: Thu, 11 Jun 2026 01:19:23 GMT  
		Size: 56.1 MB (56100309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f486ca9c14442360dd85890cb3b55ead8d209c117325eeb0f5e2705b373743`  
		Last Modified: Thu, 11 Jun 2026 01:19:20 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04801fa2f42813f76d00b241de3f8ea63181f3aa255ba8b152adc929dc864aa`  
		Last Modified: Thu, 11 Jun 2026 01:19:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f2138b6ad5d9dcb6ccd6bde5a9b125af41aeb62b04d528df07b7a448adf0f3d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5333838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cecb09a33357abdbf8ef7f99c165ea9078fa37bd478b055d4f55497190ef255a`

```dockerfile
```

-	Layers:
	-	`sha256:d92ee91b6242f2b2516d3b657a8f7c9e64e8d5de7591e5c3098d7dcbec479be3`  
		Last Modified: Thu, 11 Jun 2026 01:19:20 GMT  
		Size: 5.3 MB (5317849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:732f2c5f23a594953a9bc6a181d050b5f46d4724b67c4379d22ed16ab3ca3390`  
		Last Modified: Thu, 11 Jun 2026 01:19:20 GMT  
		Size: 16.0 KB (15989 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6926ac1f32d5589b484ac3c52b003abc2b4ca41052f21f52d33091b5a3c3765d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229739156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa3bdbfd4350f251cabc69055ceb1dcf69edbe75df89d99071adc4ccb7266d0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:23:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:23:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:23:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:23:14 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:23:14 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:23:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:23:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:23:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:23:27 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:23:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d57c5561232539b2b4a8690391be8904a6e09d58f8df87e3eda2551e0145a2`  
		Last Modified: Thu, 11 Jun 2026 01:23:50 GMT  
		Size: 144.7 MB (144724336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ad7644fb6b2d4d1a6ddde8b98a3a6c005ad95c63f32677b3fbdff8a0f43de7`  
		Last Modified: Thu, 11 Jun 2026 01:23:48 GMT  
		Size: 56.3 MB (56267625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ba0245a13dd259548fb0c40cda8b3b01d3e400b3873bc20aad75f833e20b98`  
		Last Modified: Thu, 11 Jun 2026 01:23:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c635c4e802ffd4d7f0e6dd661e88ecb1f1ab0c091e9a56041516c6270ab7d151`  
		Last Modified: Thu, 11 Jun 2026 01:23:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c046c54c4ebeb6e407316793dcdac3de96d1651558a2acee0985a4a6c5526a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5339688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26287d2385aca94d318aed94ac428dfe2edf30ac670745fe7d08609edfbc3e2d`

```dockerfile
```

-	Layers:
	-	`sha256:cdf40a4e5ddbcb4d428a238e987b093dd997f1d3fccf8c8b53993212b6208618`  
		Last Modified: Thu, 11 Jun 2026 01:23:46 GMT  
		Size: 5.3 MB (5323581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82790a78bc8b0f57837ef69c289999882b4e3949922daee5f9e27692e87220e4`  
		Last Modified: Thu, 11 Jun 2026 01:23:45 GMT  
		Size: 16.1 KB (16107 bytes)  
		MIME: application/vnd.in-toto+json
