## `clojure:temurin-25-tools-deps-1.12.3.1577`

```console
$ docker pull clojure@sha256:a576d35b4ed8e808ce73b17d49d97a538938011344454c9bfa35f2fed27b5258
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

### `clojure:temurin-25-tools-deps-1.12.3.1577` - linux; amd64

```console
$ docker pull clojure@sha256:1f37c5cf3be3bee5f7354bca358199d4385cf5da952058f383527ec7debaa3d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221673710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86219877a50a3e539057c38b7e5503f11016fa3028dd0413c172b8695db551a3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:55:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:55:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:55:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:55:52 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:55:52 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:56:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:56:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:56:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:56:07 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:56:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75075c152363b67e1492c2f61722ac4557b2788c1e43cbb030c2e1bb1128fdc0`  
		Last Modified: Fri, 14 Nov 2025 00:56:45 GMT  
		Size: 92.0 MB (92045286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2297da66727b2e2738e8c91b258b1e15e809e67c080805448bb9e2ffba0fd430`  
		Last Modified: Fri, 14 Nov 2025 00:56:43 GMT  
		Size: 81.1 MB (81146326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6e6708f22f06b62b4f55a1817bc8960a5206908811daaa7f215bd2ebf50dcb`  
		Last Modified: Fri, 14 Nov 2025 00:56:34 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f847dd1c0e866ad967588d7977a27162bf7178d7f7c43a60de3cd83845e959`  
		Last Modified: Fri, 14 Nov 2025 00:56:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:c0d314d84d82700c8967ffad5dd5c6be69874f4eebfde17d82a6ca988e02c119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7345325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2268b49283180b685dfcdd12631e97813f3031ce1810472e3650d82f04edd495`

```dockerfile
```

-	Layers:
	-	`sha256:7ae30d0aee81f5633e66a007689754f38213f5395583d6f773b2198e5c9f41db`  
		Last Modified: Fri, 14 Nov 2025 01:46:04 GMT  
		Size: 7.3 MB (7327554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:591a6825bfc4bc4862655ae862f8da0b2f17f618ce409d4f321e6b31d8ca69c4`  
		Last Modified: Fri, 14 Nov 2025 01:46:05 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9ca2d48913e9d869831cdf1203d13dd9f2e6d396dd240b08e6df8fe168803c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.4 MB (220443763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5295ef08b330ecd4581c316d909408b66eefa29626ea720151a09e3c9f6845f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:58:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:58:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:58:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:58:00 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:58:00 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:58:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:58:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:58:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:58:16 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:58:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262cc0685394031f6ff3f3d0a86490a12fae03ec5c20c9024d342feed10288dd`  
		Last Modified: Fri, 14 Nov 2025 00:58:54 GMT  
		Size: 91.1 MB (91052512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c531d8d95ed523565f7c0a2f5e37d9aa8707fea3a171badabbcd626571f77191`  
		Last Modified: Fri, 14 Nov 2025 00:59:04 GMT  
		Size: 81.0 MB (81030730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea490f18cd2fbcb705e144b2976841d102fbbbbb89de8107a163f08892518d8`  
		Last Modified: Fri, 14 Nov 2025 00:58:49 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9bbb607d12678cc0defbd4fc8da77c8206fbeae12cf0e0605acc649707fc21`  
		Last Modified: Fri, 14 Nov 2025 00:58:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:b13bda05ca57727683591cf84f116750aaa8ceff1d0969457ece61880f3a7b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7351346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f4b04a4d900eddb611856b435b45844aac464a2763123d7322f829de223c20`

```dockerfile
```

-	Layers:
	-	`sha256:b24d6656c88d04b227d0b35ec6c9af8fe2d1a438bbe9ea0243905748c1070fa7`  
		Last Modified: Fri, 14 Nov 2025 01:46:11 GMT  
		Size: 7.3 MB (7333386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95959d22828e5891ff227b553ee0fd9a490d798dbf9b7530ed5569bd8b765087`  
		Last Modified: Fri, 14 Nov 2025 01:46:12 GMT  
		Size: 18.0 KB (17960 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577` - linux; ppc64le

```console
$ docker pull clojure@sha256:665cfed5777ea8f1e91f560841ce68e07a5b9ac4a955bef0ca27dbf11efb0d26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230925315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522ee91bc582a53f67720437e41163990e18e780b2bfe83688733fecd03f2cba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 21:11:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:11:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:11:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:11:15 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 21:11:15 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:52:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 21:52:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 21:52:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:52:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:52:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7b1be4bd5c392224945402db7277dc7a8f213a2d808e9ddd6b01efa46c2c1a`  
		Last Modified: Sat, 08 Nov 2025 21:13:29 GMT  
		Size: 91.6 MB (91610767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b53a303bb7098911cb11710ff348d8d274a962cccd6b3924c7106620c26d78`  
		Last Modified: Sat, 08 Nov 2025 21:53:49 GMT  
		Size: 87.0 MB (86986225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d49d985ca40af348c438f4bd81b4c22546685334744930197628fdb7b9ec6b`  
		Last Modified: Sat, 08 Nov 2025 21:53:42 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5751be8eebbe96676ff64d7822036001f885c481f44b2d45f102d91f7175a05b`  
		Last Modified: Sat, 08 Nov 2025 21:53:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:b5a80d6808808b59a8d155e08a340be7744655896f3828c9d21f40df90aaa0e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7351957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0fb4fe3de00dca15a0668c33f280552fbbbda01e39dfc6971a0be39231ddbd`

```dockerfile
```

-	Layers:
	-	`sha256:0c6f481b7a155679f7789f7a5bbd4548e415b0331ead8376eb39a4e890f9925a`  
		Last Modified: Sat, 08 Nov 2025 22:51:10 GMT  
		Size: 7.3 MB (7334102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed1e65f223090b13103401c4c239a270b6c77dbbdcb33137d5e74570eb63e1e2`  
		Last Modified: Sat, 08 Nov 2025 22:51:11 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577` - linux; s390x

```console
$ docker pull clojure@sha256:7d747359efc78a45084fa5f298be7bb06d672227485fc4d2ce3468bfa9d198b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215307019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9564d292282299c1bdb3a484aff612644bc168b86075abaa85517cfb9f8e91fa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 01:03:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:03:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 01:03:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:03:59 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 01:03:59 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 01:04:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 01:04:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 01:04:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 01:04:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 01:04:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b31a2913f32def8de76f5434fa7856bb6c0db043a452a8fbc5f0adce6cec920`  
		Last Modified: Fri, 14 Nov 2025 01:05:01 GMT  
		Size: 88.2 MB (88210702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb64c7248a92b7ca05e06d05a493511e50bf685a1f465b50b7c62257c2d2a0a2`  
		Last Modified: Fri, 14 Nov 2025 01:04:59 GMT  
		Size: 80.0 MB (79957175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0955564189faf595b095a0c77f3bba49b5599b00fd6da2e7a2d17d5e12dbd8b2`  
		Last Modified: Fri, 14 Nov 2025 01:04:45 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a93d8fe4555ff580116a4314daf1461bf36fd2bfd37ce643e098e4dd59af420`  
		Last Modified: Fri, 14 Nov 2025 01:04:45 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577` - unknown; unknown

```console
$ docker pull clojure@sha256:5c46eb97042c01c115ced9128419af9d70d4a6103f5570b59cbab1d74d80c0e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7339192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d51fcd097cae857b406700011143eef128b8438a68c4153b08118cf63e5d51e`

```dockerfile
```

-	Layers:
	-	`sha256:c6ca8ec649f023770cc74a830a50ec1be9b942c0a1a652759a9b7863761a334b`  
		Last Modified: Fri, 14 Nov 2025 01:46:23 GMT  
		Size: 7.3 MB (7321421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7128328c692496c744de2276854737a5c8f5d2572875823a7a7d21aebe72df9`  
		Last Modified: Fri, 14 Nov 2025 01:46:24 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json
