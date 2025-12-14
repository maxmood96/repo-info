## `clojure:temurin-21-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:81eae010ecbf71e5e271f90a272496dbc3c62d6f3b1a973968e92750053d5355
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

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8e58d1e3d9fd39d4bc6d3f86fa09fe8bed6ab62c5aedcdfd094efde027b4fac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259596114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726c4faa111a01d33fa2af23aa3ce54fffbc9227a2b7fe402c90573b5ccdf77c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 22:40:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:40:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:40:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:40:13 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:40:13 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:40:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:40:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:40:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:40:30 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:40:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07b6ea401195801a5d2ac7dcee6c7138b4b629fb7e454a34a694deb19b6ff14`  
		Last Modified: Thu, 11 Dec 2025 22:41:18 GMT  
		Size: 157.8 MB (157826042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8113cbe3bd0908fcc63998e648386f49a3cc4917d579718c8895336c853c48`  
		Last Modified: Thu, 11 Dec 2025 22:41:05 GMT  
		Size: 72.0 MB (71992537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20d2cdbf97623cf80155d16d4c1d02b2a306a2560d144db489ee9934fc74770`  
		Last Modified: Thu, 11 Dec 2025 22:41:00 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940f2760dce3e37dcf83fc6cb343f324891bf0e8edd41b4d515c686da4d3b2e1`  
		Last Modified: Thu, 11 Dec 2025 22:41:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:13e5d4d1504fe22f602bad1e13b61d79a95a2a14fe5784b379084c3c7f6ac821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99154289ac8213b4ba7cd94c1e51945d847e955aa68c5f6ad8a1179baab7d0f2`

```dockerfile
```

-	Layers:
	-	`sha256:4b523583a48ca8d20d3c8c62330c92b34fa1ceb28f1c289caa423cf024b41547`  
		Last Modified: Fri, 12 Dec 2025 01:42:56 GMT  
		Size: 5.3 MB (5259301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10995dd876df44b075c6c976598f442b57fe0dd8d09b25594ebe0aeeacdc4dcf`  
		Last Modified: Fri, 12 Dec 2025 01:42:57 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d56ef4593cafa593d12722bd7eb4fdd945ac8d1115a7fdad4367009326ff9bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258054197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cad1a4341a8139e0827bb1de267c8b482d1e0ff6573b22a5056209c1a4ab4c6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 22:40:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:40:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:40:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:40:06 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:40:06 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:40:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:40:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:40:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:40:25 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:40:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a384c4fb3cd2bca60628d18532b208969c422446ce4507dc549a18d7f94336`  
		Last Modified: Thu, 11 Dec 2025 22:41:06 GMT  
		Size: 156.1 MB (156107637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982592c29e55ed335906a5a89554da41613f37dfc11a5bb8dd1fe56ab8fcd088`  
		Last Modified: Thu, 11 Dec 2025 22:41:01 GMT  
		Size: 71.8 MB (71806893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae45c9be4dd651a8ece55f909c91506ad9c006d2a3d316d717ece00fafc324cd`  
		Last Modified: Thu, 11 Dec 2025 22:40:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898ee0d139204011bb391d4005b9c83b575ca0358a0d4df6dec6edde15d7f65d`  
		Last Modified: Thu, 11 Dec 2025 22:40:54 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4aaeb2f0dd51c1019bb3039740e49679c4e6ae79237c442a87aa657e84a71a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8d23e0956ae6b1a56cd0a6ae9a6db8973dba1a4272cbf0ec8b3e95203a413e`

```dockerfile
```

-	Layers:
	-	`sha256:8bdf90cd07790422a79e856f14eee1b9af9fde3d82b963396da2ba726aeb9c8a`  
		Last Modified: Fri, 12 Dec 2025 01:43:02 GMT  
		Size: 5.3 MB (5265070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14ad9be96e8e343b00c5418357addd2707701cc4e0dff26dc8194f8b0b6856b9`  
		Last Modified: Fri, 12 Dec 2025 01:43:03 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:02aae3c2acc8053dac14e2385dd9f1019b09237a33a66e9e0825b3bbc36a2038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268927872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b17a3feee919017f321f45405223aa59232b7e1cdc067d1e9650696afcf2b4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 03:53:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 03:53:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 03:53:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 03:53:31 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 09 Dec 2025 03:53:31 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 23:03:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 23:03:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 23:03:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 23:03:53 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 23:03:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1738f5a3e98755bfb9425681189b2a44278e8171bee65caa143a42717b2cfb8e`  
		Last Modified: Tue, 09 Dec 2025 03:55:01 GMT  
		Size: 157.9 MB (157942950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b212c4e24861ff3bcc4214097d5bd46a4c0e73c39d9a8b09c53f2bbbf649d04`  
		Last Modified: Thu, 11 Dec 2025 23:04:55 GMT  
		Size: 77.4 MB (77386991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4450cf83a0580fe4c55ee14cb0f7404f0d7191e7d9f3219a3174e4521599d1b6`  
		Last Modified: Thu, 11 Dec 2025 23:04:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6362ad0db87bfb554d678345678446f65caadd22d0e41b6fa94adfa2f092071d`  
		Last Modified: Thu, 11 Dec 2025 23:04:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2ddd694b9415dfb50f3f20909d7afcacff8506c37246d245b53c90f358a0753d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cfcec34087639ac69676f63ce7471495e9bd8e2e1f199d94304a11a34f10bf8`

```dockerfile
```

-	Layers:
	-	`sha256:1b00e818b200e8033e7e3ab72c871ca7c45c3ddee8e1ca1afaa2139ee4c7f53f`  
		Last Modified: Fri, 12 Dec 2025 01:43:08 GMT  
		Size: 5.3 MB (5263672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:220564e56654309803f48701450bda20fdc2fc3c76573b26a549b7098bdb28f3`  
		Last Modified: Fri, 12 Dec 2025 01:43:09 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:256dfa807be07889292edaf1c49e61e9998884703b23b2a0dbd03a7c481f4677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.3 MB (256346362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa5693ceec7a7ce0d2a00b72f2425dfab15397a3f2a933c26d04cde5c80332e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Sat, 13 Dec 2025 19:01:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 13 Dec 2025 19:01:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 13 Dec 2025 19:01:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 19:01:12 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Sat, 13 Dec 2025 19:01:12 GMT
WORKDIR /tmp
# Sun, 14 Dec 2025 16:29:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sun, 14 Dec 2025 16:29:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sun, 14 Dec 2025 16:29:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 14 Dec 2025 16:29:39 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 14 Dec 2025 16:29:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20593941a6cd1331d645f1f4a2f48aa0653e03e20d869ae08c1cbd9b3579a72`  
		Last Modified: Sun, 14 Dec 2025 01:26:10 GMT  
		Size: 157.2 MB (157194253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd68abea8b5e579bd3fb3c401457d71b5cae593703104930dad8e50b88e3c76`  
		Last Modified: Sun, 14 Dec 2025 16:33:48 GMT  
		Size: 70.9 MB (70877913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589734882075639a1510f1a84e7fdd318d4585ff8c81c6bcfc46af16cb69de58`  
		Last Modified: Sun, 14 Dec 2025 16:33:39 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388aabd9f63a3642833bf932be1b45f46783d7e7005a99cdf0b249897394c957`  
		Last Modified: Sun, 14 Dec 2025 16:33:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c667d6f1ce595d821b08e737839f4b08345186ce99007e18b02d128c6258a846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ac6f91995f146d3484a7d8f09c8d128ecf4d59e4ffd198ce78df5c40de2f6c`

```dockerfile
```

-	Layers:
	-	`sha256:b9177019841b557eff6e5689b50d5ee6364fdc4c44f727172875aecf18f1ccf6`  
		Last Modified: Sun, 14 Dec 2025 19:36:33 GMT  
		Size: 5.2 MB (5248765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74e46029a540bcd5043d20c6d5c2204ed3ce11e083e3b8db478bf845a104932d`  
		Last Modified: Sun, 14 Dec 2025 19:36:34 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:55904a58b45a94ebefefe9bb9280a84adb6c1b315e69d57881e3878e3bb11ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.9 MB (249858558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0865d6ee4b6f9b653950acca79773794db48dd626bee23aeddaf20109d40693f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 22:36:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:36:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:36:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:36:21 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:36:21 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:36:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:36:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:36:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:36:36 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:36:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b5f0b9e88444b3ab53aed4715df75451388c7fc7d5e2bc707f5ff3b36e560e`  
		Last Modified: Thu, 11 Dec 2025 22:37:40 GMT  
		Size: 147.1 MB (147069831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb69f08056be245a689da120276747727d7afcd3c68a9019b81471240ac32be8`  
		Last Modified: Thu, 11 Dec 2025 22:37:21 GMT  
		Size: 73.0 MB (72953288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e40194e46989c45e3ee9ef3fc7522b548c564c07fda28208f8453b7064a9fd`  
		Last Modified: Thu, 11 Dec 2025 22:37:15 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1274084bbf882331a9c495841c7fc9cd694a79f476909d6c4098d1f5234c81`  
		Last Modified: Thu, 11 Dec 2025 22:37:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e91ef6905cea054cdeedc63ef283950a302a94bddee580c10fc2be2ecc61a73f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57d583ba3a3fef014f11ad29cba701d45a00d0961ff814fec0acce9fbbdc768`

```dockerfile
```

-	Layers:
	-	`sha256:a52da0dc0d4bbb593cc43abde64190ad77bb022ec30aa47b11a98622b4c6f3cb`  
		Last Modified: Fri, 12 Dec 2025 01:43:16 GMT  
		Size: 5.3 MB (5255225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df895bf8e2764d49d923f59bd9cad25818d63f7cd744db7d634c4f8b41f8e4aa`  
		Last Modified: Fri, 12 Dec 2025 01:43:17 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
