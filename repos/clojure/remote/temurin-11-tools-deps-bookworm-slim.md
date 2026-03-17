## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:2637d4c047207786e68a0cc5f576e751d87a32b942ca463d2cc186e9acaa4889
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

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ff4f67f2c3320b79d8ba80495993224c8b5f09df1dce0eb27ac2f5747c9a7391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243745289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cbb87fdc9aaafbb3521838e1a110671e7bf33499f5111fa3e62533e2673c546`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:57:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:57:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:57:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:57:18 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:57:18 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:57:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 02:57:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 02:57:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9d947a4ddbd004f6a81a71f1e541b7a2b5349b44a91e343ce419d5c46bd7d2`  
		Last Modified: Tue, 17 Mar 2026 02:57:55 GMT  
		Size: 145.8 MB (145806912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23200fd5e4a18440a1954fecef64bcaefecc642f064d17b9bebe32e5fc7dce72`  
		Last Modified: Tue, 17 Mar 2026 02:57:54 GMT  
		Size: 69.7 MB (69701509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6328f10cf3ec65a52277d3f740a8e718de095b3aae744bf2a1c24014140c15a6`  
		Last Modified: Tue, 17 Mar 2026 02:57:51 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ce3b2cd9ff60ed2dde32be5c4f8c84779187eb6035d55f51374a3d8eca5bb346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68eec8d848372811790caee3c60aa40ae5250f3bc3fceaa033fbc6d5b7e79b1e`

```dockerfile
```

-	Layers:
	-	`sha256:acda66fac1ce607111569085e199c9e431258e452663013b583926711246f8ad`  
		Last Modified: Tue, 17 Mar 2026 02:57:51 GMT  
		Size: 5.1 MB (5136308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5f3cfa77b02a214a5a88f8f2086002330e1b0c426b3343b94a4fff654bb9921`  
		Last Modified: Tue, 17 Mar 2026 02:57:51 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:60c266d21b30d3b947149bc34b35aad9dbc51b0ed38a580a6b27c87ef4b70b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240305429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f9ea659bcf5efc4d0a84d26ef4d6171d8012dec0fd9856e5d4b145ccca44fb`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 03:01:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:01:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:01:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:01:43 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:01:43 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:01:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:01:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:01:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9c398627859f76a393595822c959cc160f7df27236cd6a5ffe13650d6dd5a8`  
		Last Modified: Tue, 17 Mar 2026 03:02:22 GMT  
		Size: 142.5 MB (142500002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9d784db381a9502c9bd7251d763f3aae01f1e5a3b668041f9a8edc48496793`  
		Last Modified: Tue, 17 Mar 2026 03:02:21 GMT  
		Size: 69.7 MB (69688720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fac8b992bc3aa54822bb59e088f6fc4e4ffff01426beaaa9fdb8b22f52d55f6`  
		Last Modified: Tue, 17 Mar 2026 03:02:18 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:12dd9b12d8ac6da805c1c12dc7030c8ca18768e7e9df6692bf905aa9267c0b80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5157071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ce7b7ab6e15bd55aafcf69d9cdc0e6cb240742c4334d7724b364d0585ae3f8`

```dockerfile
```

-	Layers:
	-	`sha256:a815d17cdf9f8b3cfb2d776bc13ccbe165d61e731ff8954978399cbaf24963f9`  
		Last Modified: Tue, 17 Mar 2026 03:02:18 GMT  
		Size: 5.1 MB (5142687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8423c6ca99a772863e6ca04191364339212855397c3b060dfd4ec7fd7a00061`  
		Last Modified: Tue, 17 Mar 2026 03:02:18 GMT  
		Size: 14.4 KB (14384 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:89066c87df3d91e93e24dd37c3d31462cbe3d799abbaafbf67ac25a8563fca72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240610225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaac2c212390547dd7cfae139e1f69452715a34682287af8732b229c20256863`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:46:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:46:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:46:08 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:46:09 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:46:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:46:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:46:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07635c2a81b963c59cbf4e59ddccd52bfee62c195984683505beb6f3aff0b8fc`  
		Last Modified: Mon, 09 Mar 2026 20:47:34 GMT  
		Size: 133.0 MB (132997797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de96a720d12f06f9fadd7af40c23312c705ed75aeda3fcd795bfd0f8498f1da9`  
		Last Modified: Mon, 09 Mar 2026 20:47:32 GMT  
		Size: 75.5 MB (75533449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8d88f340ad4cb5c6d70c760d0256d56c3c75c47c965fe068ecaf0fe0a8bd23`  
		Last Modified: Mon, 09 Mar 2026 20:47:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5df745b09e847fee79d8861c47ac9de7e47d4fae2b7751432d340ce87407d839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5155166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29cdf50f2c1432f0fab576312617cc031112c7b15d3d181b8eb9b873ed8d7db`

```dockerfile
```

-	Layers:
	-	`sha256:407e8dcfd71bededdb56a659d5f0f29da370a667df2bd867b4a4ac7fe9d57a41`  
		Last Modified: Mon, 09 Mar 2026 20:47:29 GMT  
		Size: 5.1 MB (5140851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b466036632e36d0384394301c9f20d8ad38bd6546922235c6a27509e6822fdc`  
		Last Modified: Mon, 09 Mar 2026 20:47:29 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:73357869a4719bfb3b3ad868c7f515d1e96c1f18629212059e6bbd50247c4574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.0 MB (221967994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa1e19ede347559fe477df8b0a8cf3fb83ec0e3d36da9990a49286fed6e1995`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:32:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:32:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:32:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:32:13 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:32:13 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:32:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:32:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:32:31 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78455097ab053fd4a095369b6037e8270ed42dee2c12d398c3ce66f2d955316`  
		Last Modified: Mon, 09 Mar 2026 20:32:59 GMT  
		Size: 126.6 MB (126562061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3392d179574653d939612370537b737ff49d307e01bec020c02897eef0748c35`  
		Last Modified: Mon, 09 Mar 2026 20:32:58 GMT  
		Size: 68.5 MB (68513764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48cb70fb717bfa2edb74de6384e733afdc2169bb09b9dcb16b261d5cc1893ed1`  
		Last Modified: Mon, 09 Mar 2026 20:32:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:102c31d548276908d643b2b57f869e5b052884b6cc921e50750ac48d994678f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5141900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b03617c7c3a02987b5573b1be9f18e0265dc48d93503f4a9e54d3e564ebcec`

```dockerfile
```

-	Layers:
	-	`sha256:28bae32112a7a48f11adaf5c39262ba36431376b2a9ef42912ad2b285305a5ae`  
		Last Modified: Mon, 09 Mar 2026 20:32:56 GMT  
		Size: 5.1 MB (5127633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac683156d89805e4b153812724d649cc8617b1d01d55ebafd1524fe3e672e593`  
		Last Modified: Mon, 09 Mar 2026 20:32:56 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json
