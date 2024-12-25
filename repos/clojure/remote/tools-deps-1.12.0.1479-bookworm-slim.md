## `clojure:tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:3a373f93105c5210703ee816ec878be07dd5f58a36b2fb887c873aa9a616f267
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:570cf91c920733028f3cf1a59b491f862d8b2343b4cd703476ee054218fa0b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255094510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57e6a428a3791b3e70fa317e45f82ef3d99157ba47e0c610dc9e2f8357946e83`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688fd16e9afddb6033aab9fa1a9a9052c33b294c202df5b2c80bcfd1abb85a7c`  
		Last Modified: Tue, 24 Dec 2024 22:38:31 GMT  
		Size: 157.6 MB (157568720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157593d36f039e662222aa39134ee088c1617ae2a65c0dc2247cf73ef6ee8912`  
		Last Modified: Tue, 24 Dec 2024 22:38:30 GMT  
		Size: 69.3 MB (69293171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcc89434e8961e12026e467f0c2f0ca3a5e72f8080b1d8f03ad164adf563b59`  
		Last Modified: Tue, 24 Dec 2024 22:38:29 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44afbcc1a8d3147c25d0cd80b9022f4219ea6b3410fe79cd7ffbfa0068f7b6fe`  
		Last Modified: Tue, 24 Dec 2024 22:38:29 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fd347de41e5d06c293253c926be0d29391485afeb32da444173d5d9c57437003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be64cdc9ed5e091e9bb322cca543d449a7aa446027b28f8c639581d96bb383b`

```dockerfile
```

-	Layers:
	-	`sha256:0b54d79517f30a7b6b260cde5704528126854286926f9808fe3756fa1d73d377`  
		Last Modified: Tue, 24 Dec 2024 22:38:29 GMT  
		Size: 4.9 MB (4916305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0749c3e7c1fea66ee2a624b456d35e3eb56df83cb1d36c73364bda4a08899ea`  
		Last Modified: Tue, 24 Dec 2024 22:38:29 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9ce4bd6cdc736c0213038ff1f622f3cdf727e24300e82745ae2073326657d7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252994066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a8a27145b1a23ce8a51065744d26951cb9442bb29f9886d4bd902ec12a641d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260e6f636d1eb05d00e219fab56e3c7bcc3684217f5d55e0e62a3009ee3468f9`  
		Last Modified: Wed, 25 Dec 2024 07:31:19 GMT  
		Size: 155.8 MB (155793090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b01f8f6fa963d34e6fa754c871ac641a9e90ad6ccfc93e963a5e8c58d4f65c`  
		Last Modified: Wed, 25 Dec 2024 07:34:45 GMT  
		Size: 69.1 MB (69141214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73d41257067f0d1c81602a42f93bb99ccd2b2112f3a8d66470125b9383c093f`  
		Last Modified: Wed, 25 Dec 2024 07:34:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534323e4b4041301782f5cc9544ef54b16d8482812f45b02a8966a40bce0b740`  
		Last Modified: Wed, 25 Dec 2024 07:34:43 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:984ba73ac6fc7568c75330cfeedab5ac103396241919efa895582f8e636e9092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4938807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2a5bc91d2b7e4125ef345de6e7c05427269ae816e24419a16e3e4f30356cc52`

```dockerfile
```

-	Layers:
	-	`sha256:7b956811525c4b99ba177a4aaae565eec91fddd1bfe534ad1a4c21256f724fa6`  
		Last Modified: Wed, 25 Dec 2024 07:34:43 GMT  
		Size: 4.9 MB (4922090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6531ed08d793b675152efd4f159e1fbd3c8f9037aecf274f4f89b680a5e36d02`  
		Last Modified: Wed, 25 Dec 2024 07:34:43 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
