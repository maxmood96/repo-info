## `clojure:temurin-17-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:85075f1cf7ab55cdf9ed3f8dd8b53b5471f59b08b2a2435c1201432450915a4f
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
$ docker pull clojure@sha256:5d71fdf36e06b33a87c335f298a1be9c8970ba32ac0cd7b5999223a04d97d138
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246308228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cbc0cfaf69ad9b3f8b32089778bafb714bc3ab2b273caf1917b88a15615f4c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7be5a063ce2fc05139349ab64a6429356efeb7760960d223ce4f65fef93c25`  
		Last Modified: Wed, 13 Aug 2025 00:21:41 GMT  
		Size: 144.7 MB (144693300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf957bd649ce604de2467a14a4d961b5f13ee43324812fd62676a3853d7ced5b`  
		Last Modified: Thu, 14 Aug 2025 03:19:12 GMT  
		Size: 71.8 MB (71840603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebc37fe6a8d9b0316165fc41205d962c1a93ffcb486f707f96d5fcde6a18139`  
		Last Modified: Wed, 13 Aug 2025 03:39:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a641170a4906eeb767ca245f35e04af555e1e7981639ff5a9b318b02b5121ad2`  
		Last Modified: Wed, 13 Aug 2025 03:39:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5b644fb261403e6bc9eb957dea442ae3dbc7f1d5de346ab6c609214748046f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bc3b9e8a13d66a7f3d8917bc285a1a50b541a24a5d91238f16e48eb7a936b72`

```dockerfile
```

-	Layers:
	-	`sha256:2df4a8a012cf36dec9539ae89492986cd085cc20dd86b8c7d24c09eb963977ef`  
		Last Modified: Wed, 13 Aug 2025 00:38:02 GMT  
		Size: 5.3 MB (5255208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bee492583d4e4ed8987e3925c1b659535b6dd87b4084af8aa719930f4ef7199`  
		Last Modified: Wed, 13 Aug 2025 00:38:03 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:85473827481d46d41b906033668f60f4b3251b0898c253da7f8012a24c631ca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245342990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce6e41ea5582216c9cc007b432b62dd7079b9ea600b473141df6816038af3d6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b7ea60e474b1ec8ccad21cf85000efbe5a968f46282971acdbfc861b567272`  
		Last Modified: Wed, 13 Aug 2025 14:25:17 GMT  
		Size: 143.5 MB (143542152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c9fb3fc6942e71f81d03e3e9cbdc9eed8983423ae0779f692fcca6fcd1b7f9`  
		Last Modified: Wed, 13 Aug 2025 14:30:54 GMT  
		Size: 71.7 MB (71663754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f14d8e9a78e3bb2259f080d53f9183960e54a6d7c186e6d64ce5bfac499b2e`  
		Last Modified: Wed, 13 Aug 2025 14:30:32 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb4d115a92ee273d0c82c9654f3dd1a595b36c0c0685e013e16761af80cf52c`  
		Last Modified: Wed, 13 Aug 2025 14:30:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d8a662d380d43a77a1f270247c97d9fc279c497e4ae6fb47b36c3b1e33dd12b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2953c93dee58db7bc1576b31240707889366cb76f17b7104ad8ae2709114ba`

```dockerfile
```

-	Layers:
	-	`sha256:608497a36cad33806838d117ada07be7342a9ffca258ab6800933ab3137b338f`  
		Last Modified: Wed, 13 Aug 2025 15:38:23 GMT  
		Size: 5.3 MB (5260977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dc15c31f3815bf9844a3713333ebccf8b9d3dc488a93e4821c0af0d8ac90e78`  
		Last Modified: Wed, 13 Aug 2025 15:38:23 GMT  
		Size: 16.0 KB (15973 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ea65e9527244d030aee12836e776f9812c41ae0f1f8f8d282297b596f112b25c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.2 MB (255214880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fabb93bdfb7bfcb56b22b9ab98853c860748a6bc60735e7ce8c990ddec38f25b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d8b8aeff364003bf6d98326f9028e6a68e79b40eb193739fc1b8d0ad462b35`  
		Last Modified: Wed, 13 Aug 2025 19:53:19 GMT  
		Size: 144.4 MB (144372827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e69c2b0281748e766a9253b8adee079ed6357fff9c705ad7feb4d03ac63b51`  
		Last Modified: Wed, 13 Aug 2025 20:01:52 GMT  
		Size: 77.2 MB (77246796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd57c7aeba4e45b6571e9000801fcaf28e2800d91e5e5eb01b390641ec12cf42`  
		Last Modified: Wed, 13 Aug 2025 20:01:31 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452fdf9d5b10551da7f0e4f3e9b2685d2de71723d9c9b4fee50a9113adc3c5f6`  
		Last Modified: Wed, 13 Aug 2025 20:01:31 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b2f85f81c113ce4c7c6dc8361aa62940e80952aff3b186ba8a62d5dc55a4b792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0caf7039c447fad5616b9fc5a0251d510eae47e477f2ca6476572062d7bc8025`

```dockerfile
```

-	Layers:
	-	`sha256:6fe3b305379e45ca9fc4079374c6e57ec71c578ef6cda1c69e441f70181e52fd`  
		Last Modified: Wed, 13 Aug 2025 21:37:30 GMT  
		Size: 5.3 MB (5259579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13824f6aa617566b578d7a7ddbf54b7ad83e70dade04cb4f68f4700922d74ea0`  
		Last Modified: Wed, 13 Aug 2025 21:37:31 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:15beea66cf7cb47e31e0b382e78db40f6cb54982c7cdc32404e150e0c0415686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239889331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bcbdc870c358762566e27db164db45ab47987c20a5fbef1cebd6691faf6e108`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1753056000'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d692e5a896089ee06890893a0c24f533de09594ed45903a21057919b125f85db`  
		Last Modified: Tue, 22 Jul 2025 01:06:25 GMT  
		Size: 28.3 MB (28271356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c9a46932a4056c19e274f8aa8f89143f8e2a4ee82c82e5921ba97ad4e69492`  
		Last Modified: Mon, 04 Aug 2025 22:06:04 GMT  
		Size: 138.6 MB (138575708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff32fd5f8e43661f717b1478ffb7a2629227238db976b1687fdaa24594eccff`  
		Last Modified: Mon, 04 Aug 2025 22:27:18 GMT  
		Size: 73.0 MB (73041222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24e5b9a937b10649d2aac5c9a255c2c08ad10f859f66625a5d374f983202191`  
		Last Modified: Mon, 04 Aug 2025 22:27:12 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa4e63fbe4c0e619d1c00747c66e113a92cfc05092e6640ccf2dc255e3fd4ef`  
		Last Modified: Mon, 04 Aug 2025 22:27:13 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:18e45decd4d2dda672e8fc659e2092b394e0b613dde1786d147641ae78367c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5258640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:966b3ee4d4f1cfa4e784c9fe7b6291a7184287cadbf20baf9f9ad4e7e53a7621`

```dockerfile
```

-	Layers:
	-	`sha256:4608726f88d3eb4c673a103d8d7dac96cfb6ad0fb9d634db3df72cefe01d665c`  
		Last Modified: Tue, 05 Aug 2025 00:43:26 GMT  
		Size: 5.2 MB (5242737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93f2bc190bdbdff07cd378ec1b874e1bd14ae575a6027a7ab015eba2cff84ea7`  
		Last Modified: Tue, 05 Aug 2025 00:43:27 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:00b981cb2f21bbe021536a51f2754cb03e0a1532abe8dc3db4096fb557ce5bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237363117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7188f6e49c269df210dfd729d24f5ca772beaf1b93bac8961013457635a080`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcf32213940561b1cd1d884f297ae4d5362b6e637204eb4da1045d520045135`  
		Last Modified: Wed, 13 Aug 2025 07:15:09 GMT  
		Size: 134.7 MB (134724419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891387aa884b6b4ea8fc48022dbd0f8cde5cb7095a5c96050f2290914d0b0d15`  
		Last Modified: Wed, 13 Aug 2025 07:19:00 GMT  
		Size: 72.8 MB (72804600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b15e5725bc67c9e63f610ff97be3c6a11b9e716e0eb63f29325be0c12e1091ad`  
		Last Modified: Wed, 13 Aug 2025 09:00:10 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a51ba53afd6846a25edeb1d4118765e456d46389d2b5c1abf208fe48b005e3`  
		Last Modified: Wed, 13 Aug 2025 08:16:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:166e4d60beb66c394fdef74de3c20589a489c9f90197165aa68c384b28c3fed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5266987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96235cf849bcb55fe7318e0a415c20fee8574a5f96c1bee2625ed31ee997b89`

```dockerfile
```

-	Layers:
	-	`sha256:ef6297e3f9fa90d9414162e1deba5b520f8393b16904a4b28631888e898b3310`  
		Last Modified: Wed, 13 Aug 2025 09:37:02 GMT  
		Size: 5.3 MB (5251132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fdc0d3ddcba6ef9ac59abaa28fd860da8626764ac04662fe442010bc20ff160`  
		Last Modified: Wed, 13 Aug 2025 09:37:03 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json
