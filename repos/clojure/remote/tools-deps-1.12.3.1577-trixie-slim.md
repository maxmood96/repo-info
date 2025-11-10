## `clojure:tools-deps-1.12.3.1577-trixie-slim`

```console
$ docker pull clojure@sha256:88c62e40ebb3a4f0c668ad67f6a04a0123ddac549189961af28a392c6eed519b
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

### `clojure:tools-deps-1.12.3.1577-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e8464eef088733fd38bef8a1f00ceac1da38f3a099e9dbf1e77012df8728253d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193819681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53e11a83459401f0361e23d1b8cf9fc7600a34e7a57fa833ca4a2bfbe2bf3f6b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:46:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:46:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:46:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:46:19 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:46:19 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:46:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:46:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:46:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:46:37 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:46:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f81d8750fde4d893bae319ba5290ec80063d488f67295118e1c30c38af84a3`  
		Last Modified: Sat, 08 Nov 2025 18:47:23 GMT  
		Size: 92.0 MB (92045301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e00fbb4f5a87d905e1608446b410710bce634cba722a3e0d781e428e940a36`  
		Last Modified: Sat, 08 Nov 2025 18:47:21 GMT  
		Size: 72.0 MB (71995230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf5cecf95da920fe756ad0966b0ddf60e04e10c0c5c89f8fc19c8dc32664fd3`  
		Last Modified: Sat, 08 Nov 2025 18:47:07 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f97ce715e3da5aea1e412a352359869fe6777404a3e56241a70582c41118edc`  
		Last Modified: Sat, 08 Nov 2025 18:47:08 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:82ce1859d16c05a1d0c15b96e269ac9d1cd3e9050d75e7113df259996a4f4c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a566fdb044e0afc81ed1f8e2ff0396184f5fe9e24e406d511b7d3030e9f989bf`

```dockerfile
```

-	Layers:
	-	`sha256:05f5249770ec83e667c31e0dfd03201a5c224b36713d1d7b71aaa506bf64fec7`  
		Last Modified: Sat, 08 Nov 2025 22:53:32 GMT  
		Size: 5.2 MB (5207519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11e452ec6c801678ae375f7a3f85ef9d6fe5a0aba37b2230f79501b5e9f79745`  
		Last Modified: Sat, 08 Nov 2025 22:53:33 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1a06bf7de89cd9a0c3b16922fcd80c812fa545ad279f01e8ed65442254474ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (193004345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e411950a5a4cce0360ede5c73b8b3cc1b6ce7bffba9c756e29250229dfb35f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:46:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:46:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:46:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:46:02 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:46:02 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:46:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:46:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:46:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:46:20 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:46:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786eebc84c6d52d9fa0866dcee093a214c578a1f329393d0626f9f70f31ddee7`  
		Last Modified: Sat, 08 Nov 2025 18:47:04 GMT  
		Size: 91.1 MB (91052532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36a5c95d82250f33be8795394294796d4106d179e5cc5f38241294f8a0f881e`  
		Last Modified: Sat, 08 Nov 2025 18:47:05 GMT  
		Size: 71.8 MB (71808472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69f53ea307c586c15db1ff6fbe5f3b433fb4ce9366e3a04fae00884d46f3ef4`  
		Last Modified: Sat, 08 Nov 2025 18:46:56 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b911b77cda92063a7e896d9e70ff0b647f25c08ceaed46641bb06a2302b6ab`  
		Last Modified: Sat, 08 Nov 2025 18:46:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ddd75b853aaca3e69a4aabd0def41d918006f43a62dcbb3208a85c6d24f73021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf44a476e185e3ce3fb73007f6b587fa430c0105108cdc37a9aa218e8c6e5a82`

```dockerfile
```

-	Layers:
	-	`sha256:1e37129432e1570de2cdc3e809f5fda468fe3491995eb98d72ceb4f6d4128e47`  
		Last Modified: Sat, 08 Nov 2025 22:53:37 GMT  
		Size: 5.2 MB (5213309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cb0310ebf1dc678d55d46a6bae898cec8a1e864c774a75c583345dc998403f3`  
		Last Modified: Sat, 08 Nov 2025 22:53:38 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:48d1b8da3a890b3b75b2b49393ceec1344ca1e2038b3e7fd8730b1e2676576ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.6 MB (202605902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22904cf91a921aefe6fc222fc1e73e7fd066fb905e68020ea4aa7b4020ced1b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 21:50:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:50:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:50:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:50:52 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 21:50:52 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:59:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 21:59:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 21:59:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:59:36 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:59:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cf4e8b84d3ef0d8674350cf270e37134e319d3eeaa20958d07a8901e83de35`  
		Last Modified: Sat, 08 Nov 2025 21:52:16 GMT  
		Size: 91.6 MB (91610755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c45efc3fb0cddfdb78b6e959b66737d7416d440b84ac1959d23d2eb0912d9c0`  
		Last Modified: Sat, 08 Nov 2025 22:00:36 GMT  
		Size: 77.4 MB (77395457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae869b6a58e766e040fe0c4cc8b24f1160d9590d934f74d8499055092b233727`  
		Last Modified: Sat, 08 Nov 2025 22:00:23 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6173ca1cbdd7f39f9d8cab439620952d591c758712c68abbcc51cb6eac869b47`  
		Last Modified: Sat, 08 Nov 2025 22:00:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3049ee6ec57ca3d95d0521d9549bb45b22da824b94b2195ce57b301953997dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e2a1f8533a70456cb71591a1589ecb3363116060c0a879a864a3c663864d3b`

```dockerfile
```

-	Layers:
	-	`sha256:04ff62c1ff6317e526a74fba9ece687ae2e6127ae97fd74b4d975d4287a5815c`  
		Last Modified: Sat, 08 Nov 2025 22:53:43 GMT  
		Size: 5.2 MB (5213200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36c880c1da3132b2948882ac183b30fee364440f4c750e5ca2e29542a3a0c9b8`  
		Last Modified: Sat, 08 Nov 2025 22:53:44 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:9c3a10b3a1822a4b5de7d33abb7528e173bc11f169c3cce9f4e82e8920e48578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189910643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e7758e4bd9a01efce276b2e39cbef3d9166708b2ac7034d0c7d1fc85ad2e73`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Mon, 10 Nov 2025 04:37:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 04:37:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 10 Nov 2025 04:37:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 04:37:43 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 10 Nov 2025 04:37:43 GMT
WORKDIR /tmp
# Mon, 10 Nov 2025 04:59:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 10 Nov 2025 04:59:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 10 Nov 2025 04:59:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 10 Nov 2025 04:59:39 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 10 Nov 2025 04:59:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bdf934bab212db989f237b784a2a17e7c8de762196739b48dc1cdde3c370ef`  
		Last Modified: Mon, 10 Nov 2025 04:43:23 GMT  
		Size: 90.8 MB (90752912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75feb09a560d47a7635e68ec0d3466875a2af7812a3f2e0b31e88461f79bdfb2`  
		Last Modified: Mon, 10 Nov 2025 05:03:24 GMT  
		Size: 70.9 MB (70880901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30712a6276ed21055e0e2c2dc8315540f2c575b8f658300be9d5f9a86607d0a4`  
		Last Modified: Mon, 10 Nov 2025 05:03:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d268a4c7f16bdf073478c290ade4c20ddc5d351f71283041ad83cbcfae86163f`  
		Last Modified: Mon, 10 Nov 2025 05:03:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6c5279f6c4d95db3f880f8c44b528f53dd1d6c17a6666c8780eed34ea6a7890b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bf9f793e7d79d5c3ff0d85eca7ce5ab757542d3e621fae8cdf33a37d7bceaa`

```dockerfile
```

-	Layers:
	-	`sha256:c986a33fba6dfe97a9697c6854b7d2b6d28578c8952a07d7d7c9a277cad46e32`  
		Last Modified: Mon, 10 Nov 2025 07:38:10 GMT  
		Size: 5.2 MB (5196992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f419a37463157579915342e7bd0a142796a482b05bbd893cf55890308c96bd6c`  
		Last Modified: Mon, 10 Nov 2025 07:38:10 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:4dd8acaac03661ad923da6947ef5eb81db0ba30ed2cbbd262f88b8dae04f22c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191002861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e853cedcae4d8bbd88c1a4857b14af0b68658d3731a28ad326c23faa764930b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 20:40:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 20:40:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 20:40:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 20:40:12 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 20:40:12 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 20:45:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 20:45:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 20:45:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 20:45:35 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 20:45:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0875292777271dfec52272a481583511bcd8559433138dbc7ada6556390ae03`  
		Last Modified: Sat, 08 Nov 2025 20:41:27 GMT  
		Size: 88.2 MB (88210682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f0e9cf67b770b66ce77b53bbcdae8cdaa6941f43a2462dc81b1af4a4ebe06f`  
		Last Modified: Sat, 08 Nov 2025 20:46:09 GMT  
		Size: 73.0 MB (72953746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be550cda015c35fb40fd4a4cb7fac2a04a0d65c6e8b1e6e65d853070c482b9af`  
		Last Modified: Sat, 08 Nov 2025 20:46:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b473d6b3a70d32cd684783e9e056f266467335d31893ffa33e88e88c70f60240`  
		Last Modified: Sat, 08 Nov 2025 20:46:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:40a904c678f8d3ad5732218f396e18443f0f950bceb37b83a05bf6b7ff85055b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf8925d555936027e4a35fb4ddcfa30a5af4fa99fc65d5a0778070a7a01a7fd`

```dockerfile
```

-	Layers:
	-	`sha256:e8eb8d1e7c901a4673dce18dd568494bcaf7c8b6a37665a85c8450b712eeee42`  
		Last Modified: Sat, 08 Nov 2025 22:53:52 GMT  
		Size: 5.2 MB (5205991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:261bc77959396315887ab5ec48db881299e164fe6325f973836204a7dc10cce4`  
		Last Modified: Sat, 08 Nov 2025 22:53:52 GMT  
		Size: 16.5 KB (16492 bytes)  
		MIME: application/vnd.in-toto+json
