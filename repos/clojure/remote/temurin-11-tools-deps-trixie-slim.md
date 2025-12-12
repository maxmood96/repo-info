## `clojure:temurin-11-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:15e38cd024e11569059b2f36208536452fcbd8d07b343b592e3df48920ac50e7
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

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:54e26a006ed4a34983f695401c51aaae77319d3d033eefb8e036582f391e47ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246736244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0a01d983ba88b62c5d14f6864f9cb3ed804e8c9f0c9a15bb69171443864117`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 22:38:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:38:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:38:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:38:30 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:38:30 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:38:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:38:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:38:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1d7fe5b167f2507b372fe922ec7016363fc08c7d85073b77626c28e4f67691`  
		Last Modified: Fri, 12 Dec 2025 11:52:33 GMT  
		Size: 145.0 MB (144966626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6daac298d5aa21580bf018738d849de2469ff5414e7eb745cb084626cc997f85`  
		Last Modified: Thu, 11 Dec 2025 22:39:24 GMT  
		Size: 72.0 MB (71992478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66531606605a4f036e969f85e5cfa49a6a724486b919d13ad54aa24a99203afb`  
		Last Modified: Thu, 11 Dec 2025 22:39:16 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:66c5c2f3b51605a9ed9b400718e9e359859feadf2f7f9e88fb772b21f5a50870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5290581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574d6b1d53f105a7bd818d9b8682e47db862ac0dc46574491c4973bcb997003a`

```dockerfile
```

-	Layers:
	-	`sha256:3a09f5d31d9c820128be88410ed08a61d30675aaa6e6f9a3685bd8b2a25b2390`  
		Last Modified: Fri, 12 Dec 2025 01:36:56 GMT  
		Size: 5.3 MB (5276338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd5124cccd7b88ec2019844689764e856be3718600261f69ad009d6e039185c9`  
		Last Modified: Fri, 12 Dec 2025 01:36:57 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c715b5ba2394ea66efed041ef17eb3858ed4a75aa2c58c38ddc497f670de436f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243677623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a644d01760e3323d1b9dcc026d9227dcac85590fc5ecb35488cfa660b7c48b06`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 22:39:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:39:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:39:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:39:07 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:39:07 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:39:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:39:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:39:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7fe4b6c4072ca7b0b088d9f3735084b586b90dd927e5cdf4bf47dbde9312fe`  
		Last Modified: Thu, 11 Dec 2025 22:39:50 GMT  
		Size: 141.7 MB (141731577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f54bb9310cf7da7936e904096cba0602a3e2788a823f066fefb7b55fe306a1`  
		Last Modified: Thu, 11 Dec 2025 22:39:59 GMT  
		Size: 71.8 MB (71806774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ab24bf5c0e243054acc79c57766510201701f3d93d0c3ecb44fced1387541f`  
		Last Modified: Thu, 11 Dec 2025 22:40:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ea0896acec1fc2087a4652f9e4246bb2006493e84272bc90c0602ff8e593005e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15847d7c2f8d095a6cc17c360e28792a0bdc0801cc42a4a5cb65fac9b9aa16a5`

```dockerfile
```

-	Layers:
	-	`sha256:869ba98a639c31fbf3280f8ebb1d32d140e96c9ae993c39980642b2183bde689`  
		Last Modified: Fri, 12 Dec 2025 01:37:02 GMT  
		Size: 5.3 MB (5282725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0184ac8de7d9aff1fc00f0987dcbd65d59e80159d41a75c681c19ceeea674c9f`  
		Last Modified: Fri, 12 Dec 2025 01:37:03 GMT  
		Size: 14.4 KB (14361 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:a7385e0bec1e0e81f2c73d45a12d4108cb395e906833648331e4a38356f7c4a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243066244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17fa36112029a2e89f84eb2298e1dc543e102e1f5484d2be3d1e397202295a48`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 03:49:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 03:49:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 03:49:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 03:49:47 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 09 Dec 2025 03:49:48 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:53:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:53:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:53:37 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79c7c03426c1aec44b221775d1d53747ec67f1e33a2616e70c690b2a6e30b72`  
		Last Modified: Tue, 09 Dec 2025 04:03:19 GMT  
		Size: 132.1 MB (132081973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300f8b9360abd46f7a61ab51e3afa40f82a7a88748029bc276cb646388646378`  
		Last Modified: Thu, 11 Dec 2025 22:54:34 GMT  
		Size: 77.4 MB (77386736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5e50d9430ef2780657496dd06d67356b7b3375c70b168ba4467d6ed34d0097`  
		Last Modified: Thu, 11 Dec 2025 22:54:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:42c2a414bfb780cb216c7b953b14d960779717c08ddce14e6fed5869c613e362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0ee6d7146cad01f794ef96e24650470a2fd0d700cd06af6011d5a863358494`

```dockerfile
```

-	Layers:
	-	`sha256:10fdd9a1b238304e7dbcee92d2b02730bbdbd8fc6a65f380ec07bf2875426eff`  
		Last Modified: Fri, 12 Dec 2025 01:37:08 GMT  
		Size: 5.3 MB (5280094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a48c5955e7bc2c697ba4f9a30aa7404a328b69ca57d47cc0666e88e8cfb9656a`  
		Last Modified: Fri, 12 Dec 2025 01:37:09 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:af2b798e082e4b18796c9524dab581bd0536af8256014f7c4eb1945b1a48bc73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228483150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5670ab58afc522677ed36dbabe47ecb536652370b6a2e35fe4045c6f8e9d5d5f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 01:26:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:26:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:26:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:26:34 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 09 Dec 2025 01:26:34 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:33:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:33:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:33:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994be3cdeba56428b75353d1a063313e5474487ae1762114cf539a2b179912da`  
		Last Modified: Tue, 09 Dec 2025 01:27:33 GMT  
		Size: 125.7 MB (125694399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1678beb4519e51345a5c88bc30455d2b5b02063085b414160f63c51a39021140`  
		Last Modified: Thu, 11 Dec 2025 22:34:04 GMT  
		Size: 73.0 MB (72953707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58a746a6ba3c6f5ba8cee57ad8b8baecb4415077a1b1427769f64559354f52b`  
		Last Modified: Thu, 11 Dec 2025 22:33:56 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cabcdca8c715981b62c30ff792480fc85e4661a0afd7696e8fbce5cd13bf6f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5286509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f257a9c1b64d6db4decef610f7610722ddcfc144a67eebcdb7d2e8a5461a88`

```dockerfile
```

-	Layers:
	-	`sha256:52e5048dd088bdb9602a3310dea711c541e7d60df3f5079d16aee66cb020ee2c`  
		Last Modified: Fri, 12 Dec 2025 01:37:14 GMT  
		Size: 5.3 MB (5272266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e861e5784e16374a21770e6efa2006d432a414e70b7f96a927617dacdf449afe`  
		Last Modified: Fri, 12 Dec 2025 01:37:14 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json
