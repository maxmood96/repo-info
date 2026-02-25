## `clojure:temurin-17-tools-deps-1.12.4.1602-bookworm-slim`

```console
$ docker pull clojure@sha256:f9a433308c58a9ececb279600ce0b1e3e54ad000979c6173193da940bf4b1843
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

### `clojure:temurin-17-tools-deps-1.12.4.1602-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e18b0dd3e278575c6f46376ed667d130f6ee1e07f88c3ac4b47c8123c6c5f1ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243543487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b595d2c8521e0d6c985cada01603b323be61e3909c708ff6b3bcd6457964c2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:55:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:55:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:55:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:55:09 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:55:09 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:55:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:55:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:55:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:55:24 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:55:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60736bda4a126cde07eb9cfe023df12424cebb8f8097d50feadfdd582d1ed0c0`  
		Last Modified: Tue, 24 Feb 2026 19:55:46 GMT  
		Size: 145.6 MB (145628711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8dcd7011ca0b198700356e933d3c182e66f691eaa6ff380e1d0742ee215b6d`  
		Last Modified: Tue, 24 Feb 2026 19:55:45 GMT  
		Size: 69.7 MB (69677460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd16d20e1eb1cfdfd042ea849fed7a1d6fdb701eee048032f82af00dd966ec3`  
		Last Modified: Tue, 24 Feb 2026 19:55:42 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ab166a7474605658c8f48f4e6f705167f5ac007f803618109f6aec8b93a27f`  
		Last Modified: Tue, 24 Feb 2026 19:55:42 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f066beca628a76be006afa3d1bd511ad736e60fa3966205f52965e52856c5be5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5130490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d191aeac6eb6be8899c3f4cb4dc6e7d72d49fc5f0acf0ac2bf21505d9b64618c`

```dockerfile
```

-	Layers:
	-	`sha256:2297ca580c396ba5c3a7485b5e7b3f13ad7bb0787ae441432c17971c0bb9a211`  
		Last Modified: Tue, 24 Feb 2026 19:55:42 GMT  
		Size: 5.1 MB (5114654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7931e8414badd5b96767dae80a37334f999c491fbb845b622b4fff9622105e0`  
		Last Modified: Tue, 24 Feb 2026 19:55:42 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:85688ddc0dd8e2ef1464847425de0b6483ee58ac71fd4fcc2b170e4d5eaf5e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.2 MB (242225957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f57c4831acf0e38594be2831df977bf96606f7db319f251778e0d0ab17c86ea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:05:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:05:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:05:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:05:46 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:05:47 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:06:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:06:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:06:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:06:02 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:06:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47c2742c5137d1adc9a98d2d04fc2af2b324f40c2bb44d64cf745d7fc28fbae`  
		Last Modified: Tue, 24 Feb 2026 20:06:24 GMT  
		Size: 144.4 MB (144436198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93afdc5a90782f31576de5f1d4ac872726bed77f1c7a870252e50115bea3075`  
		Last Modified: Tue, 24 Feb 2026 20:06:22 GMT  
		Size: 69.7 MB (69672639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecc60605120f4162ac1cc494f9303cff558b93a3e5c963e611fc91430a21f25`  
		Last Modified: Tue, 24 Feb 2026 20:06:19 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1505f6dae05b13ab2d88ed57d5dcf8f0959c21b0ff693661921c025e5ee170e1`  
		Last Modified: Tue, 24 Feb 2026 20:06:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ec0a119fc5492aad752dea9ff79a5b2514011a348098cb093b5d156862f593d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5136369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2afcee8b11c2bc86c0d38ebd6714459ce6be2b15f69c1ae0e2de4f749df01e01`

```dockerfile
```

-	Layers:
	-	`sha256:2069f65882dd35b955efd1086ea3aa4ce72b8a8e5249d61f57aa4f042fea74e4`  
		Last Modified: Tue, 24 Feb 2026 20:06:19 GMT  
		Size: 5.1 MB (5120415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb0c4660032702981c9f775c6b371e9de2b029e7d1d2baf00eaa522c7c0527b0`  
		Last Modified: Tue, 24 Feb 2026 20:06:19 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:57dc696fe0ab15bafde87a53bd4c991657ade674b8a33ac0a8d37e5614f32565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (253031699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd334efc20b261229fc666d99545071b5dfffc0bfae0577b8ce43c1d8f08d21`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 25 Feb 2026 01:57:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:57:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:57:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:57:33 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 25 Feb 2026 01:57:34 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 02:02:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 25 Feb 2026 02:02:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 25 Feb 2026 02:02:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 25 Feb 2026 02:02:44 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 25 Feb 2026 02:02:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5dce4318783a0719a116da2642ffc1e720139258359bf09a330578610611a0`  
		Last Modified: Wed, 25 Feb 2026 01:59:10 GMT  
		Size: 145.4 MB (145438176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e9b8bc5cfebe4e635e308f7ac944815f5e46f19d72f57d76119c1a0e29c22a`  
		Last Modified: Wed, 25 Feb 2026 02:03:22 GMT  
		Size: 75.5 MB (75514146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496429aa2c63971b07eebbba5ef164f54c71dad8051054533b24f0dfd2da4bc0`  
		Last Modified: Wed, 25 Feb 2026 02:03:19 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7315a14a2698f15a8c947e1ebcb334db5236a13d4652398f385f6668ee30de88`  
		Last Modified: Wed, 25 Feb 2026 02:03:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ba15b6f836f648e40af8995fa6a1257825785d74a33a53a56ba1cf0b820e0e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74025ef33d6356d9520eef739bbc114822ef5108d7ad4e5e0fd2793c87f37563`

```dockerfile
```

-	Layers:
	-	`sha256:5ca29b926098803b74e38439a2198ae120f643d85674a4f390b333f39e2ecde5`  
		Last Modified: Wed, 25 Feb 2026 02:03:20 GMT  
		Size: 5.1 MB (5119812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6463e666e187cc59a485f7996bdfc233f379b6b7d6441ad018a060af34d4726b`  
		Last Modified: Wed, 25 Feb 2026 02:03:19 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:13a8f9eec4e0cd86a698aaaeeced10f3d1dbcec799c7270e272559bf72d30aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231009774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6b52e2b959c7624c6b0b23bfd2cb96010c8cb586dfd5186059f4f85e4797e9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 23:15:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:15:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:15:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:15:05 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 23:15:06 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:17:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 23:17:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 23:17:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 23:17:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 23:17:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f803dd7bc2d733b564da46ba5a231113967783e3416f03d86ef7ca2b792f6a`  
		Last Modified: Tue, 24 Feb 2026 23:16:12 GMT  
		Size: 135.6 MB (135627087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ea9426f58c1054887418b2a2d43fca7414831d0b39c5db25528d745346924c`  
		Last Modified: Tue, 24 Feb 2026 23:18:09 GMT  
		Size: 68.5 MB (68490120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4468a3b3dd79b7da628debdfd7ee2430aa5241efd38331de85f5c864c23e0715`  
		Last Modified: Tue, 24 Feb 2026 23:18:08 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76e5c89720262f1664615bca94467142b24edfa38ec5a62fa02ffb1487a188e`  
		Last Modified: Tue, 24 Feb 2026 23:18:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:361d481e87721100af584a27141c4fa38d5fe6d511de0de6019c98cedf3fc775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5121811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1074b0313e17e90962cc8ae2aa7be6ea346156d330f104d26fa0804e00507321`

```dockerfile
```

-	Layers:
	-	`sha256:a643072bf6b023c0d407cc7e9c6f8ac7b35ba036f114d4470e57e7bf7483dad7`  
		Last Modified: Tue, 24 Feb 2026 23:18:08 GMT  
		Size: 5.1 MB (5105975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07db4325e65eb215375f14824afa8d00212fe1ec924e9ec51960fff45bf78d73`  
		Last Modified: Tue, 24 Feb 2026 23:18:08 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
