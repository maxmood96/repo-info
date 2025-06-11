## `clojure:tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:1ef65f5c6cddc34902c3099b0fa8030610234eb4b421e4ff61468864c9322f3b
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

### `clojure:tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3c17d8de7e3d140689eb0f1bbc6988284485c34cb6887ce701455c46cd83c44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255395264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81c20f3a06c5a562f5f7ab480cdcbc9990cd4712a2279a566e5e35ec15b7996`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea0841ecb4003d4597efe5a0bedc6ba99c1d194cc4748fbd5ccea042f02cabf`  
		Last Modified: Wed, 11 Jun 2025 03:41:20 GMT  
		Size: 157.6 MB (157634498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b8249b00dce978c98c7d04df061208845e2fe11bb0d3abb776a96fea5bf8bc`  
		Last Modified: Tue, 10 Jun 2025 23:52:46 GMT  
		Size: 69.5 MB (69529594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cad78bb9468faef939bc932b338dfd5106cecc59fc848844639a14dbc11d595`  
		Last Modified: Tue, 10 Jun 2025 23:52:40 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5762cf8c3a3cddd3ebc71172abfde4aaf2ad45ab903ceacc4a48648017599e63`  
		Last Modified: Tue, 10 Jun 2025 23:52:40 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6a121e8a07463e8dcc2496d599fb41c9f5bdb2658caebca87c9d4a60f898f967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5130261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc6089ea1427dab2c0c90ebf0908d95a94aedcd1d1e3b2288da0a6739aeefea6`

```dockerfile
```

-	Layers:
	-	`sha256:39516686d2df83066c66ae94bd1fef0eea5437b2d4a1a88f47026e91dde04660`  
		Last Modified: Wed, 11 Jun 2025 03:38:18 GMT  
		Size: 5.1 MB (5113686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2840dbd42ea9d743011ee8a3554a6452609b6c3ee0fc700c2c57954de798eba6`  
		Last Modified: Wed, 11 Jun 2025 03:38:19 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:971bdeb0f900fba79c7e15e4305a77d9bae688a771f70b1f8a856da32271371c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253398271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f01b1ecb0da6d41d45ab70b378dc6083628b1dbc5e26fef3abe9c61f1e0349`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2385790c9fc4ddc367e00ff6d030af1b186bd2c3408c19ff409a2b813cbbfcbe`  
		Last Modified: Wed, 11 Jun 2025 08:38:18 GMT  
		Size: 155.9 MB (155928816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744e8a072cdd5289b4537f063f0649e587fd65b3e22201a8aec34d317d0901d3`  
		Last Modified: Wed, 11 Jun 2025 08:38:53 GMT  
		Size: 69.4 MB (69390739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f04c7c2b870ff38a153458ff45589862ef21a95b085413a1673818c85e86d3`  
		Last Modified: Wed, 11 Jun 2025 08:38:45 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df42a04490dc679287a062608aed2a118aa8b94269ff8a27a8542e44c9cd9be`  
		Last Modified: Wed, 11 Jun 2025 08:38:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f6e287dc2278a98422229be00e0b8662da23f3c84219e8f245521c2575b88543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5136188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c9d4a8bbd39b3b432109deaa45ae06009570df599df87efbe81a0ecda71ecd`

```dockerfile
```

-	Layers:
	-	`sha256:4a5b0cc5eed8065caf1067340216f57855bc7fdbef3d53bc41f65c08f9cdf818`  
		Last Modified: Wed, 11 Jun 2025 09:39:23 GMT  
		Size: 5.1 MB (5119471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbbbdc11b376fa8482f98c3e97dd94e7a6fd38f81562d90e8e624d7eadf690ca`  
		Last Modified: Wed, 11 Jun 2025 09:39:23 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b5b360c3d5c939762918e36dd61d9d8d6a10489ac4f2e6e6900b29701de2d491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265224400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6d38022cecaa92dbf47c3e0ee0479c920515f9a1535ac266386b061b0526b2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cdf81c5d56aaf265c171a330e71e09588b462a6ad48e8465246b1f0395ed41`  
		Last Modified: Wed, 11 Jun 2025 08:39:50 GMT  
		Size: 157.8 MB (157804904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299f37a13ebd0648711ea407949e2d6e8ceb6cfaf92c2a1f20003236ec3bd79d`  
		Last Modified: Wed, 11 Jun 2025 08:47:36 GMT  
		Size: 75.3 MB (75345661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3a1c5ce74607071049cf47cf921bced5a661b8d1d851df231963a91976bb35`  
		Last Modified: Wed, 11 Jun 2025 08:47:20 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956ab30f4d81dc78a13ca0562e2327d2252f697135bd22d1adf847b46b0028ad`  
		Last Modified: Wed, 11 Jun 2025 08:47:20 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7d45cdad836323f4c96d6c2b65dee8dbdf252b71e2cfc9565e1ba8c3a528afcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1137e7bb3731557d8afb201bfe2b9df496978217de5a0ea0759d2fbd36176f56`

```dockerfile
```

-	Layers:
	-	`sha256:22a986dc6c1a342a1c4b7f35fbe1d3160b913c868e9a18e8414a77e838193eb1`  
		Last Modified: Wed, 11 Jun 2025 09:39:28 GMT  
		Size: 5.1 MB (5118856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba0616f95fa935e4fcc70dde1f869705ab91cb02483845935d3c1246891703ad`  
		Last Modified: Wed, 11 Jun 2025 09:39:29 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b28edc4e20b843c15094e0b1cd08e368e048ff37c39916df45e9b9bbf68ce79c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242133922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046e6b23c434f8c88590b62c18b113ee46e4f03b9f422c2ac6f40df588c250e0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673e668202bc0fee9d946b6e751fdfa4f44e78bafcbd62664f38c9ada375a597`  
		Last Modified: Wed, 11 Jun 2025 05:50:15 GMT  
		Size: 146.9 MB (146911003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32568fd8c36740b45c4c64fe9102be1278756e2c5461450a591fb263f9e9f477`  
		Last Modified: Wed, 11 Jun 2025 05:54:14 GMT  
		Size: 68.3 MB (68334027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43b428b2ebb93e5c29dd32f1801fea4e0c9d01cda7c9f93a527ca3c380a94ad`  
		Last Modified: Wed, 11 Jun 2025 05:54:34 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56755d4d089d39ea1b1be622ead924f94241c98d30fa9bfdb3c169c405bf8d1`  
		Last Modified: Wed, 11 Jun 2025 05:54:38 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:590e8d8a2c58c6899ca11d5e841d554cae688fd7d005016d4d54aa44607422a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5121582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b13f931cab362134d3073b5b6eb1dd5c7824acec7ac154bc6d0836c0e2d7c7`

```dockerfile
```

-	Layers:
	-	`sha256:7653b76531056e1644775fed462b9ac25b2ee73ca0ae027d928d142d97f2f1ef`  
		Last Modified: Wed, 11 Jun 2025 06:37:44 GMT  
		Size: 5.1 MB (5105007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d5ba586e10b404cf5f3ecf62341cd0e84f4fdd8872ead34bc746465ba6f7fd0`  
		Last Modified: Wed, 11 Jun 2025 06:37:45 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json
