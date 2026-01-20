## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:3a48dcc50e521384d840bdf97962da18fbd96fe78a2a043ef082ff92c6c3a8c6
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

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:dea8f799c7879884bcefd84ed480be394826700f6bd4692355457080f1197704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274595065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f35ae9f080670d6e2de82865e7c2726b4321e98b32628613185edf3229a3fc`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 01:48:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:48:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:48:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:48:38 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:48:38 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:48:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:48:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:48:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342e73393df7e0a133007fec0fb305d12160e4fde3ee25572b856cc19874dd2a`  
		Last Modified: Fri, 16 Jan 2026 13:18:22 GMT  
		Size: 145.0 MB (144966605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0973f1e881cb7719327e672fac88940d626cf9aa1c2b60b8018ff7a53b399175`  
		Last Modified: Fri, 16 Jan 2026 01:49:34 GMT  
		Size: 81.1 MB (81146193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec3190d68a69dceb34fee1b9cc92f41cae2940d1a04402dd7735d928df2db13`  
		Last Modified: Fri, 16 Jan 2026 01:49:28 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b1acd89e03c4188c5bc5452f88af23294193977f2808232068a29790658bda78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7409882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04ada676e044975a3b239eb678a1906018c3fd85751bbdc424f8fc73c0837ec`

```dockerfile
```

-	Layers:
	-	`sha256:2bc0e3c41b8cc4868fe29f03e8ee0c1bd973a725f706ee0785d641f2148d8314`  
		Last Modified: Fri, 16 Jan 2026 01:49:13 GMT  
		Size: 7.4 MB (7395674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca1c56e7c0dd2bd5c8ba9edf95f15120618fc9e6f14f765d6a5bb75b3c1a3141`  
		Last Modified: Fri, 16 Jan 2026 04:36:35 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8e59666ea885c74d73a141d9ad85809c423538ec8c1d0b0f1ca47f831006020f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.2 MB (271235558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844bdd712928a9595566d7b49363aa769a32396a4e33e5d64d786e29078e64fe`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 01:49:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:49:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:49:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:49:26 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:49:26 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:52:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:52:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:52:50 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68993437777b5d670ec9b7aeddb678683498e7be55882f88da00c0254462de4c`  
		Last Modified: Fri, 16 Jan 2026 01:50:23 GMT  
		Size: 141.7 MB (141729892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97870c83a9da7d210feb88c99141304864e34de4a5cf17761c773ed607014e53`  
		Last Modified: Fri, 16 Jan 2026 01:53:20 GMT  
		Size: 81.1 MB (81138948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0939ea76bd05d0b4f7d0298d1c064781254e88e9e18df54d00bda08782f9a5c2`  
		Last Modified: Fri, 16 Jan 2026 01:53:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5592bdcbe6863daac40b445d5ebc7fa533b79b76d9b44063103e28bb3c8e550c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee3ae1ebc7ab61d377593ed45f7d739f60836e6779c054958685d68fa665eb6`

```dockerfile
```

-	Layers:
	-	`sha256:665a200c0bd2c5fb4903e5cd627eefe403ec1aaadc6d18eb206a3b2849ab8933`  
		Last Modified: Fri, 16 Jan 2026 01:53:07 GMT  
		Size: 7.4 MB (7402055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d986225256b9ce9055fb72489c445c6439cd1c9994dc2b31e5533f55a6649f5`  
		Last Modified: Fri, 16 Jan 2026 04:36:42 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:72cb9f6fd35c86458c40dbc8ade1d4de90c4404272e341ab02a316f1edab1241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.4 MB (271394507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6048f9e6fa9dadbc9551d9d3cf28b19c7ee027cc4ffdadb9ac767f35559385`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 02:57:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:57:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:57:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:57:36 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 02:57:37 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:05:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 03:05:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 03:05:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:14 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eead296b73556d112badf522de2dbc3e1be7cda774b3a4b3b8e819c745a21881`  
		Last Modified: Fri, 16 Jan 2026 13:18:38 GMT  
		Size: 132.1 MB (132079791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9881531dc2bb36c260e251f48367ca0161f9a41d76502af1aab31f58f7cf23`  
		Last Modified: Fri, 16 Jan 2026 03:06:47 GMT  
		Size: 87.0 MB (86986695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a627ad3939f8188508bab4fc092cad01a9b5b206e5a563f13c0cc9ab03ef446`  
		Last Modified: Fri, 16 Jan 2026 03:06:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f15d42fcf3c4b290813ecf8edcc90541a2a5487707703570ff20d402ee52d0b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7414532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a095828bd2b3232eef3d59f6d8e8ae64ef4dcbe090a5373bf3a393d985d27cab`

```dockerfile
```

-	Layers:
	-	`sha256:11871814756cf7feb9502e04d9825f8f8ad860a6cc9ef4072758419b129e93c0`  
		Last Modified: Fri, 16 Jan 2026 04:36:49 GMT  
		Size: 7.4 MB (7400275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fefb18a16c345e15e198bbd3feb62cd3d86666407c41de2f176f5b3dcf58a892`  
		Last Modified: Fri, 16 Jan 2026 03:06:29 GMT  
		Size: 14.3 KB (14257 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:1a6a665841e04ae387de1d7b8f3775ff2ed236674a8c46cc1d6fbe7cd3d9d543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252793203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fc0fcb553424b482b59a9a62fba5801e90328b4337e5a0d869d6bc28332327b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Thu, 15 Jan 2026 23:09:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:09:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:09:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:09:26 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 15 Jan 2026 23:09:26 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:11:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 15 Jan 2026 23:11:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 15 Jan 2026 23:11:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:05 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59abf91bf32833ab74c59ea60fc048ddcd4ca740e0a01d6956ae969a791f34e`  
		Last Modified: Thu, 15 Jan 2026 23:10:17 GMT  
		Size: 125.7 MB (125694886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db8e920fc308e5df033e4e5f00bb2a487dbd60624a7cdfbd00587903641a965`  
		Last Modified: Thu, 15 Jan 2026 23:12:34 GMT  
		Size: 80.0 MB (79959242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0cd2cb7bd64316fdc613fab46b2e9936dd3d2041d101c4d658afc8d4c9b561`  
		Last Modified: Thu, 15 Jan 2026 23:12:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:438b415f48d5aeb480ba80ae3b77fbfe28ac41cb94957c292e93f077a4f96c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8737951f18a4854d2fcdb20f0ca66fe74e72dd6e4c7ceaa5920dbcae4f2ed70`

```dockerfile
```

-	Layers:
	-	`sha256:a6d055ce78ffdbc9f9683ee1675f9f67d70a4afe249d6b8c50f2354699f01ffa`  
		Last Modified: Fri, 16 Jan 2026 01:36:53 GMT  
		Size: 7.4 MB (7386997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59befbaa26203a2da91a50dd12d9b9da2587e9db4f90b264b139e9d165bd0a17`  
		Last Modified: Fri, 16 Jan 2026 01:36:54 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json
