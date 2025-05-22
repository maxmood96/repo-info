## `clojure:temurin-24-tools-deps-1.12.0.1530-bookworm-slim`

```console
$ docker pull clojure@sha256:21589abf942bd635009033359bfbde5c0df9675ce772c12248570e023041ef6d
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

### `clojure:temurin-24-tools-deps-1.12.0.1530-bookworm-slim` - linux; amd64

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

### `clojure:temurin-24-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-24-tools-deps-1.12.0.1530-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:eaec22846005e8dc82590eef471dd56172eb8677812405244086674c74858c49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.5 MB (186536676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ef85dd1ac6d9a39fc2ec4b381545b2c1b27bf0007e8162f1765b02a68ff184`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd34a4187aab23db272b0b1a8f05c1c712bfae4b9fc1c192607343790479bfd`  
		Last Modified: Wed, 30 Apr 2025 01:50:23 GMT  
		Size: 89.1 MB (89091270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6d96fd8979346f0f9cc60166257e33f62ab25c8955b5449c1d043e6ec779ff`  
		Last Modified: Wed, 30 Apr 2025 01:50:24 GMT  
		Size: 69.4 MB (69377743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bb2b644b28b4a060f04b00637881be61793c2835ffe2aca3d32c53017f3fb9`  
		Last Modified: Wed, 30 Apr 2025 01:50:20 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3dee57edae75636480827485ecb40526f6fbcb1413d963fe7b91d655be8916`  
		Last Modified: Wed, 30 Apr 2025 01:50:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c25bfe79065b748ce5bff38380c959a5ce3ca4b23aeaedc0764b75d60c493991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4886359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a244957d989c314d26cfe4d16e8a81aa5b3fa3d479b4334108ba04ebf10c0665`

```dockerfile
```

-	Layers:
	-	`sha256:13a79ed77796f13585374dde8e8f1b7f05f03590eb7f10697c513b3dfffee084`  
		Last Modified: Tue, 06 May 2025 00:49:31 GMT  
		Size: 4.9 MB (4870369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4380bcee6b9ef76ebcee87f75158de159eed52e2d4f686c424c15a74da5f585a`  
		Last Modified: Tue, 06 May 2025 00:49:31 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.0.1530-bookworm-slim` - linux; ppc64le

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

### `clojure:temurin-24-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-24-tools-deps-1.12.0.1530-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:bc4d52741c486f14d9fbac058f10bc15bf957a0fdb3b75d2e654904ccae2b322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180435364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe7704b9cac9d1214b7894bce786d28b2fa90757ea1f1c83e563bd2e5892c43`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
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
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231b40215e1dee03d245ee29850896a91e172c888befa78a1361cb7ac1719735`  
		Last Modified: Tue, 13 May 2025 18:35:45 GMT  
		Size: 85.2 MB (85216757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06feb30f18ffc0226f7b35ef7a72db12f5eaeb452e0d37ac9a7ecf740cbc0afa`  
		Last Modified: Tue, 13 May 2025 18:42:09 GMT  
		Size: 68.3 MB (68332703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5744dfa4e715db55eedc6aa93298258f6a26387d1da03a21a5919fbfd82e492`  
		Last Modified: Tue, 13 May 2025 18:42:08 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b20187da9da40f910f599b7871e7785a173b3ffe2045f40e03155df91d180a`  
		Last Modified: Tue, 13 May 2025 18:42:08 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8f60550153b05ca5ce3091e2b432851f297c5f646fb6c1250a7a94225a172029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4877244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f70a09d321b810a1487844cff50da251caa649217e77695d2966867b9074705`

```dockerfile
```

-	Layers:
	-	`sha256:d90847470b941d11d3b8892727f032808ca67caead0ba6ad037c8d96fe3efc7d`  
		Last Modified: Tue, 13 May 2025 18:42:08 GMT  
		Size: 4.9 MB (4861372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7e4bc4d98270396f2220902ffc5882fde6bd849f4c7b8273afa5581666e780b`  
		Last Modified: Tue, 13 May 2025 18:42:08 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json
