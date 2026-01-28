## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:042ad522764d6ed095796ee778793509dd6c3900010b9d952d1d2e898f3a49b2
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

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:f1e3b2b570515d58ec72a8820c4eb60e2bcd64952fab3f785cad0f08286b2412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274599210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a13d5bbb0e50f80da059f58457a402d73efcd21046dbb1be707d60c11dc9a7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:02:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:02:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:02:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:02:37 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:02:37 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:02:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:02:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:02:51 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a477e2f25889a0f4bd4a8b949131243ae2d158b466da5c7ef8e02ac3bf5c7a`  
		Last Modified: Wed, 28 Jan 2026 18:03:14 GMT  
		Size: 145.0 MB (144966652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e9f328acee6cf60d9c0e10699cde68901b3b59a69a3f5ba237d0230c641b82`  
		Last Modified: Wed, 28 Jan 2026 18:03:13 GMT  
		Size: 81.2 MB (81150292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8edc553b341d74cf05408c883c3832dfb0a370fc80c9c8f2388f2cd0680c48`  
		Last Modified: Wed, 28 Jan 2026 18:03:09 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:535a8db2cf366f55a7f0fc4ca36cc8769dd2f95748f49eb03af3a9b30fc6ca7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7409885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:333ba2c76862e9181d67a8549b11420252c14013f989daa24db22d8e2b8f4d57`

```dockerfile
```

-	Layers:
	-	`sha256:9eff5a5ae85b25147056cd3c5a0950201b747ce96ea9920ed1b0163df155a777`  
		Last Modified: Wed, 28 Jan 2026 18:03:09 GMT  
		Size: 7.4 MB (7395676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:418e94d573cb1add9afd7063e4226a92b7ec948a9a43c95e66c715c0f67a36f2`  
		Last Modified: Wed, 28 Jan 2026 18:03:09 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1207f4eab183ed612a70525f252ecbf8740d3b0a40e08972fd026904dcc0e390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.2 MB (271235461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229f893bdbe626cefb112531281789e68a038aee090a6e887c758fb645522d48`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:03:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:03:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:03:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:03:02 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:03:02 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:03:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:03:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:03:17 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1165060f784058b40cc5e189973504f895219fa093264ab172da92d4e32a755`  
		Last Modified: Wed, 28 Jan 2026 18:03:41 GMT  
		Size: 141.7 MB (141729869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0948a2cba10b593247b9ad6f7c98dac8890de05536c482034122e3dacece38e`  
		Last Modified: Wed, 28 Jan 2026 18:03:39 GMT  
		Size: 81.1 MB (81138874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401ac182478ea6b219445d9df8ddfbc187dc5fcbc99c175cbc61ad5242d50b78`  
		Last Modified: Wed, 28 Jan 2026 18:03:36 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d311f0e86d6ae9114913fbcb85616a272b24bcab78956f13d577746296b996b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10837055d9cbd8c5b24cf264b9ac528c81417bcd4668772bd18d52a1fb9906d`

```dockerfile
```

-	Layers:
	-	`sha256:8c373383d16f13b824a05bac37c7b8821b1d5da0d8ea3d5ee6e345b8208e6a80`  
		Last Modified: Wed, 28 Jan 2026 18:03:37 GMT  
		Size: 7.4 MB (7402057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e7eb69d4e6b6285fba112d76d59bc659827224c58cf5d95c4d8aa7d85c84bfe`  
		Last Modified: Wed, 28 Jan 2026 18:03:36 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:322b4695d87f6762f4ba913d3c9b9316b3d961ce940beb89a3eb201be580e15c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.4 MB (271394953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58467c6bd29c480632044d563cd99287d7abc026a9d7e61403abe953fc9ebbaa`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 28 Jan 2026 18:16:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:16:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:16:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:16:50 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:16:50 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:17:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:17:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:17:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:14 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ebe14f9bf3bd6292d3005c52dcc6a3a34db873e59d856fdb773a8f3f886f37`  
		Last Modified: Wed, 28 Jan 2026 18:18:13 GMT  
		Size: 132.1 MB (132079737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae8c579aa025f68231a24d525bc8ca88d1a0f8d820357df3d87cf43eae1e2d5`  
		Last Modified: Wed, 28 Jan 2026 18:18:12 GMT  
		Size: 87.0 MB (86987195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4984f6e20f1002caab2c0d3cc35b4833dbc7f63bfbd58a2dc51ab24b0e4a4be9`  
		Last Modified: Wed, 28 Jan 2026 18:18:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9dbf3afeb6037b4d8ac81a56b91e9f1e902b4794c9c4def16e07e866274ed3c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7414533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b080c2bbbcc6d2670e2fe17cc52d10b18c59fea9ee3b18d17fb63f471ab117d`

```dockerfile
```

-	Layers:
	-	`sha256:fedec7854420d231bf7f4dea2d058f55694ce91765b254aaaa2fa8d2aa0ec15b`  
		Last Modified: Wed, 28 Jan 2026 18:18:08 GMT  
		Size: 7.4 MB (7400277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8371256abcd502fc384017a3e97bd6a167cd95c683a18b451aafd52454e692da`  
		Last Modified: Wed, 28 Jan 2026 18:18:08 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:12e73cdd68cfdf58b0f17b0f8a49127b4999edc3cdbe8cd43ab36e0fc39c3946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252797313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f8d54c4433113386a673af438baa691db1aabe0d19b32823a950413796bd4c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Thu, 15 Jan 2026 23:09:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:09:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:09:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:09:26 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 15 Jan 2026 23:09:26 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:00:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:00:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:00:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:05 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59abf91bf32833ab74c59ea60fc048ddcd4ca740e0a01d6956ae969a791f34e`  
		Last Modified: Thu, 15 Jan 2026 23:10:04 GMT  
		Size: 125.7 MB (125694886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e0c4e2c5612b08588ccd75deeb80f3e52de47454fd8828f281ec98f1d730ce`  
		Last Modified: Wed, 28 Jan 2026 18:00:56 GMT  
		Size: 80.0 MB (79963354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bcb1b40962f3f0d95a1d8b4d1c63cef483ec8b7d9721d0a43cc27a3eed2311`  
		Last Modified: Wed, 28 Jan 2026 18:00:52 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ab99cd4657aa58e2b8af0ee08f805cefd2d0a50f341adeab01887ef61f09e5c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7f69a200f6061ec47f884946417be5a0712bb7339ebb86412d56debb691b84`

```dockerfile
```

-	Layers:
	-	`sha256:6f28685184ed9a233d688426c86a9ec0a8d30f1772a468ded17c48e107deebd5`  
		Last Modified: Wed, 28 Jan 2026 18:00:52 GMT  
		Size: 7.4 MB (7386999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4987330520bad37e3062265e337e27ba382d0f2df676f2eb04d0b58bff56aedf`  
		Last Modified: Wed, 28 Jan 2026 18:00:54 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json
