## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:725897188e9bc02c839a2cb6930015ab115ce5ae71858156a2f8524f49aa387e
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
$ docker pull clojure@sha256:e953310c19b5773130ed3122753261e53892bc353d06a5ccabcf80d16540f070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255732678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86b9e3980223e76d2867f4a666a3707d4a9b318d32be8986abcbdb22db7ee0a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:03:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:03:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:03:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:03:34 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:03:34 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:03:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:03:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:03:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:03:48 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:03:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39be0bc0ae70c71f5a22c79426a35cb4e8ed11cbc9b280cf055cce21bd2b8419`  
		Last Modified: Tue, 30 Dec 2025 01:04:27 GMT  
		Size: 157.8 MB (157826042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1079b9021a442ae26e8d72a7ee5f1be35127eb4b6659183750c19246803f188`  
		Last Modified: Tue, 30 Dec 2025 01:04:23 GMT  
		Size: 69.7 MB (69677174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c5f106f9ba97b1f26d79e61f42161ca0c49997104f1686fe14c6a7203ae499`  
		Last Modified: Tue, 30 Dec 2025 01:04:14 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5427a36c345b5b5ff64e0123e375e4159bae9c4824c68328be5533006fa148`  
		Last Modified: Tue, 30 Dec 2025 01:04:14 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c5663bc012222a7734c1776f0091e355176f77087b53ada5744fa9b5f5135e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187490c3add6a1c40a3bc4e38321c625fd9ff89243bdc2bea30db42ec55a2cc7`

```dockerfile
```

-	Layers:
	-	`sha256:854e08dcdad6fe2e0e9df600793b378faa2650b720112861decf1264a8c5ddd0`  
		Last Modified: Tue, 30 Dec 2025 04:42:56 GMT  
		Size: 5.1 MB (5116492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:831473b783c0a91192fb4a222dafea73ce2111c41947cbf7075dc307db1f30a6`  
		Last Modified: Tue, 30 Dec 2025 04:42:57 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:313f36cf901204fc4a0104970f88547071dafe6121308469bcb1222626051e8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253769420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2733b089ad9979a822a047f3fcaeea831f409b075e2ebf6a37f4c8628aa285d6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:05:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:05:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:05:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:05:27 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:05:27 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:05:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:05:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:05:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:05:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:05:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41bf8a4417f750772613f49cdda34cad5a241574564374288a0584acb1c2a3f`  
		Last Modified: Tue, 30 Dec 2025 01:07:48 GMT  
		Size: 156.1 MB (156107580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06429ad13f622e4fd4628ab886fe53b3add8adca8c95342e55d6238c1e916f0d`  
		Last Modified: Tue, 30 Dec 2025 01:06:16 GMT  
		Size: 69.6 MB (69558591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f95627e10c83d204eb4cf5801e803484c9f7fd0a2b1845e0c797f46c3e384e`  
		Last Modified: Tue, 30 Dec 2025 01:06:12 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d2a850b8765412f9f6e5df704cfa1891f7a8b835ee5c678d6b8fe51ab6c9c4`  
		Last Modified: Tue, 30 Dec 2025 01:06:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9b7ca19a49b68b789199238a1a75c99161756817ce126537cb5a38e081a98825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6fb3281408ddc675e797c3d0bea9f1d679652b9652f6a94cc799be1a3811c4b`

```dockerfile
```

-	Layers:
	-	`sha256:edaa46777a13e4a1503b77fe4603272f60b3265a9808bc5a70a5b48a1d99defa`  
		Last Modified: Tue, 30 Dec 2025 04:43:02 GMT  
		Size: 5.1 MB (5122253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:477910b840b0ed787dcccc4c4abe472554d76e4b898410a7c64982423341a703`  
		Last Modified: Tue, 30 Dec 2025 04:43:02 GMT  
		Size: 16.0 KB (15953 bytes)  
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
