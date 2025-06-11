## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:790babe6017733f4b9ac3f1a4e7adc5687fe8bf29afc6deb2160cd1e174c4c75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:be758bdff6626643a338ed29d743136a8b392e53d43770828cc7c63ce7f6168f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242395450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525e420a3ff84a918e34437c90385f1d87725479e7dd83293e32dae9f0530089`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1815a20fd7a32d4bbf42a0603242e9fa4e6ada340432d1812eae3181d47643a8`  
		Last Modified: Wed, 11 Jun 2025 04:06:11 GMT  
		Size: 144.6 MB (144635025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511007650e487ec14f8bdeebbe786b6787a122ae0a112b4f2f6b34aa19510811`  
		Last Modified: Tue, 10 Jun 2025 23:52:22 GMT  
		Size: 69.5 MB (69529255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65fec1f2679c70056dcd834e5953073fa6d3c7043032b1e904971149ff116569`  
		Last Modified: Tue, 10 Jun 2025 23:52:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ef319ede9d80100837e43569767ca3b2a4e84fab0d52f3208e8e180b803467`  
		Last Modified: Tue, 10 Jun 2025 23:52:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c046e4c6bf5ac54b8b18595b13d3014e0d975bf8b423232eb09f8b29dd05a196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7217062b4eeb1c7c370fd256686c85208b8f24d36add7b70d463499baa62d4`

```dockerfile
```

-	Layers:
	-	`sha256:7e2f9aac05ccc73ec4194a4d7d8f537f9157870440020c3a8d1a705995fcafb7`  
		Last Modified: Wed, 11 Jun 2025 03:36:39 GMT  
		Size: 5.1 MB (5109888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c148e73863bd1c534926eb7cba13899238502b52b7ceef7ae4ea21bb116a69aa`  
		Last Modified: Wed, 11 Jun 2025 03:36:40 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3685334ae81edba74f08e6878605dcb5dd452298d7b56c70eca9632fa99078e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240982191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27045a012d1920f9fd323dc683a097e5583a0e7092ece0dcc37550951a00755`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d445f89a86a5a0de06289041c3386131f0f843fb9af5e73aae74d3971e03f1`  
		Last Modified: Wed, 11 Jun 2025 08:24:53 GMT  
		Size: 143.5 MB (143512629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7372b8451ed56fe82ad07c018cfaf78c7e4992e922ca07e3d16214f475781ef7`  
		Last Modified: Wed, 11 Jun 2025 08:29:52 GMT  
		Size: 69.4 MB (69390848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682c404a7a8318528106cfd5295a2a2a8cf0a9393d9640733dfa7f4fd63f0667`  
		Last Modified: Wed, 11 Jun 2025 08:29:49 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed3f95111b2a31eadbe7b7afc288ed5fd926a5cccf7c366b82c26538eabec7b`  
		Last Modified: Wed, 11 Jun 2025 08:29:49 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a20736466d332fed69c65637b2c8ba1a6902809f9ca7803b558b957e39a09d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5131646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e2ca100c5f3b7165517a07128cb1bc87a743c25c88ac3815c953c62bf8f485`

```dockerfile
```

-	Layers:
	-	`sha256:fbc84032ae2d54d6b00b998369b24fc7c8c41fb77cd2ec8d426f9b05ea781a19`  
		Last Modified: Wed, 11 Jun 2025 09:37:22 GMT  
		Size: 5.1 MB (5115649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b3b77cdd37f2bf16be1d296535fd2b34cdf865bb4b0922c9268ca08e4c5f966`  
		Last Modified: Wed, 11 Jun 2025 09:37:23 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ffdde185e98467006c8ae86d720a0f7d71499443e68dda81dd82b2fa0aea1527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.7 MB (251700157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00bff7736c7b003264c18ab33eae68ac5c80ec53f40ddcc2fbe0be08ae7901c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63828befd7f3ce93f31d4515e872628bcdb7682c4c04580b3fb66dad86181318`  
		Last Modified: Wed, 11 Jun 2025 08:27:38 GMT  
		Size: 144.3 MB (144280582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ceaf64ce3d26d64165f99e03c9586c932158bcb52e705c9c25775354e2d2d2e`  
		Last Modified: Wed, 11 Jun 2025 08:34:52 GMT  
		Size: 75.3 MB (75345737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff131212dd984cda5168ee36fcc6c8751f2e17517fe6e8e1997a00cbc23a670`  
		Last Modified: Wed, 11 Jun 2025 08:34:41 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c34068b258466f0119f06c727905a4f8e97f64a95a819fded1ef0b283cc4fad`  
		Last Modified: Wed, 11 Jun 2025 08:34:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8562c9f0d234513371db56792ad64eb705a8bed96fb7545efbb85507df609ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5130973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f8389332b787be2e4e37b0b0b2ee59b2b74c8f8c0f5785647f3adb0f077fbe7`

```dockerfile
```

-	Layers:
	-	`sha256:c0853a1ccef407cdc71957688ca9548c0511f16e0cf9c33a2f0eff3ed81fa23c`  
		Last Modified: Wed, 11 Jun 2025 09:37:28 GMT  
		Size: 5.1 MB (5115046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57aafc3d3ffc1485a6e97b019538a222cb921221a64df246361b95c24484ab25`  
		Last Modified: Wed, 11 Jun 2025 09:37:28 GMT  
		Size: 15.9 KB (15927 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:ddf463af919dafba1a8f6f59874ea7d2388186026c9122f92f7f524e3492a254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229896396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:648be7efb933af1212ecaed8c6f257225b324d16a8de9d1afba018a606898c29`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c887542c65d63d98138af1a0d5048d07e8a05ae9b69b4e160bd8ff254de67cb5`  
		Last Modified: Wed, 11 Jun 2025 05:42:41 GMT  
		Size: 134.7 MB (134673544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb0c318a40a392d48c8c716a046235fbf506a5b44a1fb775fe8ed14116c7c2b`  
		Last Modified: Wed, 11 Jun 2025 05:46:55 GMT  
		Size: 68.3 MB (68333960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e935413ca633dba54d4970b8bc2ba56a7b7850226bc972dc6ede4d8af85f6cc`  
		Last Modified: Wed, 11 Jun 2025 05:54:20 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4e04c1f4c84ec7f62705cab90de01ec2d3968a424f3c2909a2ed7993c120db`  
		Last Modified: Wed, 11 Jun 2025 05:54:24 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b6cfb2c5dea481e161f70b8471171c1485097917a0edb4b92dad01788f3a241a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5117088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246ab87733e4b21a7aabec3ea27ca9ff416e2f4d52cbbc8f73dd749f70ca8ecd`

```dockerfile
```

-	Layers:
	-	`sha256:6ce0705545b15120e4cd740ce19d01d2b23d95ffbcad03dd8f8e2186070a50d2`  
		Last Modified: Wed, 11 Jun 2025 06:36:22 GMT  
		Size: 5.1 MB (5101209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f652decfc0f0a8f13770840295d447c43202b76e62bd3df430dedde8d63f4ac`  
		Last Modified: Wed, 11 Jun 2025 06:36:23 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json
