## `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim`

```console
$ docker pull clojure@sha256:0a548e7c3917cf8b6cc249e16dd343236ba73da0560fe2979ebc6416ce3bbd87
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

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3a6f853d4bccb86c9b4f5acabc4912ce039e42227041236e0c4e626a59c98d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246621103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959ee76237a71d0501f10517eb254a079a25d3ac3afccf0b1a542bc3c9758229`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:53:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:53:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:53:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:53:39 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:53:39 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:53:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:53:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:53:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:53:55 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:53:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41762d16e0636abc03eb1b187d80ada18581de13cb19ffbc7b50cc8a0631d83`  
		Last Modified: Mon, 08 Dec 2025 23:54:45 GMT  
		Size: 144.8 MB (144847951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283e9c610204b8d7eb222a122ce76b2522f5636740db49e4b73418d461d6702c`  
		Last Modified: Mon, 08 Dec 2025 23:54:32 GMT  
		Size: 72.0 MB (71995618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea201bbd950f7e5cb02cf6169321c788c6f6ee7b98a475ecfe4ba7ae6ccfc51`  
		Last Modified: Mon, 08 Dec 2025 23:54:22 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c349d5b23cfbb5a6fc1513480670fda3b13ecd624716d54afab6186a964674d9`  
		Last Modified: Mon, 08 Dec 2025 23:54:22 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:428c9ea93d02190c43d9806c020a0fea296ad9f843f0854765596b966a24f446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4fdb2334cce6ae70a41f1af985b995c580bcf8f6ba38618ea521ba5555de54`

```dockerfile
```

-	Layers:
	-	`sha256:c5acc078ba943943f39d5d1b5e5b4789229c3957c16b4c9582caa460781bb83e`  
		Last Modified: Tue, 09 Dec 2025 04:41:40 GMT  
		Size: 5.3 MB (5256199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c527ac043fa2d79503aceba39ddd8b1d714616b370f2342768722edd1822941e`  
		Last Modified: Tue, 09 Dec 2025 04:41:41 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7e55f179c53445fba379bb0b31fffb97da359d23766a7e2aba849ad2e2deb947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245628263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f56217b7e09ccc6bce31673dc1629fb398a10e98d8ca1336e4dafb1c63d9dd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:01:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:01:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:01:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:01:17 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 00:01:17 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:01:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 00:01:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 00:01:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:01:35 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:01:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cae8fe60f4430c9d322abf44551ff661105f999531466c85ff4254c85a89e9`  
		Last Modified: Tue, 09 Dec 2025 02:47:22 GMT  
		Size: 143.7 MB (143679920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee182ee46390aa48fd57b2ac3c6f05feb60e31d1b014e68440dd7eac90fe62e`  
		Last Modified: Tue, 09 Dec 2025 00:02:08 GMT  
		Size: 71.8 MB (71808674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7acdeca40b002bd69387cb0ed3e0c33228c1c354355dd5d8fb86507b056f8bb3`  
		Last Modified: Tue, 09 Dec 2025 00:02:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07c6c38da50fb8a6505ee3d3c92d395ca4968d8b9574e0e330f75138840e8ee`  
		Last Modified: Tue, 09 Dec 2025 00:02:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:17590c216bb61014c2b9f774651920f5ce8b046d31a6a931575bbfe28fb28dc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad202f65f7efbd780de7d50a2ab3da64b98473a7a59f6c06dac7a794761dcff`

```dockerfile
```

-	Layers:
	-	`sha256:fcf5721771ebe7d16309ec78dd2824d2319635c99b83e0f8624367666d32c896`  
		Last Modified: Tue, 09 Dec 2025 04:41:46 GMT  
		Size: 5.3 MB (5261968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29317fdef10efe50682b3132da564d5051352b89ae26d7932a4109f366c4221a`  
		Last Modified: Tue, 09 Dec 2025 04:41:47 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:335ed3a603c39409c2c1b67ceaf982851408ef6160ddbdf5104227f6fd6b4d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255514554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beda54841b8a682abe64536a0974785d4a4038237612a8fe7812138393cc7c68`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 03:51:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 03:51:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 03:51:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 03:51:36 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 03:51:37 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 03:52:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 03:52:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 03:52:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 03:52:53 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 03:52:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bf16378c0060db84f932d737d6c281316c915f7a3a4ce2efa43f2817d95192`  
		Last Modified: Tue, 09 Dec 2025 03:56:09 GMT  
		Size: 144.5 MB (144525257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66f157556b4c136ddf844c79d47c9a1f07270eef4474629f0c66e401be3c018`  
		Last Modified: Tue, 09 Dec 2025 03:53:46 GMT  
		Size: 77.4 MB (77391366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ef3c241b2a3135cde920df8d4d9a9005337f9b28dd4740dcd197301627167a`  
		Last Modified: Tue, 09 Dec 2025 03:53:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6163417277f001c20d6d558af4fc656ea22214d0882bacef41f0c21840df7b45`  
		Last Modified: Tue, 09 Dec 2025 03:53:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f2dd39b0db1b31d4a03cba76f21b41b487c47d8cde2660bf56760e0aa535caad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e2312e6b8a9f08922034c9558dd937456558f29f27d11a78131308c2d052ec`

```dockerfile
```

-	Layers:
	-	`sha256:4011b4ec58b0fa88eeee078dd4962bec33970ccbf96b2944cb0123402ca6c3c9`  
		Last Modified: Tue, 09 Dec 2025 04:41:52 GMT  
		Size: 5.3 MB (5260570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c659bf1cb1fe03480bd34ecba824e81882be143582c2977b2da43fe1293d5b18`  
		Last Modified: Tue, 09 Dec 2025 04:41:53 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:b7fcba47385387d2f5025ff51c69567048200b21752b07cb61600f11bfd779b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (241044426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8b9ee9db7c2d983773340998002aba044d39a901b71b844d94791f1fe8b38c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 17:58:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 20 Nov 2025 17:58:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 20 Nov 2025 17:58:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 17:58:06 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Thu, 20 Nov 2025 17:58:06 GMT
WORKDIR /tmp
# Thu, 20 Nov 2025 18:15:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 20 Nov 2025 18:15:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 20 Nov 2025 18:15:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 20 Nov 2025 18:15:33 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 20 Nov 2025 18:15:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d74684f217d805ec7013972d089a9baa3e158cc8603592f0e9ad77ff195488`  
		Last Modified: Mon, 24 Nov 2025 10:03:10 GMT  
		Size: 141.9 MB (141889576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1eea98d77616be41c09934cb46b70eba0ca9ab138e93b4ee6b79fa3e83b2662`  
		Last Modified: Thu, 20 Nov 2025 18:19:35 GMT  
		Size: 70.9 MB (70880679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c914af89d78b8885c7b112dde37fb3caf15da1ea18b890f10f7427d6d49220f`  
		Last Modified: Thu, 20 Nov 2025 18:19:27 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600638db24b8bbcdb7a9b56b79196800ce0dd63d4d39eb5d7af6728f79c8aed4`  
		Last Modified: Thu, 20 Nov 2025 18:19:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:090c80513ed6d785f23be04dd755b76efca95a75d03188a084e89a2235385ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e819d5cfed22a7b5148e52714b7521ec2b6c2c24f69fc8d1fbee67f9179416`

```dockerfile
```

-	Layers:
	-	`sha256:25a4538fe012ce286c44205ea66e598f405ab3c5ba93672f5d215bf19af20da6`  
		Last Modified: Thu, 20 Nov 2025 19:36:14 GMT  
		Size: 5.2 MB (5243744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83f0a97c28cdb53e71d158f3ef847b637125036ed5d3394e252cff9786be2328`  
		Last Modified: Thu, 20 Nov 2025 19:36:15 GMT  
		Size: 15.9 KB (15858 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:af1e1d6d029ef00627ce4a9fcd8b8b6ef48660651fe937812e37402291d8a970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.6 MB (237647907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4e969944510c41554ed370f9b1f447ee0b0714ce649aca02d8677357aa10ec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 01:28:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:28:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:28:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:28:50 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 01:28:50 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:30:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 01:30:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 01:30:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 01:30:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 01:30:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3260fdadccc7546154b4e7a7be47bf1049c46ad309ddf771b36f324535df05`  
		Last Modified: Tue, 09 Dec 2025 01:29:54 GMT  
		Size: 134.9 MB (134859033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7416e7adf22544d54ea85a65809f49aed6bb3b9007be95eaf9c82329273199`  
		Last Modified: Tue, 09 Dec 2025 01:30:51 GMT  
		Size: 73.0 MB (72953435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788d9de6ae62977ea4a8d246b74033ea5c22510367cff38891f1bf1eb4c7247b`  
		Last Modified: Tue, 09 Dec 2025 01:30:47 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324c20927fa2179a1c0d1bfcd7037cb7f22012365608f9c9b33cd391c3122e5b`  
		Last Modified: Tue, 09 Dec 2025 01:30:47 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:010e1a5c5ff031d093d184c07e1e234fc0973449d9eeaee66e1712c91fbd7923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5267935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf7b86c489fd0f5cde028dfce709a5d37bd7691983c6ff98c0a63f02942ef97`

```dockerfile
```

-	Layers:
	-	`sha256:18dee70fc869aa6054dc40cf2ad92d3ae75f1ee2c92c4cf8256c89f88f975e1a`  
		Last Modified: Tue, 09 Dec 2025 04:42:02 GMT  
		Size: 5.3 MB (5252123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74ac0360c173425c64ffe8f2550cc28c3cbe5b270ac754c19b819abcf6d8b1c9`  
		Last Modified: Tue, 09 Dec 2025 04:42:03 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
