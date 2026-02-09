## `clojure:temurin-25-trixie-slim`

```console
$ docker pull clojure@sha256:cd8cc890210386f23065839ce634d918e37c9d903d43c7c13f455515b9116c46
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
$ docker pull clojure@sha256:591d0994eebbf22d8181dc14eb24eeb483baee5f8d2b8f5e509aa24d1e062660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (194031516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:317a3c5b009227af07de2214838655083f3cebf9e520ce3f39e97b7a4e1978f6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:07:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:07:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:07:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:07:35 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:07:35 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:07:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:07:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:07:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:07:53 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:07:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3632cba13a3ab7871841fcc2a916c2ea3661ed49a289e3fb9b85cf609cf5cf`  
		Last Modified: Thu, 05 Feb 2026 23:08:16 GMT  
		Size: 92.3 MB (92256283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14018b9f26a39e8e3d4a56254041aa8538d4f7be1b97756796895912720894d5`  
		Last Modified: Thu, 05 Feb 2026 23:08:15 GMT  
		Size: 72.0 MB (71995594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f88a75800c67258608f494fd450ed1d5fbaa7dabf256792545bf28a8c25a06`  
		Last Modified: Thu, 05 Feb 2026 23:08:12 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e95efa1c490db2389dd4fe991c1c09063d568eed585fd76991a97014fec977`  
		Last Modified: Thu, 05 Feb 2026 23:08:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c7a7f5516cc88ecc50533a64a8ce363f1ffc9f22e9effddc8f901fc190267fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5242128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e283659d7061c915e223fc3e90564dd0e322cd9ed00b20ee7526eab496fc0f`

```dockerfile
```

-	Layers:
	-	`sha256:bcb192086758753b7773f3b7a59817321b2d331ed1f1dbd70a64ac974ca0f56f`  
		Last Modified: Thu, 05 Feb 2026 23:08:13 GMT  
		Size: 5.2 MB (5225637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1b7669c9aa9dd91dd4bc22e1185936e865fd820b35bffc759ac8d93af7149b6`  
		Last Modified: Thu, 05 Feb 2026 23:08:12 GMT  
		Size: 16.5 KB (16491 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4d744bb37bc8004903678e38e46a3b4db0fc557dcab16c07c34bd6237212b71b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 MB (193235814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab49bfebd02ad1a198a066245e847629f9b3c5265da1c5fa2cf04ac17b65a856`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:09:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:09:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:09:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:09:00 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:09:00 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:09:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:09:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:09:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:09:18 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:09:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce844fb829c7e694003e64e20038641cb03f0b9ea53794d12c0c29809702437`  
		Last Modified: Thu, 05 Feb 2026 23:09:40 GMT  
		Size: 91.3 MB (91288277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcfd110eee6ae695b56362f6f4b13ccf29bf87d6f2fce0b352bf422a305fc02`  
		Last Modified: Thu, 05 Feb 2026 23:09:40 GMT  
		Size: 71.8 MB (71806431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834a6a7e5cf9d0cb1cc2023fcaab766edb720f8c26d2ecf908828a7196c7942c`  
		Last Modified: Thu, 05 Feb 2026 23:09:37 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ffd68ba3501fac369953da99baa2c40936f91bca859a18fe57d8e57260c252`  
		Last Modified: Thu, 05 Feb 2026 23:09:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:28b637fa5b98af6161617df2c68ef6cf9224d18999a23a6c5f4b9e77c5ab988a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5248062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30dd57f5765476716b75fe54bc937564f1b59ce49a8fd4ab4b0a718c618f52f`

```dockerfile
```

-	Layers:
	-	`sha256:6944c2823d47c6a0bb4721769715da44335391ccaba564010c14ef7facaf227e`  
		Last Modified: Thu, 05 Feb 2026 23:09:37 GMT  
		Size: 5.2 MB (5231427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00516c9d1a8beda6f6ffb81183f30b9fb676f7384b9369166d7ccd97cdb76666`  
		Last Modified: Thu, 05 Feb 2026 23:09:37 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; ppc64le

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

### `clojure:temurin-25-trixie-slim` - unknown; unknown

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

### `clojure:temurin-25-trixie-slim` - linux; riscv64

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

### `clojure:temurin-25-trixie-slim` - unknown; unknown

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

### `clojure:temurin-25-trixie-slim` - linux; s390x

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

### `clojure:temurin-25-trixie-slim` - unknown; unknown

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
