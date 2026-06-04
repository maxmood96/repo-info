## `clojure:temurin-26-bullseye`

```console
$ docker pull clojure@sha256:9ca1b4a4df0c920b7d74dace7b0c3d4324f654e83ce00111bc3ea84497bacac4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:3f557f5cc13a116c1443cf600294abea5a6c94dd23e1545767f2cb43ce0c9204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214806360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbd466e3f6c3bcc7adbe9c8a6cc2f7ca140e75a2cee13cd9f244cf5683f46f0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Thu, 04 Jun 2026 17:47:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:47:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:47:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:47:47 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:47:47 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:48:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:48:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:48:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:48:02 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:48:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d0d98eecfa3b5c942eada879fdb4cf6f79f0b9612ede79322d9d16fc3e984ee0`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 53.8 MB (53768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e8f62402a0a429c11eac10f014de0e6bdd971f9659df473c018b3d2ae8ede8`  
		Last Modified: Thu, 04 Jun 2026 17:48:24 GMT  
		Size: 94.5 MB (94524311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0bbb51493c56dafae190dc5c96f5f79b56b8581c17051da87adbac99a999de`  
		Last Modified: Thu, 04 Jun 2026 17:48:26 GMT  
		Size: 66.5 MB (66512153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d680fe26b7fd4c52d9687fe3fe8982bd1258d5b29aed17eb05cc34aa8b9cf8cb`  
		Last Modified: Thu, 04 Jun 2026 17:48:21 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1989b92bcfd94beddb87a6f68914ee51b5884ad81052df1791b5f526cb4de0c`  
		Last Modified: Thu, 04 Jun 2026 17:48:21 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:16ca3df815d0fa0ba91aece8d8dd3d039fb719cf3fb9b17d55998933fc959eb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7386261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1b1b763f95bdde5b156d712c2e00d33ddab6cbf573bc08634b4938dc3869efb`

```dockerfile
```

-	Layers:
	-	`sha256:eaf403b6a6bd80922516ef155b8c03cf17b1118ec6035390845c570e1b51918c`  
		Last Modified: Thu, 04 Jun 2026 17:48:22 GMT  
		Size: 7.4 MB (7370336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d99dc3bd089898102f6caff5a3775141052fcd2e59dfc0e45583805a63393611`  
		Last Modified: Thu, 04 Jun 2026 17:48:21 GMT  
		Size: 15.9 KB (15925 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:72e5b52bc7a9be27f88ba58b177c2fe84472cfb988af12aede13a011cf67b0ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212439670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eaf61ca3854a00455bbff2f2a04ef962d4e90f744ed319a80ff2627c67661e2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Thu, 04 Jun 2026 17:47:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:47:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:47:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:47:42 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:47:42 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:47:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:47:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:47:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:47:56 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:47:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9f08527663b6ddbac974253d3632db7fd8c400d9acb6601fc251de137ec53a8e`  
		Last Modified: Tue, 19 May 2026 22:36:30 GMT  
		Size: 52.3 MB (52256578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7a3f92d6b80f8e45e14858955fcdad80dce52d01d1e24c3a1d1da94123bd67`  
		Last Modified: Thu, 04 Jun 2026 17:48:18 GMT  
		Size: 93.5 MB (93504334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4af5a937d61cf73cc3f24a03f0486ac11b76882a8f2901f5401b24146994b5`  
		Last Modified: Thu, 04 Jun 2026 17:48:18 GMT  
		Size: 66.7 MB (66677714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b865b1468e731948a922f2f372cbea65026f8a540aa01f55fff324e18397a07`  
		Last Modified: Thu, 04 Jun 2026 17:48:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac714e0ae90b2199b4643617b3c79fe927c825d7e5254ab9cfc60882ae0abf4a`  
		Last Modified: Thu, 04 Jun 2026 17:48:15 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2ffa3dbfc3263f154f600a032d4b51b36451969ca74d9c525ef0f1836e23d26f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7391475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1078f49bc3705163ebfc4c9521d2e940effdde6a52c9f86b8088ccd00eb22d4`

```dockerfile
```

-	Layers:
	-	`sha256:dd1e7c50d6310d015caecc228bbcd6bddb35568583b5dd9a2d68c0aa948f9aa8`  
		Last Modified: Thu, 04 Jun 2026 17:48:15 GMT  
		Size: 7.4 MB (7375432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e688b39e9f17c2d7140649fc14d99ae0b3074fb25e6a7454a655fd729272cb6`  
		Last Modified: Thu, 04 Jun 2026 17:48:15 GMT  
		Size: 16.0 KB (16043 bytes)  
		MIME: application/vnd.in-toto+json
