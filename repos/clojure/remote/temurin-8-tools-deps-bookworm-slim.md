## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:d7b4d7d3ca9956f3a41e00c9b11d95c242754c9d9ad8f96621f958b345823a00
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cb10bbe8eb696fcdc9c99b062cce5cd3a8e25094ff45eaf4d2a12f55da3da9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152480910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4184d38980fa106b5925ece123ae20603ddc425595a6b7d116a2440c77d4c250`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9295dcfaf08c48c9afa8483b12c147dcb0f5dd7545689b4e85708caff1dae21d`  
		Last Modified: Tue, 01 Jul 2025 02:37:17 GMT  
		Size: 54.7 MB (54716179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69166c228d3522d1b925b118ceeb0b5f9012dedb3fca72357984ce17b5d9f78c`  
		Last Modified: Tue, 01 Jul 2025 02:37:16 GMT  
		Size: 69.5 MB (69533944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0723ffdaa7d917503c3eb981e51bc7ccc37adbd7f550e34a4074163094d3cc`  
		Last Modified: Tue, 01 Jul 2025 02:37:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:02606a0070024718a0895a9b7fd24712d6bf5647480aacd379e97bf1e0fd9e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5247145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4848c0027aa7a35812c28ce933d54cf6e4cb61ee74c8e3350a8868fd018683`

```dockerfile
```

-	Layers:
	-	`sha256:87e4ed06e898a487a0c037c51af15132e1822275216465629703064b5e603b12`  
		Last Modified: Tue, 01 Jul 2025 06:42:13 GMT  
		Size: 5.2 MB (5232854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a269bbaf097aa393fed7fd7341cbf82fd9c40b79ed502c17fd51400d8990b8e`  
		Last Modified: Tue, 01 Jul 2025 06:42:14 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9e91660dc282735529dd50bb12eda9a13a06e7ed1cf4aa9ea1013ccb9a2f0c53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151300104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cccbf4f07b06cfe85f25f515a6002515b0cd130c64972ef43f44f214053de1e3`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad0563892583b6c6ec5d5fbed80818f17182d77b30b2494ba804acaebf04701`  
		Last Modified: Wed, 11 Jun 2025 08:05:34 GMT  
		Size: 53.8 MB (53830509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be00ede887e92938cdd854dc5eb9b4fd821c0f1e01c6644a06a249ae2042e60d`  
		Last Modified: Fri, 13 Jun 2025 17:53:18 GMT  
		Size: 69.4 MB (69391274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d78805309a277683f9cc1de60b7ec131232dc2c073e5d735af22649b0f149b`  
		Last Modified: Fri, 13 Jun 2025 01:36:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8c1f90c4dc3535e111e40cab9a27bb0de616d2d85c425d72a5cc7cbad45d0425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167d915276015a082952f026b253bc72a91f116006193c128264eea4092d76f6`

```dockerfile
```

-	Layers:
	-	`sha256:523965540ef182b75c7db092b82ff63534d07f197f6d78fbc5fb963e5b5d3a61`  
		Last Modified: Wed, 11 Jun 2025 09:42:46 GMT  
		Size: 5.2 MB (5237957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b7f215ae04180a976fb8e02694e2f0107f457b36bf4ce46ff580fe9d2479be2`  
		Last Modified: Wed, 11 Jun 2025 09:42:47 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:285e51cbe07deafde08e59a9a21e57c1d9cbc939d366a6418558a4a183b4feb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159599971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff9ac4064ab5b40d67f112c5799c110fdda6e3712e44cd8f655451e7ebdb1b9`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0942298fc2abdf69cf3e6a970afc1659ec0c0948df86dc3a34aacc3e87a41dca`  
		Last Modified: Tue, 01 Jul 2025 08:16:09 GMT  
		Size: 52.2 MB (52167961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688306c19214c9f446d35e2e3713caaf3997eb659fc03c85b865fa5052a7c37b`  
		Last Modified: Tue, 01 Jul 2025 08:23:25 GMT  
		Size: 75.4 MB (75358545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b2dbb8ef4334ee0523f4fed8493942756aec3b6b4b056328a69048ac712aa5`  
		Last Modified: Tue, 01 Jul 2025 08:23:54 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:359bf5b4ee8e679f2603811269de94c83227968ab81cd882ab604c8b1f7562aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5252944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67da6a052a6f0f58d2ae782afd593ffabb1f324448d6241ff9d48349eb551cd6`

```dockerfile
```

-	Layers:
	-	`sha256:033856111456f8cf09922b6514f525f2a4d957f4d8719ad24858c22cc845e9d5`  
		Last Modified: Tue, 01 Jul 2025 09:42:03 GMT  
		Size: 5.2 MB (5238605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:856c6a81f7a53b3bf75dcbe7d5fc966d413623f8b645a31a93410ea6ad68f36e`  
		Last Modified: Tue, 01 Jul 2025 09:42:03 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json
