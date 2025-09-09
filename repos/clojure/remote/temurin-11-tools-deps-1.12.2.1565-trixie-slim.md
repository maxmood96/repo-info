## `clojure:temurin-11-tools-deps-1.12.2.1565-trixie-slim`

```console
$ docker pull clojure@sha256:631456fa02fa04e5cda3e66b16836aa085a174180e308254358dae604df97209
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

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:41613eaa9d110c1ab9edd151ef5404626a2fc2a719c7093896655f852cab0453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247414768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0b53c20860ccbfca72731ed5828502a316acd404f44d946f933fec4bfbf0451`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dfec0a94b76810a218fe17a8af420fac087da290a27e9ae9adc13e477ab638`  
		Last Modified: Mon, 08 Sep 2025 21:42:48 GMT  
		Size: 145.7 MB (145658209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47278d1217da3de4186c5431c2946c983f368f5232a7adea86c34fc07ef4089`  
		Last Modified: Mon, 08 Sep 2025 21:42:47 GMT  
		Size: 72.0 MB (71982421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcdea1b7d5f8441f37d10e8ef4d05bcc9a4f937f1af3be5109aeed54cbf2da7`  
		Last Modified: Mon, 08 Sep 2025 23:01:47 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:658e3c81ebb688784143f59e33d061702d11dd240056625dc060e2c8a762a61d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5290539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d5d72aec80d907649d6f4baf7a8479a8efff346685e3ad549b4c686b7143adc`

```dockerfile
```

-	Layers:
	-	`sha256:ec670a371794b3e2cf4977c77c86bbce7af68ceb7d7e23970ea6bd428c9ad81d`  
		Last Modified: Tue, 09 Sep 2025 00:37:00 GMT  
		Size: 5.3 MB (5276254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e459ac84618b4af0502e4f87d9add54a9b4e9a41cb6a1169d8599e17803b980`  
		Last Modified: Tue, 09 Sep 2025 00:37:01 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e14de43640a2816e24e3d66e091f2547f71693f8f08285162e6fb2a432f3286a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.4 MB (244400400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b151094ec9240662535939d57d7de03a4c23fe0344101269249a82715c108a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22aabc2b1eaa3d66bd246a649f70aad2e0cc1a2983c5c9d081ec3534d423734a`  
		Last Modified: Tue, 09 Sep 2025 00:38:13 GMT  
		Size: 142.5 MB (142459120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d1ed9400e9771e60d13c53e39673d875eb49a1f93187c04982774dc9b5dd4d`  
		Last Modified: Tue, 09 Sep 2025 00:38:12 GMT  
		Size: 71.8 MB (71804005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d41ab849412c34d4b5a0f66d0c650f54597f6b02069b62db6611da3f4ab761`  
		Last Modified: Tue, 09 Sep 2025 01:15:04 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f492f149860bb54b455875235a3c5475333750bbdb1905a33e59ae509e6f8856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02026b8ff72b8ea2c50478c421fd41d9be136f01da62f35fb7d988f5c091f4ec`

```dockerfile
```

-	Layers:
	-	`sha256:e158b7fed471f96e472d8146be4f8a9003c32b3a74efb20e0fb1a0775fd76684`  
		Last Modified: Tue, 09 Sep 2025 03:36:54 GMT  
		Size: 5.3 MB (5282641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:448bcf7bea09db65ad4f28c1c0db00776dec6c2bfefcdcb0f40866031294351a`  
		Last Modified: Tue, 09 Sep 2025 03:36:55 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:96f4faae709e3c1107bd949a2756f37a24aec9a84aa65385d6a2ecca752a5f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243837320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa034d93ee668256941e361409694bccc6b7adef4b81f1355f0d8b3090b0fd44`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adee34b5367d1099f54497f4aa263aef11888acef04df6d42006db6cf1a4bc4`  
		Last Modified: Tue, 02 Sep 2025 08:19:02 GMT  
		Size: 132.9 MB (132853137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c6cae3057979106144cc348a8bdf1f3616c6cbaa0e38e5edcdf0d33e6ff58d`  
		Last Modified: Tue, 02 Sep 2025 08:29:21 GMT  
		Size: 77.4 MB (77389324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a835b7cc286b17ba64a90cf67f814651ec5438435b46a5ea976224ef7e2e1007`  
		Last Modified: Tue, 02 Sep 2025 08:29:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1c4d0b180cd6deff2a343ce6220a8dec1c75b194ef90c68a2e0ebab0f9b1b3bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ab43cfc3449ea7e004849468d2e29ecaa4613266ff1a35ef1790eb6f5d93b6`

```dockerfile
```

-	Layers:
	-	`sha256:bfee6e90a8410278424f52cbcc92bcbe36be22935cedeed6c1630bf89a595279`  
		Last Modified: Tue, 02 Sep 2025 09:37:36 GMT  
		Size: 5.3 MB (5279134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a985cbe048ba80e41f5b883ddc2004d31b4de7fe9b5d57330e0b978167f039`  
		Last Modified: Tue, 02 Sep 2025 09:37:37 GMT  
		Size: 14.3 KB (14334 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:4dede646615e74d67af1b332c097de9962bc41f8bedcd68c6f5ea94203c6b045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228407243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f2cbb0a65c9fd5d4fa354b8ff3cf9502971e84dcf54bac14c1456b519fa5e60`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5b3dd12a4d4a204979dd98c6bdd5fd4e2ce8094fed17860ab58a98a1e9df72`  
		Last Modified: Tue, 09 Sep 2025 12:35:09 GMT  
		Size: 125.6 MB (125622199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1940a7376671ce603601a9074088049734f412cc4eed9803f68ccfa30da03f`  
		Last Modified: Tue, 09 Sep 2025 05:33:25 GMT  
		Size: 73.0 MB (72951495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724c4912cfa36798193bc83a00e41fd5aa9bc47d0ce4481d12af2dad43bd9afb`  
		Last Modified: Tue, 09 Sep 2025 06:11:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cc7d7b392b388df64c6b6883070f87a4c72f7878939c1b41206353d1655e6ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5286467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e773b284fb27fd2b3819b61462cbde9b13961de9632f169ba19250f3e4054fa`

```dockerfile
```

-	Layers:
	-	`sha256:05efe475753eabf85e275a2795a3580c3bdd41b31575bfaff423a675552af845`  
		Last Modified: Tue, 09 Sep 2025 06:36:15 GMT  
		Size: 5.3 MB (5272182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:844e48e43f043ee942d195816ce8dc93107c3e0ca8f7b1929051462731bc119c`  
		Last Modified: Tue, 09 Sep 2025 06:36:16 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json
