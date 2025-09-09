## `clojure:temurin-24-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:68f78fffb5bce53f3e6dcdbe77de33b529bb8d7e67aa832c12b554b4a3665ce3
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
$ docker pull clojure@sha256:d5e8a9da7b42a99ba33792887f5494d1da22ba1183b246936770cbe2d2c4ddc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191732276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9f9b895fcbb67adabf1ec366eb0198c344f3d657e0a13a79161c90a6440b61`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddc3fce4317ae0ae2f3fa0aeb0c5a46ac5a267d694ffccdc1f0491557059cfc`  
		Last Modified: Tue, 09 Sep 2025 06:41:35 GMT  
		Size: 90.0 MB (89975251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f468e95c04dd8bd8c6a8ea928a9280a48bbc86c859a67763f3ce434ab27a85c`  
		Last Modified: Tue, 09 Sep 2025 06:41:35 GMT  
		Size: 72.0 MB (71982487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4036646ea629c2b91c537aa51e931458ef633dcc33164c472fe0e2477d3b6a7b`  
		Last Modified: Mon, 08 Sep 2025 22:34:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2a5c9ad0a6762426375ea439231c82020cc053748ed0c16c57cfbdc267c91b`  
		Last Modified: Mon, 08 Sep 2025 22:34:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e5c93a5be6a458f5fc344c3127908864f2a60842b323176273c95b89866e020b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2565dc33d6b3cfb547b4bd8d44fb0d47fb552fb4142db7db8056f220e5133560`

```dockerfile
```

-	Layers:
	-	`sha256:0ac81c2f88d6a3638ee271392ae6be8f2942e46855a622c15b7f230388855575`  
		Last Modified: Tue, 09 Sep 2025 00:45:01 GMT  
		Size: 5.2 MB (5206761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:919d53052f8374e4d39ed22469d43babcc0d6695e364168bce1d4b27cc4880c7`  
		Last Modified: Tue, 09 Sep 2025 00:45:02 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:31bb864b270b7008520ac56082cee5bf0cb89ef7c29b1ee7bd76aca6602f0a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191034120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f881302e245817906e2ac234cd70b3579633bb74180f776936276d0ccbe1285`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb788c3491ed80aa1227ed8a0dbc4e422ef4c45ebebe967dda058233aa426c1`  
		Last Modified: Tue, 09 Sep 2025 06:41:33 GMT  
		Size: 89.1 MB (89092520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a529368882a68233629a3233adf3bc63da71484feeba54d70350a9d3975de075`  
		Last Modified: Tue, 09 Sep 2025 06:41:32 GMT  
		Size: 71.8 MB (71803931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5c2a5c7d298e0f27f4c2d6d87337716a195cbf9d12186c67fbc848be986b66`  
		Last Modified: Tue, 09 Sep 2025 01:23:25 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db432fb22a40becee58f7e2c357bf5b8dde7385ef02106e88772ec201a240095`  
		Last Modified: Tue, 09 Sep 2025 01:23:24 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0d836401a1ef392ae4949cc44fd6918228baba86a932d078bb918293b6eccc30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb21525e35d1e4697f8affa19455485dc2688eb377d87cee5df81c8b468274a`

```dockerfile
```

-	Layers:
	-	`sha256:7abe21562dc6d18fb223040657424fb38d0ef114d3d73f6f2a6bb81bc769966d`  
		Last Modified: Tue, 09 Sep 2025 03:43:04 GMT  
		Size: 5.2 MB (5212527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2feec1deb1a99f4dc60b28dc2c21a15c22774a93ec2d70a6f932987fb8aef1e3`  
		Last Modified: Tue, 09 Sep 2025 03:43:05 GMT  
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
$ docker pull clojure@sha256:13a1aa8e0f063d289449523e2895a2bcaa93a7c46c39dedf8fb2cd78e7baef76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.8 MB (186818499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe1199def6547b8f443bba52fd862d96f443b3636ee67da8b85b86d04fbb766`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
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
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5802301b5e43e1938fc4d3c6e84951cc5aa9881aa25362f5d2cc7bb7be4c9e`  
		Last Modified: Fri, 05 Sep 2025 19:32:11 GMT  
		Size: 87.7 MB (87670403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758b3acdbcf28884108fd74d2ade6dae9f9cc4eb5e96da4ab7ca316ecf2b8146`  
		Last Modified: Fri, 05 Sep 2025 19:52:52 GMT  
		Size: 70.9 MB (70875432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b242f2bb511a6d2d0f0f3974895310d98e8f3632ff7f540c1b4fe7bd6155f3d`  
		Last Modified: Fri, 05 Sep 2025 19:52:47 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a3663b8fe534d4716bddd8d3d17bab2f0186f4809769e2363e61dc2d31b48c`  
		Last Modified: Fri, 05 Sep 2025 19:52:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c1e505559edad5daf8ed18ad5ef2c04e5c69e3a5682b3a7c87867158ebe8d3c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160999a1bfaaecf9d00da94e70bee1a35e170c502d333965eb205a2d3eaac94b`

```dockerfile
```

-	Layers:
	-	`sha256:fc3937aa265e64ddf84a533f26827f9dfa5fe590913276d4930c4df5388c80f0`  
		Last Modified: Fri, 05 Sep 2025 21:38:20 GMT  
		Size: 5.2 MB (5195346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d190b4d0c9509a6ebbca52b77e1ba69f06e286ba531a54a4f9c3b3044c94d23d`  
		Last Modified: Fri, 05 Sep 2025 21:38:21 GMT  
		Size: 15.9 KB (15896 bytes)  
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
