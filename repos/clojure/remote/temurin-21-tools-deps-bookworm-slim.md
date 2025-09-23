## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:900257fcecefa4914f3838be44345e896d042f170718eb3b82fe17d3e384b7a9
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
$ docker pull clojure@sha256:f6af37f60f13d80cf6f6d3284e1a49a8771f64ec5a97141f2f519ed931f12525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255709537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458d62a40373ad70fee4d63189212e24254dac2f917800a2b2af77b8e046f159`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85373ae23b9c39c1275d64ff40af830020620de21a284ec13ca80c897746665`  
		Last Modified: Tue, 23 Sep 2025 00:51:34 GMT  
		Size: 157.8 MB (157804776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f935ec24216a97f4560a38bae2cad06ba17effef5849ab7e151f92b99f498bb`  
		Last Modified: Mon, 22 Sep 2025 23:46:28 GMT  
		Size: 69.7 MB (69675374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51785b495856538fdd232b6561dd86e17ffe4740347df9e8cfa030f1c7ce77b`  
		Last Modified: Mon, 22 Sep 2025 23:46:28 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d91fd1bf352be819ea48dee97560ed43f9daf2fb3570c4eaee423becbde272`  
		Last Modified: Mon, 22 Sep 2025 23:46:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:48827d0447b6748d2f6f8aa3d8398d14c0073c206326fd0c7175fa8a69fbacd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1f98f5aaaa5f2392b6710b3d77e0d8f406559af7f25d53caef270f7aec57ca`

```dockerfile
```

-	Layers:
	-	`sha256:15afdfda0681dc3620450920e0b2cc58fc64a30a5204cf7c51e67b88aa004f89`  
		Last Modified: Tue, 23 Sep 2025 00:41:10 GMT  
		Size: 5.1 MB (5117186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e47f5b341499f6d14fad5f0a1da264ec660605c504dc542f6a743825d0293ca7`  
		Last Modified: Tue, 23 Sep 2025 00:41:10 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bac068b5e5ba17ca7e5bd00e3df388123bb4efbe0a91da59a47c7dc74df26d38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253748130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:202350fc7d9b34c5712027fb69f9ff13d86284e2ff4dee944d20abcae5a92bb5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838d791c46d91a151130a260b4869660f8105d58c0db353238d27e0140aaf65e`  
		Last Modified: Mon, 22 Sep 2025 23:12:38 GMT  
		Size: 156.1 MB (156081216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe11af96da20e1f245bad978d84b1277d91c549ca5ec464ad493ba19fbf6cd8`  
		Last Modified: Mon, 22 Sep 2025 22:20:11 GMT  
		Size: 69.6 MB (69563773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507c77461f9f71500c866fc81242c934b87c15de53199fa7f6e227de1052d840`  
		Last Modified: Mon, 22 Sep 2025 22:19:55 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076aaaa47f4b368dfa40d8c61d7b505d3ce0c0a4e0319b7b5ec81bb8842d39f6`  
		Last Modified: Mon, 22 Sep 2025 22:19:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:01fe32edb4acd7677f82bd941198c04c35855b4eba2a3d8ae4081a41a88808ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53313209ea21489c6018120118bafe44db944fa939d47bdcf6fc73a17804e22`

```dockerfile
```

-	Layers:
	-	`sha256:c76dc6b413e40f2729664f75ecf12dd23833dc71e907adab2df0a193ab94f40f`  
		Last Modified: Tue, 23 Sep 2025 00:41:16 GMT  
		Size: 5.1 MB (5122971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7494c3fb0f48c6b47b2821e828031691dfcaedc7a1babeea63cb96e652b50693`  
		Last Modified: Tue, 23 Sep 2025 00:41:17 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ef040e2b32b1972dc590ba4f07cc54edbbe52d9642ca914a71f57b949cb348ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265546549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c6de283b6aca0e9f9a5d720278bc4f4fe552bb72edaf256c7cbcf7d59549bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a438293490bbc2af66661166949a4d86358eeb39f9fadd5b0146666f05b9b9ac`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 32.1 MB (32068762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2959f109b81d6369cb4c4d72db588ee4273715e7579994466fce2c60dd0c1abe`  
		Last Modified: Sat, 13 Sep 2025 03:42:32 GMT  
		Size: 158.0 MB (157963469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9756ac0f544f3d541fb3bb0685625f7dbc5f634200fa877cc827a751117356e3`  
		Last Modified: Mon, 22 Sep 2025 23:13:12 GMT  
		Size: 75.5 MB (75513272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e09363585e0c55d632b94e5166117c8e334aa0abdebf633b190a194d30dd56`  
		Last Modified: Mon, 22 Sep 2025 23:12:56 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9af678aaaa5b17513a7c1a8c5118ded86b868bcfea17ac14c5bd859da7b746`  
		Last Modified: Mon, 22 Sep 2025 23:12:56 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2e5f98999f71c96b5b0103c2511c54fe69fa4ccb1ce608d19b267a228ef83895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de07b5eee47caf3d168682a10cfa73b8a336315253e4accbc5cab5208e1f9ea`

```dockerfile
```

-	Layers:
	-	`sha256:4343132e843d50d6f14e8f20e6e236d33e704759bb84f9dd7862de91b3789eab`  
		Last Modified: Tue, 23 Sep 2025 00:41:21 GMT  
		Size: 5.1 MB (5122356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c22d589aef370ddfd18d6556622ce7b16071e356a65b585f0420fedcccfd37a0`  
		Last Modified: Tue, 23 Sep 2025 00:41:22 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b0476a79a2464644b6d4a14aac3891c88a02914c8dd171dde5b508b09ae1e20a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242403008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dfe8cc2a8e7ea8bfd61cf16f3e1bb96fea095dd38e8b3e42b09df830d0011a1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209327a5cb75c8c1d8464e1562aa66efe9b66ed99f6f5603c3b5a1ccb9f3d9a3`  
		Last Modified: Fri, 12 Sep 2025 23:55:50 GMT  
		Size: 147.0 MB (147026988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a39ea21058d0ad48438e29c520185e740913d43f967ec1b3076a2ed9828b91`  
		Last Modified: Mon, 22 Sep 2025 23:14:01 GMT  
		Size: 68.5 MB (68490677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04cf1f90c8f19211e6f7c479541bf97ef880527e1ba4232081c38ce3987b54b4`  
		Last Modified: Mon, 22 Sep 2025 23:13:56 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6537c0a84aaf94d3b4a509da3e2c52b5c46fccb90883d21b779ec0128724b0`  
		Last Modified: Mon, 22 Sep 2025 23:13:56 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c60a97dd2104dc81cf8f578b8ba55cf2b120409ff4b1e8e631609021ed8ee7bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9267d8e5f5eb6c1e2088542eaaec68f540ddd61cebd6dd11d0377d8d916cb6`

```dockerfile
```

-	Layers:
	-	`sha256:6abfa2ba2386c9ebef7ba8734e27d780c87f9885d2867d3417ace55feb74cfdb`  
		Last Modified: Tue, 23 Sep 2025 00:41:27 GMT  
		Size: 5.1 MB (5108507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d7419b7ec5074eff2c8bc02b6a899c681f0672246c8ca3c91a6f3caa66335df`  
		Last Modified: Tue, 23 Sep 2025 00:41:28 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json
