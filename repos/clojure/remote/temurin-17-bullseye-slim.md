## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:dd184fdf266f82053c37483656cec01672da9588e6abc8d7d471999fd5d2fde5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:447b27f8e440e2edf9d3df28e86ac124b4ff73fd62c1d3f035af9cc57f65daa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235050961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af282a845533c33c5512acab1b1f58af611eb423c9281f3a4eff5874bf088833`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:55:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:55:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:55:29 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:55:29 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:55:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:55:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:55:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:55:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:55:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e6dd252cba243e33351b8f19aae7663b72e36616e5c348c8e805dc10091037`  
		Last Modified: Tue, 24 Feb 2026 19:56:03 GMT  
		Size: 145.6 MB (145628710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8af3517dfdd5ced673b224e19c5a30709eabb0d6384a2180a36f7675dcdd98a`  
		Last Modified: Tue, 24 Feb 2026 19:56:01 GMT  
		Size: 59.2 MB (59162833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbd1b6218758add121ecca13022efdeb0e42218bf3ff4bca9091d618f8e6a99`  
		Last Modified: Tue, 24 Feb 2026 19:55:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a90957747dce3f4d2f9a810cf95ec35cbaba98eb906837b45dc2793a38d8e24`  
		Last Modified: Tue, 24 Feb 2026 19:55:58 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8157a5c7ff9bacea9c7444a913240550b4d86ede914797d8f16c356d019d6c8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5336000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865a15bfa1c59d518ca6ac279ed569fe84e376a92364c4d92312b5e7e4656906`

```dockerfile
```

-	Layers:
	-	`sha256:b2ce80ce8df7aea94c914ee9b8f92402223361285eead4480bac1612c0cdfade`  
		Last Modified: Tue, 24 Feb 2026 19:55:59 GMT  
		Size: 5.3 MB (5320164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e998b1ed79a0f932b2ce370f22944cf54d962ad7e5b87ef04b65a3d80026381`  
		Last Modified: Tue, 24 Feb 2026 19:55:59 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:77207f69f78684a49db43094951a893458a8c7aae65907664fe77efdd8bb71c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232484954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c40f09ae86069bdeb927f2a1c6ecf40e92e31c6e8c188b36a3ee9e066f9b62`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:30:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:30:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:30:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:30:43 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:05:48 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:06:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:06:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:06:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:06:02 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:06:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652594bff40e944dac4d4a4e91bfb8c86f88fcc29cf9cc65aaba4b881bc692f2`  
		Last Modified: Tue, 24 Feb 2026 19:31:48 GMT  
		Size: 144.4 MB (144436199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fe393eae7227b8c5073c54e850763fd5c8470ff43e54c6a022bf45c9a2e8c1`  
		Last Modified: Tue, 24 Feb 2026 20:06:17 GMT  
		Size: 59.3 MB (59303246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8dcd7bfb715effa2a392e9432724ce17fc88eadaf4eb8108e6ffe52859801c`  
		Last Modified: Tue, 24 Feb 2026 20:06:15 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb8686a24a55306b03a54451bbf623e889d33fd892479674dc13b8b0e4e8196`  
		Last Modified: Tue, 24 Feb 2026 20:06:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5ab2656cf7be120f438a06cbcd656e352da9c55db7e70cf190e9268848fa0e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5341850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f5f9866fb3712fd41bc79b3d30ea789a6395b29c882cfd96ad6d450c5664d7`

```dockerfile
```

-	Layers:
	-	`sha256:c88c966e6efecca9934ed93c10a60d91d1e294ca520b7fd5c29151761e8718ce`  
		Last Modified: Tue, 24 Feb 2026 20:06:16 GMT  
		Size: 5.3 MB (5325896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0f9d6779d25e9bb9d280306634f4a89c00a987ef55414f9127f772752c334b2`  
		Last Modified: Tue, 24 Feb 2026 20:06:15 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
