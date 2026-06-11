## `clojure:temurin-26-tools-deps-1.12.5.1654-trixie-slim`

```console
$ docker pull clojure@sha256:dd543b813ba5fe367e437437cda386a120d53c59cdfa303c9af4ef405300cb27
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

### `clojure:temurin-26-tools-deps-1.12.5.1654-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:dbf906a6eb9ab6b062270b3b7842bb05e10eb12d36157c08952d9723c8f21d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193262465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:535da20a2f66f3a2c7a8cdeb2b3135d7f0d6c30b9bfcc96c51ffdec4a66bda78`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:22:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:22:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:22:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:22:26 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:22:26 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:22:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:22:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:22:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:22:41 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:22:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ec0e1a058d2d2d6f21d1a2165e6c385eddfafcb7e505f616446f42baa077c3`  
		Last Modified: Thu, 11 Jun 2026 01:23:01 GMT  
		Size: 94.5 MB (94524388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d74b0aa08aa26328968ed61bda78ae0f49dae5830304322d5c18fd561f47a2`  
		Last Modified: Thu, 11 Jun 2026 01:23:00 GMT  
		Size: 69.0 MB (68951623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08efb5baa73de3349e3f6aed7a9fbab6e9c9287531c94fce2023e71300eb97b`  
		Last Modified: Thu, 11 Jun 2026 01:22:57 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45356d4f2a5b67031a27e737ec6dc393ef0671459c56bcabb2f855be9c5b3182`  
		Last Modified: Thu, 11 Jun 2026 01:22:57 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5af0336632f9a9734dae81bcf4919b40af987d05603a5fd28894f188e55ca4de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5238092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a121ec23c9de4a752e29b125595893939c5a1f71df3c68fa5c29ca6cb2dc80fb`

```dockerfile
```

-	Layers:
	-	`sha256:89e1d247228147c40c9a27c88dcc41f24e9fe9d75e3a29d0037548ac2170a7f3`  
		Last Modified: Thu, 11 Jun 2026 01:22:58 GMT  
		Size: 5.2 MB (5222133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:414e9821499d39e8ac4d4aff321b8248dfe89e6df8a2bc41a3198e3332977bf5`  
		Last Modified: Thu, 11 Jun 2026 01:22:57 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1654-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e99079e72be928237a5fee7916d1eca722c5fec42f92b48f013fd52b2fb44368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192431290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26d4c97b82be47b559a79b89e6606ecadc82dfd1cc0a83cbdd37ed2d055b4ff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:26:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:26:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:26:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:26:44 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:26:44 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:27:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:27:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:27:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:27:01 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:27:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650a0df9b4274389d9cceee6d7b13bc75806697f48c4b79c7f3a7e24c5aeabdb`  
		Last Modified: Thu, 11 Jun 2026 01:27:23 GMT  
		Size: 93.5 MB (93504349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ca7fbe79baddc9bf6fb2020a6854b3f1dcefde4cdfb3514d6eadf7a066cfdd`  
		Last Modified: Thu, 11 Jun 2026 01:27:22 GMT  
		Size: 68.8 MB (68777373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3934dc4c8ec2f8bc556ee4ea49257915f2ff14ae29375696d21024555b0eb3`  
		Last Modified: Thu, 11 Jun 2026 01:27:19 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88cbe2911ef3e003db2b290e103d59fa41d4cd2dedd453ab1afaf80e623b6a16`  
		Last Modified: Thu, 11 Jun 2026 01:27:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7d77ef7fc4701b3266638b2f6717069bdf742ec513b7db6569403307a53625a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5243968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8ff35d92f3077ff2281751fd8020b83191243ef6ea9319ae1d4482d1ea23a2`

```dockerfile
```

-	Layers:
	-	`sha256:2524937bf4fd4543cf495c938c4c0830152711b7553d068fe0e9ec05609560d0`  
		Last Modified: Thu, 11 Jun 2026 01:27:19 GMT  
		Size: 5.2 MB (5227891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18a36303b4fa86b156e62eace18c536ce168e6809ad1c2dc5b34fe87094b7d13`  
		Last Modified: Thu, 11 Jun 2026 01:27:19 GMT  
		Size: 16.1 KB (16077 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1654-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:cda5154c751026184b430a854bc70e1f6efa87c19b685e11a1a92ff2f52334c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.9 MB (201872888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a113ff1630af652abc13d8727f9edac59027fe34e45bb17a25606f81804825`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 18:11:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 18:11:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 18:11:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 18:11:49 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 18:11:50 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 18:12:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 18:12:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 18:12:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 18:12:33 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 18:12:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f636b6ca285aa4b80f814ff4cd48e03ca678cbc494379c15e3bad72919b21fd5`  
		Last Modified: Thu, 04 Jun 2026 18:13:14 GMT  
		Size: 93.9 MB (93902081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c58400a390e56b41a82a63618b94da041df19edad3e213dddb1d4a476b4282`  
		Last Modified: Thu, 04 Jun 2026 18:13:14 GMT  
		Size: 74.4 MB (74369309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1eaa3d8c91982554b51e311003612f0bec24ac01e6e1c5ada3daac8ee5c0ea`  
		Last Modified: Thu, 04 Jun 2026 18:13:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c49dc6ee02244e4732d9e27a5cf892eb2fdb74011adafc8ef92cfba49d570f`  
		Last Modified: Thu, 04 Jun 2026 18:13:10 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9a79d5a44c9ba3cf3b5214e37f2cdbf1f81109ffecafe8f14f1714f5c8d7d179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5226447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfad9a9bd61b935b0eecfb093574e60a775edadb8f9a4fae9ba4bec2e620435e`

```dockerfile
```

-	Layers:
	-	`sha256:4566d547b7aabc17700b41d1505be6630350b11e74548058833d77d38f07d3f7`  
		Last Modified: Thu, 04 Jun 2026 18:13:11 GMT  
		Size: 5.2 MB (5210440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23ac0b681f4c8e100ee1b95b440611f97d52583620d7db7fa44f73967601efdb`  
		Last Modified: Thu, 04 Jun 2026 18:13:10 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1654-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:dc6a1a9fb48f51ffa4c8ed496633f18bdcc353f9a64ac55f1613775092c276c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190321840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:950350ce58cb4cf64b972d9a4964fa1c7f111e31b8f129254359e6092efa8729`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 03:17:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:17:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:17:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:17:27 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 03:17:27 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:17:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 03:17:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 03:17:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:17:42 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:17:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f3ae1604951f3843a1ec1ff3de5fea3c9ce05428295a11008e69f46442246d`  
		Last Modified: Thu, 11 Jun 2026 03:18:11 GMT  
		Size: 90.5 MB (90536949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673f5345cd7b92827641cbed34999114a0dfae6336b6997cd0326dd29ad19834`  
		Last Modified: Thu, 11 Jun 2026 03:18:11 GMT  
		Size: 69.9 MB (69932496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d1ba25f19bb114e657ffb62b43d09cec7846cafe6e207643efa7401b3c71fc`  
		Last Modified: Thu, 11 Jun 2026 03:18:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f9504164a0701ca09b248d24f2832710d684399fff76f835242707468de916`  
		Last Modified: Thu, 11 Jun 2026 03:18:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1ac5a8671e0f6ea8c339507ab5ec87be89a4de42c8ed0ed7dd36db905870099e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d721e612cbcdb91a5b9c0fc189f0075bb280c7c8ddc76dd36848e15aacf03dfa`

```dockerfile
```

-	Layers:
	-	`sha256:bc13d7d3847c415e60573e281bcf6b55822c436ee826d6333707f9fa89770d9e`  
		Last Modified: Thu, 11 Jun 2026 03:18:09 GMT  
		Size: 5.2 MB (5203243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33564fb6b5ad34e7be7c75d337412c158a767b4fbce9de40d5f8597fc1614614`  
		Last Modified: Thu, 11 Jun 2026 03:18:08 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json
