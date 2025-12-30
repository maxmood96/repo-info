## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:a4a4c6f5fadd738f0bbc07f7c75dbf02d5cce2c249d19752c8f7ab2ac9fc9bf5
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
$ docker pull clojure@sha256:27a11aaa5398fd3106a4b5302dc91cd374893c141822b17b9adc3e1dce172ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152639491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f50bb334b8fbc76fb804f54aef296d50801cf597d08b7f4a5cf0f985a30b4b84`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:51:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:51:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:51:06 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:51:06 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:51:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:51:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:51:21 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c849172ea6a19bd4c8c93920c4a8bc7300ba8a00c06dabd33724b8b93621a22a`  
		Last Modified: Tue, 30 Dec 2025 00:51:59 GMT  
		Size: 54.7 MB (54733390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585f01ecd5e836ca871821ef4864b557b26a6257bae8d94ad496024006364dd2`  
		Last Modified: Tue, 30 Dec 2025 00:51:50 GMT  
		Size: 69.7 MB (69677034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc40b9f25237d532a52e460aff02be3426dc118f9b5ee14bc976f2e289f7484`  
		Last Modified: Tue, 30 Dec 2025 00:51:46 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4d453397df5e8e9ae8b9a07ede84e264a9065ed6fd5f48054b9f6650933168a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178ab58560a4dae24ac6f2a419930bc236a329004e6a7975c3abc4096e31adeb`

```dockerfile
```

-	Layers:
	-	`sha256:519ae8694fad23981825e21ad6ef3f72f6de5e5bc0145da3d21b92272e3fc409`  
		Last Modified: Tue, 30 Dec 2025 04:48:22 GMT  
		Size: 5.2 MB (5234998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e22ad6b6e28f26e7b2e32ee680055299f91883ffe2081e882ddcfdd3215eceb`  
		Last Modified: Tue, 30 Dec 2025 04:48:23 GMT  
		Size: 14.2 KB (14247 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ef744e6e7a17a25c51700b906c10c951a0675771a7ff026c8f36c27fba4ba0f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151476247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef68d966a5060957c65936eafe2c3199eb7ce928c284641e75210c0db575669`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:54:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:54:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:54:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:54:39 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:54:39 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:54:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:54:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:54:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30214f1492318f4a2362ac906f8fa13aa70826716091930a643fa5f3a1629d1f`  
		Last Modified: Tue, 30 Dec 2025 00:55:23 GMT  
		Size: 53.8 MB (53814985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfd625757204cbcf3b8ee9860859b49d5ae6dd1a2ee4926f751f1847206c5f2`  
		Last Modified: Tue, 30 Dec 2025 00:55:24 GMT  
		Size: 69.6 MB (69558408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7c33f6110b21403eb225f70a5d8fbe01deddd622f03641cc4d6b4b07cab97a`  
		Last Modified: Tue, 30 Dec 2025 00:55:17 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:af12e6cece6008e8b40d624111468a53fe687b979c7ed89e6501f4fe8dc645ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff944d3254cf30a7fda1c30f85aaa8cb97cb6342962149587ede4ab755e40fd`

```dockerfile
```

-	Layers:
	-	`sha256:35f4905d9430b2ba2ee6181348d785405c7e27c9124f5cfb3168b40feb587853`  
		Last Modified: Tue, 30 Dec 2025 04:48:28 GMT  
		Size: 5.2 MB (5241457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:867926429341e867a4dd615c276754346c6a191c871671a0391a858fc993284e`  
		Last Modified: Tue, 30 Dec 2025 04:48:32 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:82cf1307c5c50bdb24aa9ba59b34fcdfb443eed18656e95dfafd2582afc55bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159754403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370d552b6c469c79da415e4e608df59005a93e58e1a31a2feef0faa5f97b7db0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 16:15:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 16:15:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 16:15:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 16:15:13 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 09 Dec 2025 16:15:15 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:43:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:43:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:43:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:85c696326521b18996e4f030a7e27e2c57ad4956710f12ec3011da2c017e09ad`  
		Last Modified: Tue, 09 Dec 2025 09:15:52 GMT  
		Size: 32.1 MB (32068845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f64fb487d3e6808b902444ad63dfe41ea36c5a144cddfa20a3772f42fbf0c63`  
		Last Modified: Tue, 09 Dec 2025 16:16:47 GMT  
		Size: 52.2 MB (52175161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1de750c1418f3cf25868f48058b39043c6fce3acd3d6fdc9a6306d13f04bafa`  
		Last Modified: Thu, 11 Dec 2025 22:44:48 GMT  
		Size: 75.5 MB (75509751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bdb842628be921ffe1df22f8c2c0b3dd72869d0f5f811d5896aefb3cbdc70e`  
		Last Modified: Thu, 11 Dec 2025 22:44:42 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:98159c6c339c425b59fcf167a3f3cd718cc5f7ed1fb9d071036457c839da0945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb45a711c417b0fc5649ea571a5d2463aad9331420df9ca64a2305f9ed90b679`

```dockerfile
```

-	Layers:
	-	`sha256:14be6059ad0644fbca72d15bb4edae64a646792894fdff90590c2ab01004fd58`  
		Last Modified: Fri, 12 Dec 2025 01:46:37 GMT  
		Size: 5.2 MB (5240749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f22338a12958a79b8d7102e267599c9a97db52cf384e8460d7d591dbcc49bac1`  
		Last Modified: Fri, 12 Dec 2025 01:46:38 GMT  
		Size: 14.3 KB (14296 bytes)  
		MIME: application/vnd.in-toto+json
