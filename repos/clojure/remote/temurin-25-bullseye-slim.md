## `clojure:temurin-25-bullseye-slim`

```console
$ docker pull clojure@sha256:a762507faa29ef3d9e9b350332f4cef582ae6d3821cbe9583811267735f62af3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:689e3b98f6540e14a042054c27e8e36fa8b0829ad7df2fceee9e70696d236e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181447258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37481f521c2b7ca8a4294285ee19e0adababc1f1d211a7c55b7568bb0ec5a15d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4eb1dd59a73886acc6a3cc9d4c8f8e66d1fd6ba6d6195b05ce21c22b0658aab8`  
		Last Modified: Mon, 29 Sep 2025 23:35:18 GMT  
		Size: 30.3 MB (30258363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a93b62b063a13ab97de40a1aa40c279a08c9851d2917cd74062ffc0d9f32f70`  
		Last Modified: Fri, 10 Oct 2025 03:51:22 GMT  
		Size: 92.0 MB (92036049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34814faa7678611f51d04b8f584f18fd6534c47ecd3fce55c5f79ed6521e5312`  
		Last Modified: Fri, 10 Oct 2025 03:51:20 GMT  
		Size: 59.2 MB (59151807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b492e266ecb4a75f5bd2bbf6eb4d2a7f4b1406d32a07fb23f717882461264b6b`  
		Last Modified: Thu, 09 Oct 2025 22:37:25 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fde7095bca527016593e8c206de337b7ac46b1b18eb864df4884c6009dd33d0`  
		Last Modified: Thu, 09 Oct 2025 22:37:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d61e203e5e70ac897f5d581b42d4395a6b353be403fe56ffe6189cf6e9a9f504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae009d7c677c5497656cdf81cb5cb36ed1283c1ceaa7cc8f17f5d7ae6af866fa`

```dockerfile
```

-	Layers:
	-	`sha256:49102869e2171533834d3e7a020794a29a9a9d6f507c83017461021fec71cf73`  
		Last Modified: Fri, 10 Oct 2025 06:47:30 GMT  
		Size: 5.3 MB (5261037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43a0ca732577de8299d6ba0f9f84ffdd3ac616664c82cd986829bd0574bfb7f9`  
		Last Modified: Fri, 10 Oct 2025 06:47:31 GMT  
		Size: 16.6 KB (16568 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:23a6619484f104786a240334381f6f17646903eeb621830fdce0232ee56ae01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179082324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2669ce46fcfa6d82b61dfa83c05e604f3c39cf5989468603e6b08c979f67b7a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:93b0b88e50eb7468103e583a7be2e8ee3fe5f86e6c74df4baca40a3685b5eee1`  
		Last Modified: Mon, 29 Sep 2025 23:34:34 GMT  
		Size: 28.7 MB (28748427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f515232feb536832f99b5caed361b667d090e2839288036f1bc220d0a0cade3`  
		Last Modified: Thu, 09 Oct 2025 22:31:23 GMT  
		Size: 91.0 MB (91045212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dda96a14ca863131eb54f30cccb001b45dad328d4f5e401fd243dfd070ad6c2`  
		Last Modified: Thu, 09 Oct 2025 22:31:21 GMT  
		Size: 59.3 MB (59287643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc33792a8ccc7ed9ec5bbb9a6f1d45395d8a4a4a7ac8124e99747b852ac3e87a`  
		Last Modified: Thu, 09 Oct 2025 22:31:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e5f70baaa97e85acafac19982cdf1efac7127bc89913c8eb0508f6cae2ec3e`  
		Last Modified: Thu, 09 Oct 2025 22:31:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:881ce128771f86ad810472f3540d931d3136fcc6149c8159e185fa2ceb8006c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5283500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf155d8a21eb695ab5405114dbd408e741e42839b40d1012c9ecc63ebdd39929`

```dockerfile
```

-	Layers:
	-	`sha256:43a79be3b4ac9f490f57b8f99be354938aa6fbbe2fafb98909d6f0ca3e2ec170`  
		Last Modified: Fri, 10 Oct 2025 06:47:35 GMT  
		Size: 5.3 MB (5266790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3050cd7b1cce328ca47be2981df20b3dc4b192bee4332299c5f138d0cecbd9a0`  
		Last Modified: Fri, 10 Oct 2025 06:47:35 GMT  
		Size: 16.7 KB (16710 bytes)  
		MIME: application/vnd.in-toto+json
