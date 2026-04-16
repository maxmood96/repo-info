## `clojure:temurin-26-bullseye-slim`

```console
$ docker pull clojure@sha256:6967596f0924cc5ae19487b580b54df069e0f7d09f51414cf701cbfed71ebeac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2a22169c43bbb3d52281354a8b0e43b70d2aadfb0fefb5bf86c922d2733a83ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.9 MB (183905942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c95a5708d958e0693d30b952cae2a7a72299eddffdc643c1e0265c92d1711b18`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:08:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:08:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:08:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:08:06 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:08:06 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:08:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:08:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:08:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:08:20 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:08:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fdeb2304bfd7c482d3d846cc816963e6cd1d4d3c36a3154908b6a9683b1695`  
		Last Modified: Wed, 15 Apr 2026 22:08:42 GMT  
		Size: 94.5 MB (94455682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ac27580f5b4ca7b5ae556b4125c54e75281e3cdf2df65b5b221329721f65af`  
		Last Modified: Wed, 15 Apr 2026 22:08:41 GMT  
		Size: 59.2 MB (59191200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c566828e2a87aa64def0b0899bf5a7004afe1559a21329ad7c3fbbc0ea18e09b`  
		Last Modified: Wed, 15 Apr 2026 22:08:38 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891683173de1c6a2632b1afedf9d1a5b9dc8f228a907be6f6fe93d386dd5aa6a`  
		Last Modified: Wed, 15 Apr 2026 22:08:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:106bea69472833c2b88e2e7b18b65bc6a594ce14b6f2dec7918032aff6ee366a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5301386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9516d5e630bdf1d41e968e9c438cde17fe59de35e39df491736d407b93507c2c`

```dockerfile
```

-	Layers:
	-	`sha256:3996bcd7e7b7e41da9b4008d4c4c3039e98984c57f193cb11235b3f49d01479f`  
		Last Modified: Wed, 15 Apr 2026 22:08:38 GMT  
		Size: 5.3 MB (5285557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e375a4b4a6078c47c5ba333b54426d20600b8f91220b488849da7fb305bd40b7`  
		Last Modified: Wed, 15 Apr 2026 22:08:38 GMT  
		Size: 15.8 KB (15829 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:80e759140e61864245ac0b5fcb202a0d41708a0c1fca4c7ea795f21d4dca99f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181471067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb9099615d42466bbfe6edaf220793b7630d8bc7d1f219c9a5bbc12de87f9be2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:20:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:20:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:20:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:20:00 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:20:00 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:20:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:20:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:20:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:20:14 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:20:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab5c4274342ada0f896b55378d793f9bb07d0f83661f940fd8fd8c9256a11e6`  
		Last Modified: Wed, 15 Apr 2026 22:20:38 GMT  
		Size: 93.4 MB (93395199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7cbd28a0b7fe80cabeb7ec68c200078e5710fdd035a30c68f581097de7c7742`  
		Last Modified: Wed, 15 Apr 2026 22:20:37 GMT  
		Size: 59.3 MB (59330138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c3de9334bbbc3e7f61f90b1ecb9ae98dca49c3a5cfd982bb6bca842fd975a7`  
		Last Modified: Wed, 15 Apr 2026 22:20:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e39da838555b1087a9f9a613b12a9e60a7a874a227d332d7dc5961114dc09a`  
		Last Modified: Wed, 15 Apr 2026 22:20:34 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9a3364bd2f0c6026799a6b67caec313d03ac1abd4d356dfab0716b2b75b098fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5307233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffb9b255b7d19f32004d0f65b9c065a7dbc3788aea0bcb59e4b772786dbd5ac`

```dockerfile
```

-	Layers:
	-	`sha256:1915e81dd95d2bd31e4e04b3e704a9a4564d8c4cbc0f0cfdbe3d1a74d3fdbcae`  
		Last Modified: Wed, 15 Apr 2026 22:20:34 GMT  
		Size: 5.3 MB (5291286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62754a28bba4b068c9c28c55f3331d4d64a33a15399c32fcbbf72d4957eefc7`  
		Last Modified: Wed, 15 Apr 2026 22:20:34 GMT  
		Size: 15.9 KB (15947 bytes)  
		MIME: application/vnd.in-toto+json
