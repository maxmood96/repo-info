## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:ab58c6d5047f2dc1b5ad93c04efcb892c42ff0276b4acdf5b0862a331dffcf7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

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

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

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

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dfedba68ba5e4f1978641131c29ab36405cbf189aa37b381e5f5d6593d4495ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141714902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3facf82c64a8197790897b676ce12476f1c2cc5402ff8205a26a86eeec4aa7ad`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a26ea748e01f6fa271cb5c99f02841ad6f2c475c5d2be97781534dee920e77`  
		Last Modified: Tue, 03 Jun 2025 19:23:28 GMT  
		Size: 53.8 MB (53830497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59dde2c4896f90ce1cf9d2fa6b6b467d61fa7a6605ebec7eb20ce71ae635b0b`  
		Last Modified: Mon, 09 Jun 2025 17:34:26 GMT  
		Size: 59.1 MB (59137504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126fff26562b1d7507a6c0045069b13c5baa3663c34317e96a305bcd55b18aa6`  
		Last Modified: Mon, 09 Jun 2025 17:34:10 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:caf2102d0dc7b7d522ce4aad492fb7e98f1248ce9b1281687bd735f467435678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5452111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536cc93b2b27aebb5569ad7edb9555bbce38ee81929ba389042110724750ca02`

```dockerfile
```

-	Layers:
	-	`sha256:4063d6ddedb286cf6a9c485a39f733d3b3cb334663c05a99ecf3b20dfc769fd7`  
		Last Modified: Mon, 09 Jun 2025 18:42:57 GMT  
		Size: 5.4 MB (5437702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6eac334417ef7bc563113aba790930bd4448261242756b30786d2ae370e887a3`  
		Last Modified: Mon, 09 Jun 2025 18:42:59 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
