## `clojure:temurin-21-tools-deps-1.12.4.1602-trixie-slim`

```console
$ docker pull clojure@sha256:66fb1123770685504846d2bcc00d298cf7a616993ae18c34c1e57b5e1cd85b0b
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

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:58cc5d392dbb9f7be18361aba52877a2a5f6c4cf4cc3a1aa11a80040df33c76c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259632366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fc6482d177b0b7efb23517b11ac117b66d8d93458d4312262cb7459583ccf9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:06:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:06:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:06:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:06:44 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:06:44 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:07:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:07:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:07:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:07:04 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:07:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c014222af08156c00974b8d73b49d686fed7ccb4ad0c7eddb3bc3f6f82c758e`  
		Last Modified: Thu, 05 Feb 2026 23:07:29 GMT  
		Size: 157.9 MB (157857074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695c3a10ac345bcd54ed1394ba4dfaafbe499e8254f157a6d0129a887a683631`  
		Last Modified: Thu, 05 Feb 2026 23:07:27 GMT  
		Size: 72.0 MB (71995654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201e1bc91974084b8fae75b8472c6e98c0ea3d1e68c7e58dfcc02aa5b3b3ce61`  
		Last Modified: Thu, 05 Feb 2026 23:07:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7fc3d4bda2f160dc2957b47e8237759f1a25be756ab1193ef13ed81d3df9fb`  
		Last Modified: Thu, 05 Feb 2026 23:07:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:58e6461b238b791e3872eed41e88607c60614a354a8839c06c6c2d7e0300fa60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17098daa86f1b0492edc18c129eeaee5340cf43af8ee198fa0ae0f2ae08399a1`

```dockerfile
```

-	Layers:
	-	`sha256:bc010c61bdd97acbe45ede9773b97acc176458104c85013f9704b0502921991c`  
		Last Modified: Thu, 05 Feb 2026 23:07:25 GMT  
		Size: 5.3 MB (5259403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcee4da2215d6b898092358d36befc244b40c3c409d3c2435db6ce244eef834e`  
		Last Modified: Thu, 05 Feb 2026 23:07:24 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:32e84d156a3cb1a5c04e2482a51030302db628a7264c3aad66a48860fd33e77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258080814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546769ddf0b2e9e542213ba822544b521f507aecc5bf6d0add8de83de7c4e3a7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:07:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:07:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:07:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:07:37 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:07:37 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:07:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:07:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:07:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:07:56 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:07:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f87d110ade5325018b720c1fc1cd45b6d0d88997b13123ed8eaa847ef9a465`  
		Last Modified: Thu, 05 Feb 2026 23:08:20 GMT  
		Size: 156.1 MB (156133060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eac0d3062d44ba690c3fa4006aa11ed76b3054a11e2f24e40ffbf998e4dd44`  
		Last Modified: Thu, 05 Feb 2026 23:08:19 GMT  
		Size: 71.8 MB (71806648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c34bbe6ce8da6820228a25203450a3b971fdd34d284972c6ec0ceee4a61175`  
		Last Modified: Thu, 05 Feb 2026 23:08:16 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9057f426ff76f19ada56f0492c4f9c2741b5508aa95ea0c9cda8f609528fadc8`  
		Last Modified: Thu, 05 Feb 2026 23:08:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:816b071fdd95e39cec2ca84c0f03e28fe57176809f1c31f5ebac3c53624daf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5043280056f90ac3f52fc79be30d8721fde9aae7ed3acf4e1b215606d791ff89`

```dockerfile
```

-	Layers:
	-	`sha256:a82f2870747837e6fa77ed94094aa0fb4b014a02f391dd21d786c288e223bcae`  
		Last Modified: Thu, 05 Feb 2026 23:08:16 GMT  
		Size: 5.3 MB (5265172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9a5d2e2f9233d4ad4c9b7add438531b689ef0f19b3b18aa2d04d7dc5edd4b5c`  
		Last Modified: Thu, 05 Feb 2026 23:08:16 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b1480cb19ef225ac71af394596d5d25fb1d740dc327ee143fbe16ca0fec4bf53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268967314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9abd399ed2a7d964748dca3ee00a4709046ed60e7f4cb762248c2ca1d1348052`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Fri, 06 Feb 2026 00:37:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:37:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:37:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:37:54 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:37:56 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:44:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:45:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:45:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:45:07 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:45:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d803d46010c6f6fae7ea82f881a836bc9d2bf4afad631cfb7ffd52616e4eec`  
		Last Modified: Fri, 06 Feb 2026 00:39:44 GMT  
		Size: 158.0 MB (157977492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d9d94dd49a553eb6136a41fad225a0afc6d956a42bdb9b005769df910a3a26`  
		Last Modified: Fri, 06 Feb 2026 00:45:51 GMT  
		Size: 77.4 MB (77388594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85d1e7fe6f35913773bdde43f9dbe517e6226e1edb2d2830777f8a208bd3990`  
		Last Modified: Fri, 06 Feb 2026 00:45:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d14c407954658464ba427b45e5d4df4f7bfb10593481a4ecd3e42d9773d07ca`  
		Last Modified: Fri, 06 Feb 2026 00:45:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6a277f05786eed439f792da2c119098ae9a8609eeec3116c4111811016d7d34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db42a2db797f04425f4272c41983224f4401d19c001a0ebfe9ac407715df265c`

```dockerfile
```

-	Layers:
	-	`sha256:6b7647cd6a9309d26b21344e1f109e6a044813c1122284daa16e3266f7e06cd1`  
		Last Modified: Fri, 06 Feb 2026 00:45:49 GMT  
		Size: 5.3 MB (5263774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a7c4b5e85c6e9d8fe9f14734b169969683dc4af581bcc20febf7f98266b9cab`  
		Last Modified: Fri, 06 Feb 2026 00:45:48 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:7f9dbd3a84040835f3acb7023b924fb2e555bd1c3bb7c88c7f15a3568be9b26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256373573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef70d6eb49ee71c4dfdb5aab34665c3ee674a330eb77e3fe466c28b5b8e9e530`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 12:21:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Feb 2026 12:21:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Feb 2026 12:21:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 12:21:24 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Mon, 09 Feb 2026 12:21:24 GMT
WORKDIR /tmp
# Mon, 09 Feb 2026 12:45:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Feb 2026 12:45:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Feb 2026 12:45:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Feb 2026 12:45:07 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Feb 2026 12:45:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28f24ba54976c45441db0230fa1714d82b492b6ad8590ec1b4c327b709e7e83`  
		Last Modified: Mon, 09 Feb 2026 12:27:28 GMT  
		Size: 157.2 MB (157216910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77bf493b9c1e5f3f025f75579a796da1a09e109ebb88882f8b62265a2b107de`  
		Last Modified: Mon, 09 Feb 2026 12:49:07 GMT  
		Size: 70.9 MB (70879227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d803c8f4b3d83ae2e5a139a646d207f76362b1cefb23d03c9e1a549e5c0d7b23`  
		Last Modified: Mon, 09 Feb 2026 12:48:55 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809237e34caa1fe3be21026e08f8b9a3180f6d9e3bf3c36403f7e5f5e6a31e5a`  
		Last Modified: Mon, 09 Feb 2026 12:48:55 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b8eccd9ff75f45dc6b3fa5af1ec597457da3f89c9350180bca34b63065c13c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510b493359f71f3b57f8da3f3635ea55e4ab5cac13f3c78b4e9d6f7a7cca3fb3`

```dockerfile
```

-	Layers:
	-	`sha256:131b8c70e07988369df75563885cfd63ef83e817883b6050b3911e92c1fd1dba`  
		Last Modified: Mon, 09 Feb 2026 12:48:57 GMT  
		Size: 5.2 MB (5248867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd2bbe9dce59938c5616489ff847b4fd64b1c612d8bda9d2b08b1591333a250a`  
		Last Modified: Mon, 09 Feb 2026 12:48:55 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:5863d81b7f49257d9214f50dc043a31884d96f4b750eef2f6b61f84ad380afab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.9 MB (249897649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe15b2a42cbacb2bea7f4243a07429ac6f1fb4278c1c4168487e63e599a6aeb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:07:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:07:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:07:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:07:48 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:07:48 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:08:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:08:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:08:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:08:05 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:08:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7db0a1b6752cc0d06873f40aa9309942760c633cda5d42b6216b8311a487ad`  
		Last Modified: Thu, 05 Feb 2026 23:08:38 GMT  
		Size: 147.1 MB (147105286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f3cb72d23058ea13db9c7662f21d57f034d390b0305445dbeb47ba60623e22`  
		Last Modified: Thu, 05 Feb 2026 23:08:36 GMT  
		Size: 73.0 MB (72953172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b29b3f94256b50e293e0503c666072359769cbe5945b17f54491758d94ad55`  
		Last Modified: Thu, 05 Feb 2026 23:08:34 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ad50026779c7c80386dbc2d3cd2fba775a48af7ebbc7d0e4e47bff2e91595d`  
		Last Modified: Thu, 05 Feb 2026 23:08:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2dae024d7e0d188f5a93ffa817045186b33a30990b5b95d64f267a07506ac2a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68ba8a0c1bf3960e44aa03722dd5580334d4e52bc4c5dc3c12f432f882545c7`

```dockerfile
```

-	Layers:
	-	`sha256:5c4440b950cdf688c8cf8ec1a46de3fd73a7975791648fe7631886524f4d40a6`  
		Last Modified: Thu, 05 Feb 2026 23:08:34 GMT  
		Size: 5.3 MB (5255327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec30d52a9d4497f1d917f17bee8a7637726ad1c51b97940ddded729c7d476771`  
		Last Modified: Thu, 05 Feb 2026 23:08:34 GMT  
		Size: 15.8 KB (15811 bytes)  
		MIME: application/vnd.in-toto+json
