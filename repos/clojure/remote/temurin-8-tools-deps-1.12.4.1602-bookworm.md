## `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm`

```console
$ docker pull clojure@sha256:05657f576c1c9d521e73b3342c8c8e5dfac9caa9edb4745cb9684c60e9a39913
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:c041842281e41b5b35accb27704779c97f6ea1c9039d6c426ad299b876fc75a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184802964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730e310bf1472feb5423389854a73b88e994ac7d67d07e1d224a8d7c12ffe2fa`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:40:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:40:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:40:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:40:47 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:40:47 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:41:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:41:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:41:03 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e83775579f1a8b3c6b48d04d75a0c5fb566aff9692e0a0342e4643920ab6b5`  
		Last Modified: Tue, 17 Feb 2026 21:41:24 GMT  
		Size: 55.2 MB (55170117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b25116f70941d71d5bd90c40fd3fb799297dc667cf2b16ae3f10f44b7d29dfc`  
		Last Modified: Tue, 17 Feb 2026 21:41:24 GMT  
		Size: 81.2 MB (81150719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e364350ef7ae1886569dd945c570145540834b7269fff05cd024bd515f5947`  
		Last Modified: Tue, 17 Feb 2026 21:41:21 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:300ad7128854ab691e1ec62412f8fe8479fce163cec48491880730ebea1d29e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7511970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc3a1bbb3a343dbf5cd5964706a5c3c0218b728cc20af4649e37bc10128ca20`

```dockerfile
```

-	Layers:
	-	`sha256:904df6fbec45e41c4372ad77bac847c93ed0e62bb3b67aebb1bc3fe1f688397b`  
		Last Modified: Tue, 17 Feb 2026 21:41:22 GMT  
		Size: 7.5 MB (7497776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9410692a88e5efe8951b23dfd620a3dcc68ff426baf675677edc5063e06bce1f`  
		Last Modified: Tue, 17 Feb 2026 21:41:21 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d941cf5df3f825d34e01065c59078d63c6f40c481e82cb103a77fba7a12cf8c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.8 MB (183756524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17853509b75235dd4e1ca011b6ffef5ef6e4b67b166eca45498d652e8ef91906`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:40:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:40:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:40:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:40:39 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:40:39 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:40:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:40:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:40:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b86dd18bf76e7b4818cc5367b487ea19bc222d06add7f1e12b4aa28ad8002c9`  
		Last Modified: Tue, 17 Feb 2026 21:41:16 GMT  
		Size: 54.3 MB (54251639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585d17e84a8ff3029c287c327375bcdfef369d84a3a9151531e46dd9ec22e45b`  
		Last Modified: Tue, 17 Feb 2026 21:41:16 GMT  
		Size: 81.1 MB (81138282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d91ac38e28ba29cc7445ac3c4b935ffb5af88150823d437c38347c33a92fcb8`  
		Last Modified: Tue, 17 Feb 2026 21:41:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:69118b925f85b51a5ee774c0fc60d8bb07cd67e204ef7315723db3522713859f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7518551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b135c4ac2db26dbc3bc2732441cfe1f47881e7b8911746f6d159e09d39d4b8`

```dockerfile
```

-	Layers:
	-	`sha256:9bce8aa32eed271348bdb02ac04fef5129c1b010dad77339aafd6ed6acdd4ab6`  
		Last Modified: Tue, 17 Feb 2026 21:41:13 GMT  
		Size: 7.5 MB (7504239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15b6e7afe9061e7bf3888cb8a000d8124bc49c4186fb1a259b2c14dbff956c6c`  
		Last Modified: Tue, 17 Feb 2026 21:41:13 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:1c335c7b17774e2c787f6233dda80606bd7f17954732934378121667aa9c06c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (191965445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec9c9a187d1c84db1f0ff09d3123c270e610e6c14a30555ca227e6b405a0161`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:55:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:55:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:55:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:55:41 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:55:43 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:03:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:03:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:03:13 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081c85e0b853be6e0d03b2fbec5e5c7dc3f5e5b6e6f27d9574958d9f52776d65`  
		Last Modified: Thu, 05 Feb 2026 23:56:59 GMT  
		Size: 52.7 MB (52650375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a2f301a831dc7cbc558f088450c2cf45b3c5f2e488ee9f6ea35709dcf89fd6`  
		Last Modified: Fri, 06 Feb 2026 00:04:05 GMT  
		Size: 87.0 MB (86987133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d705504f3e16763e7ae933471916cd0d41c2e47031f616a694a9732a7532cde`  
		Last Modified: Fri, 06 Feb 2026 00:04:03 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6c83e5a581f353fe1d2ec01c1b8e95d79b03b4c5252f1a7b7bf535d672a5622b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe4611e5836c925f719b615df4bdad38ae3f462ccf588cb732c8756475619f3`

```dockerfile
```

-	Layers:
	-	`sha256:ae7d46c3f73bcd6d4232ee61648455a17ba4f2e1cd1d9983342acf355183af43`  
		Last Modified: Fri, 06 Feb 2026 00:04:03 GMT  
		Size: 7.5 MB (7503587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c6a091d696c4728369e7bae9c0b875ee21b12f12ef952ff7e077db3ff1c74d1`  
		Last Modified: Fri, 06 Feb 2026 00:04:03 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json
