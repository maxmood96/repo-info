## `clojure:temurin-17-tools-deps-trixie`

```console
$ docker pull clojure@sha256:7894a75a88c33c7f9b95c2d80c56e9977c380642f758fc044cd1a032d2f299ca
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

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:e2df82ce084c06bb3f60d36facf579549c8a69bc52c5e8b008c1e6d261fbc578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.9 MB (274865328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9fd40f700b1689e04f8b0f68c85f150ec92eb9a5f45a9d065d6521a00ab245`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Fri, 27 Feb 2026 21:20:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 27 Feb 2026 21:20:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 27 Feb 2026 21:20:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Feb 2026 21:20:56 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 27 Feb 2026 21:20:56 GMT
WORKDIR /tmp
# Fri, 27 Feb 2026 21:36:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 27 Feb 2026 21:36:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 27 Feb 2026 21:36:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 27 Feb 2026 21:36:30 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 27 Feb 2026 21:36:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3be247472b67578a1d05739722d8adeca41098796e5d6210800176db58046fa7`  
		Last Modified: Tue, 24 Feb 2026 18:57:42 GMT  
		Size: 47.8 MB (47776936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f27f4bf7ad939ca2936c66027f77feab15c20528c320fcb92eb833d88b76cc`  
		Last Modified: Fri, 27 Feb 2026 21:27:01 GMT  
		Size: 142.7 MB (142662998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb458e28279666b452fa1a83642b925c284d11c7644b5a9373035d201e9d1ae`  
		Last Modified: Fri, 27 Feb 2026 21:40:52 GMT  
		Size: 84.4 MB (84424346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8ac6abc14fbb5137d1fb9de2666cb1bc844ca379acacf7ba37e75eff968e48`  
		Last Modified: Fri, 27 Feb 2026 21:40:39 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35123d56f3dea28446067705d0f695aba837a357dd6281ce8f3727340f1f923`  
		Last Modified: Fri, 27 Feb 2026 21:40:39 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:cef1e05b187d9ff96c5c7ba6ae74148df432fee28245c5ba1494bd2841b1a507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7470878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2965d86f538abd26602567e8a5f9d5f728d19ff862f90a2b450bbbadecff978`

```dockerfile
```

-	Layers:
	-	`sha256:1e2e2a6eb27ac9b1ff316c383764239adfcafb9da046333f61f06bcbdd32ea9b`  
		Last Modified: Fri, 27 Feb 2026 21:40:41 GMT  
		Size: 7.5 MB (7455076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:974ffffc29c65f86482811b4019ee0df5f26ec7ccff1bc10cf0811e9fcd7ff17`  
		Last Modified: Fri, 27 Feb 2026 21:40:39 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; s390x

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

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

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
