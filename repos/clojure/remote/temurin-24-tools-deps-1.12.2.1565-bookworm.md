## `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm`

```console
$ docker pull clojure@sha256:3f99b8111ebe5edfb78fa8a52353b92d4ab3118795976a9d442f861ff85b0ab2
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

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:61dfc02dd459f7e84671b14375e27bdf2f66e5e6b78f2ace8a46c51e38a74e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219595314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42d8937da432b393015478cdb12a7d9239403c466e2e21315709b39c5218dda`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aef6c1606a15fb1170cb41785713e043a98e1cc887aa9d56a517f2b0e515eda`  
		Last Modified: Tue, 16 Sep 2025 00:22:46 GMT  
		Size: 90.0 MB (89975165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3ee150915ef7e87cac4d40dbb628a5d583c296f3f4ab410016c042ea25b17e`  
		Last Modified: Tue, 16 Sep 2025 00:22:40 GMT  
		Size: 81.1 MB (81138495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11d93b74ae97a279fa147942c27eea03d4d5341f01db8dfed3e518af5518034`  
		Last Modified: Mon, 15 Sep 2025 23:35:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6405c68dab60494e4b9888ec2623390eaffd4ff4bf264e179ea09663ecb9493`  
		Last Modified: Mon, 15 Sep 2025 23:35:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5ff3e48b906fe7436da91ba3b02731e08e56825b91c8ac2b963b9b1e508138b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7342720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89777581ede3f3db5dad686979f096bf7a3bdbf15846667c2e7cbeca5b9d28de`

```dockerfile
```

-	Layers:
	-	`sha256:d36e1956eb5318dd62cc06de9a0ee3bc153147f476e408eb85064334d2541e72`  
		Last Modified: Tue, 16 Sep 2025 00:44:25 GMT  
		Size: 7.3 MB (7326222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:890ea725b4b4b024a684f1d439aafe7c6d02b0c9d243d2b259b5994f2be6e484`  
		Last Modified: Tue, 16 Sep 2025 00:44:26 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c8a7838892f2e92aad18c792e55024ceed2c5fb05caa97eb7f1973e27093329c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.5 MB (218478279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17a3cce72f27919f6eb7791c007acc2622e02a979b3e6ab47a8be5126db58c9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247135a1bf86492dc7b8e8130a2a36a0e799559edc08562d2d53d9ef59d20319`  
		Last Modified: Mon, 15 Sep 2025 23:29:08 GMT  
		Size: 89.1 MB (89092539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152f9faa2202a6bbad763544baf972bf514771ce410d4820b3861c6756c14d24`  
		Last Modified: Mon, 15 Sep 2025 23:29:06 GMT  
		Size: 81.0 MB (81025681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a10363f8a5f94c2971fe980721562da1e7f1110c8b51764b341c43ad31f67d6`  
		Last Modified: Mon, 15 Sep 2025 23:29:01 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bab6924ff7b74d1d2da56a4d24cc7004a05cef6d00855e9d38c29c715fd0d74`  
		Last Modified: Mon, 15 Sep 2025 23:29:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d853b703aee92b27fc641e0a270ad7cd92e88d4451c10dc1dbc98cebd923056e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7348646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1618f8ebd58bdf1bd0f3d8af786aa8b66ca175648f45752947b10b23e423612`

```dockerfile
```

-	Layers:
	-	`sha256:d0353b44f84f026ab80b218b12d26914959716e0067b24b80c9444743555e645`  
		Last Modified: Tue, 16 Sep 2025 00:44:32 GMT  
		Size: 7.3 MB (7332006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae3a090cf8254527c7feb8932126eb719343db3374d4c7bfb95ad9fad8c5cde9`  
		Last Modified: Tue, 16 Sep 2025 00:44:33 GMT  
		Size: 16.6 KB (16640 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:38eccba8ca6faadf7e19dc85e8658363233e5c028fd0458bc7fdad1cbbb0ee8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229224753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047e4463dfc2d5e35115cbf8037b5eab02d57b490387dc52643b4ef67aff062d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:64b8116dd43c29a2a4aa3131cb4895af0a7267cc5883e3761556e54c369be9af`  
		Last Modified: Mon, 08 Sep 2025 21:22:08 GMT  
		Size: 52.3 MB (52326822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86172f15372b948e9acf8523414dcea949da4bf6c2e68bc45159e62ddfee9e65`  
		Last Modified: Sat, 13 Sep 2025 03:50:01 GMT  
		Size: 89.9 MB (89918193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a01fc236877ff46e61b7e857e43f39c1a51bf2ccbc238a48fd3603d3cc2f7d`  
		Last Modified: Tue, 16 Sep 2025 01:30:52 GMT  
		Size: 87.0 MB (86978694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60697119c425cc84ea5ad18786e38307ffecf6e7d3ae9c52e83ae73b7833bd9d`  
		Last Modified: Tue, 16 Sep 2025 01:30:46 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22dff482f9291224640831f8f6e277f4202ac7fee5f2c7f94124e0b45d98ea4`  
		Last Modified: Tue, 16 Sep 2025 01:30:47 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3619b6a5271023b8fb725239bb60c5fdae24b699104e97a202ef6b41a9fdd409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7349304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7564c5b0e05a719675a5836e316c1d609d523a4635e651f263455a5034efc2bf`

```dockerfile
```

-	Layers:
	-	`sha256:c01c8ed0fee824a174d88b10b78e51cc2e5f2aa70f2a6e713bc8573455267529`  
		Last Modified: Tue, 16 Sep 2025 03:42:28 GMT  
		Size: 7.3 MB (7332746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89369fbb3a26bc92e4b7cee137195c10ddbadd0fbe05d89467188e3efbcfcd53`  
		Last Modified: Tue, 16 Sep 2025 03:42:29 GMT  
		Size: 16.6 KB (16558 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:aafb80472288d77a216f30ac47f69e3eea4c54707781b97303b7791cf9587940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212315947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395342512dce457cc3884c215df1fa255e3f1a7edd4c63b79392d1a4194c7e5b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:67e2d91fae4fd9af13e4e364bf8120dcca7856e8273995cc0651acae70b27e8e`  
		Last Modified: Mon, 08 Sep 2025 21:18:01 GMT  
		Size: 47.1 MB (47137539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a194a3e86b38170126e14a8a4967e24dd619d46e1914dcccc96f552585ef697`  
		Last Modified: Sat, 13 Sep 2025 00:02:32 GMT  
		Size: 85.2 MB (85226409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8135c79e1ca61cc41f2ab63667ac9bd4b9da6c26601b9ee405afa11dbdf4d728`  
		Last Modified: Tue, 16 Sep 2025 01:02:44 GMT  
		Size: 80.0 MB (79950954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765fee400bdd1552fc3ed3fffc070136534d423a2f7b353c09034f3ea7b4f00d`  
		Last Modified: Tue, 16 Sep 2025 01:02:40 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca176853b8bf756ec8259d51d7c180c90f516d7bf4633b332fd83cc48868d7e`  
		Last Modified: Tue, 16 Sep 2025 01:02:41 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1565-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7095e95a3a29b7e4f966eeeec38d814e4eb064605f944edf37fafb77bee889c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7336587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cdc2412828add4e0e0a3afeae2659aff985a3f0e399eef6f82c275b38dc2db9`

```dockerfile
```

-	Layers:
	-	`sha256:9e9f56071fc4158c23d4b1ebbc2c886e040728ff1c8f96298501cddc04d0f7a9`  
		Last Modified: Tue, 16 Sep 2025 03:42:35 GMT  
		Size: 7.3 MB (7320089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0411d9b7f3ef829613667954fe721440b2790381d7bf1a27a0ff435ccf0d36ad`  
		Last Modified: Tue, 16 Sep 2025 03:42:36 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json
