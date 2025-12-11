## `clojure:temurin-11-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:373540a37cfc4907b8941d0e8b4efd01cff5131a139decacb034f12da71b6524
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
$ docker pull clojure@sha256:aa4f6ad52bbef8b327da1a2312fe5ca6d4b95347cf3f480cd3a90ff457dc3f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246739923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308168011e98fb004c73b8592212bc893ec1890dad796fe9bf1fbe5fb56f8572`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:52:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:52:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:52:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:52:08 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:52:08 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:52:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:52:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:52:25 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec72231242dcd7ad4e0471fb3cea0fc648eaa76ee15ce1ff003bc77272fc5a9`  
		Last Modified: Thu, 11 Dec 2025 03:33:00 GMT  
		Size: 145.0 MB (144966600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82d487472e55181ec440d82d2ba40b60d5bbc626f5bec8fc6edc84186bd6dc9`  
		Last Modified: Mon, 08 Dec 2025 23:53:01 GMT  
		Size: 72.0 MB (71996185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b8d6d1efc74828b42a948e69b20845af062173bfc966915432001ed917761f`  
		Last Modified: Mon, 08 Dec 2025 23:52:54 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:24043ec0b7a727b14e68082b935dfe4981fab4b867b2d6a6e0801e5b71b33f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5290579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec562bf9f62de7ba7c048ffcb8d795fa1630706d302a343b9039686e2c261b59`

```dockerfile
```

-	Layers:
	-	`sha256:c38966ac9d0c9ce22448da090759be89ba3e4904f4d0c741ca527c50e3bd758c`  
		Last Modified: Tue, 09 Dec 2025 04:38:33 GMT  
		Size: 5.3 MB (5276338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8368d58b73fe9044fa851294603951849f9d517f21681d4734b11085fa55d7e7`  
		Last Modified: Tue, 09 Dec 2025 04:38:33 GMT  
		Size: 14.2 KB (14241 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a0300cbac8934f9ae55c94cd920d62626b399f8854b6439f41a1495297c5aaef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243679153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922785694c972e07c378eabe48693ed406a7f771d5159cd51065b92cb1e3c313`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:59:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:59:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:59:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:59:56 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:59:56 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:00:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 00:00:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 00:00:15 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412892524d697d1cc22067db1507daf7735959ca3a10c528ef81da26d7af5a13`  
		Last Modified: Tue, 09 Dec 2025 00:00:55 GMT  
		Size: 141.7 MB (141731561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0420c5a0be6b03cc5e223ed42f2642cac7b0931b610b2d90de33ab2ab109d3e`  
		Last Modified: Tue, 09 Dec 2025 00:00:53 GMT  
		Size: 71.8 MB (71808320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c6707da66f0dd17e444f657fac12c1a8d47169f9f43825a3c7be8277a04618`  
		Last Modified: Tue, 09 Dec 2025 00:00:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6a5c4ffaf1da15fd90f8ebc79d82d5a36ec6ccedc91f8e359d8b3cd472323587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6434c737d91b1a45a1860e03eaa7a2c143aea4437a5104ad290bdce60400b48d`

```dockerfile
```

-	Layers:
	-	`sha256:9801b0d976b800229e0211567f6580c6e61ae531562db05dbf0b65f5e5e72fcc`  
		Last Modified: Tue, 09 Dec 2025 04:38:38 GMT  
		Size: 5.3 MB (5282725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee1d4aa14ddd5f8e9e9b7c82b9fd395170f99a4423ec17a189a2da4e0adeaa66`  
		Last Modified: Tue, 09 Dec 2025 04:38:39 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2da7f666f8be8ab2bf892d48fa59c0824ee99320a1a9d54b082a71016fed9246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243070298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72dbce878b454ad62bd8ce3abcb61feeabf145c55334982440198f1d622be07b`
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
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 03:49:48 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 03:51:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 03:51:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 03:51:13 GMT
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
	-	`sha256:799a5f0204845b953bf043cbf3d03c59b4c619de9b7464402f39fab64093795b`  
		Last Modified: Tue, 09 Dec 2025 03:52:06 GMT  
		Size: 77.4 MB (77390793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f643fbdc28f0281f3833f02b4c5bb57c98a29a9cac6824fe46f761decba21ae2`  
		Last Modified: Tue, 09 Dec 2025 03:51:58 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a4d907fe01bbf253df39f6ee98465c18a0cb1385e8d3866acbf248f926e91668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c23cedb967a0320bfab0650cd9ebbcff16a13be6e94b53747a196b3f17187dfc`

```dockerfile
```

-	Layers:
	-	`sha256:ba5826242ab1c7c8c403a0961708e27ee7fb4e7f3c904d2fd1c5ad0f047f3d5f`  
		Last Modified: Tue, 09 Dec 2025 04:38:45 GMT  
		Size: 5.3 MB (5280094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b53b1fcfea1a65546fd6267c732a368cfa4e15267175c7ee6aa1b5ab40cb2eb6`  
		Last Modified: Tue, 09 Dec 2025 04:38:45 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:35a0d779f23f19450192286a4d9808e25b1ea27d264fa77bab253487aded1720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228483728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e5eecbe8b18fe8f912b046c6b1724048dc7fde413e535fb26925a9ac757c7e`
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
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 01:26:34 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:27:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 01:27:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 01:27:58 GMT
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
	-	`sha256:1fa7afe6b54972f12cdb5de2b57acce035014904914fc389eb8d1a3ad3d57d16`  
		Last Modified: Tue, 09 Dec 2025 01:28:33 GMT  
		Size: 73.0 MB (72954287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdf73df251a506353b30c2e1f7b3933ab8fa82ea019daccac4f728f20ca4eb5`  
		Last Modified: Tue, 09 Dec 2025 01:28:28 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:586dddd329d0cb9b94449f98757aeb6b222484f4683231e0f8783053e785b6e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5286508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e779dcc8e6441ff8bcc1f5983d544bc0c7689f217d5c2dcebcadf3ccbd95da2d`

```dockerfile
```

-	Layers:
	-	`sha256:12af4d44ef55406924ad0d19540d56cb1ca4b5ac6475d410a48306210fee2038`  
		Last Modified: Tue, 09 Dec 2025 04:38:50 GMT  
		Size: 5.3 MB (5272266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:462dffd9c6726e673a08958ab3559c96c47634b1706c6f9c7b1e8bdb379fc318`  
		Last Modified: Tue, 09 Dec 2025 04:38:50 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json
