## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:8a4c13ad0a347a1c2f1b5ae61c07dcc35f74e4fdbf1f1722f99c9fac23efe336
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2d40bfb90fb2cda3bc2d2604918f6d2d61253884bc08b55babe2997ee7d8afc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152639951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afcbe18d782822cd62de3c78aaa04f64a5974cf9e871917730965bdf190b8130`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee21f42dafaea8ab250cc6a7e75f8a211174a42326407a201a411d46cd40139d`  
		Last Modified: Thu, 09 Oct 2025 22:26:23 GMT  
		Size: 54.7 MB (54731352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82290a3002f2264e1372fceaad9c60a8ef8931d01b4521381e068019e5b81e4`  
		Last Modified: Thu, 09 Oct 2025 22:26:25 GMT  
		Size: 69.7 MB (69679620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d2130c1a1a86ce85eaa33e47d9e0ecebabfc5a01daed8b8a7b90f51bdc06b7`  
		Last Modified: Thu, 09 Oct 2025 22:26:18 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cd80d8cdfa6ffc14a607d68ecb7d67307ea070d5c7aa0afa6f79af2eb51892c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01fe2e13e72d55c358bc8315f4be242faf8df9fe442297fde701ff40169fb506`

```dockerfile
```

-	Layers:
	-	`sha256:d4ae7342bf0af297f54c73265b233283e30edfdb43b13ffad575f535a980648c`  
		Last Modified: Fri, 10 Oct 2025 06:50:06 GMT  
		Size: 5.2 MB (5234998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74cd6edead62c1bce1a7efd12ead74f2aa8df3d56e859d25334cedd6b935fea4`  
		Last Modified: Fri, 10 Oct 2025 06:50:07 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3450e9eaf85b3a72a05e2236c4c9e0824d0931511d7cd626366d26da515ed0a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151498599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e54ac1e5c23421df13131065ebeebc95c34c77534ade1d6692f5c7e5ed4e865`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d088abfaa253d4a3b6288ece152babd3cc19690e94ed18528f9b24b7577aa9d`  
		Last Modified: Thu, 09 Oct 2025 22:26:27 GMT  
		Size: 53.8 MB (53835637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2faebea61a01f0a0166d2e7c8ec3d39707bae4f0d5aabd5e256f6019d0e4c8`  
		Last Modified: Thu, 09 Oct 2025 22:26:28 GMT  
		Size: 69.6 MB (69560172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db33983e0c699462fcfe6c8f04ee531ea8458e3c25e972b7452fcd4ec68792b1`  
		Last Modified: Thu, 09 Oct 2025 22:26:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b177e6af3e540ce45c5d3bc9e26f11a42ad4ec494ae84600bb11e2cf54e86223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d503e01cef5aa1d7d1635822e622f4a5c813a30f1135bf4024ade0bbd6e5b60`

```dockerfile
```

-	Layers:
	-	`sha256:e483b3652c67a950ff4135d66af3680b55d6c210f58135cb945a9e6fccedb149`  
		Last Modified: Fri, 10 Oct 2025 06:50:11 GMT  
		Size: 5.2 MB (5241457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a5ed222bc453c5b516ca472e686df4fb99cb1df9c018098f21aae3253d512b9`  
		Last Modified: Fri, 10 Oct 2025 06:50:12 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:22c3837338c95617ec1bc39cfb648924de17babcd30232e16eb561ff4f1e60af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159747432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c646621a43240d6d51e67fa481e7bc8842e438daeca45b4c45e77f84e63f8e5c`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4808b36faa8f51beaeed0fb85c1eb939ecd3b64b53ab9d96dd338710855719`  
		Last Modified: Fri, 10 Oct 2025 04:43:21 GMT  
		Size: 52.2 MB (52165456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d79c8b67448cd151c1713b590879b817aae9839797f59b343232e0897fe1085`  
		Last Modified: Fri, 10 Oct 2025 04:50:36 GMT  
		Size: 75.5 MB (75512634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d64460c01bfcac62d6bb3dbfea275fc6344fde0665158e7fc26c7437a079f6`  
		Last Modified: Fri, 10 Oct 2025 04:50:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ecdc0394ff5cc6f958d10651ce2443f405c287f86dd3234c01dccbee44deea5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be05a028f2ccaf99ba7d11a531b927cb741147db0fd7e825d78615deb0780977`

```dockerfile
```

-	Layers:
	-	`sha256:387f93e3f63ce5ff22d871c6b9f8d46a01f80f20595fa099005139083709f230`  
		Last Modified: Fri, 10 Oct 2025 06:50:16 GMT  
		Size: 5.2 MB (5240749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a72bc6799b3d8002bec9c65dd0aa9e9e29562e133e47503f34e281e9020218a3`  
		Last Modified: Fri, 10 Oct 2025 06:50:17 GMT  
		Size: 14.3 KB (14338 bytes)  
		MIME: application/vnd.in-toto+json
