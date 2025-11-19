## `clojure:temurin-25-trixie-slim`

```console
$ docker pull clojure@sha256:b3deecd2bc1fe2b7230addce030b4a66b992e3fc9715a07c3353ac4ac807fba5
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

### `clojure:temurin-25-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bfb077842db883bda1a038860389986e6d0d5967173736a396f245e36a7fa9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193819175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c7abe4407433675e2d829ba77bf047cfe4747282ee059026091acc3097ab46`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:18:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:18:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:18:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:18:09 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:18:09 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:18:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:18:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:18:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:18:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:18:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd4a6ce053eafa26cb3a7795455a2b1ad1418e7f5002cc857be7d2191ce6037`  
		Last Modified: Tue, 18 Nov 2025 06:19:03 GMT  
		Size: 92.0 MB (92045314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899239ba86ef1528d3d1ba66f822985652bc0ccacf3ee12e1bffe0fa975315f7`  
		Last Modified: Tue, 18 Nov 2025 06:19:01 GMT  
		Size: 72.0 MB (71996335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364e97e86d514cd926bf5a036623fe0acbfbd0f70d97a0c806d15e4e9be81cf8`  
		Last Modified: Tue, 18 Nov 2025 06:18:53 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc6d6fe67da32b32dfa920eb0957eecb37b6998e7824a73ff038b125f06f1d4`  
		Last Modified: Tue, 18 Nov 2025 06:18:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aea7b8f3c8480694b06cd714fe8ca223728a495f832a0936fd8e019293a6a87a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90df3177a043f2dd2ee8cffdbdc14ea4a433b6c26bde289bbb135bc64017fdb9`

```dockerfile
```

-	Layers:
	-	`sha256:e32021e8ba0f8c61f426acf421cd948bb3b26f72bdf6a9f0380327852c9eca5c`  
		Last Modified: Tue, 18 Nov 2025 07:48:47 GMT  
		Size: 5.2 MB (5207549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:605dc0b3eae8cf17ad61c959d35fbe39283d5fc8f92eeb21c6cd81c9163bca29`  
		Last Modified: Tue, 18 Nov 2025 07:48:48 GMT  
		Size: 16.5 KB (16492 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b67b5095c17f521ff2ca0c3a857e0e32a98c371ee9eb2f3c24a73608f3721626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (193000640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a74b94b269d253e4b4da31786cf5b88a89d05046ac6805e2cb6435dfb999920`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:27:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:27:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:27:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:27:28 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:27:28 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:27:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:27:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:27:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:27:46 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:27:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c3b0e2b09e06b8ef6560026b3822a92debca74caca38669fdb9cf11ccc4f22`  
		Last Modified: Tue, 18 Nov 2025 06:28:22 GMT  
		Size: 91.1 MB (91052511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bf4b5c05dd49e7bbe670deeb5cbba4dcf3671d713249af22999bfb729849eb`  
		Last Modified: Tue, 18 Nov 2025 06:28:18 GMT  
		Size: 71.8 MB (71808481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8dbf24457d3c6c2c6c2974e565d14989e3b5da4740a92917eb36a2d6356d3c`  
		Last Modified: Tue, 18 Nov 2025 06:28:13 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2538d50119be2244095700a644205af6a3b39cbec10026b1c53a59fc370a6c0d`  
		Last Modified: Tue, 18 Nov 2025 06:28:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0135059bf3e0ac40eaa6bf09be90f383e70e28c0e0ca32e5e7d1102a9014de9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fa7bd16d4ce71d679f7f7f810a60e39c2ce8aeef1df66ae8bd7ae0d2105860`

```dockerfile
```

-	Layers:
	-	`sha256:80c8de749022c7371d70eaa9f661af01eedfa8eaec3a081dbb8839c1f31f77f2`  
		Last Modified: Tue, 18 Nov 2025 07:48:53 GMT  
		Size: 5.2 MB (5213339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e51ae6b08b31abe99ddf46840c2fb9c61fceecdce040f97af0246ea29e2dae5f`  
		Last Modified: Tue, 18 Nov 2025 07:48:54 GMT  
		Size: 16.6 KB (16634 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:85c508dc72d5453d2c2a51851ada408db6f2526bc129e5d73f1eacf6243bd7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.6 MB (202599207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab2b80be198957a7c6057a0a4bb0b05abae388c0942941ab5ed7eedaecf9602`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 01:22:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Nov 2025 01:22:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Nov 2025 01:22:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Nov 2025 01:22:34 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Wed, 19 Nov 2025 01:22:35 GMT
WORKDIR /tmp
# Wed, 19 Nov 2025 01:23:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Nov 2025 01:23:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Nov 2025 01:23:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Nov 2025 01:23:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Nov 2025 01:23:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c90f858597bca8ce932b97513ae303456c89b93821353bfc96936e47fded7b`  
		Last Modified: Wed, 19 Nov 2025 01:24:15 GMT  
		Size: 91.6 MB (91610745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8c056c6c9dffecf65d0ace659085df1deaba69e05e0a4287266dbf253567f8`  
		Last Modified: Wed, 19 Nov 2025 01:24:30 GMT  
		Size: 77.4 MB (77390563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72273db7ac7fa4d683451f9380c16ccfd982a76649a9b595024f33ebaf63e96`  
		Last Modified: Wed, 19 Nov 2025 01:24:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09581c4f9fdf0063d97ede314c1f5a8df628a1a669287ca528af2fb2636a8f70`  
		Last Modified: Wed, 19 Nov 2025 01:24:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:665626d6b459b5575da88d0d0eda00b1b662e6ae94224d0dc787609a2e792d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b191d5747fae395f42cece054e87d4bdb43e620920c0387a4112e747742cd5`

```dockerfile
```

-	Layers:
	-	`sha256:33e544d5700265e3db1ed14fd8e526df99f2dc6f31966e67d376338c96333cff`  
		Last Modified: Wed, 19 Nov 2025 04:37:23 GMT  
		Size: 5.2 MB (5213230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a5127d5f7e137563060f4b19dfc60aa9da525974839b42f41531348a241b48f`  
		Last Modified: Wed, 19 Nov 2025 04:37:24 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:4a01ceaed0df0b03f54d6781fda4ca9581e9648c6468e297dee2af79278f0007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192522326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af46a92f58bb6d5468933c0c2735727804a486cc42035a18c37301d1d3c05edc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Sat, 15 Nov 2025 22:24:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 15 Nov 2025 22:24:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 15 Nov 2025 22:24:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Nov 2025 22:24:51 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 15 Nov 2025 22:24:51 GMT
WORKDIR /tmp
# Sat, 15 Nov 2025 22:47:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 15 Nov 2025 22:47:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 15 Nov 2025 22:47:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 15 Nov 2025 22:47:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 15 Nov 2025 22:47:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de331da7b5fa32193d37464667be79a9514eefa9df4d5a7f8b711124d7538b6`  
		Last Modified: Sat, 15 Nov 2025 22:30:37 GMT  
		Size: 90.8 MB (90752790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27382bc87b45152e718cd5501dda54a956ac73db2ab9fea2cc9fa41650e1ed60`  
		Last Modified: Sat, 15 Nov 2025 22:51:24 GMT  
		Size: 73.5 MB (73492707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87e9dfeb8a0a8c7c7432b5366c31c367442e1a1bb1e9ac77dec28d17e0359c1`  
		Last Modified: Sat, 15 Nov 2025 22:51:19 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f5fc51ca1221dd051c3661dd8bb594d41a52e04aa05d99f9c5f8006187b066`  
		Last Modified: Sat, 15 Nov 2025 22:51:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bbb5f02aab51d85df5fc6b0205ef2b660eebfe1fd93264d28894d4f9ddc08fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb0a086dd7bee179170d6b86d6519dbace98fed61bc60f3baa0b3fd5d393191`

```dockerfile
```

-	Layers:
	-	`sha256:48a0a5d17c188356e49a1e92c8af2a7e74eb930e1572c91a536ff3d00f3107c9`  
		Last Modified: Sun, 16 Nov 2025 01:37:24 GMT  
		Size: 5.2 MB (5197022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a943fbf5af5009d230a85fa92b52b7dda3f8fdfdaf043670f4b23de578c5e8c`  
		Last Modified: Sun, 16 Nov 2025 01:37:24 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:2909d92b86129beea71ad1fe0ad2414dc87999e7306dbcfa018475ec0b804ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191000275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1043a2759c946907d491c004edf1f40b739401e2b16421428ec43b5084f359a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:32:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 05:32:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 05:32:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:32:01 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 05:32:01 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 05:33:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 05:33:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 05:33:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 05:33:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 05:33:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6e5b57d009ffc8e92434207bf8eddd2800f9112ab5f49d95410a4fdd9ca7de`  
		Last Modified: Tue, 18 Nov 2025 05:33:02 GMT  
		Size: 88.2 MB (88210704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5402c533426498236cf63171d0748968ceeb1774f805c0ae245ab3963b9faee8`  
		Last Modified: Tue, 18 Nov 2025 05:34:46 GMT  
		Size: 73.0 MB (72954158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c691e31b83c3914c7e58af04243704c14fd13d1cffb1c9aceb096da7ab688a`  
		Last Modified: Tue, 18 Nov 2025 05:34:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a2416f325851cff0dbe33b257bf837095fb5c4c2c348ec7e82f9086df69f95`  
		Last Modified: Tue, 18 Nov 2025 05:34:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7d28e1102bfcb9dafd2b8e9ae84da4ed42b6a92ebf27d51ee301b412ade2469d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5bb0d0228228830f6e47308693330e4de08ac760193ff9c41d10b13a689d65a`

```dockerfile
```

-	Layers:
	-	`sha256:55b26153f31c573a6bcd383d50515688c9eb84e35f61645ecf5c94b623245f83`  
		Last Modified: Tue, 18 Nov 2025 07:49:06 GMT  
		Size: 5.2 MB (5206021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37e491d688beb4af70f99b84b261d43f650feab5497a6e588d47eaf43b6684d7`  
		Last Modified: Tue, 18 Nov 2025 07:49:07 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json
