## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:724f8def1e499084594f435f23f051b6619e754cdb3bc02bd9433e1d6f95bbdf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8b30b952e43418924e4f84390a991f24f131d8718728a252a0bde381e4d2c527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144647467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b008a40dedf6cf535654a6ef29c2f4751f9cdc382fb154ad7eec71c71942482c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:56:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:56:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:56:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:56:06 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 19 May 2026 23:56:06 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:56:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 19 May 2026 23:56:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 19 May 2026 23:56:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8419f4a27c97b0c111ab0dc77e0159bd3abfadcb948d4a49cf6dd6670703b84e`  
		Last Modified: Tue, 19 May 2026 22:36:35 GMT  
		Size: 30.3 MB (30257598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e12bb6066833ef8817c7b4cec9d3a0e2196e1796f24629092350d9909a1aa7`  
		Last Modified: Tue, 19 May 2026 23:56:33 GMT  
		Size: 55.2 MB (55198706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8d971fc71e7664d40b735a8642e657d23a8b8bf757e2a5ccb8cfc130d3d973`  
		Last Modified: Tue, 19 May 2026 23:57:06 GMT  
		Size: 59.2 MB (59190518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f423befb1a3c384c7d8d5716bd6dc719ab73459acaf7cb6fc7b8358b65d086a1`  
		Last Modified: Tue, 19 May 2026 23:57:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b2549ce418e53237419d5649ff0952c29ab056414d3a58188f6af5685cabbcc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5454486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b16409d59776623737eeedccc80464f6576f3732c54531b52d637c6f33f0fd3`

```dockerfile
```

-	Layers:
	-	`sha256:f4e137452f9cfafa79f18861b0e88c2e831de801b325573fc5caf6085bb37567`  
		Last Modified: Tue, 19 May 2026 23:57:04 GMT  
		Size: 5.4 MB (5441038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5a08bdfaf54f85f7661f98103c227d443b883bc2d2f050e66c82355e1136a2d`  
		Last Modified: Tue, 19 May 2026 23:57:04 GMT  
		Size: 13.4 KB (13448 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f658c11be172ef7cec286f8b232b75e9f2be67424b329dfc6a7a2ff12518d3ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142376405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d1521901b94686e6ada9bd14dc472bf52b5a4b5bdf879579a6c743817f43a28`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:03:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:03:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:03:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:03:44 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:03:44 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:03:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:03:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:03:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2b99ba6638377be8e7e1e9a328ebb001513ab9f700c8168d404eed03437c7ce5`  
		Last Modified: Tue, 19 May 2026 22:36:47 GMT  
		Size: 28.7 MB (28742972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823b387351f48bab5f7445eb5eb012d8e1fca1979c127370005c195ffb0bb757`  
		Last Modified: Wed, 20 May 2026 00:04:15 GMT  
		Size: 54.3 MB (54272922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34227eeabfdb8675a86ff38e35535fc3df01bd1edc0adbb7ba8a5a2d5d821d38`  
		Last Modified: Wed, 20 May 2026 00:04:15 GMT  
		Size: 59.4 MB (59359865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2787199e48fc6994732289523860ea162b23969b25f84b442de2f506d2e5ec0e`  
		Last Modified: Wed, 20 May 2026 00:04:13 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0ce110b149a403874fa1e343bedede51c1f7fa4643e55bfd6ad9f91151ef958b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5461989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42bc0281d88843098006f45b1abd9f5a179234274384f8639bc5c0e796ee8bda`

```dockerfile
```

-	Layers:
	-	`sha256:d105802f54e6dba579448bfadd73fc51885a372f473a20a55871c44d00eec375`  
		Last Modified: Wed, 20 May 2026 00:04:13 GMT  
		Size: 5.4 MB (5447470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6783e53923add92ce1113dbde2a0f7f7aeee904f80b9858f1b21a9e106fae10e`  
		Last Modified: Wed, 20 May 2026 00:04:13 GMT  
		Size: 14.5 KB (14519 bytes)  
		MIME: application/vnd.in-toto+json
