## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:3392b83019183620b6772aea52fbc0e857adbf706702766fc9bd5281474e9985
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
$ docker pull clojure@sha256:2442370832bd303cc78f1abd876997589f12c0cb851c30982f1b4a2b4a7473f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152639324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72133c8cab1c676e26361d3053b98b13a835a7400e2f9016294f2bc16c81da78`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:20:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:20:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:20:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:20:45 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:20:45 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:21:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:21:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:21:00 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e385a739448a49a5e1ae688485241727ce651a2782a1cbcde2691312ae17798b`  
		Last Modified: Tue, 13 Jan 2026 03:34:10 GMT  
		Size: 54.7 MB (54733389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413667720faa9d91b3a224bc36beda19f90bf9d2dff3dacb42b13dbf58c00434`  
		Last Modified: Tue, 13 Jan 2026 03:21:28 GMT  
		Size: 69.7 MB (69676720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118e01f2def4902c04f64a95324bb9cc47f2542f414a2a071c793875c553547c`  
		Last Modified: Tue, 13 Jan 2026 03:21:24 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bf984608e0f4d07087e552a6c4e2b4cb107e4410c7ac7275379e0c45c58fcbd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83350fa61b068da2141ce420080f8a896936cb3b191469c0543dd4dee1e11be9`

```dockerfile
```

-	Layers:
	-	`sha256:19970415846c2f0f14766f4bdb2981ce15807ad6619693c23039c00e525c08b3`  
		Last Modified: Tue, 13 Jan 2026 07:47:49 GMT  
		Size: 5.2 MB (5235008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b39c7213a985325ef904e6cc3a7d069521b9a6461ab37f35eb697e0b3ee9bd8e`  
		Last Modified: Tue, 13 Jan 2026 07:47:50 GMT  
		Size: 14.2 KB (14247 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dd1259f5f3ead976dc1a9dc21c7c0ef8fb4c7e989e29065d9e84784317cf9c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151596051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a56dbbf5c1b84ed4fdeba3d81fbd0ddcfaa133a8e1f6b5c869603f6b9ed7a9a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:28:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:28:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:28:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:28:30 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:28:30 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:28:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:28:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:28:45 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d78cbde03cb03a76bbc8fa24068f7d19d610f8b53e5c90478bd860f16fb1cc`  
		Last Modified: Tue, 13 Jan 2026 03:29:13 GMT  
		Size: 53.8 MB (53814993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c473677bfe2a5335f91d01e50b7ad0cf1ecfdae8e44cd983dfe4a165e226d6`  
		Last Modified: Tue, 13 Jan 2026 03:29:19 GMT  
		Size: 69.7 MB (69672526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a71210196227a2e68ff835a91b6e4321add3e05f6963a3436cb9db68dc45bb4`  
		Last Modified: Tue, 13 Jan 2026 03:29:09 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:88d768409d610a30b78723e84f84e01f82fc0d350e632a2ecb11b5445cb9a9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592c25b0be415cfc91063f128b487320bd82cca9256b8fed00ab9e76e0457016`

```dockerfile
```

-	Layers:
	-	`sha256:bb1b4a7623f011e89c2f110fe253e00e9d9db2f628646e41091b6d829ae3d2b6`  
		Last Modified: Tue, 13 Jan 2026 07:47:55 GMT  
		Size: 5.2 MB (5241467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e309902a370db8ca60e5c323389de108813d7678cae25f6a41454b135fb4a2b6`  
		Last Modified: Tue, 13 Jan 2026 07:47:55 GMT  
		Size: 14.4 KB (14365 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:5cd8ac6ea8ab6e87d60c789217663a3dacbc0676c8a026333b16f375607e7a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159757130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e809e511895b9dddfea2e5ed0578ca34ce7d9604986f5bdf6d07b195ee16c251`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 02:55:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 14 Jan 2026 02:55:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 14 Jan 2026 02:55:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jan 2026 02:55:56 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Wed, 14 Jan 2026 02:55:58 GMT
WORKDIR /tmp
# Wed, 14 Jan 2026 02:58:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 14 Jan 2026 02:58:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 14 Jan 2026 02:58:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:24 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e347cbd2e91bcb301cef8b394f60db373b540ede97dc905d61207646be4178b`  
		Last Modified: Wed, 14 Jan 2026 02:57:40 GMT  
		Size: 52.2 MB (52175137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3273ab96645a1bdcf4d93108b96287024c65b8d17b86bd03c22fccd6b19920fa`  
		Last Modified: Wed, 14 Jan 2026 02:59:34 GMT  
		Size: 75.5 MB (75512639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd90ee5cc04d5eaf2f43fa42d9e1b5e7d40235fc8629b15c3fad3ae69c977f5`  
		Last Modified: Wed, 14 Jan 2026 02:59:31 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b4ff2ba724e73f17b84426a9c876db871fcf9b0249a9dd5448c13a08d625edeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e500529a8f8262806f5ab175162864dd81ea1189b2388a8c177040c8721289`

```dockerfile
```

-	Layers:
	-	`sha256:af9757c864b17247c55b746404b49b2c99f101f5c004cb0c84e35f55cbbb71de`  
		Last Modified: Wed, 14 Jan 2026 04:38:02 GMT  
		Size: 5.2 MB (5240759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79720c845c2f1ca264a32572c75c1e736b6c716242a36a5b8ef34acbfe62fb3a`  
		Last Modified: Wed, 14 Jan 2026 04:38:03 GMT  
		Size: 14.3 KB (14295 bytes)  
		MIME: application/vnd.in-toto+json
