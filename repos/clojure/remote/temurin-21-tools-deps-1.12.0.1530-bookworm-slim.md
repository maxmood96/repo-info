## `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm-slim`

```console
$ docker pull clojure@sha256:4dc88f55d2e637c953adc2518d332d7bffcc7a343c15316f0e2d33bbe2fd1e2d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:35d04b4347290e92d5e4a8dbc9d0e1308300765be634f72afc45029d9ee98fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255342598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bfe007f2c774d4c97018044fdb57c598b37e8959aec77269821dc62181d906d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4e98afafd787ff1844a33174594bfffe24f0fa42021a0d4e025b845c2edf92`  
		Last Modified: Tue, 08 Apr 2025 01:36:43 GMT  
		Size: 157.6 MB (157585931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2af0484eb61a0d7b5b604e74f76070a8ac73fd1b2f7d32d937883297511604`  
		Last Modified: Tue, 08 Apr 2025 01:36:41 GMT  
		Size: 69.5 MB (69528368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199d0e1bf42cffea63bed45cd8e7148d3982e80ac449e81b6f00643753f56a48`  
		Last Modified: Tue, 08 Apr 2025 01:36:37 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5ef343b9fe8ad50b460b2883abae6b1a2a0f3c1cc7e495d635c16331c5fdde`  
		Last Modified: Tue, 08 Apr 2025 01:36:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9c45039e4bb190be39126baeb1bfeb3f802a6d4975628d582ef3cf8b0a441a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4934338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b0b3617be45defeb8d77c48894962cf7e35c70ed4f2557937b0055696be5a54`

```dockerfile
```

-	Layers:
	-	`sha256:35b600d0385ebbcd5273fc54c6de754217fc0191bfda6ec6c4098dc5ce61a3a5`  
		Last Modified: Tue, 08 Apr 2025 01:36:38 GMT  
		Size: 4.9 MB (4917763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c328881501eb57833b27e10a526d4afb0bd13771540f0a2cb4642ce1858cd29`  
		Last Modified: Tue, 08 Apr 2025 01:36:37 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:79b65658a5777aca0448f664e01d9ea6bdef7d458bfeda5005d42411e9420dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.3 MB (253281917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293ec116b8bb45cf777536253b2c572e68f2a1f52ea48544321e9d5ba28599e6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb57ba6e2b02f933ad614475b6f0f15a4ad1d07504d61cfdc82617f99c428209`  
		Last Modified: Mon, 17 Mar 2025 23:49:19 GMT  
		Size: 155.9 MB (155859251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa805c91e54c462fec6302e8866098be6489f8ca6624bc22861ee1c5e1f5f890`  
		Last Modified: Mon, 17 Mar 2025 23:49:18 GMT  
		Size: 69.4 MB (69377589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41fac8811e6969d541dbc2d8fc508a95e59c8e2d79eef92774b0d9eb9d0fadb`  
		Last Modified: Mon, 17 Mar 2025 23:49:15 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80f3b38cb0a48573f67fb1b82af6da0ec79810531df44c6478f02bba3018122`  
		Last Modified: Mon, 17 Mar 2025 23:49:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:053d934bdbe7b1503d13b0bcf82511227a5f177015103c80a2b89fd5ccdb8e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4938896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee86154d473fa27c612dd5a9cb4641df1f70fdf135bae0fe0a0a941e05d8268`

```dockerfile
```

-	Layers:
	-	`sha256:44af36100606eda8c14d28f32164506c31f027e7e110b5e3bbafb2be3b23d40a`  
		Last Modified: Mon, 17 Mar 2025 23:49:16 GMT  
		Size: 4.9 MB (4922180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:005d98ff02d4650ee4242ddade0a1c069568dc3d13a72d37cae0115bf93c48d3`  
		Last Modified: Mon, 17 Mar 2025 23:49:15 GMT  
		Size: 16.7 KB (16716 bytes)  
		MIME: application/vnd.in-toto+json
