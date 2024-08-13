## `clojure:temurin-8-tools-deps-1.11.4.1474-bookworm-slim`

```console
$ docker pull clojure@sha256:483bd6544b5262f982f5f6b6bafe34241e4f76e867d56eef4830f1099919fbd2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.11.4.1474-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7f3bbc575c0feb81d538f0c08cf3d3c2d4cf524bf5c6a7168447e7cbe068cd4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.8 MB (201762810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e0f9f9e7ce735e068543bd2f36179a6909ff7dfb07c89d4678c3a1de8d184f`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54b26278c425406377ffb8a2b9693fb865109736aa7c09703c75fd581d7ccc3`  
		Last Modified: Tue, 13 Aug 2024 01:11:23 GMT  
		Size: 103.6 MB (103611898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70458c927e82a1cc8b19e3fcdd1c04e1c802611d0495da0bff14e505bb02514`  
		Last Modified: Tue, 13 Aug 2024 01:11:22 GMT  
		Size: 69.0 MB (69024036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ea5c4b7134848171b4848952e3aa55899fad8543218905e1fe50ade46c9c71`  
		Last Modified: Tue, 13 Aug 2024 01:11:19 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.4.1474-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dd37ee3bbf426ba81cc09b3431de6660463616b022b6056086afc1049d08ad68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4784575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8debd77cff16cb1e45fffd0fbc089ac8e2e05723a1f52f40e7c9122bf54a7cc9`

```dockerfile
```

-	Layers:
	-	`sha256:c357003a780350c04caf60d08c6dd832708394d0a2abadf39e913511537dc332`  
		Last Modified: Tue, 13 Aug 2024 01:11:20 GMT  
		Size: 4.8 MB (4770655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84dcafcefd1dbb07482e2c09123d5e7dc5ea690ca7f7560f3270e231032ea10b`  
		Last Modified: Tue, 13 Aug 2024 01:11:19 GMT  
		Size: 13.9 KB (13920 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.11.4.1474-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:91bab4aab58ddfd32d29523bfde3e96c8d11b04176390af3933a9cbd3834ae83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.7 MB (200660010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa23bc25f3f7898958a3ad66e84973bc15a3b309e8ae05f11909b9678770aea`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:51 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Tue, 23 Jul 2024 04:17:52 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36b6909f0b4d39774e340daaacee1b91b36858e2c85a2f57022155079165850`  
		Last Modified: Thu, 25 Jul 2024 19:08:47 GMT  
		Size: 102.7 MB (102729199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84b9ae6b5515626ed557b651b845f417c2ef07bf672951b1be5f360347939f9`  
		Last Modified: Wed, 07 Aug 2024 19:43:44 GMT  
		Size: 68.8 MB (68773597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8fbd90689dc8cecd100f7cb666e650376d74c74b3f04b4a0a0a6da39e83c63`  
		Last Modified: Wed, 07 Aug 2024 19:43:41 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.11.4.1474-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:58a0183d89eed296b2f90f6c47d29aded91c6f80e297158886d95d59c4b0ba9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4791501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118747b1c07f0cfc1c162af36e9c5cb9b1423862b3dd36b19ba357051d3c1705`

```dockerfile
```

-	Layers:
	-	`sha256:d4002c9e679aedbf6987a92f2270c3178c804e3eee4805f9d8cdbc6624a6ae8e`  
		Last Modified: Wed, 07 Aug 2024 19:43:42 GMT  
		Size: 4.8 MB (4777040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb669b8341827d11e5e6fa7dbb9cebcea1ca368663849b7831671ec98a390c71`  
		Last Modified: Wed, 07 Aug 2024 19:43:41 GMT  
		Size: 14.5 KB (14461 bytes)  
		MIME: application/vnd.in-toto+json
