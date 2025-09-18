## `clojure:temurin-24-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:11a2e0e9a8326b84136b91a183928925340f879b476cbc4d52bfc962193dedc1
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

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4a815ef12c9d2e520ba6820f5e9c08152e39ced84934a24fb79b3c7a37c626c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191732361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0b3453862f8acb5c94c47482dd0c47449e439a647ece6943e6313b873a2993f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9506d21ad20a64257e2c83aaaad2c9898609f35e99dad104013ab9b3cae0cd3e`  
		Last Modified: Mon, 15 Sep 2025 23:29:05 GMT  
		Size: 90.0 MB (89975196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b233c9e12d5c6b8be4e10e738ff9d43fe0e00b23ed1dc5f6d47c158f1d62cc79`  
		Last Modified: Mon, 15 Sep 2025 23:29:18 GMT  
		Size: 72.0 MB (71982630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b901380cc7d1c481c952bc699258ca03dcbb252eea605850ecbd1d0e33ef7d0`  
		Last Modified: Mon, 15 Sep 2025 23:28:59 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dcc8c01b41080f03c1dc525128e2bd2bd690af26ff59552d1da05b46a6fc38a`  
		Last Modified: Mon, 15 Sep 2025 23:28:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4f58a20e886e3d96d94ef24f789e9815660fde1b1d7d07c886269d93188eac44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa38def9f9730d9aaa2eb0ff1471892712278498d9000df6f2fd8c2f370fda8`

```dockerfile
```

-	Layers:
	-	`sha256:00558e58b78bbc6986309be440c108af168690d62cd22643f7730855aff7c37e`  
		Last Modified: Tue, 16 Sep 2025 00:46:59 GMT  
		Size: 5.2 MB (5206761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0325a61dcca206c586ebdcf8cb06b174cdef22c7aaf7b62832c89d4a5661d732`  
		Last Modified: Tue, 16 Sep 2025 00:47:01 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e8c0174c46cdb274162c10c0ae3854f3290f55bdfa500fa5dd09fe4bc1bdbaec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191034242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76e1783338afce9e38df1de31a450e91811bf98112f193148f566394ae1a7f31`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a97021d04da68f2aa1808735396a06d197b89cf8b6b3ace378cc1ee67040bc7`  
		Last Modified: Mon, 15 Sep 2025 23:29:43 GMT  
		Size: 89.1 MB (89092539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a33d0cd74e379629e7fe4f35b9d89653f79b0d6f241d862546d8e961499dc4`  
		Last Modified: Mon, 15 Sep 2025 23:29:40 GMT  
		Size: 71.8 MB (71804029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9eabaf5a0ce3e3684b31c7501e40895ba1b677cb8f952aeb93e1e10bacf3580`  
		Last Modified: Mon, 15 Sep 2025 23:29:35 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00680193fc40a92b2c29b682a721ed7fea9b25154a3e6e8c670984502d6ed612`  
		Last Modified: Mon, 15 Sep 2025 23:29:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:198efd45ee7236df418d3b7a51e311a6a58ba59875d48488addf95191c91256a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2606b19d95e9cdc3ad5dc32e05342afceaca11432b56eabdce7ded442619ec6d`

```dockerfile
```

-	Layers:
	-	`sha256:46dc4fb55827f20493b056f024f0b78ec5c0f7b403b2b6a53e310b034e4d92fb`  
		Last Modified: Tue, 16 Sep 2025 00:47:06 GMT  
		Size: 5.2 MB (5212527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a724fc6b651a59d86eb845ec2550b6a33e2272bc5e65ef9f0caa64c1a163f209`  
		Last Modified: Tue, 16 Sep 2025 00:47:07 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2f081eaeadf5f3f0d2968c4ce7599d62c0d48f31405d8fa789d7cfe2c9158bb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.9 MB (200911775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91ee8e478c1687de7fb4e6d1d06d25538d50fc49457f783524d2c874db5f3e2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab6532f47259b4baefc4644a9d2f6e61e29f5697fdc7617b9491b02a2197399`  
		Last Modified: Sat, 13 Sep 2025 03:55:52 GMT  
		Size: 89.9 MB (89918195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ae782fa739b74fc9e0ec44c569b6bc35be2f28efea9ff82259a523c5ddf868`  
		Last Modified: Tue, 16 Sep 2025 01:37:56 GMT  
		Size: 77.4 MB (77398187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebf3a986c5eeaee76854433bd23bedaf21b3d04dbf99b492eed01a9cef12d37`  
		Last Modified: Tue, 16 Sep 2025 01:37:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6264c83cf3be5da9dbbc5bc027db63cb79c6fa5c1c1ddbccdfe8bc16bcda06b`  
		Last Modified: Tue, 16 Sep 2025 01:37:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b33d2babbb1713c78b9a9b78bcce738a97de3b065dca1a32581c05f8aee4bb9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0b6e9903bffaef1616748d2b4a476d7392e32fd0fa71be3a54873c4845c4be`

```dockerfile
```

-	Layers:
	-	`sha256:577057d07a35188abe22432d6d672bace8cfe769013f87e40ab0bb71f7d688a0`  
		Last Modified: Tue, 16 Sep 2025 03:44:05 GMT  
		Size: 5.2 MB (5212430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa95c49dafeb4186d90514ec40631efa55d70f9e2f6fa10d20145956b73d182b`  
		Last Modified: Tue, 16 Sep 2025 03:44:06 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:379aac212559f6979c327f4ff74c32639973b72ab773cf6e0f070f0c61c2c70c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.8 MB (186822188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347383b7e448d86a3e8d4b6cf908b70811c57f99a71d0e40a9e8fd83633d9b14`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bc3fbdc5bd092ca0af738f65f8ae8ce176945ba88b669c5e80fb9adb3f5eaa`  
		Last Modified: Sun, 14 Sep 2025 00:38:37 GMT  
		Size: 87.7 MB (87670426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f306023afdd4b220c4d8bb52121ecf0e954b280e72f3029805a46753ce81a0c9`  
		Last Modified: Sun, 14 Sep 2025 00:38:33 GMT  
		Size: 70.9 MB (70879348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d6a7e3a7a9d6b0739613cc3645212ee48cada7a5eb61850907b3fb83b845c8`  
		Last Modified: Sun, 14 Sep 2025 00:38:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8044294e53545067b46832278c613fcdf8b9f6fb53c6579ab35e48e700592d`  
		Last Modified: Sun, 14 Sep 2025 00:38:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a73d6761043f54a639532b354557ec4e9ef122a2d1611ff73fb5e4008287a77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0c43cfdc889d95331f13473d49f9e4fc24b1700baccdefc7e1e019721bac754`

```dockerfile
```

-	Layers:
	-	`sha256:0a88c39581c054ee8ba0757eaa171aa6a54ff032ae33e086cd8cdf29becc5749`  
		Last Modified: Wed, 17 Sep 2025 21:39:09 GMT  
		Size: 5.2 MB (5196222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d88de7ee765a81a04d51ed07e7efa440273215676a25e9758a7c39c62ad15ae2`  
		Last Modified: Wed, 17 Sep 2025 21:39:09 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:e4c0c59c98b4fccddce020763699b6e1133f7e043dc9cc55dc7a14e283f21818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188011793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3538ab80781bc610c5d775afc63aad64dd9d8b0082c9fad31ea9bdc37b41b1bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001f899a0035f92502563c4bdaed319ad7f7d929742ec096c4bb55d3733e094a`  
		Last Modified: Sat, 13 Sep 2025 03:21:52 GMT  
		Size: 85.2 MB (85226409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e15013444af8fb401203ba55126220e53b15330d14a311cb2541850acc5d502`  
		Last Modified: Tue, 16 Sep 2025 01:06:56 GMT  
		Size: 73.0 MB (72951434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eacc2651dcc7cb87d0bf60106063216dbc6fb36d6d70d45d7625ae70a22a2cb`  
		Last Modified: Tue, 16 Sep 2025 01:06:50 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19d61bc46664c7c320c7b617bfc6a140cd351b152ffa171d60a5a6561e3a259`  
		Last Modified: Tue, 16 Sep 2025 01:06:50 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1c4818fd82bd7307b057cb7c66ca1ea53666cd73f70aecd109f6ccbc60fdcbec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:568a599e1b4ff5c59bec0e78e0618d03f417a28fbdb9d344877c37a050c80ef5`

```dockerfile
```

-	Layers:
	-	`sha256:922b21b4546075be623897bc085492d33bd3544da101576e3ff264feb98bae83`  
		Last Modified: Tue, 16 Sep 2025 03:44:14 GMT  
		Size: 5.2 MB (5205233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e0449e333fb25fd16110ab92c02d71a14b6c417004b1985b7325627da44a39b`  
		Last Modified: Tue, 16 Sep 2025 03:44:15 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json
