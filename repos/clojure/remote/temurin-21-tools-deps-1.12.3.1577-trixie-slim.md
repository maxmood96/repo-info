## `clojure:temurin-21-tools-deps-1.12.3.1577-trixie-slim`

```console
$ docker pull clojure@sha256:6859e8dd9bca1dbee4ef5d6cc451d4d6a3017cd8e59b100f1565a8f54de923a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:93df7bca4496dd6a58cf6aa1b8fb9f08e39984a891da9995d75d513679caea86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259578782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628aae683d35bf36b75c87c22c8a3d4340e3cce2a792a6bd922e45d73162b5da`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499630323d50d1bac3ac3747459b6af3cd93ee93ca1c87b31e66bc05bca1b16d`  
		Last Modified: Wed, 01 Oct 2025 20:36:08 GMT  
		Size: 157.8 MB (157804740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155b368562870b7f6f738d96366c7d5201e4584c468ffc191bb7ca129bbfb96f`  
		Last Modified: Wed, 01 Oct 2025 20:36:27 GMT  
		Size: 72.0 MB (71995238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfbf193bd484960a30a9561ed46ecee86a16c3d2e9ab6fada8a7af4228e5b9e`  
		Last Modified: Tue, 30 Sep 2025 01:39:27 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdf152c91795f5d24065b632e1a197478a27e424be4fca0edc4705753b247de`  
		Last Modified: Tue, 30 Sep 2025 01:39:27 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9be9e61080025f13e27ac78a55511a70790ad0e77bc3356be1bf7c9be2f9cea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c38dc7740f04156b809250a434c17b287fef853747c0da879513179c348301`

```dockerfile
```

-	Layers:
	-	`sha256:e3c56ed042b1adfb94c32ef9038b95a7375354ef4b3c317eb2f81d9d1b68f34a`  
		Last Modified: Wed, 01 Oct 2025 15:41:26 GMT  
		Size: 5.3 MB (5259215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fca2bc9e114710a8665f491d80dd2e8100699509c1829758d6cf5d5ec6c2bb98`  
		Last Modified: Wed, 01 Oct 2025 15:41:26 GMT  
		Size: 15.9 KB (15854 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2b47de7c3904b6706d04b412b7dc5088b455088762e4c38f8aac969a283e3a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (258031431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9141194434b19aa55a2737680492b9e96d514602a6671109d2b9aad0d91a5f6b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4097316d2b20d74b515cf308d345f3a218513b8f7ae99332bacc7bcf79411266`  
		Last Modified: Wed, 01 Oct 2025 20:35:54 GMT  
		Size: 156.1 MB (156081234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03ce0833d6dd3f9f14c91ff9437c7d9507a7f02c9883561183642edb5a108d2`  
		Last Modified: Tue, 30 Sep 2025 00:55:14 GMT  
		Size: 71.8 MB (71808317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0209dd1c3dd373c1dd4bf1064e58be726cc79e6a8a5d6bc7c9f6cfeb8c17e425`  
		Last Modified: Tue, 30 Sep 2025 00:55:08 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439c4aee20030274d9f8e762384c9f2e4e1ce6b0d25ca18e46e9e13cfc234570`  
		Last Modified: Tue, 30 Sep 2025 00:55:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d081bbdb472de7c5b7b3c9931cef686a7d88bcbba7be53cedf46899d0240b483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fef3f30473b448dcce50a1296316196771f25dbcd0e86af4f2fe3ec4d374b0`

```dockerfile
```

-	Layers:
	-	`sha256:d8937b7ea0c3d169f88469f82b6df3dd41f4144543285e4d8bc1632ae141507d`  
		Last Modified: Wed, 01 Oct 2025 12:36:31 GMT  
		Size: 5.3 MB (5264984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02cf53f38b7ed61776e09c67188f16f64a77398b78d914a9c71580fee5407791`  
		Last Modified: Wed, 01 Oct 2025 12:36:31 GMT  
		Size: 16.0 KB (15971 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:4e9c29f92e03b7881cbac6c3c6fa17cef3bbdfc26714473e008c8a0fe545536f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268958451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31ec01605866e7b85aba5b52f72fbbcd81fdc4bddfe34c6f36fa2a1e38d266c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc4fb41763301e571f07a0dcf2b6d1915a0e19e93bdda3c4748b680eec6eb1d`  
		Last Modified: Tue, 30 Sep 2025 13:59:20 GMT  
		Size: 158.0 MB (157963421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dadbf765ead5fd6d0c05ff33a77c7347d0a6c685e3f7d38bdf0d312156037df7`  
		Last Modified: Tue, 30 Sep 2025 14:03:03 GMT  
		Size: 77.4 MB (77395539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852e08688f34a5775ca394aeecee7529a2971fd1350a178745a3a685f3d66de7`  
		Last Modified: Tue, 30 Sep 2025 14:51:55 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2a6333d3461a44051b0f9d81c85d02a26d531c74452c7135d52931dd92bb31`  
		Last Modified: Tue, 30 Sep 2025 14:51:54 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f21786fa01ff2d454d332948e1a92eb12e19453edf14500ec9effa57a201edc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadeab6aefb319dce253986ba8f35838f60d50e206b1a71c587bffddbe019cf8`

```dockerfile
```

-	Layers:
	-	`sha256:4ee66e2afc96e0500a1233875fe06fc7d2ddbb5db1fb59e3a0ba9ce97ff034cd`  
		Last Modified: Wed, 01 Oct 2025 21:43:57 GMT  
		Size: 5.3 MB (5263586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7954750b3b262d017d0502686e89808b02d334c400bed16df8b3dfa8250a9e0c`  
		Last Modified: Wed, 01 Oct 2025 21:43:58 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:8f0638980a34346987ccc3e6c0e9bc28457cde0666f8511b95427fd935455a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252746926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7010361391da66739ba133336048d7531923a371f18396f81045a8a610a1a8d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25be0a32c196b5e86daa223045b0e32e55940405ffb33be6fe5f6bd48aeeeee`  
		Last Modified: Sun, 14 Sep 2025 19:26:07 GMT  
		Size: 153.6 MB (153593492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad65798ac3af68bb3d796da257a0138854ff669ee25377b5c0c648e9bbef733`  
		Last Modified: Sat, 27 Sep 2025 00:47:33 GMT  
		Size: 70.9 MB (70881018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dadd4cea2a07fe4570727784cb847ea0f0a240bf0462cd20c2d11eae1490fb2a`  
		Last Modified: Sat, 27 Sep 2025 00:47:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7d9cf1957104da57f9801eefa7be4852302482f90cd81afbdfb2432c4de08e`  
		Last Modified: Sat, 27 Sep 2025 00:47:26 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:803bbce4b2ad2abcf02e3dbf846df2d44ce596183694890ff5f8153dbec97b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aae94893d2a1785c3cf25f358558d14df2123aa906839d01168fec7da164042`

```dockerfile
```

-	Layers:
	-	`sha256:9c0244d422b3ecbb16c67ab330781b0db89388dbf320e2c40fe5a73007a80e60`  
		Last Modified: Sat, 27 Sep 2025 03:36:50 GMT  
		Size: 5.2 MB (5248679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b6f2325cf600513400ff9d10485f9e3bb7fb94e5a95ecfc1267b97f3cfe466a`  
		Last Modified: Sat, 27 Sep 2025 03:36:51 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:62f435bfb6b64ce7a3329024fd94a5cf736bfb7c6cc6fef59257a6a14326833a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249819022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e60a4851d3ab0a140570ec3bff127ab779c4f32aa5a83aec995c1202a281a8ae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76d12272035243cb7ffcfbda01293302d94f352e9830f35e1648e940b8498d8`  
		Last Modified: Tue, 30 Sep 2025 13:32:29 GMT  
		Size: 147.0 MB (147027031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d14956eb94e89ffc60e47389730de01c8c496677f4465391a9419fa74617ebd`  
		Last Modified: Tue, 30 Sep 2025 13:38:14 GMT  
		Size: 73.0 MB (72953721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb4e0f68390373b9c47204874b6b493929a2f79790ad6a70b94b9836571b203`  
		Last Modified: Tue, 30 Sep 2025 13:38:10 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feaac6d2f6b4a1c110746baec23d7d4f61e99610b007bffc4caa94df6d0affaf`  
		Last Modified: Tue, 30 Sep 2025 13:38:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8e6b8c07ce2aa2128ec265cae8ae0b19f3ffa5f90b3da23b4b50b722585cfa67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1364e1745eb20baa116b590011edb50dca846cfd909ca335b41f2ded7ba9f09`

```dockerfile
```

-	Layers:
	-	`sha256:7fac1318949ecdd121a849c135f5aa65baa978d46adfab4d54cd68830ebc9394`  
		Last Modified: Wed, 01 Oct 2025 21:44:05 GMT  
		Size: 5.3 MB (5255139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb580b6b1312b910f0683b03406994f6923984d1d8bcc660f001b302d74704f9`  
		Last Modified: Wed, 01 Oct 2025 21:44:06 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json
