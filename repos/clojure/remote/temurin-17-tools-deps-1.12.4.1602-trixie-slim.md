## `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim`

```console
$ docker pull clojure@sha256:beeb36b7f50243d53371937bac381c86f2595bd66284863210e73b4c33899db5
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

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3b604b59b0ff2d3599164c6b457290cfc8a6e0706996603ca45c519550b97df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247402410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a186ec081408bf7c7e40ef585a36149d36550ec53881ae9e6037c805be44788a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:55:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:55:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:55:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:55:18 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:55:18 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:55:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:55:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:55:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:55:34 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:55:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e063e6e49615f7a5574c3eb139386789087166d9e1f60b2cf3cb655881f83e7`  
		Last Modified: Tue, 24 Feb 2026 19:55:55 GMT  
		Size: 145.6 MB (145628716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44086dab13d013e7222b245e8ea34f4547d51000c72425763551f7255ba8b3b2`  
		Last Modified: Tue, 24 Feb 2026 19:55:54 GMT  
		Size: 72.0 MB (71994021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df919d28368af3a30c17e7018b7dd2c0e9bd1b80ce772a81423c27bf1b88a344`  
		Last Modified: Tue, 24 Feb 2026 19:55:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb103d80d81e8cfdd901bef51d9dc09bff8a90c80a10c29dad9eb67845b41b4`  
		Last Modified: Tue, 24 Feb 2026 19:55:50 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4610bd79c4065d77eec1ba4979d0a3969cb7f8736c850b6613b4a369d2d40d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bd45e685f6a1816cea2cfd74e9b38dd2d737eff94f252e97eb76bc0cb29d31`

```dockerfile
```

-	Layers:
	-	`sha256:8a00fac21784ef906f222e6150a22e41c289c5a3c7dda56db5982fec9503f820`  
		Last Modified: Tue, 24 Feb 2026 19:55:51 GMT  
		Size: 5.3 MB (5257551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0735a14b7946c68415f55dee75b0c699f209b3708ddb4c796024d6b536c9201`  
		Last Modified: Tue, 24 Feb 2026 19:55:50 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b194b2e06eb9bb450119707b163e074dcae5d7f8bf4b108fe98f5a3214d4a940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246385470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b5cc523453d3d3b17c705360d627515b9c7df85ecd76a9e848eaee6cb9e4bc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:06:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:06:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:06:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:06:01 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:06:01 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:06:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:06:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:06:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:06:19 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:06:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be33b841005118b59a7e12d2bac78b2346ecd05133d16ed3b21f62309455ded`  
		Last Modified: Tue, 24 Feb 2026 20:06:41 GMT  
		Size: 144.4 MB (144436218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c595c67dfe9f81a6b1c2079ae9cf6d63f04a3a3983516e49c72c75d2f68cc4d`  
		Last Modified: Tue, 24 Feb 2026 20:06:40 GMT  
		Size: 71.8 MB (71808114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab006694edc12d601756e1e45e03e5c396979943fcdea6ff83a8ccee523c2d32`  
		Last Modified: Tue, 24 Feb 2026 20:06:37 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5049c33d948d5f25b28d3fde9c3cfd7da2be92b56a26046f3020b66444801c85`  
		Last Modified: Tue, 24 Feb 2026 20:06:37 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4d24f5f285b1e8e519fb7331b9be8265e2c82c033ada6c81ef9be90e202dbef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf3d40de7994a6c86bd509be18680212258f5150819cb7e7d2010c62ec29a5a`

```dockerfile
```

-	Layers:
	-	`sha256:69d9c7f03a32e8e5ea3e5f05037cab412d1ddb67dfeef2fe6127ff3de1d9af17`  
		Last Modified: Tue, 24 Feb 2026 20:06:37 GMT  
		Size: 5.3 MB (5263320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d962dd89f76e9b88de1c0b97542f7842f28ae04f90b9b6aeb008f86c0693ea35`  
		Last Modified: Tue, 24 Feb 2026 20:06:37 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:a2c4c8bafc07f5b0eb9e258177f62538adff26b378685aace02ec2a339004bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256446853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d2560cfe1c025f4145c94ae0c4ee4d2fc8b9f608f7f83535530e088c2fdb3ea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 01:59:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:59:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:59:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:59:46 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 25 Feb 2026 01:59:47 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 02:04:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 25 Feb 2026 02:04:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 25 Feb 2026 02:04:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 25 Feb 2026 02:04:51 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 25 Feb 2026 02:04:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c93d40c272f62556f73a8f185bdb3534d9d5498e1326e609b9e0d6c7e31c711`  
		Last Modified: Wed, 25 Feb 2026 02:01:21 GMT  
		Size: 145.4 MB (145438250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092ff1b4da2f60cf70fde1b6e5c1da49887cc8c5c00ff57d874a25d22ea12ea9`  
		Last Modified: Wed, 25 Feb 2026 02:05:31 GMT  
		Size: 77.4 MB (77407344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cf7d1d5a4888750736d72989202bd1ee2f432883593a3a8e59bba3c5f32352`  
		Last Modified: Wed, 25 Feb 2026 02:05:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f6cf50fdc03826f51ecf56f9d5a48e04dd3f697a8e148a7046c53e94f8a7cd`  
		Last Modified: Wed, 25 Feb 2026 02:05:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:63d796bdaf12bda67435929b799fb8fcee9afd0a7e1e3a830a5244c2455b4468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce7e385dc1bfe4e522e675cdb699bd40b9c02a220edb6b38263b51b92985ad6`

```dockerfile
```

-	Layers:
	-	`sha256:9155f15978ab37e60c2deae7108c635cdd686fa6560aa1623082cb204eb77190`  
		Last Modified: Wed, 25 Feb 2026 02:05:29 GMT  
		Size: 5.3 MB (5261922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23e4548325463d3d51a4be05fb9177f4a322a065a19a09286b428ec3962e8eba`  
		Last Modified: Wed, 25 Feb 2026 02:05:29 GMT  
		Size: 15.9 KB (15859 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:1f484cbeb0adcfc5072663e7180e41010ce0e11f96e061becbd605dfa123e162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241819194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72488fbbe823a78f36f5883d38079d2a2d2dee0f7f988f65b2be24ac7ed1e0f8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Fri, 27 Feb 2026 21:27:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 27 Feb 2026 21:27:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 27 Feb 2026 21:27:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Feb 2026 21:27:32 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 27 Feb 2026 21:27:32 GMT
WORKDIR /tmp
# Fri, 27 Feb 2026 21:44:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 27 Feb 2026 21:44:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 27 Feb 2026 21:44:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 27 Feb 2026 21:44:01 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 27 Feb 2026 21:44:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09e3a601e9732dcc8a0f82d761fe91f0f721e0c071867bcb2447d017285e0fc`  
		Last Modified: Fri, 27 Feb 2026 21:33:20 GMT  
		Size: 142.7 MB (142663031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d6dbd491e2e5c5f21b290d268e80d6d22f1aeb620004a6aa04708ad0e2127b`  
		Last Modified: Fri, 27 Feb 2026 21:47:47 GMT  
		Size: 70.9 MB (70878703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16590c37fd4153e047baa268683fefbe5594a416217b7a12d657ae03c28a9b0a`  
		Last Modified: Fri, 27 Feb 2026 21:47:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e716dbe33cadd6f3afba93bee976c0511da6576353d73e9c1e2e457f95d159e4`  
		Last Modified: Fri, 27 Feb 2026 21:47:36 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bee64d9eeec0324aea4bc810b1d8f09d9e354adcd7e160f0dc3bbff0bcdea525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5260956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:879183b5a95742299e43ac2fca1c3b8e0f5da2048fb47d1ece2617a5c6c525cc`

```dockerfile
```

-	Layers:
	-	`sha256:5752f774b1ee3f0b614578d437c138aa9024176ed0f2ef617e67f17382748461`  
		Last Modified: Fri, 27 Feb 2026 21:47:37 GMT  
		Size: 5.2 MB (5245096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d91b848a40284d8ef42f3100ac89256fd7bb1b0457bfab8603972df774dba8a0`  
		Last Modified: Fri, 27 Feb 2026 21:47:36 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:6991626fa58f4aea0567b6c70b86987cc633b1fe1bf8afad128a192468e19e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.4 MB (238425729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ffeaa52714573f1896ad7be4d04d96dd25a96f1868b65a1aa0418165f74d90`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 23:18:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:18:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:18:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:18:44 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 23:18:45 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:19:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 23:19:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 23:19:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 23:19:21 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 23:19:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67295a4cb07008304f03069ea30b4d5c6464cdcb515ed616ceb1c17202753dd2`  
		Last Modified: Tue, 24 Feb 2026 23:20:06 GMT  
		Size: 135.6 MB (135627117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e32cd3e96b249180a9558c59e81533bf958f2a76b46beda9877236c772542d5`  
		Last Modified: Tue, 24 Feb 2026 23:20:05 GMT  
		Size: 73.0 MB (72959395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453952bfe244ec565c835b82f3f78fbaca800487dc5952efd0d7748727ac26f4`  
		Last Modified: Tue, 24 Feb 2026 23:20:03 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a0993e6c64576753ad50a7fa75a6e7b6630873acfae81b88126c7761d5e560`  
		Last Modified: Tue, 24 Feb 2026 23:20:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3a0da213d6b27ba0a2e1347b9ffca178c03b7e7f9acf0f0f0a82ac82d8d068f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5269287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d70f1425cff60b87c883f27894546956f6af71f3ccdc14f3c7d9bfd4fb08fe`

```dockerfile
```

-	Layers:
	-	`sha256:1b9d681dc0bf1b57cfb37e892a1ba2dd8b3e3aba99ab84a25033ef33bfee1437`  
		Last Modified: Tue, 24 Feb 2026 23:20:03 GMT  
		Size: 5.3 MB (5253475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6db95f167dbd76e976f8024d6bf62ec81dfaa0c3e5232fc313c124488697c381`  
		Last Modified: Tue, 24 Feb 2026 23:20:03 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
