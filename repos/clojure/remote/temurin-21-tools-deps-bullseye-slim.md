## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:ac5d18cd084f40adaf1555f8e3047a6554b859b37fc50c41d3e5185c67aa8eff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f104dc70d8b33e08ac30f7f0d5ae879bf9ce4f0b8e4f60e2c644403188ad9b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247237652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780db74a075e5b367fb20d2a6aed13d92afd59bf1f14d95284079ae3fc86ae75`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:55:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:55:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:55:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:55:07 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:55:07 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:55:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:55:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:55:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:55:22 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:55:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a88499d92e58a9f7d74dc939bd949d9c2d87abbbaaec03b5f87553e69d901a53`  
		Last Modified: Mon, 08 Dec 2025 22:17:50 GMT  
		Size: 30.3 MB (30258465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f2b9218dc0233b915438883af5a76ff91a31ccf3ab0fdb1875f3f7f7a7bd00`  
		Last Modified: Mon, 08 Dec 2025 23:55:46 GMT  
		Size: 157.8 MB (157826042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bbd7e58f090dcafd3e0c880b3dd5e090ecd8d75fa100be0ecae4445cbcfc9b`  
		Last Modified: Mon, 08 Dec 2025 23:55:54 GMT  
		Size: 59.2 MB (59152105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c510155890ae3cd5c36b218aa3a9bc0e6205869b3125904bdaef95dd41cf7406`  
		Last Modified: Mon, 08 Dec 2025 23:55:49 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c74d860c8269e01b74c16c8ba80aad0a3064673eb17df0e119d05047033b36`  
		Last Modified: Mon, 08 Dec 2025 23:55:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c7a0ec057236e3db5d664fd29b8dd51a6007a026d1bdfde01e10d47d12044ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5327007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ada906972ccce98587d2f36722401a3aedd29276df77a795629076534648acb`

```dockerfile
```

-	Layers:
	-	`sha256:2fd0c4d11d71e9de9b3b521a35df39824076c5af248a10f617f54c31d2213702`  
		Last Modified: Tue, 09 Dec 2025 04:42:40 GMT  
		Size: 5.3 MB (5311171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06df11ccd7d960ee6ffa731afab5e2ad8d5fbfdd927a649d7dda7906a48b2d0f`  
		Last Modified: Tue, 09 Dec 2025 04:42:41 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:02b098e1d6adf07a3b80ffd40601c3e41f9dd70cb1ece17e814aa71242bcd799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244144823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7deff88a2bace8e50bc157bc3e5523c8896e8667fc5080bd742f9667ed6e0574`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Tue, 09 Dec 2025 00:02:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:02:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:02:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:02:28 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 00:02:28 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:02:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 00:02:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 00:02:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:02:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:02:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7d43510e20279c4831f5ca1d424a1d56c6c24251d7c93288a50a066dc7e72bda`  
		Last Modified: Mon, 08 Dec 2025 22:16:06 GMT  
		Size: 28.7 MB (28748482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd40b78786b442189f6b8ae55c3928e90c79e2370e3d10c55d66c0d25e61f38`  
		Last Modified: Tue, 09 Dec 2025 00:03:28 GMT  
		Size: 156.1 MB (156107654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fce308b1f6547caa43bc1c4b87685ae75f5ca44dc33de4a767950d8d46d6ce`  
		Last Modified: Tue, 09 Dec 2025 00:03:18 GMT  
		Size: 59.3 MB (59287648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25427074e8c1051b22e5cc5902b2286ad7428f6c75061e0862bcf2d89e7d6c70`  
		Last Modified: Tue, 09 Dec 2025 00:03:10 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb37b353669027e8c851d1bf0b16c8f755dd54d20ab00c63637b372a0bee5af`  
		Last Modified: Tue, 09 Dec 2025 00:03:10 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6515bd1b736103c1d4160c2ac96f1efa065ce88cd9874494bf3aac6c73c8b5db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5332856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f87e7082090ed7d1e18498a55a662eddbefc3f27662216aa07eca140a38d2e0`

```dockerfile
```

-	Layers:
	-	`sha256:aee3cfe429f29a2eefbebdd015ac42a8982a79b418f6c5608d31b8676b694aaa`  
		Last Modified: Tue, 09 Dec 2025 04:42:47 GMT  
		Size: 5.3 MB (5316903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d4896e17f3835597f0ebbdb691998ca6979bee093d96b99a8e531534e905399`  
		Last Modified: Tue, 09 Dec 2025 04:42:47 GMT  
		Size: 16.0 KB (15953 bytes)  
		MIME: application/vnd.in-toto+json
