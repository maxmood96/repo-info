## `clojure:temurin-26-bookworm-slim`

```console
$ docker pull clojure@sha256:0ad5101e7796e6923932a3e38e7fea42f7a2b02c7fdedcfba90cc8bd259df6ff
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

### `clojure:temurin-26-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4f731d12db77ecab25810b78066c87b556980b8679a5c53d58d62a58b57f5542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 MB (189405559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d10e2f5e38a6a112f9cb261832e073ee10b6c5328ebc57a1ffc5c19ea9e3140`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:21:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:21:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:21:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:21:50 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:21:50 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:22:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:22:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:22:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:22:03 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:22:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41b242d7b3a1f205f106b588d82c399f56d0a35ecef25aa9a611ec67917c66b`  
		Last Modified: Fri, 19 Jun 2026 02:22:24 GMT  
		Size: 94.5 MB (94524377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0200d4e56601dd360df60193337386c2494abe0d55c43ab649f2e58ce3aac3`  
		Last Modified: Fri, 19 Jun 2026 02:22:23 GMT  
		Size: 66.6 MB (66642516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbef80682190c5f7e97a16ae3cf04c96117b8512024914cfbde73c07c8887bf`  
		Last Modified: Fri, 19 Jun 2026 02:22:20 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1c49213cd9b0a9f6904146b0552735278fc99cde9e344bd545531fbb450de8`  
		Last Modified: Fri, 19 Jun 2026 02:22:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c30a9c55b8c840291aa39326b54a3572cd53f5ec3100c45cd168209d0efcebb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf807c520cfe75ff63ccd5ce82bfa8615de39e7f5d9f2b62d29766d220b5f3b`

```dockerfile
```

-	Layers:
	-	`sha256:dd52cd39c36ebf4f3b4830553a52d1d8e8967195c5bcd88eedaab893dfeba4f9`  
		Last Modified: Fri, 19 Jun 2026 02:22:20 GMT  
		Size: 5.1 MB (5078890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be41d1a706885dbe4e385c516a1c5266bc3a74ada198452a769cbf95fe8ac2fd`  
		Last Modified: Fri, 19 Jun 2026 02:22:20 GMT  
		Size: 16.0 KB (15982 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:094ba4c1ca4c15a18c3dc06169a819584b181a624cf81dbf61527c9369a22841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 MB (188270880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d784e04109e8e331bba07dea9d5875ce9aee9efd47ed991abe3896415799d526`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:22:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:22:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:22:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:22:03 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:22:04 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:22:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:22:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:22:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:22:17 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:22:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84798b4455ef4fcda64d47f87bacd274a09b46719cc49cedc35b036ed96c2c1`  
		Last Modified: Fri, 19 Jun 2026 02:22:39 GMT  
		Size: 93.5 MB (93504353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66c26c4651290a20085b7ca46027552d3e1b922bb15074d5634df6e7e3277ed`  
		Last Modified: Fri, 19 Jun 2026 02:22:38 GMT  
		Size: 66.6 MB (66643178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1f833f897113adf3646f63dfe5dec52629b14fdc90492e023b8d73ae8f4ad1`  
		Last Modified: Fri, 19 Jun 2026 02:22:35 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b3ccdf36b74f57a5b6ef45252490e4d5aee39694d1d848d2fae918dce87242`  
		Last Modified: Fri, 19 Jun 2026 02:22:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:573f97e6ef538c30b432e20aa374809dc1d59d6a44e28d1957cf2016374e724c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07424729ee43883ca1944c5910e6318105c6d57409cccfd4dbcebb5d3c74a145`

```dockerfile
```

-	Layers:
	-	`sha256:07e8d71557d89bd6107577ae9f568d18a323bdd5d52724be49ab33752ab8b71d`  
		Last Modified: Fri, 19 Jun 2026 02:22:36 GMT  
		Size: 5.1 MB (5084648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9249577433c1dce947a40aaad2b9c36a06ae0fd8c65ee3362764ea5faa17eaa9`  
		Last Modified: Fri, 19 Jun 2026 02:22:35 GMT  
		Size: 16.1 KB (16101 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:eb78d16b427fd0451b7fbd9c56af90f74a46d658057268d7e727ea6d497bf54b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198461296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb5ecd9cbac51729f5f7f85e01c0f1cf06f74f35df6713a24803449ae524f09b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Wed, 17 Jun 2026 00:10:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:10:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:10:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:10:18 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 17 Jun 2026 00:10:18 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 03:00:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 03:00:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 03:00:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 03:00:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 03:00:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f29b00e9bc0b9af92e1b64e13edf9ecde1571af48c5d8d0fce068fb62ea3514`  
		Last Modified: Wed, 17 Jun 2026 00:13:19 GMT  
		Size: 93.9 MB (93902081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed08e2bae7d64244f7ca140327e02f1900cbf17e7ae9cfe6f3a602b4dba3c77d`  
		Last Modified: Fri, 19 Jun 2026 03:00:58 GMT  
		Size: 72.5 MB (72476233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3853afc64ac098a49454f9bfa5cbafbfc6152cdfbdea9912c1233ec1aba3b9d5`  
		Last Modified: Fri, 19 Jun 2026 03:00:57 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b810f7f241f7891842f13067f6a91e0eb15c5e00c219dd5f5c713dbefa18b91`  
		Last Modified: Fri, 19 Jun 2026 03:00:56 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b41e8402ac754efb90d2305cd74455e0f250d683a4fa13c475c7f694495f2aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5084014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a06e67759dab66f884756c9ab72f60c7489aa3b4f617a9a5322ee49d18bd6b3`

```dockerfile
```

-	Layers:
	-	`sha256:1dd32dcf94a3ed28da62c5460e64fce3e9a41edddfce650ba5fe6d5bf71f0f26`  
		Last Modified: Fri, 19 Jun 2026 03:00:56 GMT  
		Size: 5.1 MB (5067984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7eb8964dc5b3490056c358769448650eee63574f4359879624bea7c476b44cc0`  
		Last Modified: Fri, 19 Jun 2026 03:00:56 GMT  
		Size: 16.0 KB (16030 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:561e84368748078612ebde78836c0e3f499c5369a06fea8a0cbed63f377e4a1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.9 MB (182883593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bcd230768a748bf861dededa89a79d988a233487163999f284f7d5c8a2b056c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:41:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:41:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:41:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:41:38 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Tue, 16 Jun 2026 23:41:38 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:24:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:24:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:24:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:24:23 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:24:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf175e00b02ff27e4e23a84cea45ce5d6e96921b94bae771e56baf106f5ca05d`  
		Last Modified: Tue, 16 Jun 2026 23:43:12 GMT  
		Size: 90.5 MB (90536986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a02278344e3ae963ee27ae0fa98d25c697da9b7a5c3d68ef0e55a8b60001621`  
		Last Modified: Fri, 19 Jun 2026 02:24:46 GMT  
		Size: 65.5 MB (65452059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8983bf23a270885ecbfe5052e5a93bfcfe134f1c86589ac89640dbdfddf636`  
		Last Modified: Fri, 19 Jun 2026 02:24:45 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea67fa011f886fe2fcec3d7871f3c0592613e1dfd8d7a357bfbee4b2dd2da97f`  
		Last Modified: Fri, 19 Jun 2026 02:24:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2d8f45163ad8299a3ed0ea46870471108f0982c661d5f6c7ff25fe27f05fb6b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5071380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33dac28fd8d248b4928c34cd81b4e424c911edff5e3dff603a70cb24fc6383fb`

```dockerfile
```

-	Layers:
	-	`sha256:75fac332319857cb9cb7dac338f8b41bf2e8d72344ebe4a9e03f309d9194e395`  
		Last Modified: Fri, 19 Jun 2026 02:24:45 GMT  
		Size: 5.1 MB (5055397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2132e1b5e39b63e74de1a77bfdfeb01093bf8191fad5899f11ec666d69e669fc`  
		Last Modified: Fri, 19 Jun 2026 02:24:45 GMT  
		Size: 16.0 KB (15983 bytes)  
		MIME: application/vnd.in-toto+json
