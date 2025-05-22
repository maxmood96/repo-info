## `clojure:temurin-24-bookworm-slim`

```console
$ docker pull clojure@sha256:34ccf4d6f33e0410f4375717173b4a2c393dd11102afd46a6c595faf483dae25
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

### `clojure:temurin-24-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4394a4ea9be9e9780f667d23a259781f63518899af29af07be844dc9da2f12ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187709620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc24ddf9e54eba6b5b9c091ed61a666cfbe193f383c3b33659781c063a75bd4e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4de3cccbb44e73be6db1cd1c698b1c35a23502204a190f4ee7311924c73c99b`  
		Last Modified: Wed, 21 May 2025 23:33:45 GMT  
		Size: 90.0 MB (89952000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2daa1a6d55354499cda42a240465e03378823e2973d25cf962bd793eee437cb`  
		Last Modified: Wed, 21 May 2025 23:33:45 GMT  
		Size: 69.5 MB (69531250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54370bf70c81269f3776349f6282d0fcf50dfeedd5982a505df5b3afa2121c1e`  
		Last Modified: Wed, 21 May 2025 23:33:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7338638d3499622e7541fc57c0da4ac06b96d8f6341a65f5c23eb37ad08d175f`  
		Last Modified: Wed, 21 May 2025 23:33:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f2132046ffb6a7f3faa6720d781a38694838b1e1a66918f63a1ff5d27ddca4cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd5bda7eb35e550e626d8b99b463186e75a2e32a6dea53475f7b6bc1fd5296f`

```dockerfile
```

-	Layers:
	-	`sha256:38252b5d28b9c7e4e67a47444ce6c22173375bbdbaab2f6a03976b7fd3be425e`  
		Last Modified: Wed, 21 May 2025 23:33:43 GMT  
		Size: 4.9 MB (4912144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f0e6095aec78f10cfb95b6fb93a63134248852485ea366874b1a8332004d34f`  
		Last Modified: Wed, 21 May 2025 23:33:43 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e51ed09b2fb1bc0e72f8608249fba0ce297d06c5222d4fe7e5d13024f3050cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.5 MB (186543783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978bc30766fc8bf140d8fec0bfc3e28c44167a3ddb34458bce57b57b7a0bb6df`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6817c00a35ed33ec5d0a26775ce61734765ce7050a5b559cfe2d379bcea015a1`  
		Last Modified: Thu, 22 May 2025 08:39:33 GMT  
		Size: 89.1 MB (89091257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265d1137a545bc4f1008b7e789d9d44023c6b77fa83b38c5d7fb34a79dafd215`  
		Last Modified: Thu, 22 May 2025 08:44:41 GMT  
		Size: 69.4 MB (69386205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696317182a64cbfd24b382a932050869b7aaea8503b7d296f87ca3dc2603bf87`  
		Last Modified: Thu, 22 May 2025 08:44:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539d49140e3a5f2282dfe3f6d265b8028a5cecf9f802db32206ff78eb88b32f6`  
		Last Modified: Thu, 22 May 2025 08:44:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8ce06eb3a2051db236d5851c58dee97f450949cf263de88d0f0767c4bcf9da92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f915d96687c437e53473d3829cedd447fd8a89cffd10fc98d0d0d55a1781cb32`

```dockerfile
```

-	Layers:
	-	`sha256:cd9fd63028b6b1362138c2476fdb45cf06b284c2bdb055f3e18cf1bad02d2e49`  
		Last Modified: Thu, 22 May 2025 08:44:39 GMT  
		Size: 4.9 MB (4917902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7db4fc69174822246d9354792aa30eb6583b83b22ae2eb5734136ba5f7b6a9fb`  
		Last Modified: Thu, 22 May 2025 08:44:39 GMT  
		Size: 16.0 KB (15989 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ed03193b0b5f4dc2af369275f9f364b1eae1a5efb6bc0ecb09bd72c9073748dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.3 MB (197334367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0358e268b8b1791f8d98509e9446837ad214e3f2f55a1fe889a6679f484db1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be9dc822e6eae36756c1b8884d36306ddbe0196781d2d67dee4df325851278d`  
		Last Modified: Tue, 13 May 2025 19:32:20 GMT  
		Size: 89.9 MB (89920243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c957b2d0f83b6f42e356b7a001da2b0ff4c603bae08066b7586a22a71d1e6e06`  
		Last Modified: Tue, 13 May 2025 19:40:14 GMT  
		Size: 75.3 MB (75344637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4d18d3339c04a723f74c6e78d5cb49258deb4b87c6b141ace2bbdbdc746320`  
		Last Modified: Tue, 13 May 2025 19:40:11 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c577f407633f42370d1357ba1b8d6565e4f3083a3fd064843bdcfacf0e6cb32c`  
		Last Modified: Tue, 13 May 2025 19:40:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:35046b176128f19922d7de4210f53323a488c58c8c275d4e2114ea070223c87d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4886819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc074cb426b824c17107700f945a7254aa7df221ad51bddd7dea04de017ec9e`

```dockerfile
```

-	Layers:
	-	`sha256:a3c2127c6feee4dcc3605e2924878b799448fdf70b02584941b4ba58e716d2bc`  
		Last Modified: Tue, 13 May 2025 19:40:12 GMT  
		Size: 4.9 MB (4870901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54a08cbf0c83f25fb736144b1448ff75f2c5d301627865ce104f1844c9393578`  
		Last Modified: Tue, 13 May 2025 19:40:11 GMT  
		Size: 15.9 KB (15918 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:3dfe51ae083e0336fd36c94fd413f016f32adf5502bfb1391cb83acd5bbc0833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180428180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c548f5cc94fadb69688ddd4ab1347da4e75646bbf94ff8b0bb3e34ef730e68`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16eb1357dae40bbbfec5d640d12ef1b62cf430e53f7b5386db46858bc35b45d`  
		Last Modified: Thu, 22 May 2025 04:06:42 GMT  
		Size: 85.2 MB (85216728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08791ea1e05238f71e68d7d522086dd9061c9af6f1845f26b5d277030404402`  
		Last Modified: Thu, 22 May 2025 04:10:50 GMT  
		Size: 68.3 MB (68327604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfaedb941dfd7842b5ebdd83a21e1e259f611bcbb109000a403b84a1c7e9161`  
		Last Modified: Thu, 22 May 2025 04:10:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6f33663e222bd93874f30699f82539cc0b426c858f92eec66cecf31a635d8c`  
		Last Modified: Thu, 22 May 2025 04:10:48 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fc99a99a536868e23886e8fca976f6f749944dcfd78c0968b6eab184a2c224ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4924777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8703f76e6196d314578e13db1b3c7295f7178b73b11786f577d9cecda36aeba3`

```dockerfile
```

-	Layers:
	-	`sha256:775d35b8bf579bd2fb7c5efd9ca0918fad8073a9f78ec3abca42e174b5bbf399`  
		Last Modified: Thu, 22 May 2025 04:10:48 GMT  
		Size: 4.9 MB (4908905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cdc23f1224e8a7e53fc532ea63e583aaf9b457a104f21203d739041bee03e0c`  
		Last Modified: Thu, 22 May 2025 04:10:48 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json
