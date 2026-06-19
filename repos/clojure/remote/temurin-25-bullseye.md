## `clojure:temurin-25-bullseye`

```console
$ docker pull clojure@sha256:1229a4460edc42569b304c01c89c33dff251df28bba468cda8977931533307f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e3d6d20265f41e6a0466de41e981a67c1c1962701b1b97c987873c64842255ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.9 MB (212860013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:832ea6cddcd439cdcf69fdb2dc08e67963a9574aa63f1a479a12da6902e05ff5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:20:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:20:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:20:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:20:17 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:20:17 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:20:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:20:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:20:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:20:30 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:20:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b65b44e18cece837832e647ba74a14b7337485d665d5b30d966f3848e562325`  
		Last Modified: Fri, 19 Jun 2026 02:20:51 GMT  
		Size: 92.6 MB (92574566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e09811e57fa8321c1ca3285093978610d841d0b9324ef7b343a54556b5ba8`  
		Last Modified: Fri, 19 Jun 2026 02:20:51 GMT  
		Size: 66.5 MB (66512638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77838dcfb6bd56ced09671d4d451e6d7ef92eec85a7abcdfafcf26a2f7d83972`  
		Last Modified: Fri, 19 Jun 2026 02:20:48 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c000a23215a78d0694b49ba033ff477aa9eeeec9b8bb81fb356be79a4f175b8d`  
		Last Modified: Fri, 19 Jun 2026 02:20:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:383ffb85d3146ce796f406aea0a920ed8e88a6a6fd9a9c55454b5db38b721052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7391744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57fd7b2bbf2f1af6b967e4f71b89987d14bcb9b9cdabf09b2ffb949f194ca873`

```dockerfile
```

-	Layers:
	-	`sha256:ab1d4fcbf973bce55804c03cbed89aa34a4db5a30649fac88c25d3b5307e8bc6`  
		Last Modified: Fri, 19 Jun 2026 02:20:48 GMT  
		Size: 7.4 MB (7375143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c573430c3f94588422da0213ed5340cb4e5a61a2cc797f98e7782756149c5d`  
		Last Modified: Fri, 19 Jun 2026 02:20:48 GMT  
		Size: 16.6 KB (16601 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aba18c450e1984530580edc856ec1b7ba3bad2b9ac8d3a32a085380918e235e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.5 MB (210485525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87beeb69da7f783a45c48ce308b70601a930884e61bc405f4d6d22e634645c3b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:20:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:20:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:20:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:20:42 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:20:42 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:20:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:20:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:20:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:20:55 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:20:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd6900752c26eb7bf125402899eb89b75ff97244dc9d1958dc0c5c4acd5fff0`  
		Last Modified: Fri, 19 Jun 2026 02:21:17 GMT  
		Size: 91.5 MB (91542236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5c2afd3f56a3875cb29c7dc3fd1ff533f608c0f930a1b7a01b0ef6c67c7e67`  
		Last Modified: Fri, 19 Jun 2026 02:21:17 GMT  
		Size: 66.7 MB (66678132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b296100441b0ee5de8d683ae8be323ec72c5911e3beb0f2e382e7642c5fc37`  
		Last Modified: Fri, 19 Jun 2026 02:21:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28254580fea14a2178ecd633047351b2b3c6cb91a8fc6013ff9cfb6b82b5229`  
		Last Modified: Fri, 19 Jun 2026 02:21:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d5cc293979d6f110c9f360da1391d3e28292ebb7a45a68907093aadcd427e469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9097b8874e54a60e4e45b6c76b117b696b9a1f1eb3d21412e1a0eae8d1a5d694`

```dockerfile
```

-	Layers:
	-	`sha256:f75ff8cd2b15e672846e85d539e6bace57ff711e866c628e676e23eb2f3ec792`  
		Last Modified: Fri, 19 Jun 2026 02:21:14 GMT  
		Size: 7.4 MB (7380263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0aed81009dc04ad6b8562ed101c95d8b43278ae66dfe6439d861be6782c46a5`  
		Last Modified: Fri, 19 Jun 2026 02:21:13 GMT  
		Size: 16.7 KB (16743 bytes)  
		MIME: application/vnd.in-toto+json
