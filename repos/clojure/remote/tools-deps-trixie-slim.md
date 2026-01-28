## `clojure:tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:2730411ccea73502855b0a6d1a5d31e5bfcb34ba89e821506d45bf4352fc565f
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

### `clojure:tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:86e46538b5542956615b7cc0e597bf31208ced6bfc82674fe4f1377d18ca791b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196764308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5567d53af822186e80dd09f895e60a6c8a8795c5fc979c3eb60d924c6020e6a9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:06:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:06:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:06:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:06:52 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:06:52 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:07:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:07:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:07:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:07:08 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:07:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2324899029ec84ce59e2e688b54e41a3d95efde4079e6cba8e9dd7bc29d6a004`  
		Last Modified: Wed, 28 Jan 2026 18:07:28 GMT  
		Size: 92.0 MB (92045329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378518943a6a476e33228e85b0001726fa2f00c7bb583fc46dcde45004ff06eb`  
		Last Modified: Wed, 28 Jan 2026 18:07:30 GMT  
		Size: 74.9 MB (74944252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b046c3cae57a070fe9a09b7d224942018153f10c60a5502c9859327aa53e246`  
		Last Modified: Wed, 28 Jan 2026 18:07:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a37d0def861616ec97617a2e9f8286898a188ec84bd757de503eeb668489112`  
		Last Modified: Wed, 28 Jan 2026 18:07:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:132142cbedc873f91c9a341a507cefa0c6ba94faf1c520cfe51fbc09769678e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d097a4223347ab12179e431e8c9382be755e7582d4cbc1c25f98ad5a786ec678`

```dockerfile
```

-	Layers:
	-	`sha256:2f16d9b4a8558d28811acafb12976f67eeb6ce05f14e026baf307ca8b10c5c1c`  
		Last Modified: Wed, 28 Jan 2026 18:07:25 GMT  
		Size: 5.2 MB (5207649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:846eec71159b440517b0073ad43f79c5c5b878f7dbfe22a252b0cb1f0cb4bd15`  
		Last Modified: Wed, 28 Jan 2026 18:07:24 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1eab5766c11c7be0b098e568e7c54b342294c419d1689cdf5b21d845012a2b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196309886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717683fc650bcc6aa3dba641c19a8eab82a464866dff078f66f6f0080829c4dd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:06:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:06:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:06:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:06:52 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:06:52 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:07:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:07:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:07:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:07:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:07:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74500f6c76c2ed38c7db8d9b37bb5da9b6f78c223d5dce7cd45c87a5056528a4`  
		Last Modified: Wed, 28 Jan 2026 18:07:31 GMT  
		Size: 91.1 MB (91052475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d748ee021a7969a6fa1fb1bac94b7c9c14eccaaf09450803c58eeb2abe76bb`  
		Last Modified: Wed, 28 Jan 2026 18:07:31 GMT  
		Size: 75.1 MB (75122327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5aa9db06ab5f561b7dc121ced9d4c848b4ce368db2c1a331f5e9ae359397f5`  
		Last Modified: Wed, 28 Jan 2026 18:07:28 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28275eafa73275369127701f634fd1589978fcc92ca3f651a2224ac86c6a705e`  
		Last Modified: Wed, 28 Jan 2026 18:07:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f210d2af73337b731e0f92c8775a0f7d7a9fca8c907dbca3b6e317f7bf539665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5230074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3ccbb177bf95a40c3519798e827e5734f54c54b063c65e67a8aef422c14387`

```dockerfile
```

-	Layers:
	-	`sha256:7e491310bccd068f55f8358113c5b128aa1fc0b2f4bfaf23f9252b416bba59cd`  
		Last Modified: Wed, 28 Jan 2026 18:07:28 GMT  
		Size: 5.2 MB (5213439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e517e056981f0984347c3eb56c3362d3a8a18f85e1af9a7b11942fa14d2630fe`  
		Last Modified: Wed, 28 Jan 2026 18:07:28 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:78771bced1fd66f4bb2422263bd4c18f30c118b9cceec7cac9b82c745648df65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.8 MB (205797960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a12761ab010bd964700baf980b9362a2d0d153ea16f7e2d489c139557146a1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:35:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:35:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:35:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:35:19 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:35:19 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:36:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:36:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:36:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:36:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:36:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b367f49452386f5648bf3948a486b48474525977f8798c80af3b3240722b801`  
		Last Modified: Wed, 28 Jan 2026 18:36:52 GMT  
		Size: 91.6 MB (91610768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e49a8135c0c38402a68bed3899f1be03cf9daa420180e6f02d8d762067deed`  
		Last Modified: Wed, 28 Jan 2026 18:36:52 GMT  
		Size: 80.6 MB (80590551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f24a09db3b09c303855f1919a89d7aa5163b891cc73923e351d326e3ed9707`  
		Last Modified: Wed, 28 Jan 2026 18:36:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f362db66306491abe62f8af55d27fd05bb078a8acbdc99051e656ec7d92e63b`  
		Last Modified: Wed, 28 Jan 2026 18:36:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c6ff817a276178b9d3681742c149218913d7d1501a177ddf6102f06b64d82790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51404253a1f9da8bcba507a236d4e06dc1f61ff629c9de297e2ce6bc9d3c2c2`

```dockerfile
```

-	Layers:
	-	`sha256:3daa0930804d38ab127e36aed5b991c78871188c7b99b7400add0df74a704cdb`  
		Last Modified: Wed, 28 Jan 2026 18:36:49 GMT  
		Size: 5.2 MB (5213330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5abc4fa8d173ab74d751997b4d8a48a10acd1c08f9ec4622ea605a2bc124f12`  
		Last Modified: Wed, 28 Jan 2026 18:36:48 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:92e2532348045ed47c435d3a11544968b274006e8f30e983c0c18b57a466d891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189904353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f35ef2374dbfa7a85fe46bcbcdd3b4b763aed7599dbbd585ca730f0b98c211c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Thu, 22 Jan 2026 04:35:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Jan 2026 04:35:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 22 Jan 2026 04:35:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jan 2026 04:35:53 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 22 Jan 2026 04:35:54 GMT
WORKDIR /tmp
# Thu, 22 Jan 2026 04:57:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 22 Jan 2026 04:57:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 22 Jan 2026 04:57:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 22 Jan 2026 04:57:57 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 22 Jan 2026 04:57:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c69cdd71ef06850eefda28596d4212304f3101cd9d101f44fb4cf0c74701f3`  
		Last Modified: Thu, 22 Jan 2026 04:41:12 GMT  
		Size: 90.8 MB (90752894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6d3a24e9d95f0a53d69ef1e185241c625a41b38f404e11d840c904103e56ed`  
		Last Modified: Thu, 22 Jan 2026 05:01:36 GMT  
		Size: 70.9 MB (70878730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b476d3e9776c236b085a0fac9bf9688b2075c785db6db5441d6b35b870153e4c`  
		Last Modified: Thu, 22 Jan 2026 05:01:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ebf67b75368031bcbccfb2b55210c9b55d09be236a21b0cedd77ccbce8ccf1b`  
		Last Modified: Thu, 22 Jan 2026 05:01:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:19773bcbf4ba7724e951b0f2f421e37b20ebcdea7d8d22106a3925f36e843024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bfa817792c85cf3a17a950e8e4baa05425bad4984aa40fd36b83fd7cd6ef340`

```dockerfile
```

-	Layers:
	-	`sha256:f836df0b753bc98eabb8debb449f1f6961b29a1334ffef48afa9a5bab6ef03aa`  
		Last Modified: Thu, 22 Jan 2026 05:01:26 GMT  
		Size: 5.2 MB (5197120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab3e34b5822126bcf79d703e0039a9de285c818f46702ab468c3a1bd699b2126`  
		Last Modified: Thu, 22 Jan 2026 05:01:24 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:3aa1105552d2dd1b8ba16479718a43b90a3423854288a35492b0b715d57f5f3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193612516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2600087d69071064b43d0aaecf4cbca8d8225b5269c9096d1c6957d85a72f86`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 23:23:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:23:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:23:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:23:10 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 15 Jan 2026 23:23:10 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:16:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:16:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:16:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:16:10 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:16:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:27 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2b60cbc839537ac9d2d64e95bf99e1c19c3b75f06175e544fbfafc8cc5fea1`  
		Last Modified: Thu, 15 Jan 2026 23:23:51 GMT  
		Size: 88.2 MB (88210671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87c07331fb0c8e79a4db7b4963a9ca46c41069723f01a866c1ab11d7308d6b9`  
		Last Modified: Wed, 28 Jan 2026 18:16:35 GMT  
		Size: 75.6 MB (75567395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fde3fc2ea86ec16b71ae94ee6484b0df948497216e879d9d858c49f5e45bc31`  
		Last Modified: Wed, 28 Jan 2026 18:16:34 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647ab24f49cdd51cd3a05466f5bbece8f204d2a6c668ab26eb6363a6c335e40d`  
		Last Modified: Wed, 28 Jan 2026 18:16:34 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f048959bdeafa86beafa4b9fb098f446e941cf9243732fcc8fef760c99634c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c34a05d06521a3fc675c3490deb6f4422f5a8b28b6e5d325a3fe6a02be958e`

```dockerfile
```

-	Layers:
	-	`sha256:a51a7a97681253c2a558709bc40110f43ffd86b29e97ea1a04fedbf983bc7cd3`  
		Last Modified: Wed, 28 Jan 2026 18:16:34 GMT  
		Size: 5.2 MB (5206121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e344d74abb1f6adb3e85ab888ebcb01a55f2ecbecd3c4700f4a021beddcddba`  
		Last Modified: Wed, 28 Jan 2026 18:16:34 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json
