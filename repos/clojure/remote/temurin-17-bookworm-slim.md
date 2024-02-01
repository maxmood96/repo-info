## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:22046ea22d51b1f5376a7aa5dc6c6b01f1b9bc9a1f69c70f14ce927854045209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:197276ebeeefe2d8f59811a1d8c7c82f934c148b08fbc1debd04617750a30ae3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243109750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd0c54f7b0a2e36659667be9013bda937eb7be415838da4888c48758eb92408`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:43:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:54:34 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:54:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:58:22 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 31 Jan 2024 23:58:22 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:58:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 31 Jan 2024 23:58:40 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 31 Jan 2024 23:58:40 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 31 Jan 2024 23:58:40 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 31 Jan 2024 23:58:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f958f51a0d7ee5eda8bc3fd3d244ea755a14a4ce5fc81c38ce16b8f68abf581`  
		Last Modified: Thu, 01 Feb 2024 00:12:29 GMT  
		Size: 144.9 MB (144892493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331ca2cc691ac4e6621678203f2181a9719e4a0ccead1179a642397c87167666`  
		Last Modified: Thu, 01 Feb 2024 00:14:34 GMT  
		Size: 69.1 MB (69065775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86458911030e7937fef718dcd2f4f7c38c9d08fb419f641039a4db0fc26ba116`  
		Last Modified: Thu, 01 Feb 2024 00:14:25 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d03ece911eb5fb1c0f1e2e8cd99f9b58a4d3ece4734ed9b8e71c735fa2b56f0`  
		Last Modified: Thu, 01 Feb 2024 00:14:26 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8242dc36a406fa3f2c460b1682609c3ad003d195eb79d0a59df345a24f10cb01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241722747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0188baa891eba2ca1c51a414c88008e5b3cab8f79afde0d8ead41cd1577df644`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:20:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:30:04 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:30:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:33:30 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 01 Feb 2024 06:33:30 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:33:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 01 Feb 2024 06:33:46 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 01 Feb 2024 06:33:46 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 01 Feb 2024 06:33:46 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Feb 2024 06:33:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8541bec30ce62241d4247e43427e2cfb0f0dd456024f3b7c2bc64e85374f9c`  
		Last Modified: Thu, 01 Feb 2024 06:45:48 GMT  
		Size: 143.7 MB (143720887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a104ff68c32be05e1d13998d396d3b00487b50a3cb9dc4dffa3ebceab0daba6a`  
		Last Modified: Thu, 01 Feb 2024 06:47:47 GMT  
		Size: 68.8 MB (68820010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad20082da33ab8b8d6ba22b7fee2d75e00e115d9a5224a35921fbad9a2fd658e`  
		Last Modified: Thu, 01 Feb 2024 06:47:39 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05ba4c0c328e0a6722656a9b0e5ddec1195df48a471e390ac663df35cbb0c24e`  
		Last Modified: Thu, 01 Feb 2024 06:47:39 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
