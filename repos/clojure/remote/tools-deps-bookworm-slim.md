## `clojure:tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:0a9311d8d33a99c82da8c48496b34af6de44f695e960fe599dd841487e239970
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

### `clojure:tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cca299a0aa9a9c4c09512f57ec05a8cc227d4466d28876b3398484ab07113d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.5 MB (187456074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5faec51ddc958f4bc73c316cc97218bf84fe0e4ab52fb7b8bd6507d7a37f765`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:20:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:20:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:20:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:20:17 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:20:17 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:20:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:20:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:20:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:20:33 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:20:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b65b44e18cece837832e647ba74a14b7337485d665d5b30d966f3848e562325`  
		Last Modified: Fri, 19 Jun 2026 02:20:51 GMT  
		Size: 92.6 MB (92574566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d9049dbe3e08fd9a76123e7098c68bb69a09ccf91bbdfe96d5cb2b911b7579`  
		Last Modified: Fri, 19 Jun 2026 02:20:54 GMT  
		Size: 66.6 MB (66642845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a21b1a4208cece9079f3bb95cd2de6e00a4a9dd0298d8d9f8981fa718609a6`  
		Last Modified: Fri, 19 Jun 2026 02:20:50 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ba23c6e5a21ad40c91edfa3705af9af2442dae7750b56f28a77620deaff751`  
		Last Modified: Fri, 19 Jun 2026 02:20:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1b8396f72007bf53574ca0d297a777be28f7f8cd9e9b6fafc4c1162944b2af4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5098768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1656ae9ed19314afb85f90ca0eb7dbd3817d882e46d592e06ea9114cf5a7841b`

```dockerfile
```

-	Layers:
	-	`sha256:d0b91d67336189ca1448589a916c361043eafc3e63df5f926851ac393e54db44`  
		Last Modified: Fri, 19 Jun 2026 02:20:50 GMT  
		Size: 5.1 MB (5082089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31dbba60dc5fe9eba10c6901b8f6d5b7ac4f6d75dd7741b288270c34669e5804`  
		Last Modified: Fri, 19 Jun 2026 02:20:50 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b39f56233e43cede1faf7de2d81f37ce7e0e762429ec9ed3778d6b3650d872f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186308803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e6d143e79525d241e51daa991a594407ba9511cac9c7dc204366532d9cd8fe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:20:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:20:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:20:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:20:37 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:20:37 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:20:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:20:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:20:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:20:52 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:20:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061e80d5bf2f138c381d3af47543f1e4ba1739d68a25f8f8782b508d3239b754`  
		Last Modified: Fri, 19 Jun 2026 02:21:14 GMT  
		Size: 91.5 MB (91542237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce496cd9063ed3a6d1f5e52550f65e58a483b780a91519616362e538b3de9471`  
		Last Modified: Fri, 19 Jun 2026 02:21:13 GMT  
		Size: 66.6 MB (66643221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf708183c063d02b8cc0403dee5b315296184cd04b52bf761a894b85c385f80e`  
		Last Modified: Fri, 19 Jun 2026 02:21:09 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3287988c733fbde2b67d4d6ab4c0b56147f4cb815879dcfb02c24d4f1403af55`  
		Last Modified: Fri, 19 Jun 2026 02:21:09 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9f8173e193ea69f2b6789d557c8501739c5e50a5ee402aff3e461b2ade7fa8ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5104692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4e339217ad8e449e50e2e935e1a69182707dd78b3c3e18589edc5ef43ff4d1`

```dockerfile
```

-	Layers:
	-	`sha256:c7e51a27be6bd168f94829a9baa951b5a1c74da7b91c65d4a43ffd78a7df0ef7`  
		Last Modified: Fri, 19 Jun 2026 02:21:10 GMT  
		Size: 5.1 MB (5087871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:842861e5a3e8fa578dd24aa05d68ff7f41442b8525db1925142111185e21f0c4`  
		Last Modified: Fri, 19 Jun 2026 02:21:09 GMT  
		Size: 16.8 KB (16821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:1709f9d5d72cc626d6805abe5d12be49c1c63eec864ba805b3ef7b202bb270bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.5 MB (196473295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b3c052e6949024d9151a80d2420c41a9ced43d978561374e607808f46a989b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Wed, 17 Jun 2026 00:03:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:03:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:03:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:03:19 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 17 Jun 2026 00:03:20 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:55:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:55:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:55:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:55:38 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:55:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ceb0eb5280b5d711b09e7b6fc60f0539124c87d3b78261261a7696dc0d1b48`  
		Last Modified: Wed, 17 Jun 2026 00:06:20 GMT  
		Size: 91.9 MB (91914038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd04172e70ec74e8809fc5ad091eec63513d8ead413ff86ba78864470e1f68ac`  
		Last Modified: Fri, 19 Jun 2026 02:56:20 GMT  
		Size: 72.5 MB (72476275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd028238f62af350e76aaf9b47644b00ae8783cfd5d26dcbfd08d1c2a3863b2f`  
		Last Modified: Fri, 19 Jun 2026 02:56:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716a1fa406d268129021fd8d8011e986d3d7a9069101b9a350bee143c488b1ac`  
		Last Modified: Fri, 19 Jun 2026 02:56:18 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:825ea9cd0767caacdb6e6d6e7378c17250a23030800b43779ea3f87e8dd0e2ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f4d133ca16053e0a621c5ba12bf28256a7e429ed47d461ad39f3b61bcc64ca`

```dockerfile
```

-	Layers:
	-	`sha256:41c22855a0c00d4475aeb905b7b3ad8f6dc5e3af5b8d72320f1286691735193f`  
		Last Modified: Fri, 19 Jun 2026 02:56:18 GMT  
		Size: 5.1 MB (5070571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:612bf34aa50d71c12a4ca15b95b751f38c7f90835fa91eff1cb71a05e688afdc`  
		Last Modified: Fri, 19 Jun 2026 02:56:18 GMT  
		Size: 16.7 KB (16738 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:951ed0129b73b78d23827176055ad6488a42f5d8837da90926808e592ec4b48a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180767112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb175f950b890a620a370a0ea09d35708d083ce250e10c1fbb131e8c98f0beb0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:21:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:21:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:21:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:21:00 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:21:00 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:22:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:22:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:22:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:22:03 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:22:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f24253f44b61e08a6eea6c9ac2c141af3fb831e29f77c9f2a38981b7fd8a04`  
		Last Modified: Fri, 19 Jun 2026 02:22:31 GMT  
		Size: 88.4 MB (88420366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52888742b274d00c6693595a1300781775918f9c9cc24566ba7e946538767f11`  
		Last Modified: Fri, 19 Jun 2026 02:22:30 GMT  
		Size: 65.5 MB (65452195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bbf87fa3ff4a081600bc68d1c08b948f960af346fc59d12aade709cdabb979`  
		Last Modified: Fri, 19 Jun 2026 02:22:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edce25db9956d291c2d63f096d173d4848f6de12bb85c74a5effea6c23f8bcd`  
		Last Modified: Fri, 19 Jun 2026 02:22:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:69fa5dd346a51a221bcedcb8bb692169dd2587f331e4f04445a493a63770fae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5074651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9698a9719ff5ca718b2de8fb107312625ecf7e8a200d8e4be7e3c8b4d539d12b`

```dockerfile
```

-	Layers:
	-	`sha256:f107cc9751250b0651fe456052cddabd0a77145bb91d5524ba33a4cd8c35ba92`  
		Last Modified: Fri, 19 Jun 2026 02:22:28 GMT  
		Size: 5.1 MB (5057972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05843329ca6cf891bf3df1fa49c19b0c5bf3a75eb407d5c814b3632bc8de13e7`  
		Last Modified: Fri, 19 Jun 2026 02:22:28 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json
