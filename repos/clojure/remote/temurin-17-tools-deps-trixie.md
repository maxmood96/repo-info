## `clojure:temurin-17-tools-deps-trixie`

```console
$ docker pull clojure@sha256:f52d6cb4366a2c2e6b28448f218a3e2549f6f62c51bc0ee0e400dda2be45fc7d
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

### `clojure:temurin-17-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:129897e9cbd84a8fdc1bd968a82e74eb07c755c6fb1c1a43403d3149f9087faa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280462600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f449165fd1295039ef602f5e5fd1e5b9db566900be10dcdf5cc4a33309017216`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:55:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:55:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:55:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:55:31 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:55:31 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:55:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:55:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:55:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:55:49 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:55:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:488b3563dee4d64d4ce36bba4381d90f3903106b3fa7c01ded27f152aa16497e`  
		Last Modified: Tue, 24 Feb 2026 19:56:12 GMT  
		Size: 145.6 MB (145628754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0942af08cf2dce5f796c7e9aaaffe5ba12959458c5b57e625d5ed169fcba2ff4`  
		Last Modified: Tue, 24 Feb 2026 19:56:11 GMT  
		Size: 85.5 MB (85539681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64f8e1b4569d77e4b631a8061459e47aff7f73d3588056214e647801229e3ed`  
		Last Modified: Tue, 24 Feb 2026 19:56:08 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9de4f0163c092afcab8a076724373d3bb60e1519f83fbb513f7b82ea360cb2`  
		Last Modified: Tue, 24 Feb 2026 19:56:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9c117b2bb403f88eeccf31a63a8b82c8467ac0015ff15a23f4cc66cb895b95b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7484834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a156a4216652f3431e83f9077b7a9f5466259739f151e95a70c1824bfe3de43e`

```dockerfile
```

-	Layers:
	-	`sha256:ba7033e2c322769ed83fe7ec9ecf7ed6504ab383fd9672e74b03ff98cee2ea22`  
		Last Modified: Tue, 24 Feb 2026 19:56:08 GMT  
		Size: 7.5 MB (7469080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a81f9056fb4b036c3d0d593f65d9ba0525dc120e8942ec7c3e200dbe519b3316`  
		Last Modified: Tue, 24 Feb 2026 19:56:08 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:49fa2cf455b33ecb8fc116f76892814cb1ded40d74bffeb1b135ee437b1a10ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279453687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f30350f51017aee8f50baaf71918438d6a48ee03cc0fd3605bde0509ee2541`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:06:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:06:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:06:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:06:01 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:06:02 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:06:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:06:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:06:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:06:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:06:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be33b841005118b59a7e12d2bac78b2346ecd05133d16ed3b21f62309455ded`  
		Last Modified: Tue, 24 Feb 2026 20:06:41 GMT  
		Size: 144.4 MB (144436218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4411226af139ee905c1a45727cd8297cbccfa99026aebf385235cf99d3bf691`  
		Last Modified: Tue, 24 Feb 2026 20:06:43 GMT  
		Size: 85.4 MB (85364263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc52b4f1bdc667fbbfe42372474e2c56223f5bd191ee74b7e010d26d9e6b7943`  
		Last Modified: Tue, 24 Feb 2026 20:06:40 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a8fd7596b96ffc0e2edc2153206c8b0b5d6919ed7d363bdbe26ed95b2f722`  
		Last Modified: Tue, 24 Feb 2026 20:06:40 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d1991971173ed58c83e47c8475c33dd9a436f0b24990e0d2d6ee6d4d0cdbf8bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821c282b2703d710ec7452b15c14a8e627f466ee37623c2c1303eaf3db03c398`

```dockerfile
```

-	Layers:
	-	`sha256:f18e5255c4647353753b0f4ab7022dce6ca9cba916344a20dc118164510190e4`  
		Last Modified: Tue, 24 Feb 2026 20:06:40 GMT  
		Size: 7.5 MB (7476110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec95061c571196bf298b0d6a1b6f24a71be0fd4daea7846ea1f770cbbfbee28b`  
		Last Modified: Tue, 24 Feb 2026 20:06:40 GMT  
		Size: 15.9 KB (15871 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:b5438792a8d435a780d893963adcdadb5a3a08b43b1b3a88a9ef0b55a4d45e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289498954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0b860d9e527d8ddf6e7652649c72ca8b09b9742bff7bd49aa9d7ce6f8deb508`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 23:48:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 23:48:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:48:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:48:37 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 23:48:38 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 23:55:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 23:55:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 23:55:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 23:55:50 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 23:55:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b4cabddd66d71e97ccb04d7861e4511a418edbd43a9f1a73ba473b7207138b`  
		Last Modified: Tue, 17 Feb 2026 23:50:19 GMT  
		Size: 145.4 MB (145438194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4cf53b8db1c2aed6f5237c04438f7b130c4dda8feda192480f8e952fe511787`  
		Last Modified: Tue, 17 Feb 2026 23:56:39 GMT  
		Size: 90.9 MB (90947599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60027f35b226184dc9ffa079a19a29ab0a18cd7c13c9e6e5d85519246f1a5f28`  
		Last Modified: Tue, 17 Feb 2026 23:56:33 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae140fcd67828b0c5d3cabd2abe5e0b320de4095266766959b5dae19a838e093`  
		Last Modified: Tue, 17 Feb 2026 23:56:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e9eff2c4b59fbba3c2c5d3ce873b44e3a47e673733a801a286d5cd638f6fc3ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700040a1660645770df84e15712e4d31915df837c3ddab07eca25ac94cd546bc`

```dockerfile
```

-	Layers:
	-	`sha256:cc1b6d1712627bf09ff80f018ea42d06955144bdf8e7cc42148e260bf28e0ba5`  
		Last Modified: Tue, 17 Feb 2026 23:56:36 GMT  
		Size: 7.5 MB (7473501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd0d8535891b875eea1698a8814c539832fbd8f0d628984d9ebd28128aaea8ee`  
		Last Modified: Tue, 17 Feb 2026 23:56:36 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:c7475c9913e97c05250f8cd52038503593984e59e9ec53056692086345ea74a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.9 MB (274865895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6386611f7532f5388b5e8e726175ea1cb30fc6a2b12b9d35995001dd3beff37b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Wed, 18 Feb 2026 10:19:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Feb 2026 10:19:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 18 Feb 2026 10:19:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 10:19:58 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 18 Feb 2026 10:19:58 GMT
WORKDIR /tmp
# Wed, 18 Feb 2026 10:41:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 18 Feb 2026 10:41:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 18 Feb 2026 10:41:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 18 Feb 2026 10:41:56 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 18 Feb 2026 10:41:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:618efd37f74728f7dcba60c231fad7f2d777dc65e4da32d0adae5e032e1fd125`  
		Last Modified: Tue, 03 Feb 2026 07:13:10 GMT  
		Size: 47.8 MB (47776763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a68b91c900b38b25108404deded7395508254e83b0954c22570460e94fb1a34`  
		Last Modified: Wed, 18 Feb 2026 10:26:05 GMT  
		Size: 142.7 MB (142663031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6106d0f2bf31c2330086ea7f8b5281d870282a61af671c4bd2e6619bc0c38c0`  
		Last Modified: Wed, 18 Feb 2026 10:46:21 GMT  
		Size: 84.4 MB (84425056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d0b6c5015e71a1da02f432ef745c2644c324407a45137c5338cbcc453bfbfe`  
		Last Modified: Wed, 18 Feb 2026 10:46:08 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257898e0e59186355d312fd1b3e96044906e9dec31bb39c2a69c1f9601cfa353`  
		Last Modified: Wed, 18 Feb 2026 10:46:08 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1fa08fd60de5ff648180c669f9ece11c0537411dbfdc8b52e2e8a593e0fba6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7470877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13c0b4df35b711cd839d734d8cd9f97dda0fa4fb6e57bae866d215c306243e6`

```dockerfile
```

-	Layers:
	-	`sha256:ae5400400ea0d106ae52f24f270450f0cc0f97ae9abc1ca93907c65a5f6e7f44`  
		Last Modified: Wed, 18 Feb 2026 10:46:09 GMT  
		Size: 7.5 MB (7455076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:889cf516c1475fa2f43d3e39db239f3df57a95bfe4fba59e2d0351ba8d2d4aa3`  
		Last Modified: Wed, 18 Feb 2026 10:46:07 GMT  
		Size: 15.8 KB (15801 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:91d8db1552ea7e9dba89408ad579955acaa364136d35e03bbb6f5913eb2a3f6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271494624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370ec6c6ff55fe65a7b00b988bd330c3b3ff7551a8d8a8b211fa97ab415f4cf9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 22:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:09:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:09:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:09:56 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 22:09:57 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:10:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 22:10:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 22:10:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 22:10:49 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 22:10:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868d422d07fcb06624c9f60a8bf6f9f34a34f93817bcffd68a63a327f55e0e11`  
		Last Modified: Tue, 17 Feb 2026 22:11:27 GMT  
		Size: 135.6 MB (135627116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66802d351feaa5515da5f4ae69601b137c86309431790646c50f76060421df60`  
		Last Modified: Tue, 17 Feb 2026 22:11:32 GMT  
		Size: 86.5 MB (86512084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859ff4808a6eab1368c73eda3eaead105a2a7f0204b63f9f725c553907a3c891`  
		Last Modified: Tue, 17 Feb 2026 22:11:30 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7df25eda8372c5e32ee023fa7e2a583d88454dccfd0184b3307944d61778b5`  
		Last Modified: Tue, 17 Feb 2026 22:11:30 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:56d0683410df60aed64775f04d5fada316c6efb50bdecc936c1a799deec6629f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7480756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e70965b8c714be35a71697d6670c90bb0ec48dcb18e00de0050efba32984bb57`

```dockerfile
```

-	Layers:
	-	`sha256:6130f2e2e7cc591118dd6b55417f9fdbf27fd6f0c085033366a9c2ea46efce67`  
		Last Modified: Tue, 17 Feb 2026 22:11:31 GMT  
		Size: 7.5 MB (7465002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:188b8f8ed4ffee522339ad4d1545b85c47c8f3e9a48a5ae9a52366497c147a1e`  
		Last Modified: Tue, 17 Feb 2026 22:11:30 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
