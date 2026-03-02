## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:2efb75794f53931a6bc4ed518fde8c9e159b548b58382e00e6d8bdcdf8dbd7c6
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

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:538cb4624d01489045500649663228d6c18a943e1dbe05ddb35c18d1696d23f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255785366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2823ebc1c580061a1f9d3bade38fa3efe956e2ceba0960b6c81b4ffb2aa3e804`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:47:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:47:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:47:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:47:31 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:47:31 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:47:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:47:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:47:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:47:45 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:47:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6731d0c1bf5585ca2addbd55a8b84edb697583f73eda88c6e87d00133fe21fca`  
		Last Modified: Mon, 02 Mar 2026 19:48:08 GMT  
		Size: 157.9 MB (157857124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4605402486e52f0faca96b0696bf3fca47cb3cef282a71a924e99a68558e3a25`  
		Last Modified: Mon, 02 Mar 2026 19:48:07 GMT  
		Size: 69.7 MB (69690922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75d22dac5bfca32d0795566743027c311ad3389696effa0954ef14b441954ba`  
		Last Modified: Mon, 02 Mar 2026 19:48:03 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a898368cdef14fef9c27d175a41000d8d910af74daa5449a86d777a6d98857`  
		Last Modified: Mon, 02 Mar 2026 19:48:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2b91c075311fc03a01f0a7f27c326189a64c6199375cbb57fc40a7100476ff26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632201fb636a951cde1ca32ea61bd5c9031f6f28a48d1da1267eddec03557b78`

```dockerfile
```

-	Layers:
	-	`sha256:71507df54ca2bf9f93fb4c977a9b726f386ecc2109cb40b850fd68649911ca32`  
		Last Modified: Mon, 02 Mar 2026 19:48:04 GMT  
		Size: 5.1 MB (5118019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a064b4b2086bc437064063cb16a13d903c3f6e0bc4989b084f084fe3a14700c`  
		Last Modified: Mon, 02 Mar 2026 19:48:03 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f2da0a77149079bfbb1774e325000730d50805c8af463eabf15d59f84b6874fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253938221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5484deb0fe4069ba3c3203f346797831918d0812d5704808303a8aa00131f12`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:47:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:47:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:47:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:47:27 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:47:27 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:47:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:47:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:47:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:47:41 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:47:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a16609b8ef7e33ae52ae2495151fb109caad6bd5559fc33e69ed482841f6ed6`  
		Last Modified: Mon, 02 Mar 2026 19:48:04 GMT  
		Size: 156.1 MB (156133063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47335a6dae746f5374e24286d8e026e30cadd452643e1a3c45850d5816afbd47`  
		Last Modified: Mon, 02 Mar 2026 19:48:03 GMT  
		Size: 69.7 MB (69688036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d38e6490ed698166349eaf5a395f4c0538c83be90d744b73b89bc9be7b12e3`  
		Last Modified: Mon, 02 Mar 2026 19:48:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33c0d45b0ea4b5451edc3bff2c8acb18f59aa50d2f41df7acaeedae44d5f5e0`  
		Last Modified: Mon, 02 Mar 2026 19:48:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:209f0051eeb01dfd1031a13d4a37969571e7786b6a7238d55de322cb754071ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcecb4595007574888c6143dca2e6072117cd904efa144e76fb0db13d5d0cdb9`

```dockerfile
```

-	Layers:
	-	`sha256:5d55e8555831638c4cd4390a690f2a2f935f0fc6ccdd2380029742375b1bd04e`  
		Last Modified: Mon, 02 Mar 2026 19:48:00 GMT  
		Size: 5.1 MB (5123780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b4b9fdfe611a246e48951f39ed888be56756bd4892b5d53f58ba9162248688c`  
		Last Modified: Mon, 02 Mar 2026 19:47:59 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:993869b4a6284419fa179b3dd971888e3d9cf7cb21797d833face4494edc4300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265584848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:148ea745d041686fbaf9057006d94d5917ae56a27929602b8d4992147cefe269`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 20:01:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 20:01:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 20:01:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 20:01:55 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 20:01:57 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 20:02:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 20:02:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 20:02:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 20:02:49 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 20:02:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b28f3d67b5fc2c007cc7e3cc43eb565bb392b55d28445ba48a426744bc2eac`  
		Last Modified: Mon, 02 Mar 2026 20:03:34 GMT  
		Size: 158.0 MB (157977552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1042e320408edd8dcd0c725a350b21120eae2fe64c80691018f4abb4b293f77b`  
		Last Modified: Mon, 02 Mar 2026 20:03:32 GMT  
		Size: 75.5 MB (75527917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c12493876ec73ba7fc9052f982f0735445110baeaac831b74ec15c84e9a5ab`  
		Last Modified: Mon, 02 Mar 2026 20:03:28 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6818516e6e47b731616283c96d5f7313872695aced516cd9cdf9dd5ddb38fd`  
		Last Modified: Mon, 02 Mar 2026 20:03:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:db4f6c2c6f0c0c64e6531e1cac8e4c561aa33d8e7da2defd92368e104b0eea1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf951f6b14d1ec6acfe8df503a4261bfc8960c7cf7ab8495cbb6a15c766ac82f`

```dockerfile
```

-	Layers:
	-	`sha256:3fb34de38d3b2ef82302ee0e7b85356510bea5bd28307eb6186eacb98cc4216f`  
		Last Modified: Mon, 02 Mar 2026 20:03:28 GMT  
		Size: 5.1 MB (5123177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f39bc370afecb2f0fedb97e177c6ba01c8d8bd2bd16a4cd9965373ba6e3ebecc`  
		Last Modified: Mon, 02 Mar 2026 20:03:28 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:575cef43ec65b07a4dde6216776b50628cd28db4314b1eecd49b8617f2b3cd0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242501528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:051ef6280ba48b792a396de8e827a4cf82aed8ee7b47a973d75c4e7804f26b03`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:47:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:47:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:47:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:47:13 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:47:13 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:47:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:47:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:47:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:47:28 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:47:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec820ecfcb4a37108d38272c3e23df03d4a3fe7b2fe853c4f6b359033fb5cbd`  
		Last Modified: Mon, 02 Mar 2026 19:48:01 GMT  
		Size: 147.1 MB (147105249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb5ac40849f134d2f106de1a44c234ba6433c1e36e857a95f28383076b080c3`  
		Last Modified: Mon, 02 Mar 2026 19:48:00 GMT  
		Size: 68.5 MB (68503715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1a6570ac13ea1206104b88592745d248eac3a38fa6b26538f38c014f161460`  
		Last Modified: Mon, 02 Mar 2026 19:47:57 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683b0f97c7b699d1387133f346a2f3efc68b17764651ab5fed160ef3ae648bf9`  
		Last Modified: Mon, 02 Mar 2026 19:47:57 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eb3617eea6961547168b22d8424867effd64266ecd97c45b1c079b996e265d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e6092cead7856dabf9293da7edbb57383bde88f6dd38ce02c0890836eb764b`

```dockerfile
```

-	Layers:
	-	`sha256:6dfe43c197ac817a55d8d6789d0bf346f18de22145962ade2e537447124b534d`  
		Last Modified: Mon, 02 Mar 2026 19:47:57 GMT  
		Size: 5.1 MB (5109340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:933288ff18fe4e7795f90bc1f62168480d36de534c97a13576856a5a302db12b`  
		Last Modified: Mon, 02 Mar 2026 19:47:57 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
