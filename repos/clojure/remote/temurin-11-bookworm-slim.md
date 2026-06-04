## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:860472f2a8ff20e7d5cc72eb2437d4462e4b22b5f7c0bb0ffae2db6b9544e5cd
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

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:afc2af7f99bf11fd12c4a9da052c466c98c7b093ea8baac4a3e147c6efddf062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240762146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be6f1fcab9ceb1f66c709f5ab69eb7870369d79dafe7d892a2aa2d108b21a04f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:43:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:43:42 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:43:42 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:43:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:43:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:43:57 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1f4b9a21b84d2dced0279863d8a99731e97c3bcb306adb1b71b741c694a265`  
		Last Modified: Thu, 04 Jun 2026 17:44:19 GMT  
		Size: 145.9 MB (145886201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c003a5bbaf8b1db795d111ccee023b252b5b3e13cbd27a538e6b9e3be7ee45`  
		Last Modified: Thu, 04 Jun 2026 17:44:17 GMT  
		Size: 66.6 MB (66641759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37452fead5296df7254a78cc41c90b56f5f2f70a48d1d34994118843efda4cf`  
		Last Modified: Thu, 04 Jun 2026 17:44:14 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e5077d78235c947cc10ecb618db7e84931a9e988b7b2d6c68182b54e812bf42c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5147917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74f62c78234a3540b2f22cefee7f864d04976bda44987724e77a8d6b3f56ab2`

```dockerfile
```

-	Layers:
	-	`sha256:19ea83f2eef10d0696a6c562df2e48ffd576afb805ad5943123bccc51af8856e`  
		Last Modified: Thu, 04 Jun 2026 17:44:14 GMT  
		Size: 5.1 MB (5133497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a6a406adef0ef9ec357c21d6305bf98645395633b52c59247a1c692455a55a6`  
		Last Modified: Thu, 04 Jun 2026 17:44:14 GMT  
		Size: 14.4 KB (14420 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5751d4f5f65fd240dd47a6e912817a863ef7962cf643e6b46c400a890d7ad334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237341215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea0f92fc31deb945597fb0e657e2accbf2f369094781b4d8820151ff1c1a3fb`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:43:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:43:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:43:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:43:26 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:43:26 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:43:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:43:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:43:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820ad44411a77efae3f857c1cfad230f7e40d633181a29cb9d450b6abb05e3fa`  
		Last Modified: Thu, 04 Jun 2026 17:44:02 GMT  
		Size: 142.6 MB (142582235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e11cc2a66f2e40e07273751dbdff42c8c6596ed9465daa55945d13be66dbff`  
		Last Modified: Thu, 04 Jun 2026 17:44:00 GMT  
		Size: 66.6 MB (66643290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bd1c13d78f034a58259ac96414f3eac526b10d8a55eaaf2d65cc4f09f3e0fd`  
		Last Modified: Thu, 04 Jun 2026 17:43:57 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c85c9fb76b4c149c7af0ceb2a3e4d282e1b4e1ba9bf9bcc411b8a137da30d356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5154414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5dcf37ca3af2b76ec1e02bb63c6478a48e59479b88de41770fa0da91bef8e1`

```dockerfile
```

-	Layers:
	-	`sha256:3245589e56e9430e9badd0252a1951edcd0d1462e7ffb38ae895e18320fee339`  
		Last Modified: Thu, 04 Jun 2026 17:43:57 GMT  
		Size: 5.1 MB (5139876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c6b3d4f143b1c4e0921db2f5bdff38c6dfc7eda5cf40e07f7ad37161eedd7d0`  
		Last Modified: Thu, 04 Jun 2026 17:43:57 GMT  
		Size: 14.5 KB (14538 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:5e13332232c38e0b7a4d22762d942eba854c38bc62ffbe6de7b68f14f812092f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 MB (237662295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851e6cfb30024bbc12841d690c32356f6bc4e3640128579be252eff4952f5cfe`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:47:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:47:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:47:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:47:50 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:47:50 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:48:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:48:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:48:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617c0d285f6de64db1a5978e6b8056ebad15a1c14c41574df90fd2cc4d026505`  
		Last Modified: Thu, 04 Jun 2026 17:49:12 GMT  
		Size: 133.1 MB (133110217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948177c9cc2f84801073612b513cfcd37999f61e5954a8f37e0c768dd4c8de68`  
		Last Modified: Thu, 04 Jun 2026 17:49:11 GMT  
		Size: 72.5 MB (72475692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdd9d791b302b4eb56bfc52d94451fffa4e5a592ca133397742308379276a0b`  
		Last Modified: Thu, 04 Jun 2026 17:49:08 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7ab8bdf46d07b55f2d21a66f751a153bc4038a439bfb07f64de3017989e77f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d60b9dae90beb33131526b43a8744dff823273953938bd739e46c2895d00c7e`

```dockerfile
```

-	Layers:
	-	`sha256:35c20607c3b0eeaa11032246ef45f2ede305956d5bed805982a0637773b1cf04`  
		Last Modified: Thu, 04 Jun 2026 17:49:08 GMT  
		Size: 5.1 MB (5138040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45e08bc34eee9cef85c05affbcd8a62a64ffe572b32ced4b2669e94a7da6408f`  
		Last Modified: Thu, 04 Jun 2026 17:49:08 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:bad6d3d8b46f9d1ae2da2d704c19afb39e93a8639ce54cfec196bfca1d11ca9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (218992566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e53ba0c5e60beb2ea0ee8383560f6b5c5aa2d7aa95fed0bcedc2d872423f04e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:40:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:40:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:40:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:40:07 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:40:07 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:40:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:40:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:40:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac49fd538b5309e2488498a57ffad63ecfccbf655dbc77a5d9779e16c146505`  
		Last Modified: Thu, 04 Jun 2026 17:40:58 GMT  
		Size: 126.7 MB (126651735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c5623eb01dbaa748ae8c67201448354478b3826576de955a8d45355c023b5b`  
		Last Modified: Thu, 04 Jun 2026 17:40:56 GMT  
		Size: 65.5 MB (65451589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a35a8c60efc1cd9eefe2934fbbfa11eb30996d43d31ffdffc6a0590cec882c5`  
		Last Modified: Thu, 04 Jun 2026 17:40:44 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:39835bc13f25611bc102616dffc17caa69f16756c72045eb33d32f4ff1bc3bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b7dae8e4cb2728b39ea5c08e7ce7db8766f6171e64355989b726b6df947272`

```dockerfile
```

-	Layers:
	-	`sha256:5de061051208f5de8ee74df2bb7bebe11bb56e0b81d1a53f894f0708f0be459c`  
		Last Modified: Thu, 04 Jun 2026 17:40:55 GMT  
		Size: 5.1 MB (5124822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:595986f5430df192f0655bb8b79ef02d75d06bc78361c34b7d047b58adb39804`  
		Last Modified: Thu, 04 Jun 2026 17:40:54 GMT  
		Size: 14.4 KB (14421 bytes)  
		MIME: application/vnd.in-toto+json
