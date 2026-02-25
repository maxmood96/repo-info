## `clojure:temurin-17-tools-deps-1.12.4.1602-trixie`

```console
$ docker pull clojure@sha256:71a139b222237e22a1b8eca1b2ee33d0a53bba127576116c121a04c31d425ec1
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

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - linux; amd64

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

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - linux; arm64 variant v8

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

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:cb8aa3ef01fd30500e63ec447b484643f66b1d67c2b8e091d63a89b3c661d17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289508177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f77d624581c87cbcebb51dfdaa9305478c955a3dafdc74f0090f044b7a10bdf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 01:59:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:59:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:59:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:59:46 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 25 Feb 2026 01:59:47 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 02:04:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 25 Feb 2026 02:04:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 25 Feb 2026 02:04:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 25 Feb 2026 02:04:51 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 25 Feb 2026 02:04:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c93d40c272f62556f73a8f185bdb3534d9d5498e1326e609b9e0d6c7e31c711`  
		Last Modified: Wed, 25 Feb 2026 02:01:21 GMT  
		Size: 145.4 MB (145438250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66c23c6be5d2c56f33919a8c34e0d92dae6fc02e6a76a53198e6e0e600af6bb`  
		Last Modified: Wed, 25 Feb 2026 02:05:37 GMT  
		Size: 91.0 MB (90956624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5122f12e20b754ecc073972149cd990c8624614b13e36653b52f93caa59c2211`  
		Last Modified: Wed, 25 Feb 2026 02:05:35 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571d39b60c9f52972fad4c94dbc305e5a520b142b2fc3d5a44526c2af969d139`  
		Last Modified: Wed, 25 Feb 2026 02:05:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:45795c44be221873d88f609976fefd73f77f516d2455b795bd24b2becefbd733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceca0885ab53c2766c6112bb149bd6452ef6d196069bfd9811030a4f433c4349`

```dockerfile
```

-	Layers:
	-	`sha256:885cbbe84a4e617117405f79cb06064d9481ccc61f640aab7f54d9a26fc5da73`  
		Last Modified: Wed, 25 Feb 2026 02:05:35 GMT  
		Size: 7.5 MB (7473501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c01ce7adeda774dd1a9fc234f678ca7a0763748557f703ad94044dd977d42d2`  
		Last Modified: Wed, 25 Feb 2026 02:05:35 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - linux; riscv64

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

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:84d4dca7fd081c719aed1a7abba7d76d4abe49ecc8b652319c98a40411e9946e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271497373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8db48187cf0e9311762348072a84ecdd959509c26e8637f626ba439c61b4966`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 23:16:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:16:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:16:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:16:39 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 23:16:40 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:19:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 23:19:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 23:19:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 23:19:21 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 23:19:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1be9b165f1f0dbdb0d3d0dcb750f4dbc95a320ac91bccfe873000c67e29774`  
		Last Modified: Tue, 24 Feb 2026 23:18:03 GMT  
		Size: 135.6 MB (135627117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3295c59c71551c3b84e9e60e4cc3f9e4ad3ed366abc57060807256f4f8bf3a`  
		Last Modified: Tue, 24 Feb 2026 23:20:04 GMT  
		Size: 86.5 MB (86514680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cf208be5ab313761c0208b9f17a7e769a93b33dd8be03e1f1daf196037591c`  
		Last Modified: Tue, 24 Feb 2026 23:20:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6599b8ab834ced8de10f0cc32443c3bbdb647a4b1ece64d6f5cab7bce737693b`  
		Last Modified: Tue, 24 Feb 2026 23:20:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:00fc8bc99a60291fa884d2a708573d1478354f30f9cef723ed3878a7b8299ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7480756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e3e68f4c6c763cdbe66e6693fa4c631ae44596e5085d55e966897cac26135b`

```dockerfile
```

-	Layers:
	-	`sha256:b0bb0739fe6ae4ab7a9f791a42d570ad9d0bed5a5727c8a1f96103c80305b6c2`  
		Last Modified: Tue, 24 Feb 2026 23:20:02 GMT  
		Size: 7.5 MB (7465002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16451b997d823b53f4cd50c66cdbf4a60fa8f1207bb506c8468d6d66d51d47da`  
		Last Modified: Tue, 24 Feb 2026 23:20:02 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
