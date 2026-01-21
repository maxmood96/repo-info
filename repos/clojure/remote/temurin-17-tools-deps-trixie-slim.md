## `clojure:temurin-17-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:c7333e03cbb0cb705bc390127de067230e18fd1f9f16f2f5d3548c5dc8e69226
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

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a52228de1f0aff586156edf9e123f8208704b470e847b40bdb828e5ad72f450a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246616436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1bc34dd61d97d073f492ae218a66c2f4d604265e3a39d2b3388ea3e0002bf4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 01:54:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:54:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:54:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:54:03 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:54:03 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:56:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:56:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:56:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 01:56:58 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 01:56:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d309b74e4fe01c6f7ef9dc58e0ba4d78fbbfc19e51bf44438800d8d0f3c7ad74`  
		Last Modified: Fri, 16 Jan 2026 01:54:40 GMT  
		Size: 144.8 MB (144847971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc1c50a05becedc23ef1e9666a0cfb481c5ba4d90f6a3a35ca8471e359459dc`  
		Last Modified: Fri, 16 Jan 2026 01:57:15 GMT  
		Size: 72.0 MB (71993739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de6de1fc98951c72a989e9bce90f106ebcd8f96602705b5ec899d5c5d56a569`  
		Last Modified: Fri, 16 Jan 2026 01:57:20 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790f147520de5fdf73f26d7536742752a9fb23c69438d52bc8f23e8974252a08`  
		Last Modified: Fri, 16 Jan 2026 01:57:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:352b023465ba7f78d84722d255f6b1b80bfcf1153ed639213f0957faec6e19de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0032fe8fe35f0414513cf2c2e3a284c8f99d5b8493b910b21e92a619a70ba1cb`

```dockerfile
```

-	Layers:
	-	`sha256:4ce36ded55b7bd738b32898960b4f168a688eea95b21cf9e47716a3e3bf70007`  
		Last Modified: Fri, 16 Jan 2026 01:57:13 GMT  
		Size: 5.3 MB (5256297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99fec19b98b7f0921afb53c82ce37e3eb6e2f227f11578ac3a6f34ffe40da426`  
		Last Modified: Fri, 16 Jan 2026 04:44:23 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:10775cc4ace453b1e8637f582497e1fa621972b7c1447626417ae991f6c57ce6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245621356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d00f6ac89130ec8fe85f9e71c6c7258d5d9667861c020982dbcc95d0774878`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 01:57:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:57:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:57:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:57:52 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:57:52 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:00:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:00:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:00:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:00:59 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:00:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f4b336c8bd48a2d9728ec53b08d9a0b836219567bcfb24f7bdba74f8005b84`  
		Last Modified: Fri, 16 Jan 2026 13:15:37 GMT  
		Size: 143.7 MB (143679963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9856f4534a09574464d8534ab359d00424b7324fe47d17c70b2a684427d4408a`  
		Last Modified: Fri, 16 Jan 2026 02:01:18 GMT  
		Size: 71.8 MB (71806309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fcd8276a47c19cacc15c1fa1584063bbee88e5cc3c024d705ba725c5e8d8e2`  
		Last Modified: Fri, 16 Jan 2026 02:01:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f77656823e4ae1116e0e7a628d7919dbd3c8f38d121e529d3c5052a59437857a`  
		Last Modified: Fri, 16 Jan 2026 02:01:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e645cb5ad57f02a81b4ac1f19aa5f1e2539ffb3cbeee009f77ef90cc6e244541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaaf2cf7d16f7dca0b35f2c3ceef54c4a649181ff97f33101e3cdfd28e91bd08`

```dockerfile
```

-	Layers:
	-	`sha256:98f93d55360516c048b02dcfcbf78cc9cec0ff6cbf614e3e7e89b07b08b2f414`  
		Last Modified: Fri, 16 Jan 2026 02:01:16 GMT  
		Size: 5.3 MB (5262066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c41da971c51f6d680fd4eea0a8d582e826f970e052330635b0cce9ae8a7ba9d4`  
		Last Modified: Fri, 16 Jan 2026 02:01:15 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:67068bd8ccf0b481eacc79d75b257c06cc6bf6153d59ac777d15785d25582534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255511836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc375b7cc550df8be75314057bea5fcd85fd98430859dfd822ceaf08dbaa22c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 03:16:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:16:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:16:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:16:27 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 03:16:28 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:25:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 03:25:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 03:25:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:25:24 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:25:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6bf15ee3631779c5e8a10fa679c64130a5b54ad0969e061ffe1b160beac0d5`  
		Last Modified: Fri, 16 Jan 2026 03:18:34 GMT  
		Size: 144.5 MB (144524715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff9c46897612400ce3e82bf32f5bb36836b35c83661205d15ea6617ac4e6252`  
		Last Modified: Fri, 16 Jan 2026 03:26:19 GMT  
		Size: 77.4 MB (77390476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1f914461ea8aa5c8074b67ea456204aa6537b1b3c47040a701098c2c740a3d`  
		Last Modified: Fri, 16 Jan 2026 03:26:15 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec73fdf928fc21f1c5e62bd27392f774a541c5f4a7ab6a6904ab884032c60553`  
		Last Modified: Fri, 16 Jan 2026 03:26:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d573c0eb9083851e5c948763e39e9041c85d02c104b6b976d9bc5938164567c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e65d7bd5942ddadf1bdb337d517906306ab0933511a296f02acb6750ff3c81b8`

```dockerfile
```

-	Layers:
	-	`sha256:15c5cbde983c95bb6bad727f01794dd3a99d5c078cc53dfac4679210abf4c476`  
		Last Modified: Fri, 16 Jan 2026 04:44:35 GMT  
		Size: 5.3 MB (5260668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e8f87a9b0467e82e4f6e4140efec0362a3c7f5d06c77c337b681e41cd4b38d3`  
		Last Modified: Fri, 16 Jan 2026 03:26:14 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:e6bad6d9852e3d6f80f8fffc573c53280c53705184f50c921d552a9927ea615c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (241041662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399ed849df7879a3e7eb4bbaf5c152df3283cffd3f7f2c2e3d38ae87fc296a68`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Thu, 01 Jan 2026 06:35:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jan 2026 06:35:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 01 Jan 2026 06:35:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jan 2026 06:35:03 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 01 Jan 2026 06:35:03 GMT
WORKDIR /tmp
# Thu, 01 Jan 2026 06:51:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 01 Jan 2026 06:51:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 01 Jan 2026 06:51:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 01 Jan 2026 06:51:31 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Jan 2026 06:51:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:14 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c47e4b223479384cb91259f631c9c203246ef873e850a7fe5e6ff70d31329ee`  
		Last Modified: Thu, 01 Jan 2026 06:41:38 GMT  
		Size: 141.9 MB (141889571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cc585b93e3e20213957c5dd5b3c125d9945ffc7e093bb3d9c1d7310d9f83ea`  
		Last Modified: Thu, 01 Jan 2026 06:55:18 GMT  
		Size: 70.9 MB (70877919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0318aab2d926170901cae285fb051c89b7e991b70613cd4d507d97ab1e6988f`  
		Last Modified: Thu, 01 Jan 2026 06:55:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc085b40e88e8dea55a124943f2d673a3dd08531d24d2acca86b2c4f8e8ff4f7`  
		Last Modified: Thu, 01 Jan 2026 06:55:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d3dea53c41a2b97ea1523520a593c030046b6afdf7c6539e1fa5dc290c0c96a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102b8347d7500724ff5d38fa530575b12081d3e4e194c77c8216ec85e83d6954`

```dockerfile
```

-	Layers:
	-	`sha256:be273a0a4b1417e10c88eb9076044a523213af56f46dee41ccf576f30260b74b`  
		Last Modified: Thu, 01 Jan 2026 06:55:08 GMT  
		Size: 5.2 MB (5243744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6aa697c888d64aa30032972e268c86352ca7806002c6ffb539f54d29d0641a35`  
		Last Modified: Thu, 01 Jan 2026 07:36:01 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:03c28e8fd7b1196b8b9ec588b705de3ad52ed010bc6c7ba30abc79fd4dbd95a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.6 MB (237646277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8beab5cb6fb019b16a960b2a51471886f941ace410909529cbec49b017390ba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 23:15:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:15:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:15:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:15:43 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 15 Jan 2026 23:15:43 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:17:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 15 Jan 2026 23:17:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 15 Jan 2026 23:17:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:17:36 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:17:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:27 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee861ab10085b97ec9d76bda4b5655283ef0733479ff9f05457f5ce5423d4a64`  
		Last Modified: Thu, 15 Jan 2026 23:16:23 GMT  
		Size: 134.9 MB (134859759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a6eb2f75b51a710368a6867b4119416dd02869a481cf6802414b7ebe157d8c`  
		Last Modified: Thu, 15 Jan 2026 23:18:09 GMT  
		Size: 73.0 MB (72952068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daed60f17aca4d203357b3d091e21aa8c1063ad58ca7fec749b0d38b7190ddd9`  
		Last Modified: Thu, 15 Jan 2026 23:17:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23c449f974d28cafbe462a60eefc2c6ddb16b430a6373d0a0cc77986a707657`  
		Last Modified: Thu, 15 Jan 2026 23:17:58 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7942541311fd88205ae7f32deda96edd80858ff0e9caf19a0584104e23bce34e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5268033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb141d59ffa922f75283e6ef8f59d6e800d3c617fa88bacbdd82b76fc8754e5`

```dockerfile
```

-	Layers:
	-	`sha256:a041f5ae9a4fe6121405d0fd6c03bd9e8381e55dbf50b0e784baee4abd5cb13f`  
		Last Modified: Thu, 15 Jan 2026 23:17:58 GMT  
		Size: 5.3 MB (5252221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ea5d9a14ff7d771b37dac55b7e6769e381fae4254626e4f8c7c72f824c3ec4e`  
		Last Modified: Fri, 16 Jan 2026 01:40:51 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
