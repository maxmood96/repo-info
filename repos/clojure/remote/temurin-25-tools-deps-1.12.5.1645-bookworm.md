## `clojure:temurin-25-tools-deps-1.12.5.1645-bookworm`

```console
$ docker pull clojure@sha256:4cf962ac2d49bc3f17c3cf6ede84ac191286f70d421c68d0f032eee53466717c
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

### `clojure:temurin-25-tools-deps-1.12.5.1645-bookworm` - linux; amd64

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

### `clojure:temurin-25-tools-deps-1.12.5.1645-bookworm` - unknown; unknown

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

### `clojure:temurin-25-tools-deps-1.12.5.1645-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-25-tools-deps-1.12.5.1645-bookworm` - unknown; unknown

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

### `clojure:temurin-25-tools-deps-1.12.5.1645-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:43cf5fb9c3dd34de7e644de5770995a048b0cc73145e00ad503655bad857e740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231285146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938e2bce0c55b4df22fc364829046c5a176972c530acc037c0b0462e9f303dab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:18:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:18:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:18:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:18:51 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:18:51 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:31:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:31:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:31:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:31:31 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:31:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5de956b7a11284f1a158aa4d174299365ba072baa5eadc5c41d537c7ba7509c`  
		Last Modified: Sat, 09 May 2026 02:20:31 GMT  
		Size: 91.9 MB (91914029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a131bf079ca5d3007c0def241264e6aa497a41fc7dd6bd941144d6e136728293`  
		Last Modified: Fri, 15 May 2026 20:32:09 GMT  
		Size: 87.0 MB (87033283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e94472b23a8c063a2f313b86d8ce097895d59ec00da43551cb97bba61a620f7`  
		Last Modified: Fri, 15 May 2026 20:32:05 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96fce57370e8a543b19badb0f6d46debfc70803c265634324912d0cd00d5022`  
		Last Modified: Fri, 15 May 2026 20:32:05 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1645-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:db3c156f51789308c44571412b4d667508f2ff7c242b9fed12dcfada833cac9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7353941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9332883e84b39fba57fea3de59da82a66a6434f78631b65fc6e9d1b51cee3282`

```dockerfile
```

-	Layers:
	-	`sha256:93ce6e9d761e0f59c34b9fb73b687d8cffaad1b5631ab8e70d52aa06ac0ac97d`  
		Last Modified: Fri, 15 May 2026 20:32:05 GMT  
		Size: 7.3 MB (7336885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae9516dd7ef75d59c080b4a9052db089cab6225cba5b91b548dec82df3ffcb75`  
		Last Modified: Fri, 15 May 2026 20:32:05 GMT  
		Size: 17.1 KB (17056 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.5.1645-bookworm` - linux; s390x

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

### `clojure:temurin-25-tools-deps-1.12.5.1645-bookworm` - unknown; unknown

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
