## `clojure:temurin-8-tools-deps-1.12.1.1550-bullseye-slim`

```console
$ docker pull clojure@sha256:9d5b657e8027df25c1cb040ef8de8c6920baeb28467ee99d6e851fcb3aaa016e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.1.1550-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:faf831f2fecb2322c9105ebc68d066674ecd4d6f45f14abe4339a66abb90e4b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143978487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67dc410cd2223b944e8178449315eeb3c248d6dade5d1cfd84c6c28f09e1dddd`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317741e06158868e7eb9db56aa2712e0eb4de8f00c6fb79a16eab0ab77179192`  
		Last Modified: Tue, 01 Jul 2025 02:37:43 GMT  
		Size: 54.7 MB (54716160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b187713dbb703dd8d313f8b31ce5c2cd5bcf04eb12593d1ae2de0718f9d1d184`  
		Last Modified: Tue, 01 Jul 2025 02:37:40 GMT  
		Size: 59.0 MB (59005635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ef5995f954d7fe3a6d1c8972827731316c2f0e3ac26495a7a728be66442768`  
		Last Modified: Tue, 01 Jul 2025 02:37:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:185975fb93cce5e2aa2b4737a7f240a0e0929d683ed62ea866fd7c9fb2756103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af5ff3d5d15d69ccf4297e00cf881b36f6162b9f68e579b1399fcb4cfeb3833`

```dockerfile
```

-	Layers:
	-	`sha256:2c80e902d072c03c45c59f7c8ae0e03859f7b9d677eb5dc2f113b54f87b6eb64`  
		Last Modified: Tue, 01 Jul 2025 06:42:24 GMT  
		Size: 5.4 MB (5429648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3944392a24eb7f299d8c51e0a7a556e506891849bb31652427622c2b3af903f`  
		Last Modified: Tue, 01 Jul 2025 06:42:24 GMT  
		Size: 14.3 KB (14290 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.1.1550-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:01eb6a4d3cf7630d1e475003f6f7dcd28874213e9ab37fe9d475412214df742a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141712863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da042f2c32747ad35b9d5083bc7970b4eb23f2770117a64bdaa572f0fb4fffa9`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:1efb2a16e6255fa81193190b623ba0668ffa777ab1de41ac5c5d2d2060a47784`  
		Last Modified: Wed, 11 Jun 2025 00:07:31 GMT  
		Size: 28.7 MB (28744185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7e3baf7d4680121659eb724482eb9337195e0ee91c7f53c31cb2abe7f12f04`  
		Last Modified: Wed, 11 Jun 2025 08:07:04 GMT  
		Size: 53.8 MB (53830508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd81f75fac0b29baa95db9bf9eacfda9395458a3803093279ab0bffb6750c55f`  
		Last Modified: Fri, 13 Jun 2025 17:48:50 GMT  
		Size: 59.1 MB (59137526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100d273c0a6e83cbc0599894b0adcf6ee11869eca846529e1365a9a9d4a963de`  
		Last Modified: Wed, 11 Jun 2025 09:21:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:242a6d6c0e5e7cbfb0f0d23a9fd04d3fb1908d39c412323c53b00fa1f0bb1e14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5450487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ae8bfd984aa3a0f4f59c6def66956a0537b62e14b55b2662cf3b92bd8b36fb`

```dockerfile
```

-	Layers:
	-	`sha256:1bb47bd9ddb08dc31bb1b0863ba35b5e31e3b091e39e0f73a47e8c933cbc498a`  
		Last Modified: Wed, 11 Jun 2025 09:42:53 GMT  
		Size: 5.4 MB (5436078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53a77cae02a282143a506fbfb87971fd63c016d9caf7e6ecd2e0f0db8c30776c`  
		Last Modified: Wed, 11 Jun 2025 09:42:54 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
