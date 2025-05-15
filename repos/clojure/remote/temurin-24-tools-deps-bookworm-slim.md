## `clojure:temurin-24-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:2135e5351f86cc346f250c387a122fbb7ff77dcbd80116c53a08af1896977464
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

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:666370c432e65955ae3bb884a3ffe1765e0e03ea2513b0971d6817eda4cf9afd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187706426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8225c1f8a62bce030ee463ddcfdaaa81eb594fd5ad6deaf2f689521489855ca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b79b1600a276667a6ea3951ffba0e9d2d35aaa6f17a4063126017eb105c3d7`  
		Last Modified: Fri, 09 May 2025 13:06:01 GMT  
		Size: 90.0 MB (89952019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd4ff0f95916def0f58025e549edcec6880a4bc2f7a7142394cd881a7496331`  
		Last Modified: Fri, 09 May 2025 13:06:05 GMT  
		Size: 69.5 MB (69525726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdd9b44e3656b86bc3023173c71c1c261a1ae9afb2710d5fb85f36d2195f3b2`  
		Last Modified: Fri, 09 May 2025 13:05:53 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b18894c48d96379479793126b70812275f7668b33361d179e0e6b0fb0f77a9`  
		Last Modified: Fri, 09 May 2025 13:05:54 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:533ad9571d4929f2fbb4fba55eb48a740c54d265e3adeacbdb9d00cd21d2917e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4880482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488326362cb1d89aedfcf1b92054f73474fcc498bef5bf8289198364c37867f4`

```dockerfile
```

-	Layers:
	-	`sha256:a512f0290190a6d0130a393dc9104f2ee946d9b79bec2354c8f4752e312eef9a`  
		Last Modified: Mon, 05 May 2025 17:07:59 GMT  
		Size: 4.9 MB (4864611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb7287fc6a96c4d346a56318fcfe7a816705bc599fa602d60ff37df8be657a97`  
		Last Modified: Mon, 05 May 2025 17:07:59 GMT  
		Size: 15.9 KB (15871 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; arm64 variant v8

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
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd34a4187aab23db272b0b1a8f05c1c712bfae4b9fc1c192607343790479bfd`  
		Last Modified: Wed, 30 Apr 2025 01:50:23 GMT  
		Size: 89.1 MB (89091270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; ppc64le

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
		Last Modified: Thu, 08 May 2025 17:09:00 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be9dc822e6eae36756c1b8884d36306ddbe0196781d2d67dee4df325851278d`  
		Last Modified: Tue, 13 May 2025 19:32:20 GMT  
		Size: 89.9 MB (89920243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; s390x

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
		Last Modified: Thu, 08 May 2025 17:09:11 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231b40215e1dee03d245ee29850896a91e172c888befa78a1361cb7ac1719735`  
		Last Modified: Tue, 13 May 2025 18:35:45 GMT  
		Size: 85.2 MB (85216757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

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
