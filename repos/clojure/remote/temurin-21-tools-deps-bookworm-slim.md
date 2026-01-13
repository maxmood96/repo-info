## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:d9716727fffc26ede3345e24ac5c2686ef2a1f8404642ab7713c0d85fc26007a
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

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:fc8e9d2c6d657c8a4746dbf3a0937afdeaec2814606859318627672ccd78ad98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255732373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8326c13663c22d5d0f2a96ba6d97379eb5be26cff067e686707a30de61607768`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:35:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:35:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:35:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:35:45 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:35:45 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:35:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:35:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:35:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:35:59 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:35:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5923ceb83ced0d49735199f4791598aa5191f4ecfce292203c014a0857d9b8`  
		Last Modified: Tue, 13 Jan 2026 08:16:10 GMT  
		Size: 157.8 MB (157825957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2b3e37ae79066e36ceeed2bec7c5d835b12ae7b6fe32fbc703456015d04038`  
		Last Modified: Tue, 13 Jan 2026 03:36:32 GMT  
		Size: 69.7 MB (69676801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b99411d727a1bed083309f39d6046178c000a8df41ae7275328b90ac0e8d645`  
		Last Modified: Tue, 13 Jan 2026 03:36:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4a4ec40a4719687f1cf48a15718f9217aeef80164379497f0347c26137f3e6`  
		Last Modified: Tue, 13 Jan 2026 03:36:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3bf3e0c417f547d15ce84bb47e39254e1678ad2d3cef7bfa84dc21ed3e829bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1531484f667c5dcc8d271c48a41d4123ff1d9ef1caf0e60de03acbf672dd4536`

```dockerfile
```

-	Layers:
	-	`sha256:a2b5913ca8c339bf9d92c5385e0ac3d7e743534131aae116ae11148c11a1a103`  
		Last Modified: Tue, 13 Jan 2026 07:42:23 GMT  
		Size: 5.1 MB (5116502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05dd3cf548002e1dd41a035522d86e6d5d78d2fcc42236e0c0a038cfd7ce8102`  
		Last Modified: Tue, 13 Jan 2026 07:42:24 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3492fc6a1f761df694a2a6f27991bb620b34d8488885a29ca2468be2f881b6a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253889201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc17e4c062fd6a5b1dabc3e705491d6cd41336e793d84a054326e72e2ea2a03`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:39:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:39:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:39:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:39:05 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:39:05 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:39:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:39:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:39:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:39:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:39:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d389f14ef53abc291e26db566dc411b559aecded673e9c299675a360fdc6e2f1`  
		Last Modified: Tue, 13 Jan 2026 03:40:09 GMT  
		Size: 156.1 MB (156107580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1446fde5a888baf83ff692cb9eadd04849e6623e72fae2d5ee8160772eed4512`  
		Last Modified: Tue, 13 Jan 2026 03:39:58 GMT  
		Size: 69.7 MB (69672697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fcbb0b707dc695796681a70dd07e2252feb5a4efc548e95f5fbb76f023eb013`  
		Last Modified: Tue, 13 Jan 2026 03:39:50 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da985f17ac43ad82f119dce1c5dfe5b04fcfc68b415220388217a9f5d8b30db`  
		Last Modified: Tue, 13 Jan 2026 03:39:50 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5b1d59551dae5184be88baa945a9f44d4290c6918d6b77908812b26b38efb2ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1679b41e0d849cfd8d5a25235ec171c019dadf073e05b46139f9eafc2c89b753`

```dockerfile
```

-	Layers:
	-	`sha256:1cc288f70415fcbc206dd9677f7927fef06017e611c3b20b0a41a2c01ce9bc89`  
		Last Modified: Tue, 13 Jan 2026 07:44:25 GMT  
		Size: 5.1 MB (5122263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dc5b438102f2967502495fa1c9cbbf350c423f5e778c903c0606ffef43afe1a`  
		Last Modified: Tue, 13 Jan 2026 07:44:26 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e2ceaff619b2f045c467c454d4a22c8382197b51f8bfc08d8e26c6d9c5aab5b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265522267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7117f44417d58546774a58d482af43d12394506b99d68d9cd103378a39ff7e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 05:21:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 05:21:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 05:21:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:21:25 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 05:21:25 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 05:25:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 05:25:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 05:25:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 05:25:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 05:25:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b7648f01f6858fc79caf032b4b9ed2f7e43e57f4621dc8cb36e84eb86399065b`  
		Last Modified: Tue, 30 Dec 2025 01:48:36 GMT  
		Size: 32.1 MB (32068844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5205a1e1f7238574a7d52bb96b174549098b3440c35820756b8c8be70a79f64d`  
		Last Modified: Tue, 30 Dec 2025 09:15:38 GMT  
		Size: 157.9 MB (157942950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884922ccee58bfae788790537adf8e1b7b3a9434e1c8331159e768f3d30080e4`  
		Last Modified: Tue, 30 Dec 2025 05:26:12 GMT  
		Size: 75.5 MB (75509434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6499ab138731601a536b0c5dc8af0f43681f5b8b394694731c302a9b9ad1dc22`  
		Last Modified: Tue, 30 Dec 2025 05:26:07 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1de86815effa201e602af84bda0c79807b45e44494154f45e596a8dd8a77589`  
		Last Modified: Tue, 30 Dec 2025 05:26:07 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:66a77b72b33f1e50471006b2eb97acc56dcc9280966ad8c0c7155954ffea3e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7434c11361db9bf8981085335871251848b1fc93d18ecdf33f115cd7a1086b`

```dockerfile
```

-	Layers:
	-	`sha256:64d26bd25055bc0660fed37b8516420c2642b8c0f2ad57702594107c4e2f877d`  
		Last Modified: Tue, 30 Dec 2025 07:37:28 GMT  
		Size: 5.1 MB (5121650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebfa3c91f3d04f4b6820ab66eb6904b5014a1025f14038ab5b4e863e2f1efd89`  
		Last Modified: Tue, 30 Dec 2025 07:37:29 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:cc07864170add48b94c5fab4387ef3316a22bc95b65c7f9ae634e4bf032631d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242444044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db76f8e95d8f50a478b05066633f0a6c1f2adbec37ec205ff9a343839c314e3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:06:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:06:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:06:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:06:42 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:06:42 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:06:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:06:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:06:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:06:56 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:06:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fb6894e1f12f7f6ff68c6cd69049701aa243a341b92ef4221c450f5c1d6de9`  
		Last Modified: Tue, 13 Jan 2026 03:07:46 GMT  
		Size: 147.1 MB (147069812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88230550749b2815c44935a938caf57d7357a50d10bc81918e0576b224517c7`  
		Last Modified: Tue, 13 Jan 2026 03:07:36 GMT  
		Size: 68.5 MB (68488780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df4cd7c7b117714a5f86a29cf3061916bf9b50caaa0f707823fb0492129e15e`  
		Last Modified: Tue, 13 Jan 2026 03:07:31 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea734180d266dd12fec0ad4a1b3948eaa1a953114f522a93d5344979f55f358f`  
		Last Modified: Tue, 13 Jan 2026 03:07:32 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7d51aad169c4be03b4f6fac464cc0fd2c10b71780880f1e90dc115390fdb7cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3903dd6fdd83236cd0a2d73a36f6c90e7d4f9ca5f1afd00e9ba219489bc721`

```dockerfile
```

-	Layers:
	-	`sha256:a1e7b84af2276cbe49e2efc05e3d61c3628c90e3fa984995db6fe7a14c1ae0ed`  
		Last Modified: Tue, 13 Jan 2026 04:38:42 GMT  
		Size: 5.1 MB (5107823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f32a6a919eac2a969ff9ccac6fff02e07ea9e735284d1e49d04673dfda543c`  
		Last Modified: Tue, 13 Jan 2026 04:38:43 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
