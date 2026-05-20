## `clojure:tools-deps-bookworm`

```console
$ docker pull clojure@sha256:b99402079e4850a943db1c96b2a03a342d74fb0b409d037bb8875f6c16a1b448
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

### `clojure:tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:8bb95def57a1f0515d9aae54b13fefa634907630d930e69e048cd89a6238a01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.3 MB (222283684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3b6008c8a53e8146b93c7a73218df8e78be359dc8729304507356a5e0612e57`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:01:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:01:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:01:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:01:10 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:01:10 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:01:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:01:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:01:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:01:23 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:01:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4d7c003a9799fd0b5028602ab76b4ce46b51602570aca46308f1fce1585208`  
		Last Modified: Wed, 20 May 2026 00:01:43 GMT  
		Size: 92.6 MB (92574564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b168daaf328d023851f78a5e74a635c137c9d1e13494d18ed814c5e441760b28`  
		Last Modified: Wed, 20 May 2026 00:01:44 GMT  
		Size: 81.2 MB (81212645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e4dccf0c4b54615b6ad93d26f3c7a047cc443357a3eef08857a3a5933c9d94`  
		Last Modified: Wed, 20 May 2026 00:01:40 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a206d379db06431efd1be868204df703b4b5bdb2e9f8c11949797ef0ffefad09`  
		Last Modified: Wed, 20 May 2026 00:01:40 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:25fcf16802b88bb16bb4109e384454e6f41d205c895b2f843b7ef824ab1ffd60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7366268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4fc385dd6d0b771f8fe05308dc70f6a4ee712648a6173378aab95e45539781`

```dockerfile
```

-	Layers:
	-	`sha256:1b008e096013fac176efc9f5f8dd9c6956e9492c6891c7478bb29ded878b0e43`  
		Last Modified: Wed, 20 May 2026 00:01:41 GMT  
		Size: 7.3 MB (7348343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20b8d84104837c6b92f6b01bf773071ad9c87f154cd14aa8a610a70ea7610de3`  
		Last Modified: Wed, 20 May 2026 00:01:41 GMT  
		Size: 17.9 KB (17925 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bdc7ac4100358cbc1f89f061df4826e0b94e90e8f45fa213dcef2cabd4b5ef9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221136365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d651b7e4f97cc4ec08fbeb1c11e113dc834e11cf5b186f9770b544f793cecdb6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:07:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:07:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:07:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:07:15 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:07:15 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:08:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:08:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:08:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:08:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:08:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b80a37e284dcb6180825d8a8cae0925e3b5f62c9939024cbb94f6110887851`  
		Last Modified: Wed, 20 May 2026 00:07:50 GMT  
		Size: 91.5 MB (91542261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d757536e2a6b4bab2fd2fd726936699fb332c45d4dd7984ddfcd707642d776`  
		Last Modified: Wed, 20 May 2026 00:08:31 GMT  
		Size: 81.2 MB (81213631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61301cf64050eb4600d783887c0496f91f465d6915c4dc4fc06155ddc50f31a`  
		Last Modified: Wed, 20 May 2026 00:08:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585d031c20d5cdbf23279ce46213ead99eef83acb161be57ea8aa66a826a3bee`  
		Last Modified: Wed, 20 May 2026 00:08:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0cd5ecdaecabe05a3cf6e155d37d939afdb24dc2234d84b0e6fe98ea6b732053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7372288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e490ab01529aa145ac54a3fcf2d4375129fb87383f524db188404b37006ac870`

```dockerfile
```

-	Layers:
	-	`sha256:23d9069b67c5baf891fb098e2c4581d1d629d7e07ac1a399af8a74c1383bc303`  
		Last Modified: Wed, 20 May 2026 00:08:29 GMT  
		Size: 7.4 MB (7354175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29957ea7fa8c7d13d89c4e5791aab94d37262377ab1ed8a89fbf45e6a4c78e7f`  
		Last Modified: Wed, 20 May 2026 00:08:29 GMT  
		Size: 18.1 KB (18113 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:910c42731a2b098d3d70dc4062072e84be94497d7a2570a1d2be80a551d22d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231301209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9feb530d8cae9c06c9429e11750e67d2904c917a65919faddf38826f74e0e9f9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 05:41:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 05:41:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 05:41:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:41:51 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 05:41:51 GMT
WORKDIR /tmp
# Wed, 20 May 2026 06:07:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 06:07:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 06:07:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 06:07:54 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 06:07:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d9d252f0e38d109f9943592c87001ada39f271784191f398d66e991f1eda37`  
		Last Modified: Wed, 20 May 2026 05:43:46 GMT  
		Size: 91.9 MB (91914038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51015a6f005ffc9fb4da6611b48e5ff271438dfc4c3b4acf1a1eba1e959cab29`  
		Last Modified: Wed, 20 May 2026 06:08:31 GMT  
		Size: 87.0 MB (87045928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067e96e2d21bd4c77101b8e185705324c03c370247e74d26219376f048de54a4`  
		Last Modified: Wed, 20 May 2026 06:08:28 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce161d206e1a35844b3844751aeebacf8625afc5ae4350651263b67a7c3e3dfa`  
		Last Modified: Wed, 20 May 2026 06:08:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:591974c52689eb8ea0e0b0e71e3bb9f1473ed8b8b7ebcb7ada401725f2a3bb5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7354916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c8dcc745e1cdebd54202c839dd29c3ad3810a99c66376de8a7d84580878d1e`

```dockerfile
```

-	Layers:
	-	`sha256:44f1f925ce3ad594e301a2d50b5dfe37d4027ebd758181ded278968d17a561e5`  
		Last Modified: Wed, 20 May 2026 06:08:29 GMT  
		Size: 7.3 MB (7336907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22f6340c5ab814142abd7b579f8f72925dcb4883104f9a807bca48154292bc8c`  
		Last Modified: Wed, 20 May 2026 06:08:28 GMT  
		Size: 18.0 KB (18009 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:bbda21f9deb9553223c62740cd66d3a2030dd737f7fc021239319b49aefd1626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.6 MB (215602887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2236d12061380ff82c70180dd45f96253e2f69353eab0401dcbe21a2f3349e2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:47:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:47:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:47:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:47:45 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 01:47:45 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:47:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 01:47:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 01:47:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:47:59 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:47:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113ccf669240d0fe6117fdafee798a5fd25a6e1f72b104e98237415b0ce808e1`  
		Last Modified: Wed, 20 May 2026 01:48:35 GMT  
		Size: 88.4 MB (88420321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e4d2cddc3a561cee11feeb5423c5a1f7406905d66b81d95965dfc165b05f29`  
		Last Modified: Wed, 20 May 2026 01:48:29 GMT  
		Size: 80.0 MB (80025940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1bd1a54d43a652aa68d3d072db6b73ea464a2062f6404fa5fb9ec9e127b3973`  
		Last Modified: Wed, 20 May 2026 01:48:27 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa825d9e285586115ea864bc6f475680d20328114072a93bcbacbcc5a94f4c6`  
		Last Modified: Wed, 20 May 2026 01:48:28 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a14f87b0dfb4ea989e856c9a5c3b0d8e25c090c98dd0edeff31c259975d17977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7342149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb7f7ff1664e26f201217563c24e384e87aebf963d149f3495d428490455750`

```dockerfile
```

-	Layers:
	-	`sha256:79213347f5687aaada2c6c2b65c440df6e70760145beeeca70ded7b3741e2d87`  
		Last Modified: Wed, 20 May 2026 01:48:28 GMT  
		Size: 7.3 MB (7324224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:253b0860713b74e7266b55b35ae1c47d0681697d5fb983d3534ac57eaff5124b`  
		Last Modified: Wed, 20 May 2026 01:48:27 GMT  
		Size: 17.9 KB (17925 bytes)  
		MIME: application/vnd.in-toto+json
