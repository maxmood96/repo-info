## `clojure:temurin-25-tools-deps-1.12.4.1582-bullseye`

```console
$ docker pull clojure@sha256:10adbbd5c33e946a7a7dadf65787e84c37fe1ef47c8c3bed9c988edf948791ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-1.12.4.1582-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:2e7178bdea16ebcb8a2da502ccd57bfc65e42e50eace4af46bda8fb546b7b327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215359539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108afcb4d3fc3a38abf8bd34307ca30dc1033b587d88c0b89ec488edda317ba0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 01:08:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:08:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:08:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:08:37 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:08:37 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:08:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:08:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:08:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:08:51 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:08:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dc0c52c6f559400f5aeba53cd1e686b0bbbb4731ff04dc20d0fb5e56b22eef`  
		Last Modified: Tue, 30 Dec 2025 01:09:32 GMT  
		Size: 92.0 MB (92045301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cae68fb15c547a30ba622c3859dcd1ae770528d624afef5754aa78bc26ea6f6`  
		Last Modified: Tue, 30 Dec 2025 01:09:33 GMT  
		Size: 69.6 MB (69556758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6d0607f272ea01cb91f66d07de43e37055e5e2ef2391acbb074b64177ea4bc`  
		Last Modified: Tue, 30 Dec 2025 01:09:23 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9e906da1c9698791865b973459c2993b646ad4e1245344ff0f5491faa5f85b`  
		Last Modified: Tue, 30 Dec 2025 01:09:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1582-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b39d0b1182026c684e6ab7b5932f29c055a7613ba4805a388f45bba318e9c08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35aa4d318948a27049c151864ec6a33f3856d192ddcadfed1b273cac346ae69d`

```dockerfile
```

-	Layers:
	-	`sha256:76ea1dfa47d46e589e452f95b3ee3f4e01aa411c282269bd0b114efed7e7fb1d`  
		Last Modified: Tue, 30 Dec 2025 04:46:15 GMT  
		Size: 7.3 MB (7347007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aa997dea3f250cba9cf55a123c990e0fc566eb3dfa6865e3c3a1e181f661507`  
		Last Modified: Tue, 30 Dec 2025 04:46:16 GMT  
		Size: 16.4 KB (16447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1582-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:eed4d57bb438e419f2c41576e7ac3b6f88aa1fbc6aa6a02e5e203c55e7584330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (212997113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a0e3ade9bc1f40b69e84577ce55e5e217da631262ad79d04325b5efc23a1441`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 01:09:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:09:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:09:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:09:52 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:09:52 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:10:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:10:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:10:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:10:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:10:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9cc7bc8e086c95eb3e992d2c623bd505740ab0a6afcbc89656d0bb477878489f`  
		Last Modified: Mon, 29 Dec 2025 22:27:00 GMT  
		Size: 52.3 MB (52257770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d25990fe2009d48c227641398d913b8c8f5eb03d719463b83c32fb4bda40b2`  
		Last Modified: Tue, 30 Dec 2025 01:10:40 GMT  
		Size: 91.1 MB (91052482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fdbf2243bf1f14b193398947503d256a83661ffd614296bd24df1c293385d4`  
		Last Modified: Tue, 30 Dec 2025 01:10:40 GMT  
		Size: 69.7 MB (69685821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974c6d449247a7b2108e4f1386a12d3ee3fbd2cd45bb897a97618984560a7009`  
		Last Modified: Tue, 30 Dec 2025 01:10:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607c57852f3539b41179a6bb1bbb58053b147a0c8db1fdc372a1588b89e44456`  
		Last Modified: Tue, 30 Dec 2025 01:10:35 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1582-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:48fc15f5a89d3832ba1faa0b1f2d35e661f8ba877cd48f99865efe2457deed36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7368716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbc6f0f8dd166cbddf0c718351d7fab6057582b225cf753a2bae8b99ce4a2d7`

```dockerfile
```

-	Layers:
	-	`sha256:fbfde8d9f589c97a6ef00ddd68dc4eec383741d59646e5bd9d8bc19de2ed592c`  
		Last Modified: Tue, 30 Dec 2025 04:46:23 GMT  
		Size: 7.4 MB (7352127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e120aae358b573ec425978490ae73b6d8fa125e3b11d3d48c9209e6227d4368`  
		Last Modified: Tue, 30 Dec 2025 04:46:23 GMT  
		Size: 16.6 KB (16589 bytes)  
		MIME: application/vnd.in-toto+json
