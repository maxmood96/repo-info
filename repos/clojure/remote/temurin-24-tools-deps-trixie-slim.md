## `clojure:temurin-24-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:7c38660132f5a6945d9cfd2c5dc77c7e67587e4c402440d568232ed26c421c9e
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
$ docker pull clojure@sha256:0eb42ca691dac72bdaa8130ad6b25e49512f10942ec07983c1a9320a99004b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.9 MB (200911440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d36377298fd52856e4656952928dd87ce57123adddb741d7f25ac71e16b7bdd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08aedb11a8fc6074544cef6e37e2e73961e18ce9b953c8e8dfe7d65275a4428`  
		Last Modified: Tue, 09 Sep 2025 13:01:14 GMT  
		Size: 89.9 MB (89918192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c05e9ac84b6a3e596de68c7e141974bbf6b7762c81d997aff59260b69801f6`  
		Last Modified: Tue, 09 Sep 2025 13:07:51 GMT  
		Size: 77.4 MB (77397857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7d779dddfdd9fdadfcefcc47e6b4ad8bc38c0247aa531f19293be20220a39c`  
		Last Modified: Tue, 09 Sep 2025 13:56:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9b853c764eceb40f05e076e27fd2d1cebf14692c36a5f3f860c5a6c76a4ead`  
		Last Modified: Tue, 09 Sep 2025 13:56:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dbc7d5f750bdb7f8b9a1d9f3b68df0689322f81435c951670faa64e7838ae22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edbceee0b33b0ae05f40a0a3aaa82a04346048ecdbdec7ed529659e66f97de05`

```dockerfile
```

-	Layers:
	-	`sha256:20de6910dc490a7d94451f6ef19dc4bc9cad6607d99a8e4a7b0a861fb4c4b072`  
		Last Modified: Tue, 09 Sep 2025 15:40:40 GMT  
		Size: 5.2 MB (5212430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db0ceff16170cd4e807a630d433813b1528197cbc7081c80a3433789f2b1d42e`  
		Last Modified: Tue, 09 Sep 2025 15:40:41 GMT  
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
$ docker pull clojure@sha256:fcee84adb976a192faf93e765a5d616a56cee7043605e2afc4d2e31e6cea8a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4659e23e76d2782a5b06e2beb53f19a33b172fdf86c5b5c18369421acc54722a`

```dockerfile
```

-	Layers:
	-	`sha256:c7ececf46a8667f316d63fd67a30aa30cd476badbd0a7c0264c339b2f945b382`  
		Last Modified: Sun, 14 Sep 2025 03:37:01 GMT  
		Size: 5.2 MB (5196222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a61dce91ef1f96a476d787c8925aedec19b356fcb9d32994a82ea3b4708d349`  
		Last Modified: Sun, 14 Sep 2025 03:37:02 GMT  
		Size: 15.9 KB (15895 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c94e3a1d78f71863b46138f699ec40347cba686ff9fd79dd0f692a1a5d290328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188011858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ced2aae97cff8949404753b2c4fdce75102132c27e8c07c08a9de6ad20f4ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d98907f88fea5077a809b80fcc1ad1fac8ee505740eaf9430e062e80a3fed6`  
		Last Modified: Tue, 09 Sep 2025 06:41:36 GMT  
		Size: 85.2 MB (85226409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af404afe2184bb0f4abb83e35cc386d572b347e97031cb24405204989bcb6a9d`  
		Last Modified: Tue, 09 Sep 2025 06:41:35 GMT  
		Size: 73.0 MB (72951511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c91a6d8a9c1412735c360d74b65c6c45538c58e998f50e23d87dcc1d7db291d`  
		Last Modified: Tue, 09 Sep 2025 06:41:23 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa578a0d3d2525e0ced50c4896abd42fbb384d73b9b70e4dff594234bee43bae`  
		Last Modified: Tue, 09 Sep 2025 06:41:24 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:82ea5dc72234bcaefd29e02522d27a3d96fff8404343f42fe9f8c192b006b23e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5220282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73cd7a86c92ac91790f68bca085cbe7bd5743312ce72f716623666bb0b0f120c`

```dockerfile
```

-	Layers:
	-	`sha256:be2c1a911f79559f7028c0be8d2785742eb4977d5e871036ec9bd7db84fb4ca3`  
		Last Modified: Tue, 09 Sep 2025 06:41:09 GMT  
		Size: 5.2 MB (5205233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da3c0bc6e92230d89e0382f82c5c29a8c40a45c65868ae22ac365958ad7ada8a`  
		Last Modified: Tue, 09 Sep 2025 06:41:10 GMT  
		Size: 15.0 KB (15049 bytes)  
		MIME: application/vnd.in-toto+json
