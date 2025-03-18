## `clojure:temurin-8-tools-deps-1.12.0.1530-bookworm`

```console
$ docker pull clojure@sha256:db50220e920427dd0c2066c507c35138201f52cb585c3e54e7f4183b0727ef35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1530-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:d3051458efcaea7fd91034a00a0e4895cc980e41075f57ef99f485f0ecd5e17a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184183685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9882f9ab071ec53abf04b6e48138a6300ca084a9af7a103c2d790e2052230189`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7cd785773db44407e20a679ce5439222e505475eed5b99f1910eb2cda51729ab`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.5 MB (48467838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26191ead8625987e6d8638bd5595e5d28363f8698f3f081a78871f1c42a7ade`  
		Last Modified: Mon, 17 Mar 2025 23:20:52 GMT  
		Size: 54.7 MB (54721246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c332d747189490676850a236b186485258adf794382101e4eadeadd7012fdeb`  
		Last Modified: Mon, 17 Mar 2025 23:20:53 GMT  
		Size: 81.0 MB (80993956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3baaa5dddde90c53e57c50436d7153753b286a21d8ad8aa5db68d9d66ee17c5`  
		Last Modified: Mon, 17 Mar 2025 23:20:50 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:df36bbfa91a9e8ff1aef7887d63b96a4bfea6ef5d1e33dae9f584f4f50c215b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7306955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec21a0395bf14c30a943df589dfb5dfd64d264aafd565c7350f116f219514bf0`

```dockerfile
```

-	Layers:
	-	`sha256:4fccec45efb55687d8a65056ce549161e9bafb9c300008ca6a2828c58bd14415`  
		Last Modified: Mon, 17 Mar 2025 23:20:51 GMT  
		Size: 7.3 MB (7292718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec3f4771340c33f55aaa07424c57de56afaa814d261b0928f054d07621a53b31`  
		Last Modified: Mon, 17 Mar 2025 23:20:50 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1530-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c409b63515b739ef05927579f2eb8073218c8fa9c5cf4f350946229eb43d6c8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (182970930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc3468f5e72a3aaad4d72b195410e8ad3a7e4fc11c4ec6208581b8329840ae8`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71e06352f37c6d0a072e8047fbee028b939a5c468a25e662d78194bd7f4e0cc`  
		Last Modified: Tue, 18 Mar 2025 00:16:09 GMT  
		Size: 53.8 MB (53822757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf58d16ab08cf851492828988b0961f64b20ed072b9d326ed3bd38ac732df8e`  
		Last Modified: Tue, 18 Mar 2025 00:16:10 GMT  
		Size: 80.8 MB (80842675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566233326d937ad79cc6669ee636d4e23fb0352ab6507a9fff19f6e5af66ab22`  
		Last Modified: Tue, 18 Mar 2025 00:16:07 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:34056a9c89e8d2f941f510a45fdfdd6f3a06f51452b2c8265f757bd515c061cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7313534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a6be3ee9eccde447355b76c7ffb9ff223ba00bac76c236a7f63f982b1c87eb`

```dockerfile
```

-	Layers:
	-	`sha256:fef98b71a502003a6b2bffce97409e2789520473e89342a43c7b40fa9ae8d873`  
		Last Modified: Tue, 18 Mar 2025 00:16:08 GMT  
		Size: 7.3 MB (7299179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6261f97b26a2afbbc653376b7ed646ffe361a07e21f00664e8bf566b177b9d5d`  
		Last Modified: Tue, 18 Mar 2025 00:16:07 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
