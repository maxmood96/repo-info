## `clojure:temurin-24-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:84e08ade9559715376170311a755a5880c7964f509757cd536f44ccbe5029794
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
$ docker pull clojure@sha256:0e5e7455990bed2ad2e427d6594b74b64e4b95cb8cfd08927f35aab4c3d19baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187874500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087ff08c9b878708c2efcfa376c44c2f424353d2ebf6b4c2673817f55cb66a42`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58ddd4f0c53d59b3c9a751d5af087f84e97d403e9c08938fcad6181571c071e`  
		Last Modified: Mon, 08 Sep 2025 21:44:08 GMT  
		Size: 90.0 MB (89975189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915ce5521027c90dd10fd2d5712896107bb70967a69fedc176100fe664e7a103`  
		Last Modified: Mon, 08 Sep 2025 21:44:07 GMT  
		Size: 69.7 MB (69669924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d67dee7dfb9c2f6f907b8a496c3ad367c7909e501e69a44e69cac468036164e`  
		Last Modified: Tue, 09 Sep 2025 01:58:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1c049e09cc7f51ace4c6829bd1f79247c8493395b705321c95159bfced215a`  
		Last Modified: Tue, 09 Sep 2025 01:57:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7484efb75030322e729650e186e06e7c1b891761371620a6438e213135478644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5079907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3148741bf4748ce4a1780eeb0d86d85c0fb3bc886f0787de47a2a47e81b62ba0`

```dockerfile
```

-	Layers:
	-	`sha256:31dd643a131ca3cf019c9fcc23e54a8d748910d3777039cbce636bb159b8c064`  
		Last Modified: Tue, 09 Sep 2025 00:43:24 GMT  
		Size: 5.1 MB (5064036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e952f8371391e029ee6eb0c98d31a02738c2a6e26cec3d80b3d634873d885f4`  
		Last Modified: Tue, 09 Sep 2025 00:43:25 GMT  
		Size: 15.9 KB (15871 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0a3549021f56fa8d3e7d578fed2c91b8a3714337e9ccaf99cacecb8b77b92ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186724919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ddc8f40896bb6678af36d46d854a811ef64c2a694ac21792a4f94ab205c4cd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1156444753fb5a24e0d4723ab00711efe363bc848f2b49af418e6092fa3f8940`  
		Last Modified: Tue, 02 Sep 2025 08:23:01 GMT  
		Size: 89.1 MB (89092520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd973521ae0021251b953175d7ed2a0fdbc09f059b0bf874e4e10e3ed8bc5bac`  
		Last Modified: Tue, 02 Sep 2025 20:38:40 GMT  
		Size: 69.5 MB (69549356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b2b27b23b37860790d71830d763b1344111e53d9317009a9652d157e40c62b`  
		Last Modified: Tue, 02 Sep 2025 09:19:01 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b378d9147347db0c1a0865dcf31b65882f7ae5007ad2cc4fb8ee15ac9f2f161`  
		Last Modified: Tue, 02 Sep 2025 09:19:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6f2625da0946c1fd77f0094964e44124b22921b35e655798e15b1384a0a15289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e232d9db19b0bb4304c6d34a8f44db368a9561b87000b723784aad3e01c94c0e`

```dockerfile
```

-	Layers:
	-	`sha256:ab4d78885a2cb165ea036499db1269a334d9b086ab5b67c6aabe3cf553eb09be`  
		Last Modified: Tue, 02 Sep 2025 09:42:31 GMT  
		Size: 5.1 MB (5067679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de6ad7ca71e6fa2b4a98842a43ee746e0cad99365248ed694856b09bd36e26b5`  
		Last Modified: Tue, 02 Sep 2025 09:42:32 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d3cc801150f4f303086f921ac9f2ff07ac343242b00f348544757c69c67686f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.5 MB (197496771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10cb51f256ca13d0f10468d9eb13ec654e419a61a8452aa32cc4126171f61f7d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
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
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb6c96e586f4fcad4d46470c1837a4a905666269fd92b7eac0f40b16274c934`  
		Last Modified: Tue, 02 Sep 2025 18:38:16 GMT  
		Size: 89.9 MB (89918172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9856ca760a75af524f63b549ad687b2fad92dbacb3f4183594b24d238f4ee08`  
		Last Modified: Tue, 02 Sep 2025 09:23:16 GMT  
		Size: 75.5 MB (75504135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87d38a1d667ca2d69e20154ea01fd924b345994448817175f2587f065dbc922`  
		Last Modified: Tue, 02 Sep 2025 09:23:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa38c0b5a71d2718b2f54fb42accded0b0a325f61faccb49b085e4f27d1020cd`  
		Last Modified: Tue, 02 Sep 2025 09:23:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:08f48d7f162efc9489fa76e742bce2b6f2ac09a38f53397bde88d6009e35b50a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5084297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:473237395570c1a4bcc9fb9138064a30c23cfd3d890f6a02ae89f37e9b135896`

```dockerfile
```

-	Layers:
	-	`sha256:8b87a3fcf3a70b93194806f8f43307e10fde31146bb96bcfd95799c4e0e24d3b`  
		Last Modified: Tue, 02 Sep 2025 12:36:50 GMT  
		Size: 5.1 MB (5068377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b25094842daa10b0e1d6598e29e74686a32672c2d5dd452a3bc870886609b4c`  
		Last Modified: Tue, 02 Sep 2025 12:36:51 GMT  
		Size: 15.9 KB (15920 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:8a5ae5f9b7de45a25e44add05975436d8069fdc9d1d0e9e5954f3f8e15203b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180599560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e227ff1fcf24ed0d36e642513ea71b2a1426443bfa94f835a95cdef83657d0af`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c90ed0d6d56789641548c64b4a5818c4522e9490cd8bb164dce084d4e85b68`  
		Last Modified: Tue, 02 Sep 2025 02:22:19 GMT  
		Size: 85.2 MB (85226322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97641382c5cc646516da46a5f5885283486feec52e1bf33ff46fb853be502794`  
		Last Modified: Tue, 02 Sep 2025 02:27:12 GMT  
		Size: 68.5 MB (68484358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41981f93187ba14d4dd2c9041cb35e25fafa185f9147ef496d3e6f588cc1f47f`  
		Last Modified: Tue, 02 Sep 2025 02:27:06 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c329479e4c3601c2d0fe48ab1f2e30bccc53219a879e01b880a7978513379435`  
		Last Modified: Tue, 02 Sep 2025 02:27:07 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8bc7d48dbc39feb8fb7199764d01526adf089b337bcc54608409e7a318e14596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5071661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634ae29bf527a1648aa59c9494d2321b3f9bc605e8953154f812af1b32924212`

```dockerfile
```

-	Layers:
	-	`sha256:c66f06b05c32a63484f630ad36376bb4c3811937cfe0a972e77cd445b94cd586`  
		Last Modified: Tue, 02 Sep 2025 03:43:21 GMT  
		Size: 5.1 MB (5055790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04080c3e211fc58168494de211d97d4c12168ae9c7af19003beb00a7d3a5a7a0`  
		Last Modified: Tue, 02 Sep 2025 03:43:22 GMT  
		Size: 15.9 KB (15871 bytes)  
		MIME: application/vnd.in-toto+json
