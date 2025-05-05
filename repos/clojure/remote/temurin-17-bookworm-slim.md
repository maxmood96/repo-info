## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:1539a7e73d176d75488755d6364ced72da2b3c6f58cb25002cd5fdb11c6493d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8512d9681326bb4492a05c3922641a500122434fbcc5fa26217751600f04b2dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242389436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:092ee15f1707e3c9cb0425e22711834ebf221b89031afcf04fb87b6985217cc8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ca51f8c73c04db6b41b7420d903413894458ccb3ab6a00361f5f27d2476c0f`  
		Last Modified: Mon, 05 May 2025 17:07:44 GMT  
		Size: 144.6 MB (144635023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b70716dda9e4512c85e61acc0d2e28073314132c97b3ce470e31b5576600fbd`  
		Last Modified: Mon, 05 May 2025 17:07:41 GMT  
		Size: 69.5 MB (69525733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3556ab6be4854261903eb041c25b9736c4e52c52ac989ecb4de250c6fe1acc`  
		Last Modified: Mon, 05 May 2025 17:07:40 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4498ed3211c771753eb0992cfc7899d7cef4bc66b6d71d97a9d84d71599186`  
		Last Modified: Mon, 05 May 2025 17:07:40 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:54214937c73830b5d5816b5e39af4ea72caa82b48ccbd625d5524601088744c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4929844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e4958434d56f2cdb22a8bc596ebee75c1835fb5b2dd93c7cc1c6c9126449861`

```dockerfile
```

-	Layers:
	-	`sha256:e093988c8d528b00235863f7f3a1d3055844d9408e86de465afb6266b4ba58d8`  
		Last Modified: Mon, 05 May 2025 17:07:40 GMT  
		Size: 4.9 MB (4913965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c70676a964e17a599ed510239c3d92dde06915245acfbe7ee8a7704521d1680`  
		Last Modified: Mon, 05 May 2025 17:07:40 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cdbd7ae7c057f4f2fd4bd39d1b73972581a88221bd251c2ecaec6d56c97ca0ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240958220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9278acca554769bd04f9e13ee434e396891f01a72fbf0d5c250386616c9a9fb3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a5d985b3f4d44dd9e3980aa8d1129d879603083f1797f6cc92c291529cfd4e`  
		Last Modified: Wed, 30 Apr 2025 01:24:11 GMT  
		Size: 143.5 MB (143512676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958d55786946cbc0283f50247f900782fe1e6c643f79f9078ca1c952d836b000`  
		Last Modified: Wed, 30 Apr 2025 01:34:19 GMT  
		Size: 69.4 MB (69377879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fe1298f2799f541a16d17227d4c1f98d009b88689bc748b55b7938c14e38c9`  
		Last Modified: Wed, 30 Apr 2025 01:34:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a8a9d637dfc5932ab3f0c4b076a5b71fcc25bce0dc0c5d63c58c4d36de9eae`  
		Last Modified: Wed, 30 Apr 2025 01:34:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0a18b7dcd6232d42c0e4fc64dcf822306777571b183bf77073a9d2b34222d1c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4935723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35e322c9a3cd96c8e4cbfe9b04a34103ba163fb6938a1bebe125f191ef2c0d0`

```dockerfile
```

-	Layers:
	-	`sha256:f49330d97a20912cd0837cacda57da28e278995f0facee7dc1e60b0f8f40db6b`  
		Last Modified: Wed, 30 Apr 2025 01:34:17 GMT  
		Size: 4.9 MB (4919726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c3a322dee32d4fcd872f1773c4e22ace447ff126ab812b6a8c3f58d3bc531f9`  
		Last Modified: Wed, 30 Apr 2025 01:34:17 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
