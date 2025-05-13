## `clojure:tools-deps-1.12.0.1530-trixie-slim`

```console
$ docker pull clojure@sha256:4d5368a9290f54810803acc1d1ef76181be85eebb41818016ab6f476813fe820
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.0.1530-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3ae1d1918d8c3abc75445d5a7ecd170640068a7b6c2177c286df9e26091434c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259113372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13005b99416154850aff6cce79634011d790ba002b0aef621f865ddbfa27370e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3ae34fc80ed56f2b3a9a0b682b58e28e57fe981f5e514c3f687044f4b967608f`  
		Last Modified: Mon, 28 Apr 2025 21:08:25 GMT  
		Size: 29.8 MB (29753912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d442087327e103058d05d468d3f4ca801a98c2125c72af762dd5505946f3a6b4`  
		Last Modified: Tue, 13 May 2025 17:54:15 GMT  
		Size: 157.6 MB (157634443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c715d6c5c2be2cd2978bc378410277a9436e43a98682757be199c183476de5`  
		Last Modified: Tue, 13 May 2025 17:54:13 GMT  
		Size: 71.7 MB (71723975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330889c77699fd163694fe39a941fc372f8ed8487bc4240c67f14825ebb536e4`  
		Last Modified: Tue, 13 May 2025 17:54:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb92f5f477f1e3e8b51331fd3d58d5de8df0b7cc02d5b00d41208407da673e46`  
		Last Modified: Tue, 13 May 2025 17:54:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b3cddbf4349291a43c7d659ea634457249a4927c4c07a87c793eebb90f5fc640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b124dc9923750c77f74980c1cef27edc9a75c9dbe4a068ad2603260f6bf6cf78`

```dockerfile
```

-	Layers:
	-	`sha256:83aa6ca87948f797541b5f6e8ed2c87ced73afd398d4d79d29b411a240f9b73d`  
		Last Modified: Tue, 13 May 2025 17:54:12 GMT  
		Size: 5.1 MB (5070477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ef6b821ad4dff3e5b3b478342c162df60fe9b9b06604afe7f7f349c88b0295e`  
		Last Modified: Tue, 13 May 2025 17:54:12 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1530-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d5d27ddc491a79e10dfb5fa69542ce86d2d592071c904876938e7bcb6c28f9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257706430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147becddb78f8126b71dc19e74e75c87445dfb308fa7149fa5c33665c99df098`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d0342bfffaba1a8be0950e44b5334c6cf9a05d9eedd81a042ec7813ac91850a4`  
		Last Modified: Mon, 28 Apr 2025 21:23:36 GMT  
		Size: 30.1 MB (30130233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0151d89edf53b7ee6d783f7001ce04a78ae3663d78e9c1b824dc8cae0849315`  
		Last Modified: Tue, 13 May 2025 18:05:25 GMT  
		Size: 155.9 MB (155928823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7669214dc8fe5ae10e6b3a4b4fca0d8218c274db2d0cd6df6f59c802e00f5aad`  
		Last Modified: Tue, 13 May 2025 18:07:30 GMT  
		Size: 71.6 MB (71646332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0210c46ad4e8053c0ba5f543bcebbe44e1f6cdef2bfc7d74c5b23bda0dbc0956`  
		Last Modified: Tue, 13 May 2025 18:07:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8e768d28ed87dea6d27a23b370dfb67bc3041fbd3b149ce2e6a4a04fcab60c`  
		Last Modified: Tue, 13 May 2025 18:07:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1530-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3015c8c2c8e184b0bbdb43f4caace8057349cdd20c42150e338c53a836169c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5092955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d19a68587c0a02c777c71ddb24b5308f0d196920c927cd6462dc345ff54e6f`

```dockerfile
```

-	Layers:
	-	`sha256:2d666b701086e09986f6c9c9141c5b957d84a31b09f6e3a5cf782c78506b016a`  
		Last Modified: Tue, 13 May 2025 18:07:27 GMT  
		Size: 5.1 MB (5076270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ecc3a18fda201cd8a2e63658f61addc291d6f3ad5c3ce981434b2db358cb8b5`  
		Last Modified: Tue, 13 May 2025 18:07:27 GMT  
		Size: 16.7 KB (16685 bytes)  
		MIME: application/vnd.in-toto+json
