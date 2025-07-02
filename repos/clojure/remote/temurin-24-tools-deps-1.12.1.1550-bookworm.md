## `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm`

```console
$ docker pull clojure@sha256:b3a2b9ac63d44576f31319b6573c493b4ecaddb8de31c22074f5af45ed18cc41
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

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:369457bbb6a8f812a8ac5aa2172135bbe54869c9e683a9047e49a895c44e5b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219440359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b545e6ae92c5c54977c49b4de54f1f2576e5034ffa1c57d5de1f6843e6f048`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a1b818c5afe59e81fecd397ce1fc7959e404064670851a83d9ab53e6740a76`  
		Last Modified: Wed, 02 Jul 2025 04:17:41 GMT  
		Size: 90.0 MB (89952000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6550fdf141d0cf2bbdb7496c21da02a8e53c2f67919a4dd48a5628df38b2e55f`  
		Last Modified: Wed, 02 Jul 2025 04:17:37 GMT  
		Size: 81.0 MB (80993037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea8c71b469cdd2fef38ef25e01e3f0f3bb17477e0c8f2701ab65a7d8dbab240`  
		Last Modified: Wed, 02 Jul 2025 04:17:26 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e535c31192eb5793f310384133c47ebde510a4b1a4c25e853321eff872b6ec`  
		Last Modified: Wed, 02 Jul 2025 04:17:22 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5da59001a33f64dcb0e05af1ab0715481bbfd5b38667ffd30afe16fb17d58b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7336096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32a1febc4707789597a46a1add58e115c7c390c857ab8697d5c71ebfb17409b`

```dockerfile
```

-	Layers:
	-	`sha256:319f2bd3c3d04f6083f3760683ffebb5aede1446df999e8e41b901a35c0c2462`  
		Last Modified: Wed, 02 Jul 2025 06:40:59 GMT  
		Size: 7.3 MB (7319598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b577b0f864ee778bb09fdfc8df2c96255fddc73aa07e14f23f31acad8c05f20`  
		Last Modified: Wed, 02 Jul 2025 06:41:00 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a25508afc45374a8c9588f9a1a4197e3ff0bbae23f33c78e754a09778505580d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218283038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa766fb0859575c3de390c21e34efcd157246f29b86a39159052c111701d3189`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ed4c8912abb05c9d16227b79bd4d0c95ee19d89d3b3075be39be91242157b3`  
		Last Modified: Wed, 02 Jul 2025 15:43:39 GMT  
		Size: 89.1 MB (89091225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4840b55b4f3001553fc03d0feacf77e1dde1deb919fb4d04b42c0c3e79810b`  
		Last Modified: Wed, 02 Jul 2025 13:01:07 GMT  
		Size: 80.9 MB (80851991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c259afd99ea46ec062cdcd085ca7e2174ccd9d06051576f7b5719103af9293`  
		Last Modified: Wed, 02 Jul 2025 13:00:59 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222e17dd7b5c28243b56f9c48ba0d95a26c7725f9e39efe167555c1177ddff1b`  
		Last Modified: Wed, 02 Jul 2025 13:01:00 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b9545deb40a7e5fae653e48c8619922b7f2cc4255c9d96348c714523c3754944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7342022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1280af609a8625a3e8933d85b77c7b05d3a5d98e9e69997fdac5ac85d40f3e0`

```dockerfile
```

-	Layers:
	-	`sha256:bb2517983a55d59ed2f7ad0e0c4a419c9bb25b2858a33240020bab20975dfd26`  
		Last Modified: Wed, 02 Jul 2025 15:41:46 GMT  
		Size: 7.3 MB (7325382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37a127a9c2324389a3ec6747bd6f8d305ec298713ab20eae4a55507bf4f90534`  
		Last Modified: Wed, 02 Jul 2025 15:41:47 GMT  
		Size: 16.6 KB (16640 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:751694637bb57ac89262f41bc1e115d647cefcf04b1d3e37c5521c264225c99c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229078538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f895100ef717d2db653b3fd414e440e407c06e8d8b0978a51e7987b9c5e69c85`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d19b842940b208b4f06e0b58568d49e75601533443c8580a39697d58f645f300`  
		Last Modified: Wed, 02 Jul 2025 14:02:05 GMT  
		Size: 89.9 MB (89920275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e688bc90560bb6b1cb16fcea6148b5b46ebdaf0f2f112fc182b67ccbdcabb50`  
		Last Modified: Wed, 02 Jul 2025 14:11:26 GMT  
		Size: 86.8 MB (86819977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204bca918a6dbf0ee76fa3daab8b1c35d2ebbe14e5935b6e08fdcf23862d78f7`  
		Last Modified: Wed, 02 Jul 2025 14:11:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605f1b4e21350608b484dcc1972c0b9d352d68903318ac6d36432242561c8f41`  
		Last Modified: Wed, 02 Jul 2025 14:11:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fb2e923a78fdf7051c9cc2dae5406c97b0fb353e063c90bf7ddc8870ada300e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7342670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b1a27c36dbd698e6dc996818360b46d0d425dcafdb90af9e576eaf71693809`

```dockerfile
```

-	Layers:
	-	`sha256:eeb016ea3393c104696a1da2dae56ac89aecdcd33703ba921bfc63edec7fb00e`  
		Last Modified: Wed, 02 Jul 2025 15:41:53 GMT  
		Size: 7.3 MB (7326112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dfcd41b8c06552cfc709b7bf7fc294b9d7675cb6bac937f9eb52aae8b8d65b0`  
		Last Modified: Wed, 02 Jul 2025 15:41:53 GMT  
		Size: 16.6 KB (16558 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:20ca8e0ebf5023efb9cbda7ce0b06b296a1e3738818e479db61ee03093c8332f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212166659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a01ffac05c69c5d78fcd2c7f6a55b03b2d18494558d0b4c1766ca33ad49c772`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
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
	-	`sha256:f5e945529523ccd9610b7c0253cda59a29c297f0a697f3c402695e1c6ecf5e6c`  
		Last Modified: Tue, 01 Jul 2025 01:15:47 GMT  
		Size: 47.1 MB (47149287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d5a54602bfb697ba4ba032fdb5bd7dd65566e4d748c05b7a6ab9306169bfb7`  
		Last Modified: Wed, 02 Jul 2025 06:56:10 GMT  
		Size: 85.2 MB (85216779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d1fe512dac936fcf3435a6a221c78c6cb55fd68b82d0391418342c9cef4a3c`  
		Last Modified: Wed, 02 Jul 2025 07:00:40 GMT  
		Size: 79.8 MB (79799550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615914131e016efd7f0235eb94f9f504f80a4b83c485b10e4e36f297b6d7f9bc`  
		Last Modified: Wed, 02 Jul 2025 07:00:35 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfeb147284db54e7f68cf024e81fda730bd4da94ce39015fa083bb1aa6b0fa2c`  
		Last Modified: Wed, 02 Jul 2025 07:00:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4afa4a50317fce17fdf899e1783487cdef4c0debae631f98aff0a8f7cdd3d4ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7329963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724122c5b05d20a843da77f2cc32185294a4370398b3ec0ea43dfa8675eb1c8f`

```dockerfile
```

-	Layers:
	-	`sha256:370c0b28da40c3e17d4d65f54680b8b20ae61fa97fe6d831ef9fc554022f6ad0`  
		Last Modified: Wed, 02 Jul 2025 09:40:36 GMT  
		Size: 7.3 MB (7313465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6223c32e18f43f4f18b372b32e3c745abd972ef451dfe0dd21c426a44c758af`  
		Last Modified: Wed, 02 Jul 2025 09:40:36 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json
