## `clojure:tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:ce98f665e0f9dd6161ef5111f154a8b6d57a0e4de5626005a06573d2f66d6edd
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

### `clojure:tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:773a20134eabf69816f94122862b02e455d5c80342d6b2aebb9c6d272fe11ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193813715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa6dcf12118e185658a23ac9e81def50a2ab1bd2770f1d92b489322adf16b316`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 02:08:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:08:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:08:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:08:06 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 02:08:06 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:08:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:08:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:08:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:08:23 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:08:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956430ed11bfd074ad26384c12bb7c7511c951dc449b7c21cf5cdf51375b9f75`  
		Last Modified: Fri, 16 Jan 2026 02:08:46 GMT  
		Size: 92.0 MB (92045293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4647f3124640c2a2f9b8e01af13b24e4944bfcbc841de334233fa702c81b656`  
		Last Modified: Fri, 16 Jan 2026 02:08:45 GMT  
		Size: 72.0 MB (71993694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a654db99104fa7d89ebd1176634d04721a1f4f679e93f41188bcb34b701de7`  
		Last Modified: Fri, 16 Jan 2026 02:08:42 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40df86b16f25ba28ee58ffe09c62f59aece2870ebf52196ff4cceebd09c1322`  
		Last Modified: Fri, 16 Jan 2026 02:08:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:46250ffee20cfda4a293782e0f36c5031b0940eceb22d9c669673e5aaaad3bfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffaed29f08d1351de56fb325d49ac0f4bdf2267f578e2e40d3222f4aca6d06d6`

```dockerfile
```

-	Layers:
	-	`sha256:7e709891647ff598810b7d80e620d3a4b84a796b3370530ed71eb4bf365a53c1`  
		Last Modified: Fri, 16 Jan 2026 02:08:42 GMT  
		Size: 5.2 MB (5207647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e75219dbea3775584792dec017526803f800a243b1520ccc435697c82b600ab9`  
		Last Modified: Fri, 16 Jan 2026 02:08:42 GMT  
		Size: 16.5 KB (16492 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:20c38675757d23044f5b4797421024a1c32cabb6f0bf43794665b883155e632c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192993732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce756b3941378a4f1a9b40666c2738b8cd3075ecc3e85a52848ebea44b659ff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 02:10:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:10:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:10:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:10:17 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 02:10:17 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:13:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:13:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:13:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:13:19 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:13:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6a0e3c87a32b613f5a9f47ce1800a1b1c51b28ae8a0901d6ccd4ed5fa994e2`  
		Last Modified: Fri, 16 Jan 2026 02:10:53 GMT  
		Size: 91.1 MB (91052460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d20755232f1c1a0c237d984d68d69bfc238daef73a889977dfd0b07a9ae1ec4`  
		Last Modified: Fri, 16 Jan 2026 02:13:36 GMT  
		Size: 71.8 MB (71806187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72940a12f34c18d759a673235d8610bd7a628b6fa8bacecac123ac9a03ecb13d`  
		Last Modified: Fri, 16 Jan 2026 02:13:35 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554af9e0da5dddfd05f7b80ead1053d8de259c8d3822e678965f44ea3accc6d7`  
		Last Modified: Fri, 16 Jan 2026 02:13:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:86e4c2390d5614661d93fd951fa46c5c7bf835b1ee381547bc2c5172066a5cf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5230072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e05c29482cdbf338b73e372acc9e023f3a046cae03d308da90fa1d64a638d55`

```dockerfile
```

-	Layers:
	-	`sha256:87afa78d6e54c017fc4d51dddb01a2adafa140294ea67be0411fffb074b29995`  
		Last Modified: Fri, 16 Jan 2026 02:13:35 GMT  
		Size: 5.2 MB (5213437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae6a9acadc74fdf73e89f3886f0b5c418895c1b3198f64c05ae6f39ae87baf48`  
		Last Modified: Fri, 16 Jan 2026 02:13:34 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:154cccc1f68afae5a4a57b7c528e5d43160333bde1ef5c8cbaea359c5bda7240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.6 MB (202597441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f92e7bb1d1bed0fe40cf2ef95fa1682db408ec27009d1479e57bb02cd29042c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 03:44:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:44:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:44:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:44:53 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 03:44:55 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:52:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 03:52:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 03:52:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:52:07 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:52:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a11e063d257c7fd0378d1844308cea571e43cdc3c6ef2206a9db6629a1520ee`  
		Last Modified: Fri, 16 Jan 2026 03:46:59 GMT  
		Size: 91.6 MB (91610755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce28569797c078349ab33ce0cfabe47921257aeaaa9f1c902d96154c25f32ab`  
		Last Modified: Fri, 16 Jan 2026 03:52:48 GMT  
		Size: 77.4 MB (77390042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6ee97d259eaefcd301e74f207f166b6e35b65444741a078d08fbc029a2a0b4`  
		Last Modified: Fri, 16 Jan 2026 03:52:45 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096ea04af778b40d78b02cf889f497e857d123eab098a46369aff32b1cbd9f98`  
		Last Modified: Fri, 16 Jan 2026 03:52:45 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1a3db38c6bab46a68a7010a880aec6a9fe8b7bf9a295d789dc5947c06b4747ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22bf8acbbfe5ae1ca020f52f86a12fc285afbcccd8684a61991d89009521cf80`

```dockerfile
```

-	Layers:
	-	`sha256:b150fee3e2afc3c6935ae32407921b3b14c317e046f2a81b56f76a67d693f19f`  
		Last Modified: Fri, 16 Jan 2026 03:52:46 GMT  
		Size: 5.2 MB (5213328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dba37572cdc94a1c5ee9af2ee4ffe523e9c69195181bb7bfa85acb6c9e42d1a4`  
		Last Modified: Fri, 16 Jan 2026 03:52:45 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:92e2532348045ed47c435d3a11544968b274006e8f30e983c0c18b57a466d891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189904353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f35ef2374dbfa7a85fe46bcbcdd3b4b763aed7599dbbd585ca730f0b98c211c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Thu, 22 Jan 2026 04:35:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Jan 2026 04:35:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Jan 2026 04:35:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 04:35:53 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 22 Jan 2026 04:35:54 GMT
WORKDIR /tmp
# Thu, 22 Jan 2026 04:57:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 22 Jan 2026 04:57:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 22 Jan 2026 04:57:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 22 Jan 2026 04:57:57 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 22 Jan 2026 04:57:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c69cdd71ef06850eefda28596d4212304f3101cd9d101f44fb4cf0c74701f3`  
		Last Modified: Thu, 22 Jan 2026 04:41:12 GMT  
		Size: 90.8 MB (90752894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6d3a24e9d95f0a53d69ef1e185241c625a41b38f404e11d840c904103e56ed`  
		Last Modified: Thu, 22 Jan 2026 05:01:36 GMT  
		Size: 70.9 MB (70878730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b476d3e9776c236b085a0fac9bf9688b2075c785db6db5441d6b35b870153e4c`  
		Last Modified: Thu, 22 Jan 2026 05:01:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebf67b75368031bcbccfb2b55210c9b55d09be236a21b0cedd77ccbce8ccf1b`  
		Last Modified: Thu, 22 Jan 2026 05:01:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:19773bcbf4ba7724e951b0f2f421e37b20ebcdea7d8d22106a3925f36e843024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bfa817792c85cf3a17a950e8e4baa05425bad4984aa40fd36b83fd7cd6ef340`

```dockerfile
```

-	Layers:
	-	`sha256:f836df0b753bc98eabb8debb449f1f6961b29a1334ffef48afa9a5bab6ef03aa`  
		Last Modified: Thu, 22 Jan 2026 05:01:26 GMT  
		Size: 5.2 MB (5197120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab3e34b5822126bcf79d703e0039a9de285c818f46702ab468c3a1bd699b2126`  
		Last Modified: Thu, 22 Jan 2026 05:01:24 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c64cfb3cba27d88374fcf8b32fcaa7ed453fcc3c3f71a72ce0563f28d1cc8468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (190997394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c770344035f92f54efc3ef65b6dc9c1e99507147a18a497462362b803221e6f0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 23:23:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:23:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:23:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:23:10 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 15 Jan 2026 23:23:10 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:24:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 15 Jan 2026 23:24:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 15 Jan 2026 23:24:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:24:44 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:24:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:27 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2b60cbc839537ac9d2d64e95bf99e1c19c3b75f06175e544fbfafc8cc5fea1`  
		Last Modified: Thu, 15 Jan 2026 23:24:08 GMT  
		Size: 88.2 MB (88210671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c664acb6ba226fd064755f4e47ef18424f83ac92d566f35fb41fe74dce4b2d`  
		Last Modified: Thu, 15 Jan 2026 23:25:08 GMT  
		Size: 73.0 MB (72952269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6551e760e41fd2cd0c3d0d380018f2829795bd37d9ba259e704110ba1283cb97`  
		Last Modified: Thu, 15 Jan 2026 23:25:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b01078b1a83993c76b4567449cd8953cc59594f79dec00d7bc1d1964dbb62c`  
		Last Modified: Thu, 15 Jan 2026 23:25:07 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0a0b0fb6df342df67fa4ecf558c6d3c4c786d1ee5c8acbe1d740612fc7a3c3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda855ce01282ad07569d7e077997726862be3deee8e86ae18e988b7ee64bd28`

```dockerfile
```

-	Layers:
	-	`sha256:24a568ec0bd76a9dba90405c8a25150ef203d90e2103842815c3b322bb555594`  
		Last Modified: Thu, 15 Jan 2026 23:25:07 GMT  
		Size: 5.2 MB (5206119 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:407fb4e7e9902967a306c451023e1ff99d0e8a7631269aa1d4a2898ad0ff7007`  
		Last Modified: Thu, 15 Jan 2026 23:25:06 GMT  
		Size: 16.5 KB (16492 bytes)  
		MIME: application/vnd.in-toto+json
