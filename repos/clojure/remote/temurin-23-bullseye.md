## `clojure:temurin-23-bullseye`

```console
$ docker pull clojure@sha256:d4033f353b1f1ede94fb24671159d0eee5a142beed7360df98637fac06b4ee0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:76224fd8b3c4f97dfb4eae08047892ce7d5d65cd855d638426aa2ea233771c44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288194912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b26fbf8af5cf3fb3baa933f815f11b1bb8e16bc5d4426c4aac4e2e293e4939`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43171f0fff6d7e05220f57f247b8664bec92091003532f51eec3ac0f95d09a7f`  
		Last Modified: Tue, 24 Dec 2024 22:39:16 GMT  
		Size: 165.3 MB (165295091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7819d9d6ad050d621d5e365fc1a6b580edad68b079a0bd0b0bfbe76ccfd9bd2d`  
		Last Modified: Tue, 24 Dec 2024 22:39:14 GMT  
		Size: 69.2 MB (69159825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b62a70726a6d22109c85fe4ccbe00522a82be69673dcc1ee248560460653af`  
		Last Modified: Tue, 24 Dec 2024 22:39:12 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e04045375256adeaabd151d9e8663e7a85e3adde1ca767694364eb83f9f0ae`  
		Last Modified: Tue, 24 Dec 2024 22:39:12 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:fa1a22771799b244443d26a071c7d53003cd0976145e92054b1a3dba3de0fada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7225320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcdb81edc812c7450b4738b881d2a534c52035e125a414cbfec135fa0049dcae`

```dockerfile
```

-	Layers:
	-	`sha256:c28f4009255e5e613632d296a8f85a52e5688f8d9f4c33bbce54b25d1566194f`  
		Last Modified: Tue, 24 Dec 2024 22:39:12 GMT  
		Size: 7.2 MB (7209500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7091eb782da275644ea9fd1128964350060f519599d48ab72b034ccce7cc6b75`  
		Last Modified: Tue, 24 Dec 2024 22:39:12 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9cd59b07f17287af9597046e26e65a3c85be720436db66038e9a396800b3c9b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284814545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:395d4fe682932d3fa30351cf173f46469304ab8157031ffcab0315652ccc172b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e357e1f94476a03fde298261e8c007d487d3cfade45a9eef064eba724a5c5e2e`  
		Last Modified: Tue, 03 Dec 2024 01:30:26 GMT  
		Size: 52.2 MB (52245994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c8e918cd2fa2f476de90384d529eaa69e1864493a438326b02dc1ef14b0a54`  
		Last Modified: Tue, 03 Dec 2024 15:34:06 GMT  
		Size: 163.3 MB (163281807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edadd1751380d3b5dcb92b6d0f7b582a3368df416114bac752a563fb403f9c4c`  
		Last Modified: Tue, 03 Dec 2024 15:38:13 GMT  
		Size: 69.3 MB (69285701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00371b9bbce58db30c8fb3a38326cc42b5c6b49be2437e308c15f961bb0eb00`  
		Last Modified: Tue, 03 Dec 2024 15:38:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3533cb011bc5caa899997bb664965021a702f53b4bd4710b9349accbdf7300`  
		Last Modified: Tue, 03 Dec 2024 15:38:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:eb76b6e32b281a0cac1df7673226572361de85367e388b97efaba2b9c5a7d6bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7239499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ed882846772dbbde651dd4ff29333e2e986e1f3469b5dcc216b81bc5b887ef`

```dockerfile
```

-	Layers:
	-	`sha256:691591bc4410078247613a2e20e1dd723938a44be9945a466c04d92e154281f8`  
		Last Modified: Tue, 03 Dec 2024 15:38:12 GMT  
		Size: 7.2 MB (7223561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61db430659c38e07303a0599b33648af1270509d8eb08a967dbae5b0feb8f226`  
		Last Modified: Tue, 03 Dec 2024 15:38:11 GMT  
		Size: 15.9 KB (15938 bytes)  
		MIME: application/vnd.in-toto+json
