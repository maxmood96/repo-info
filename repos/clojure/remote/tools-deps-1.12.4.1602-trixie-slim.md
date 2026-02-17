## `clojure:tools-deps-1.12.4.1602-trixie-slim`

```console
$ docker pull clojure@sha256:2030022b81c01d37d8c743053513e3420dc9526d42b7243866c598eb2f32faf2
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

### `clojure:tools-deps-1.12.4.1602-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c2adabcbe8759a6356867b5689b97946660a978d2ccd250371a4563c309ab6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (194031496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c289c97e64a542550d331cc0dcafe0670816137a84fe4a9cd2739b04b7291a03`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:46:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:46:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:46:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:46:12 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:46:12 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:46:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:46:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:46:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:46:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:46:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e14028f574f67f86f95a3df652a89e4c501c1886a94e13bedcd14bd5791b0d`  
		Last Modified: Tue, 17 Feb 2026 21:46:58 GMT  
		Size: 92.3 MB (92256289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac007c339963d629a955257a31b24294ebcae734c9862378df6359a995b7a72f`  
		Last Modified: Tue, 17 Feb 2026 21:46:58 GMT  
		Size: 72.0 MB (71995570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ffbe45995b3e30ccaa3a2d17cc93d29220041936550b6814357c697c68fb747`  
		Last Modified: Tue, 17 Feb 2026 21:46:55 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d2b1d5119ffb199f441c374a3fe5f05d144e6cc9ccbac8edaf1b98591695ab`  
		Last Modified: Tue, 17 Feb 2026 21:46:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e13342f00a75002d5f0b110df779b4491d323d3677602589f9b37057ed81c7f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5242130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ed4964682381b4bd53fcb9bd75a7981a7c74b3cd9ff35e8176094b08c62fe4`

```dockerfile
```

-	Layers:
	-	`sha256:146c639b678468147ac71046097011eac995b828d101776affa349fc5f79d693`  
		Last Modified: Tue, 17 Feb 2026 21:46:55 GMT  
		Size: 5.2 MB (5225637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e2c434bee4ddbc28a1700971f57727ae53bc01e3c521a5ce145594548599b1c`  
		Last Modified: Tue, 17 Feb 2026 21:46:55 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:32c55f337a23f25068ec03baf39e5e4d97f9074b00b513a094882b599311284c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 MB (193236155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd9a35ede131610f91fd2174f3029bfb0d1783b77e24a86ffa1012c7858a140`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:46:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:46:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:46:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:46:04 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:46:04 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:46:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:46:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:46:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:46:23 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:46:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80424176c68013d3ceb2a7049cbe042719a882198832ddc42ad82131d032c602`  
		Last Modified: Tue, 17 Feb 2026 21:46:40 GMT  
		Size: 91.3 MB (91288273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b656c1ece603c9041924f79481280c2112bb2f3c20221ee10012205b36d0d6e`  
		Last Modified: Tue, 17 Feb 2026 21:46:47 GMT  
		Size: 71.8 MB (71806776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b39bf42842e5fd1f39653767accb7f41925b12e3650ef8c6851460dbdbbc81`  
		Last Modified: Tue, 17 Feb 2026 21:46:45 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8cbf71bad0761a21e649d68cfe281454f554379d366323130e285e39c7e171`  
		Last Modified: Tue, 17 Feb 2026 21:46:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5252ecdce188a0432db473a94254d338b3879f7726499543a8fa99fdd32706f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd29daea1265e9c17551198525926a909ddbac3aec7d0e02fa16d77361a2a2d`

```dockerfile
```

-	Layers:
	-	`sha256:a0ac8a491725b502d4ec95e83b740198a8f6328b29ce5f1f22fafd786fd050a1`  
		Last Modified: Tue, 17 Feb 2026 21:46:45 GMT  
		Size: 5.2 MB (5231427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f615549ab718bb30fddb6b6d51d51581681bf415141d2baa46cdc518a864c5a7`  
		Last Modified: Tue, 17 Feb 2026 21:46:45 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:716dc4d98dcddb9e4f31792ef2fcabc99ea9e5ec8397a4c28a4069a2218c2e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.6 MB (202623558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420cdd4d3e052529bcf00f32797fba986bf2df4691dd57554fe14b95dbc1a446`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Fri, 06 Feb 2026 00:48:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:48:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:48:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:48:15 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:48:16 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:55:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:55:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:55:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:55:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:55:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cfca27e4d0c0686d68682e7bdbb0f0c15c94dfea8c09b2d4c6306086826ff1`  
		Last Modified: Fri, 06 Feb 2026 00:50:04 GMT  
		Size: 91.6 MB (91632917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1fce39c7673a6be34b82e9ae1f2b6b071a3c5b5499adb00ffa225c7c1c7c95`  
		Last Modified: Fri, 06 Feb 2026 00:56:02 GMT  
		Size: 77.4 MB (77389410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7301baf49afb2a1ff39746fe8bab71b7a63081eacb72be65165f77791c36852`  
		Last Modified: Fri, 06 Feb 2026 00:56:00 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2601d7ea8f69b87a60ffb7c47214faa3b234267038edf5bd95e950ffb42f495f`  
		Last Modified: Fri, 06 Feb 2026 00:56:00 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:44353c9e54d513bd6ad67b4e9d3daf55ac652c4c1aa993af7fe92ad0d937bf2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6b08df9c495932a54e78c7227f7da277d1465a621f5769ec526d3b532aa2aa8`

```dockerfile
```

-	Layers:
	-	`sha256:58691e53c43d31616042c4537605e918bfb6b5ba1171a7ee2da42a0d07c1dab5`  
		Last Modified: Fri, 06 Feb 2026 00:56:00 GMT  
		Size: 5.2 MB (5213332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8603c01c3b74c8f119e83dc5e4eb1fc06961781d41924a29bf67672f5a28d2f9`  
		Last Modified: Fri, 06 Feb 2026 00:55:59 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:0001c2133e1c0210aafe028a154427defc9c9bca5d143376a20980f81156e589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189930199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ffa106a76dcfd5d35b04797fb8cc3ad7502661489b1f13dadd8dfebb226c7b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 13:01:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Feb 2026 13:01:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Feb 2026 13:01:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 13:01:01 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Mon, 09 Feb 2026 13:01:01 GMT
WORKDIR /tmp
# Mon, 09 Feb 2026 13:25:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Feb 2026 13:25:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Feb 2026 13:25:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Feb 2026 13:25:39 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Feb 2026 13:25:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3259c1d4e8b88a02ac6a13fb17b96d8d9cdc8d3493e158953ae177f9140e66a7`  
		Last Modified: Mon, 09 Feb 2026 13:06:37 GMT  
		Size: 90.8 MB (90773406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a8472103507a408f66e4239d214d124a48b439f62915557b134a617d0e21ae`  
		Last Modified: Mon, 09 Feb 2026 13:29:29 GMT  
		Size: 70.9 MB (70879357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e8f5b408e4ae3c1124cdbbab60da3f8cc9bd25d2c0dc10e76dd4c4b21ea3e7`  
		Last Modified: Mon, 09 Feb 2026 13:29:17 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd4992138c38e7784128831c7689da52e6419bce5c93e9c42cd60e274b09846`  
		Last Modified: Mon, 09 Feb 2026 13:29:17 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a32ebe0ae4473e185307e5c6971c61d3965dfffb930d2a2a641667b735aa7fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2706c98b0f3c19044917b421f29b4d09cf02377e8c7149b319678e94d60468c3`

```dockerfile
```

-	Layers:
	-	`sha256:0aed53e8d24025187b36018499cd7a52c6dadaa21b805a5603caba7b98481d10`  
		Last Modified: Mon, 09 Feb 2026 13:29:18 GMT  
		Size: 5.2 MB (5197124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a306258777842f8944989edfadb5c03efcc45f836e085d81ef383620e0553c26`  
		Last Modified: Mon, 09 Feb 2026 13:29:17 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b98a47813dbac35cd2865b7e2cbc4164b58fb4135ba5b7fc15f5754315df94ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191026134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc2bae9f524befa41a40ee19547f02845c3fc0fa9aa8e39db856097f89193d2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:09:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:09:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:09:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:09:01 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:09:01 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:10:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:10:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:10:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:10:24 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:10:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f346e6c932681347824fbcb087b1626c7950a778909ec292081697fb26b29a3d`  
		Last Modified: Thu, 05 Feb 2026 23:09:44 GMT  
		Size: 88.2 MB (88233823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3b242a298ab9cf93082571abc98d35c63786a42d07aa80cb344ca27639287b`  
		Last Modified: Thu, 05 Feb 2026 23:10:48 GMT  
		Size: 73.0 MB (72953121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db11d621821e995ace17b7452ba8df75bf39eca7fd46caedd0e024983d1acfc8`  
		Last Modified: Thu, 05 Feb 2026 23:10:47 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68834522710c83d343deafb1b828912c15c673d36602b94d0438e9c3d5dbe91c`  
		Last Modified: Thu, 05 Feb 2026 23:10:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5e088513893eb4367bee2965bc209c45e32ca81c7be39294126f2ac64da996ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d8a2abf084358174ffd72308f16aeb2256c4c6543ce61e0e5de7d03c584c656`

```dockerfile
```

-	Layers:
	-	`sha256:a9f6ffb37c7b534dd840e4fecd03837a61796597436b8b3a996edb1a8a024de6`  
		Last Modified: Thu, 05 Feb 2026 23:10:47 GMT  
		Size: 5.2 MB (5206123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6678cf0f0badd14f1edefd9bfbd4e8a321cae1dd763b5a61a36a618ebcea374e`  
		Last Modified: Thu, 05 Feb 2026 23:10:47 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json
