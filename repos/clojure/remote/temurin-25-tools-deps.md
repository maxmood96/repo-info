## `clojure:temurin-25-tools-deps`

```console
$ docker pull clojure@sha256:dc4f40b119af09c4fd2a0c54c1a77a6ed6bbd922b51f56612ec52883140ce9e7
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

### `clojure:temurin-25-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:853b5c6710c643edcf67bd3c635deb1dc375c4d9aa2fd3c81ce350fb24fe74d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221674109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cf6e62807fb426304d9b5ed28b240fe71538443fda670ac68d161112de6c9de`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 02:05:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:05:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:05:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:05:45 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 02:05:45 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:06:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:06:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:06:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:06:01 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:06:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0dbb350197428c04316797d233019b1f34021956c06d2297d7299b7d5d4ca5b`  
		Last Modified: Fri, 16 Jan 2026 02:06:42 GMT  
		Size: 92.0 MB (92045288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e682de133f47aa5e434513e41548c5f74c63ab840aad97e05703dd6ac5c37ef6`  
		Last Modified: Fri, 16 Jan 2026 02:06:28 GMT  
		Size: 81.1 MB (81146157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9982dbec1de2dfb005c71d3b962685ef3daff943edb440d552cf99b1762504`  
		Last Modified: Fri, 16 Jan 2026 02:06:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9695ea05b38025c8f0492a64280871132e0352edb2a4357ca1bec953b8ceb682`  
		Last Modified: Fri, 16 Jan 2026 02:06:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:373876ec6f0be0b5a8e2762e1cb1afc246718a37eaee813d8044380dfe881251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7345968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d88d6fd708d1ef595dea20cd672c8c54de0f51b1a6d9690572f1089250c0798`

```dockerfile
```

-	Layers:
	-	`sha256:9f75af9ad7915519c8926986a71c3827bcecb7e23d2db7a60f2712eb8b705531`  
		Last Modified: Fri, 16 Jan 2026 02:06:24 GMT  
		Size: 7.3 MB (7328197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c2e83a11e14ef9fe6635971883f0abac0a240e5b2fe9ae38513c563d202f636`  
		Last Modified: Fri, 16 Jan 2026 02:06:24 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0bd1e3a3b04e3634801fe405d1e72d8e0cdfaacafedda2462c16167ab2f3d405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 MB (220558422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d46209451a07bd237d4a842d5a59a39a9a13f8f292d2bd1fc66140dfdc8a3b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 01:42:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:42:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:42:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:42:08 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:42:08 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:10:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:10:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:10:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:10:54 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:10:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed151cd1f87e92a724d9a48e309d58a18cd805ebf4483e572e60dfe7d0f8d36`  
		Last Modified: Fri, 16 Jan 2026 01:43:19 GMT  
		Size: 91.1 MB (91052515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f65fb79e2d3cbe840ae09cb12497da7ab5959409083c03cb74311277609d319`  
		Last Modified: Fri, 16 Jan 2026 02:11:26 GMT  
		Size: 81.1 MB (81138795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2220e62620b1424f4917f01df3d30633e4e730f2eba880e3dc2b814842c8af6a`  
		Last Modified: Fri, 16 Jan 2026 02:11:11 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72f68ae57c3f270135efd509a5de43a835e930d9be1c2e2e30a3867066e4d9a`  
		Last Modified: Fri, 16 Jan 2026 02:11:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:60af5ce164c74513c968f5ca00ee5c628977cd1f3e5c2549cf5cd794c28e21ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7351990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30dded3f2b3fe5f438e42e39bca0dd86dd243addb3c737d57b2237777efecd20`

```dockerfile
```

-	Layers:
	-	`sha256:e44ed787cb07e4e186a7dc4a3bc54bd3efcbccdd3a3caa928d957f5d6af01711`  
		Last Modified: Fri, 16 Jan 2026 02:11:11 GMT  
		Size: 7.3 MB (7334029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3183802fe95a01d8eab00ae9003a3586724db5ca03d4a4af3cf244b505f1985e`  
		Last Modified: Fri, 16 Jan 2026 02:11:10 GMT  
		Size: 18.0 KB (17961 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps` - linux; ppc64le

```console
$ docker pull clojure@sha256:af8623096d667f23eaf09e4d8645675bbe33f8fd3b954f3a59969b87fdb7e9ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230925619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e68413bf0c2ba556888066ff614d7e42e85d099046c6bd06a49bf6d48238289`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 02:43:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:43:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:43:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:43:19 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 02:43:19 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:48:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 03:48:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 03:48:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:48:08 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:48:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:39 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96a2bd88573c70d41d7945da863a10fbc76252e0180def2eb63f3e259f7f1fe`  
		Last Modified: Fri, 16 Jan 2026 02:45:52 GMT  
		Size: 91.6 MB (91610764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65ae567a869b033a4b1a8188bb8267b0cd2276e39ff9bdad531f952906288f1`  
		Last Modified: Fri, 16 Jan 2026 03:48:59 GMT  
		Size: 87.0 MB (86986437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d83f79392a1b7d8253dae2392b5765e0ac5c8e4351afb2e81e3e60308933fcd`  
		Last Modified: Fri, 16 Jan 2026 03:49:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775e3673a2256dd1d8e99b8a5d4f881c469ffa0c6313c8fdc1dd6a49497c298d`  
		Last Modified: Fri, 16 Jan 2026 03:48:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:eadfe35b176d151e2505700374d7ba91e078d8e2d3ab75a59bdf4eb1eb0d88a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7352602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea32329094e569da77acb6def7e86f1d11471e976506a9611522bd19c5445a8`

```dockerfile
```

-	Layers:
	-	`sha256:a9219a1655ec37a09d24167af301565ffab7ab7e4432ec3c7bd63b5820d73bbc`  
		Last Modified: Fri, 16 Jan 2026 03:48:54 GMT  
		Size: 7.3 MB (7334747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e55d3f22ce1401396fa3c95df26962403c38c7d7e44059ddd6e65291aef7fae`  
		Last Modified: Fri, 16 Jan 2026 03:48:54 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps` - linux; s390x

```console
$ docker pull clojure@sha256:e85590ce45744c9323d8ee36263ac7bc0a37fc2c6d1f2e001e9a9ae5b1ddac9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215309554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a024b6758ad20e1601f6197a648c9be7cbe493c98405c824dd581319307135`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Thu, 15 Jan 2026 23:23:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:23:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:23:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:23:06 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 15 Jan 2026 23:23:06 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:23:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 15 Jan 2026 23:23:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 15 Jan 2026 23:23:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:23:20 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:23:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:05 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d228a424ac43e5b633b49f78829dd5efa41560a237d73954164bfe619c713508`  
		Last Modified: Thu, 15 Jan 2026 23:23:50 GMT  
		Size: 88.2 MB (88210666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b130280ab2fe6f155872cd30a712c99fa16b821d954979a5b2e8066fe175ac4b`  
		Last Modified: Thu, 15 Jan 2026 23:23:49 GMT  
		Size: 80.0 MB (79959419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86684d721bd0702d257b55e52d629b12b4e596389c890f04ca840f9cb2ea2d5e`  
		Last Modified: Thu, 15 Jan 2026 23:23:47 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae28dbb1b65e8b4acbb7652fa12aba496372976091eedab145b4acfbc370966`  
		Last Modified: Thu, 15 Jan 2026 23:23:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:54268646cdc141f3eb333214095f29b25b0b5091f8bf8ab17ba33c7ad6f181f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7339835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543c2c7b7e8002814df4c2aaeefac90d597230bd72578d1d62124040fdd1339b`

```dockerfile
```

-	Layers:
	-	`sha256:a5dd894de48a42ede9463cd70a8418fe946954d2e1464da54537d31971504d95`  
		Last Modified: Fri, 16 Jan 2026 01:43:45 GMT  
		Size: 7.3 MB (7322064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:771c2d8a10bd42e69678775b27c91baa4b9e4a0a912feb0b7d6ff4623e77e81b`  
		Last Modified: Thu, 15 Jan 2026 23:23:47 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json
