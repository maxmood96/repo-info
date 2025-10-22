## `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm`

```console
$ docker pull clojure@sha256:40ea24acf43bed7fda68443cc4889d7345588c878f10d06142b673fb443ddb35
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

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:984d126f7dbe28ad4627d53957ad7c1172ea4ac57bf6cacaf869850df1abe968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275287134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033d9dbb830aeac6526530391c38dee06bda2160a2401f4a13890ccb74628111`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:cd01849e3cbdfc6993640303768edbb56372cf9f1ae101d516334c8d462341af`  
		Last Modified: Tue, 21 Oct 2025 00:19:25 GMT  
		Size: 48.5 MB (48480563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801881f575f94423d8282dd87e841cfc39eb090eef6ee3a96f5695a20bbe01db`  
		Last Modified: Tue, 21 Oct 2025 13:03:29 GMT  
		Size: 145.7 MB (145658335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f1c46995d5cc84969ed8736112c3a9f557ba513b33989d5144e3e8dabb9d5b`  
		Last Modified: Tue, 21 Oct 2025 13:03:13 GMT  
		Size: 81.1 MB (81147591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e11db79818bbb5c9d15cb9dbf4f9ca659dda799fd16bbd8c3ce9ab96017ff`  
		Last Modified: Tue, 21 Oct 2025 13:03:05 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5448865b49aeccb7bd60e340676d73812ccac839cbbce84feb133cc0f6c91bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7409283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01770ff6d9f64241d6c4accb38143c4788e7817a3cfe8b9a47a8f910fbf3acc9`

```dockerfile
```

-	Layers:
	-	`sha256:711b060d14d537ee46a69780ca76137231b1350bcd115b5f9f65dd27f242344f`  
		Last Modified: Tue, 21 Oct 2025 09:35:44 GMT  
		Size: 7.4 MB (7395031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c8cf31b284eace9b90f4cf1b6e13d0ee9b9a070626089827c0fbd08353129ef`  
		Last Modified: Tue, 21 Oct 2025 09:35:45 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f397bdf8234e5b816adc8ba7d564fd4ce220e5cd77cab4dd3d0e3b9c6c3c02af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271848749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443c3742fb77283cec312e8046c34df57712481ecd04d9a6306f894797637f25`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf4ff441e1e139d3d55c506bbfe01297495240642a95ec9334409a63cdf6be0`  
		Last Modified: Wed, 22 Oct 2025 09:30:49 GMT  
		Size: 142.5 MB (142460648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5523df84bacc24e11eadb6076c7de2b41fc03fa51e3dabf2e6b725150605e30a`  
		Last Modified: Tue, 21 Oct 2025 02:26:37 GMT  
		Size: 81.0 MB (81028461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05f47e30cf9ffffb9d9591c4083cc30db044d41af0b74c76bbf7dc15dffb614`  
		Last Modified: Tue, 21 Oct 2025 02:26:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:50f418d95a675316e6ee5dff3931d8bb3bf240e952bfec610b674d861f19fcf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc46f261535a08b0481129fefde378151586afcf455074702e6e9b9ea9346f5a`

```dockerfile
```

-	Layers:
	-	`sha256:e8b555a2b20c57241a2446595a55c0bca73f67bdc1fda72f397f27bb63d14b49`  
		Last Modified: Tue, 21 Oct 2025 09:35:51 GMT  
		Size: 7.4 MB (7401412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:532b5c91072dcd77affcfee3119ca47f0f7f63611f972417c6db5ed60b587559`  
		Last Modified: Tue, 21 Oct 2025 09:35:52 GMT  
		Size: 14.4 KB (14369 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:dc17b20c75d160139e726c605836fa9d3f9500cb1101ce5e0624d4fed957c1e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272166672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89102ba81c71e86919deb7f0d28387089e5ae08303e60003a70fd0e23116fd52`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
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
	-	`sha256:297b234228c60cb6a9bc0156bdf582119f3c4f22112d7d2e8128e4d1403158cb`  
		Last Modified: Tue, 21 Oct 2025 00:19:36 GMT  
		Size: 52.3 MB (52326787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d446ddc322b3d8a6e81041d612fbaf129111f223abbbfb2eda50c0e7b34d94fa`  
		Last Modified: Tue, 21 Oct 2025 15:33:06 GMT  
		Size: 132.9 MB (132853167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10779c5945dc6a5c54cf33663e649f2155462203ac396f1c77b3842b7ca13a2e`  
		Last Modified: Tue, 21 Oct 2025 15:39:59 GMT  
		Size: 87.0 MB (86986073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae87392668503fef7537cbdac81f42cd12be2675ae76eed2400a1d5705a3da1e`  
		Last Modified: Tue, 21 Oct 2025 15:39:45 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3f51c01f31ea2990e3a376dc254250ecb686963c541c71245edcdb32ec30e26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7413930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e788a99f68c4bd5e5c4aa4985efa46472344dbb2413b868bf7c046b11123a8`

```dockerfile
```

-	Layers:
	-	`sha256:0c7a58a7af82e619f354af6d542ea98ea66ac992d165279cd9aeb8bce3be5f0e`  
		Last Modified: Tue, 21 Oct 2025 18:35:16 GMT  
		Size: 7.4 MB (7399630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b50626df8cf5891cdc49f6372d5ff50f69a6448966a016d965646237298cbeb`  
		Last Modified: Tue, 21 Oct 2025 18:35:17 GMT  
		Size: 14.3 KB (14300 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:82baa620e56bf626931e0f6c1080a9f9c5b22f2dcf68b8a10a455085fb10d60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252717068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6020474282a2ad449710b7aa244573be9e8515f158af4175610862a4daa7455`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
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
	-	`sha256:769a86a44e9ad2fad1b0132047fcc9c080f859777f09d3856b818bc85f1c5895`  
		Last Modified: Tue, 21 Oct 2025 01:19:50 GMT  
		Size: 47.1 MB (47137521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8160ea850ee88b2a6153d138c40df9d1e47f6b0d811e159d91c3a99d108a72d`  
		Last Modified: Tue, 21 Oct 2025 21:44:21 GMT  
		Size: 125.6 MB (125622121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1060cc828a6c9abb492572ab5e7355d07a8d23b21dbd38ee2a745e57c6b3e6a4`  
		Last Modified: Tue, 21 Oct 2025 21:53:20 GMT  
		Size: 80.0 MB (79956780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c5fde54552b220a9eaf1be252f332e8a94dd787464f3d87b17abb162455a94`  
		Last Modified: Tue, 21 Oct 2025 21:53:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2339c5ed6d8e7cbfe0f55d684774cfcef3e5631759ecce22584c1fdece8e0e4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96799b2deaa987501673b52dbd4294e8c5ef76554dea6cf7b6aeb201658ce8e2`

```dockerfile
```

-	Layers:
	-	`sha256:e421a739b812b73d2a22cc5b32e0cec2fdc770065911b6c77fd4cb8222dbcfe2`  
		Last Modified: Wed, 22 Oct 2025 00:35:19 GMT  
		Size: 7.4 MB (7386354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc1016401f85d6552d3da2a8c9cbdbe112d1ad6f59f8110e1abd3221354e52b3`  
		Last Modified: Wed, 22 Oct 2025 00:35:20 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json
