## `clojure:temurin-11-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:b80c50197321610185e11dbe28c0043e8f0067fce5ca3b42381db40b455e3e52
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
$ docker pull clojure@sha256:61dc6198592a2d2e8f635ee6d6aa9fa957c22becab6bca441ded97182b0ad459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244624093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37e139acf35ee6c8690005f46a42cf2b218dedd90d7b081e79c415ad902ca3d4`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:16:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:16:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:16:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:16:54 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:16:54 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29ed2b38d0eceb355c225a1ea29df7c7c356e723d29293cec122e302bf99aae`  
		Last Modified: Wed, 24 Jun 2026 02:17:34 GMT  
		Size: 145.9 MB (145886167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e210dbfe613a1692995655800937e476b18cbd8ec1b2d9b75272f77ad0293ee4`  
		Last Modified: Wed, 24 Jun 2026 02:17:33 GMT  
		Size: 69.0 MB (68951862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666d0dede8687b8673589f56dd8167682fed8aae32b9c5e519e375aa41c1f104`  
		Last Modified: Wed, 24 Jun 2026 02:17:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6ebbfd9f9dc1dc6913912c1ccc453b4b3a3093c8a0677defe5849b6f747f2cb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5291155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607a1ea7ff363e7d1f78501615af71826b876bd72c7361c86f1009d689e7e2c2`

```dockerfile
```

-	Layers:
	-	`sha256:7aff31c0eed741545f6daf8e179095675cd98785476ce25607e9a618fce1bbe1`  
		Last Modified: Wed, 24 Jun 2026 02:17:30 GMT  
		Size: 5.3 MB (5276758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b00ba2dbf93720764c93818e703b58537b0e67807b560f77bad85285c0dd780`  
		Last Modified: Wed, 24 Jun 2026 02:17:29 GMT  
		Size: 14.4 KB (14397 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7f453c1e5667f394632301429484f6baf1652b0971c326ddc7cfce1291a76c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.5 MB (241508885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a940f0eac9ac29baf5287bd0a62e2bf39ceab1713ea4d06ce9fbf75ff3f0b3c5`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:23:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:23:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:23:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:23:29 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:23:29 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:23:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:23:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:23:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b481e690ed9259247e406fb8c177ad527db3ad6ee3ae560a7bbfa2215d954e3a`  
		Last Modified: Wed, 24 Jun 2026 02:24:08 GMT  
		Size: 142.6 MB (142582130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6185b7b0175ef7ae7b7f0cd02a96421fa0b1404986a9ebee57989ce4b736363d`  
		Last Modified: Wed, 24 Jun 2026 02:24:07 GMT  
		Size: 68.8 MB (68777559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736b03594c8c12fc909c3f390af0f494c040948c44174745b10f7b6ef7a00946`  
		Last Modified: Wed, 24 Jun 2026 02:24:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:04cbe2941abf658f0d93ecb200e75d6745b84a92f9298e2d5f8cf89d7f2f77b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483132dbe01fe6162e9000e9de0ddd834d0993b52492aedd8b98d1dfea683327`

```dockerfile
```

-	Layers:
	-	`sha256:66033af8e4dc43430e7fe945d882418e6943150ba6a2e283cee24efad42fc848`  
		Last Modified: Wed, 24 Jun 2026 02:24:04 GMT  
		Size: 5.3 MB (5283137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a84ac1912c3864d42d2eb5fa6dc9a68899790fa4bb1cde94109d760f01a96006`  
		Last Modified: Wed, 24 Jun 2026 02:24:04 GMT  
		Size: 14.5 KB (14515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b9e8fc027dd21dc94b38209ddd1b0971e3657325f91efdd8f96262bdc400ab28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241086732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bed84b8143c52913ca589b6c97eb5ad0fbbddbeb4bdf1644750ff2e3e4a97ac`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 07:55:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 07:55:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 07:55:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:55:31 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 07:55:31 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 08:00:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 08:01:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 08:01:00 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:639e1c13483ea279c94219be2736856262d8dd2efeff3e6d309f11a66aba21fb`  
		Last Modified: Wed, 24 Jun 2026 00:30:29 GMT  
		Size: 33.6 MB (33606388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db522026de845aea7c62013762889066999c7eaf835c33375388fea3c6f40605`  
		Last Modified: Wed, 24 Jun 2026 07:58:47 GMT  
		Size: 133.1 MB (133110641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f257c02c6e7e6ac73aeef5603a2bf608f409fbe5edb4a8caa73419ea1a64c7`  
		Last Modified: Wed, 24 Jun 2026 08:01:38 GMT  
		Size: 74.4 MB (74369059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ede590cb94395e99a2a7e11e26676112019e16a3a320b7d7849ddd1bdba9cd`  
		Last Modified: Wed, 24 Jun 2026 08:01:36 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:adecb8761ffb2667ecb8c1c31cb3bce11bda119db843afb000f7319f8499c128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976c860d207f1423f5ac800cb171f3588e4fb4bf88b98acea9c9d7e6ae602f1f`

```dockerfile
```

-	Layers:
	-	`sha256:d0f2231829d532c8273f0c5f18ceba18bb5c7f26100b5a1e7431a28f23e580fb`  
		Last Modified: Wed, 24 Jun 2026 08:01:36 GMT  
		Size: 5.3 MB (5280514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0cf2a7a00c2fd9be35b5376b9e88740c5993bfb0779a73321db9db53c7e0bf0`  
		Last Modified: Wed, 24 Jun 2026 08:01:36 GMT  
		Size: 14.4 KB (14445 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:90447d1750a819a96ff5422a11b84c293224fdbb5dae40c635424afca366033a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226437141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd34017ebed3f22cac6629cd7410f7700c69084a4924cf1f2a60b52b37adb13b`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 04:10:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:10:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:10:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:10:59 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 04:10:59 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:11:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 04:11:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 04:11:16 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b6a0af2ceb4b698210b8776157288a3fb06e46aaf75d641139449fcc50ce430d`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 29.9 MB (29851381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92e1d8e93f5f86f3914c4f73e63834b0bc2589b294234b882a1e9d1144b73cb`  
		Last Modified: Wed, 24 Jun 2026 04:11:43 GMT  
		Size: 126.7 MB (126652564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8c99c90ee9aae35570a02b81ad7937377e9e7166b2e100b3cc55a98809890d`  
		Last Modified: Wed, 24 Jun 2026 04:11:42 GMT  
		Size: 69.9 MB (69932550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74df3f27afcf92742ccfbd5e35e2cd7ef8e55269ca33f0bcb7b2b8756207f4c7`  
		Last Modified: Wed, 24 Jun 2026 04:11:40 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f407c6a7acfe8664fd6989b695f32960ccee563e0ebfa2c161979d438d13941d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5287083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd6bbcff89c2fa841095f3897e9012d5a95981cf9c25490be131a33c8e5f4de4`

```dockerfile
```

-	Layers:
	-	`sha256:473bbc8558edb3b5474e37b54f3f92bdc6885a6e5cef4faea7be23d483b1bdcb`  
		Last Modified: Wed, 24 Jun 2026 04:11:40 GMT  
		Size: 5.3 MB (5272686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5de4a0d2cd624abd1442d0466c189ad6abfe1cc07132df3fceb90fa6d4cba02`  
		Last Modified: Wed, 24 Jun 2026 04:11:40 GMT  
		Size: 14.4 KB (14397 bytes)  
		MIME: application/vnd.in-toto+json
