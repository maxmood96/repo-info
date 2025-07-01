## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:d574ed3521542a0498d1fc1b2ebbfdee3b315baa4a3f178f01d65abab5f9783e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ac92dd8fa79e13cf10b5864e43f552ba22ee6f96ba987314b29903ea8124612f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246897297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3249a11770e262eb66affe9a892b3187b0c88ebba77facdc1d0724c87d3bf2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c31cd5c526834225ac1d69b43027ec668b7d99742f42f1b857f06f0ae6b53b7`  
		Last Modified: Tue, 01 Jul 2025 07:08:44 GMT  
		Size: 157.6 MB (157634498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab25fe7e0a9ce031433bb201f75666154389e2fc098dfc1c709ce7543a1ecc4d`  
		Last Modified: Tue, 01 Jul 2025 07:08:41 GMT  
		Size: 59.0 MB (59005712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b62e680f7b69132c1b86fe39d3f7f590ad4e3dc2e2360d8a1f9185f6f0bed5`  
		Last Modified: Tue, 01 Jul 2025 07:08:38 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c0f487c4187416e7f3003fc9c847fec686ec530b153635f62188ab80ad98c4`  
		Last Modified: Tue, 01 Jul 2025 07:08:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8a6fb11d3fb188d7b841b85116233ce4de9e0f1a9f14fe02d55592ff889864a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5328410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6485cdfdcae9b46e483e3f12fbbe27797953276b7a02f708a49f62d222500181`

```dockerfile
```

-	Layers:
	-	`sha256:208728994c4a4f8e4394d0a9d67167a1f9fde8510e37b0828bf70aca8829e959`  
		Last Modified: Tue, 01 Jul 2025 06:38:52 GMT  
		Size: 5.3 MB (5311836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0608f408a5a2bccf48634f97669d4bf88925673ff86f1777bbce3d3bb28ceaa0`  
		Last Modified: Tue, 01 Jul 2025 06:38:53 GMT  
		Size: 16.6 KB (16574 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:31ccc8b248dae681b23a5a2abd4432b8d90611b2607c616a8d51ab188d0e1967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243811685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1b2469c42a6b5c65810874b85c7688a2d041ccea1b043e9d19ed3bf947d2203`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f209ff44f683a19134a65d227eda78e676586776061dfd6857f025b7df4f82e`  
		Last Modified: Tue, 01 Jul 2025 08:48:37 GMT  
		Size: 155.9 MB (155928823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a39b68a7392be54b060b6ca3c7ab594a1ec8d5e330f0570f50195076fa123f4`  
		Last Modified: Tue, 01 Jul 2025 12:34:17 GMT  
		Size: 59.1 MB (59137685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99c86a05836c56c351a218beaf651e0e922b704c361d8561ff8b6e991f09a87`  
		Last Modified: Tue, 01 Jul 2025 12:34:13 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2e8a88444b9a226aef77caf293df982b9c13523262ded92ede654a1b7a4409`  
		Last Modified: Tue, 01 Jul 2025 12:34:13 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8838b6062004f0c6aa2b33cafbc76c5dc4639f21a39a2e3fe156b52c46ea60d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5334309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9761acd868c19463e15b5e2238842bea08a9196ab9963b50a1755ed340f1a38d`

```dockerfile
```

-	Layers:
	-	`sha256:13a511993d4d4aa5928040288648d9efa71cbed669bc15a54bf9d4ae0a488b7d`  
		Last Modified: Tue, 01 Jul 2025 15:38:33 GMT  
		Size: 5.3 MB (5317592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe3572d2255b3f2c01757e3f567a7287ff5af382ab31e79b01956d35891aa074`  
		Last Modified: Tue, 01 Jul 2025 15:38:33 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
