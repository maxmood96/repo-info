## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:a02d49b203fcc99262bb75be73ee073168b6356c67ceaf5833398bd17a96bfaa
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

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d32172117ae167e1b5a62ad3e522358499388190edbb12db37a3de6178a2fa58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243565572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019944bee8d53ae2e0cab003c68931a5884906e5c14fe086b4145f08f6de1a40`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5d36682b30815fc000c5ea237982d9d183bf00f269124d65aeeaca8af92c36`  
		Last Modified: Tue, 02 Sep 2025 00:16:41 GMT  
		Size: 145.7 MB (145658229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac72c768941aac287571f11f16045abc8d886134f07e4fb44bea826e524576a`  
		Last Modified: Tue, 02 Sep 2025 00:17:25 GMT  
		Size: 69.7 MB (69676440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8296a6328b2c275b60600515318c445129557472d84a4b65d9e2a8e5538d76b7`  
		Last Modified: Tue, 02 Sep 2025 02:35:06 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:811cb18c4bc7428011ee6e1ba793ee1be8db0722adeac529fae9294ef362078d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5145724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b404afe0ce97163c9c6dc8f45a4194b4c8daf495753b55de0628cd0b3884ce1`

```dockerfile
```

-	Layers:
	-	`sha256:0273b89ca7649d0abdaf95495ea333da3e0d4743e7296c48761a846d98f4ed6e`  
		Last Modified: Tue, 02 Sep 2025 03:35:29 GMT  
		Size: 5.1 MB (5131414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aca02d57887a051e54046be5291d08f1299715578d9d04d8197fade581f7b789`  
		Last Modified: Tue, 02 Sep 2025 03:35:30 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4e93f7e6388971e7c3aeb51dc1a6cca5e07a56a8ea734106092cb975cb18915e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240092605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:027f9af29d6bc4aa189bc725e2a179c92e29cf8f409ba875a49aab06067fd683`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f170599e0d0d7ce8452567f601dd39705883bb1c67f4c2b875ddcbef1651e1c`  
		Last Modified: Tue, 19 Aug 2025 04:12:46 GMT  
		Size: 142.5 MB (142460571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875928e609ba7ea865f1ac22346508571fc68d3ecc6bd0894187e0019b880a65`  
		Last Modified: Tue, 26 Aug 2025 17:36:04 GMT  
		Size: 69.5 MB (69549387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b01cd6da0da37e45dab5ffb36d7d87cf793b09d0aa947218efbc27110ba4bc`  
		Last Modified: Tue, 26 Aug 2025 17:35:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cc9da806c8df6da92a4019a5363c63e7970da6676951e9fe8e7504f658d4f0b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582ed83bfd9a1d28bffe348e9a04bf528d4ffb2ff0b9798fc898875d9c8cc0b8`

```dockerfile
```

-	Layers:
	-	`sha256:ef84be1a5947880015b93902205d8d40313f3a185839591576ec675e17265922`  
		Last Modified: Tue, 26 Aug 2025 18:35:20 GMT  
		Size: 5.1 MB (5137793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cc709fc3496f5d6c2dc5fc116a48590c7e5f34422a4db998b83b09dfaa59afa`  
		Last Modified: Tue, 26 Aug 2025 18:35:21 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:dd40fd6126f9d39720b57589a36160d3d902715b0142ea5bf62d7298a62f1caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.4 MB (240431243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ddf8eaab629bdf496c9ad563fe3e20df69b8ee0a015e9c4ec2a63f5f8d130f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
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
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46561d416a7c35ce0f5f369f09b10c84d52b854df0532c3ee5a10948491d390b`  
		Last Modified: Sun, 24 Aug 2025 07:12:04 GMT  
		Size: 132.9 MB (132853303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd7f7f274926ad57780e6c458611cc3530c51d1bb349efe6e1123b0561850d1`  
		Last Modified: Wed, 27 Aug 2025 00:21:07 GMT  
		Size: 75.5 MB (75503872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057d01bed82329b99fe9c9c623bc92c0e24fd516fb4d00c7d9e8370e802e3a55`  
		Last Modified: Tue, 26 Aug 2025 18:30:23 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:457f0a0484883c9be76fbb04ee1ee9b7beecb0fd6eaf8b2faed7c09e122301a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c87564dd333ebf296e473665be56dd610b93aaa527c805a7b1f77b1ec626b6`

```dockerfile
```

-	Layers:
	-	`sha256:17b70f7cf498ff20ca656ece3c5ae40f6d0b0ea9a0df2d641fa17571f2d8e647`  
		Last Modified: Tue, 26 Aug 2025 18:35:26 GMT  
		Size: 5.1 MB (5135957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66b36a02321cbfe89fcc0399ae5c13175f438098a06e46855c7ebac5c5feb499`  
		Last Modified: Tue, 26 Aug 2025 18:35:27 GMT  
		Size: 14.4 KB (14358 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:dbc152e72c7aa191b25ef5b197c108a9b843db7351ae1a81be9028105074f7bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (220995151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbeb3625eaeee4e8b8a80a5812db78d41f18ef8da6e885344bf3a063853fc025`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632e8bc83e880acb510052f87a9ce5503ba3f0b0be39945274f7d49fd731441d`  
		Last Modified: Tue, 02 Sep 2025 01:45:26 GMT  
		Size: 125.6 MB (125622191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b81ef5218dbd4487b23f0feed9ed2cf1772e97133253f8c060a71adbbb90f99`  
		Last Modified: Tue, 02 Sep 2025 01:52:03 GMT  
		Size: 68.5 MB (68484479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361cf46fc47ad4fb5098812667341ca4f26b85bd1955d312baca71dfd7e15688`  
		Last Modified: Tue, 02 Sep 2025 01:51:51 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:202ba8500628c0b6fa685c43c8398eb15aeac674328e3057fe0a7f732cb157be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de129dbb82dbdacc4d3b87f6f22e36e6c9cc54f5e58142e4bd61962eb5fbdf95`

```dockerfile
```

-	Layers:
	-	`sha256:60e6edddf10a9a00dacf8a40b8579230b6fd6fb2e4d582b8690c8cfe0a7ef244`  
		Last Modified: Tue, 02 Sep 2025 03:35:43 GMT  
		Size: 5.1 MB (5122739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7f0dd2bea3216097aff3f021ddfffb7c7293254f038519930d23940f1bed751`  
		Last Modified: Tue, 02 Sep 2025 03:35:44 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json
