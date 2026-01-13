## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:2e2ec47821eb51e84de0dfa661ecc87f06c199e2b4e66e233f3a84a0c465b099
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3b9e7a0bdeef9a066595ea372d9bc7bdc48ffae0795322cb55ce03bcb962dce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247235451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786cb4d7a34ba51c44b90c0b97e728d380e5953b3f807f8fc61f90c917e25973`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:27:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 02:27:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 02:27:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:27:47 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:36:13 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:36:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:36:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:36:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:36:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:36:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af8a5238c537bb628343624b944e3eb3ad87f0c7f77a9b2d1ea9a18955945a9`  
		Last Modified: Tue, 13 Jan 2026 02:29:17 GMT  
		Size: 157.8 MB (157826042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01309df093eef24f4794873ce3a8bc35b066762883a7948ab684e5f6e3a478a2`  
		Last Modified: Tue, 13 Jan 2026 03:36:55 GMT  
		Size: 59.1 MB (59149877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0588310f121e9db5383e8afc89901b80554b1135ebb153a2f956e72fdd049276`  
		Last Modified: Tue, 13 Jan 2026 03:36:51 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f517fb5fc760c3e7e7ef6f9a886514cc3e91aa6c0875def75961112ce3f43102`  
		Last Modified: Tue, 13 Jan 2026 03:36:52 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:39ca9cf06ee02a93f2be46379f051948046091e5172c935caca1a86a5e0972d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5327007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cdc949d31ad5b5b3376a1a685d2f804c91ec15206aa18807dceb15f4af55bb3`

```dockerfile
```

-	Layers:
	-	`sha256:e0c0417d29e4bd4cfe57aee341b7e34ac87d19dead7c1b24688208676894efbb`  
		Last Modified: Tue, 13 Jan 2026 07:44:24 GMT  
		Size: 5.3 MB (5311171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c9eb96ce90f0a7341de08c6868669c19d7c5926e8b45ee7c1cb438136cf44a4`  
		Last Modified: Tue, 13 Jan 2026 07:44:25 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:610eaf725c759e100acef53429be81dc54e572a205e52b2fdb8eef9c0a4e66cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244140960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577edb41e6e1c8290d1dedc7f5e8ff20f275d2829b16929d4dd6929092073295`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 03:39:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:39:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:39:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:39:34 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:39:34 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:39:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:39:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:39:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:39:48 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:39:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb32f196e1a3955bf6109186f1f8c746bdd11a63f637cf5e19632f9f3213cc6`  
		Last Modified: Tue, 13 Jan 2026 03:40:38 GMT  
		Size: 156.1 MB (156107580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11bee905d2d2d58177ee0f8beab52f7420be640e972750e08be59a774e8dc55`  
		Last Modified: Tue, 13 Jan 2026 03:40:30 GMT  
		Size: 59.3 MB (59283821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa66e4606b0459de4343abd3db836846a4774f19ffd9ece74a2a1926703b4a45`  
		Last Modified: Tue, 13 Jan 2026 05:40:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5685e0105fe3070087618bbfae8d60ca2438edb7603188dc7cc2f799d2c13b7c`  
		Last Modified: Tue, 13 Jan 2026 03:40:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:65212cd16d3b963b7835944c013e53b55896fe064de08f6d02e485a6e3b321b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5332855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cddcf92480ba445eced8a563cead30ef47cd7bba735c31354b2340ea5c2d00d`

```dockerfile
```

-	Layers:
	-	`sha256:fb6300e4cf2d31c44685859d8d924bf80884a5ea1b3ff8075bab7b7cbc33370f`  
		Last Modified: Tue, 13 Jan 2026 07:44:30 GMT  
		Size: 5.3 MB (5316903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f56490a877bd979a2cc2edd0fd53f3ade2749db49a2ac7ce6adeebc944d18207`  
		Last Modified: Tue, 13 Jan 2026 07:44:31 GMT  
		Size: 16.0 KB (15952 bytes)  
		MIME: application/vnd.in-toto+json
