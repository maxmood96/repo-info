## `clojure:temurin-8-tools-deps-1.12.1.1550-bullseye`

```console
$ docker pull clojure@sha256:99faaddbb65ea548cac8c4f1a761b12e2aca3cf43165602cd609d066020b087b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.1.1550-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:73dca3fb4b70fb2e2a13b91c9f70aafb8abad04c28a17d489cebe77e1162dec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177896920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:553f6ce66c566ad9e1dbfac0b2e0d9cc1c49d9034b2b2a93b2ca781e31552a1a`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d01bacc1359374ca4ca8411720badc65ec517555936b4c73c71968c8f009d9`  
		Last Modified: Tue, 12 Aug 2025 21:34:43 GMT  
		Size: 54.7 MB (54731324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d87d4edf4886c94644ac1aa87fb6edddb98e352821a8de5f2f07c89e30f24a`  
		Last Modified: Tue, 12 Aug 2025 21:34:43 GMT  
		Size: 69.4 MB (69409607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d18dd8e7144892f3cc703a4717a8a754e14829dfaeddb006fb1d022e77fc30a`  
		Last Modified: Tue, 12 Aug 2025 21:34:40 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d0b34c4c3ebf95aed23f17678005a06ce38a856a8a7176028598f9211c0bdbdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7531485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7017de63f602774820dc64f0d7ffbf1d2d5cbc5f7fdc1e3e58f865400f03b1e6`

```dockerfile
```

-	Layers:
	-	`sha256:51ff560f739c2924ac6d39a30b9c383a45caf7b4e4986c1d17f98403ec70862b`  
		Last Modified: Wed, 13 Aug 2025 00:41:39 GMT  
		Size: 7.5 MB (7517248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a5b90e4ffea9a0a6d2bbff87e5b9c11975b95af33b5ea42999238f4d1716e89`  
		Last Modified: Wed, 13 Aug 2025 00:41:41 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.1.1550-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:db3cb6dbec43d18abce39b90da30059834d23b5d4550123b3f5ffc31b9970de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175622435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3116ca53e1dcf411a37edd511f85c7bdcbd1f1fe0dc75c6b59539006276cdc`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c2670f7a03a99ef545c891d545b4f0e79a3c5fda7864feac134a0468764f26`  
		Last Modified: Wed, 13 Aug 2025 14:04:01 GMT  
		Size: 53.8 MB (53835638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0645766e0ae36de3b5acd3e0eb5f8d49e462e37f00c0caad161016d500327325`  
		Last Modified: Sun, 17 Aug 2025 09:40:59 GMT  
		Size: 69.5 MB (69537741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba41519c64fb3b47bf6c0cac6e6b03fa6f7aa6087b9879033eed2d9fcbcfe2ef`  
		Last Modified: Wed, 13 Aug 2025 14:54:00 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d69f34d1ba822e73a95b45dc682b78162ae8fa6748a82709f99745c0431bf611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7537400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b06f8009224d19948396875e2187e6ef7f81277d04f4648d930cfa8552fc7ff`

```dockerfile
```

-	Layers:
	-	`sha256:a9f772b55f70f207414d66f47c3e61d89533cb71d08f290522e1a6110de367d2`  
		Last Modified: Wed, 13 Aug 2025 15:42:18 GMT  
		Size: 7.5 MB (7523045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8b2036cab24fa175a850356d56c0255ea9af5e732fc7d6806aba5dc2f01b8c0`  
		Last Modified: Wed, 13 Aug 2025 15:42:19 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
