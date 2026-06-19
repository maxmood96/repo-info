## `clojure:temurin-17-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:2a76d78b434073162e740a4e776c1598753f3d4c7e4f2d7caccb94edd556a3dc
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

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7bceba840d86b6ee4ce87b161e3c0df249ec60b3eec4a942632ed8dd016361cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244643742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7816b67dfbe1cbec4bb1b66e17d092eeef458c534e3ccb8790c674ce16fe7450`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:18:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:18:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:18:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:18:06 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:18:06 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:18:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:18:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:18:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:18:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:18:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4cf7d12e7aae66e711a93ac6f87123ecd3e41ede34fb10e71f75cd0febe37e`  
		Last Modified: Fri, 19 Jun 2026 02:18:40 GMT  
		Size: 145.9 MB (145905426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71007ebbddf33f16b831d13c59650240f7e9c1af17328739b69ff34cc93eda9`  
		Last Modified: Fri, 19 Jun 2026 02:18:40 GMT  
		Size: 69.0 MB (68951864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f9ffb5c3e9382a3f4c3bf833d046bc9846feaf8f90343235942d8202fa990a`  
		Last Modified: Fri, 19 Jun 2026 02:18:36 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c21658cd851c490703a1662077febdf369ce9c0e7ae03529b5b0912cdfb984`  
		Last Modified: Fri, 19 Jun 2026 02:18:36 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3be5817d32ac84c97895528f396a4951c50d6c4a7a56116cec0aab2ef689c68c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25f12f1c785d937b1c8a87e136ce0be1d3f38be7d2893b36ae24b7ebeea79f6`

```dockerfile
```

-	Layers:
	-	`sha256:cafb9e7186381356bc803f227b1f866b2128dc67ff6de7a5e6df0f0dfd536c8c`  
		Last Modified: Fri, 19 Jun 2026 02:18:36 GMT  
		Size: 5.3 MB (5257242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91c0f34caf92c10347904f3ad76fb99f1621b906f0883ee7f18aa6fc57fe075c`  
		Last Modified: Fri, 19 Jun 2026 02:18:36 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ae58e2fc88f85e67e5c688570aa67d5298eea9a1ab9e9287c5b21a1b342d4656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243651292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43da7f7b990bf6175f1f6732e6e3526d3f233d736e47d7ed3b889bbfae5b46a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:18:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:18:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:18:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:18:17 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:18:17 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:18:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:18:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:18:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:18:35 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:18:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb54c68e874523fd9ef300ac16a253cdf1f787f1455bfefcf27f1cfbdd9a895b`  
		Last Modified: Fri, 19 Jun 2026 02:18:58 GMT  
		Size: 144.7 MB (144724303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e49253849242a5cd4874283fa04a468aec299733e73a8c669e452c09b4ff6d`  
		Last Modified: Fri, 19 Jun 2026 02:18:56 GMT  
		Size: 68.8 MB (68777420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a94a21f1e661130a506ae9a986e4bd2eac1af1b0a172bf0463d195f9beaefa`  
		Last Modified: Fri, 19 Jun 2026 02:18:53 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb08c37cb3f30be26ab98d8b6524827e009bdd2f7f0decf5db6c0f2fa38922c`  
		Last Modified: Fri, 19 Jun 2026 02:18:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fa0f7f6109a4f2896d0d094a9f32b5499ebdc0e9cff620ff59f0a26d8b3cdd35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729e336480e941d7fc66a83577a651a56cb683b84d14b2ed7befe3da24e47462`

```dockerfile
```

-	Layers:
	-	`sha256:79d7eede7060addea33e563828128b66a24569def4b54ffde1757a42d07d382c`  
		Last Modified: Fri, 19 Jun 2026 02:18:53 GMT  
		Size: 5.3 MB (5263003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:930548811270adaac7a87fbf599b1733d8c1144574cb34d85112b22ebed38cbe`  
		Last Modified: Fri, 19 Jun 2026 02:18:53 GMT  
		Size: 16.1 KB (16084 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:102d2910f7f2d58e29353283e2243a952c877e92dfd51b468bd270442d953936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253742819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5854224957b51cad7625c025ee8929fc828b7b71cdfcdda1bef84d459c74afc3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:40:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:40:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:40:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:40:59 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:40:59 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:47:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:47:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:47:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:47:55 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:47:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c12061528e7da232c3a05c00802e8fb865782cca2399322852ad4b4c6566c13`  
		Last Modified: Fri, 19 Jun 2026 02:44:54 GMT  
		Size: 145.8 MB (145766192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f41d7200086d79ffc5d53147e5067e72f556db3cc37776a657ce4650915fd7`  
		Last Modified: Fri, 19 Jun 2026 02:48:36 GMT  
		Size: 74.4 MB (74369244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c6996b2f1a4c7cf7c206b6bf835e49a7566a1fb24ec9270476f75a6d78aa64`  
		Last Modified: Fri, 19 Jun 2026 02:48:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224ef0475f26ff21c6084392e5d865636c3af1b26ffb5f4734d93ec7b64dcaf9`  
		Last Modified: Fri, 19 Jun 2026 02:48:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d4b425df88f7ade5b17f17ededed00698d2154d7ecac95eb47bdc3c62ed25be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7db6066c6904f4ead1f06bc567074ebb2faf7e8c9f234c045188fb8c3db64d3`

```dockerfile
```

-	Layers:
	-	`sha256:bf51882d0da10e948527eebcc6d6e83a06bb7c1563bc89ccd1f9bfadae654ba0`  
		Last Modified: Fri, 19 Jun 2026 02:48:33 GMT  
		Size: 5.3 MB (5261613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9525766feb3d13176353a3f5d530c5f445ad02bacf465ec202b88cb8bfa4eb83`  
		Last Modified: Fri, 19 Jun 2026 02:48:33 GMT  
		Size: 16.0 KB (16014 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:f522a862f3fed0faf3c61dc0f8c80d075238bca0339f4f9af67de6217c084d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235694624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4fab23e8719ab3e31cb58659fb1c6ca66c6d162e179a4673b4f62205de100da`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:17:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:17:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:17:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:17:15 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:17:15 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:19:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:19:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:19:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:19:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:19:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd16adea10fbf1d54ca2e5edb1f4b081332ccd028cf6b0964ac17b7ace1cf74`  
		Last Modified: Fri, 19 Jun 2026 02:18:57 GMT  
		Size: 135.9 MB (135910426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c83e4129a24958a7e117bc489e1660c125ee9ac508ba45ff3df2c1dc59eb412`  
		Last Modified: Fri, 19 Jun 2026 02:19:50 GMT  
		Size: 69.9 MB (69931805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103f731d874cf0dfece90cb363d7fb093af871a5b87a2f2ddd3657edf3e97b63`  
		Last Modified: Fri, 19 Jun 2026 02:19:48 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133ef3c43774860444e2150b54f225680e32c4e5e6cbe16841801cc4decd7c70`  
		Last Modified: Fri, 19 Jun 2026 02:19:48 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fa42361061cf6340aa7990c505589794b43979cbc99dfa3500da898f9f1a4968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5269131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5f0f7d76c3cbcb53539930d4a5bdad6937cfee644c92f2b7eea66b0599b347`

```dockerfile
```

-	Layers:
	-	`sha256:c270b5694dcf75a59e1dea070d52962a68c78862c9697d68a1ca7adf26fe5f96`  
		Last Modified: Fri, 19 Jun 2026 02:19:49 GMT  
		Size: 5.3 MB (5253166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:848b06e238c96eb0abaa5a42d15dc769c7b6a17de55fa5f27cd32a5050d9d52d`  
		Last Modified: Fri, 19 Jun 2026 02:19:49 GMT  
		Size: 16.0 KB (15965 bytes)  
		MIME: application/vnd.in-toto+json
