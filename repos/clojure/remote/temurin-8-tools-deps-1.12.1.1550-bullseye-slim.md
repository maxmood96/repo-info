## `clojure:temurin-8-tools-deps-1.12.1.1550-bullseye-slim`

```console
$ docker pull clojure@sha256:f484c4f880e5f7d09b4fe7e18853a9a229e6b5ab5fbb251a36a9adc0578fb5f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.1.1550-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8bfb126e1c87c73dfd9222d0ee93c25326eef9996dae81b4c41db803ab810173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143978399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90db78cc7c497d94c23a9b6788248fafc08b1db6aa4e41d4c172d4bba1a50437`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:3d79ccbe0210f4986821cddffc5c7fc6551d938e282044db7571e448bde1e24a`  
		Last Modified: Tue, 10 Jun 2025 23:27:03 GMT  
		Size: 30.3 MB (30256064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e30c230ea5c18b8a89525b3f57a474768a0abfa407cb09b7d0af5c98284773`  
		Last Modified: Tue, 10 Jun 2025 23:50:17 GMT  
		Size: 54.7 MB (54716158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7493fd20f83208a93f5e5666a8a98dff66fc3427e44891d0b2af99fb42bd94ed`  
		Last Modified: Tue, 10 Jun 2025 23:50:19 GMT  
		Size: 59.0 MB (59005533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41b9993572d671fab72595e85c79aa64d38ab0063e71dd2dd1e4fd040b72fff`  
		Last Modified: Tue, 10 Jun 2025 23:50:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8215f2a1883e46a3ea688f2b91eca9d8016ee97abea684887f86d8cb9789d890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d55a7748a9eccf03da6cbd7643446b98fe27265d81d6c8c6fc2b7c39968da5f5`

```dockerfile
```

-	Layers:
	-	`sha256:282e24af949ec00ae9cd077696bfdcb269170d18c402c9293b4823c01eb061af`  
		Last Modified: Wed, 11 Jun 2025 03:41:35 GMT  
		Size: 5.4 MB (5429648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf9990aaee9b9865f61771493c804fbd0b3ea5a3cc2496c5592f4a1c1e86d078`  
		Last Modified: Wed, 11 Jun 2025 03:41:36 GMT  
		Size: 14.3 KB (14291 bytes)  
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
