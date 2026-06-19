## `clojure:tools-deps-trixie`

```console
$ docker pull clojure@sha256:a7b2e841c28ee3c45e6ac0b482185d23bdd57482b773fd47b241cb09af345246
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

### `clojure:tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:eaf13349338a8127013b492693c78f8bd1a780fe83449e4d97c499324819bbd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.4 MB (224411981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e9f0cd0d853df1e2550a04059545a81f8ae688abd6b53e9b1fff68bc93b532`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:21:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:21:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:21:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:21:01 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:21:01 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:21:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:21:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:21:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:21:17 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:21:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00e19d19f2e6adeb7630db13eeba1ed2d0ff569297236d4377e07a25cef8b12`  
		Last Modified: Fri, 19 Jun 2026 02:21:38 GMT  
		Size: 92.6 MB (92574566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f741a16f6fffe0f4f595a03751f01d5c9f71393230c3f7a21c10e70d00dde264`  
		Last Modified: Fri, 19 Jun 2026 02:21:38 GMT  
		Size: 82.5 MB (82519254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55183c349ffafaedd12d17b5b9d5ae72f0c4eb6be3317cea976580d16260c41`  
		Last Modified: Fri, 19 Jun 2026 02:21:34 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138ef67b9d2469f161b5bc1274555118c655267f578fdf3fd8d57f5968bed0f2`  
		Last Modified: Fri, 19 Jun 2026 02:21:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:88bc06a166602587d31324615b49d7d4c386fc4a8be4b071ab7d4e1b901a4af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7453402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678e033fc939a3d9740a29cb98cd8ab0a04f8a9d5a6a2241f836ed693de81d9b`

```dockerfile
```

-	Layers:
	-	`sha256:fb52447938f8583b71ce5eb0eca8ea6ff418940d541cd1e91d2c2011f10eeaa6`  
		Last Modified: Fri, 19 Jun 2026 02:21:35 GMT  
		Size: 7.4 MB (7436833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df14d2a65f59f2a3752f351049e93e87a87fc355191c5fd1cae98599f7971bf8`  
		Last Modified: Fri, 19 Jun 2026 02:21:34 GMT  
		Size: 16.6 KB (16569 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d420cd4a76bb60c764dbce0327069c262b4ab03c8cfe815c961e20cad64404ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.6 MB (223559872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b856be14749b9d91d6921591b2ae68ae0d4578bde2175e79ee9347be8ecd6c5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:20:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:20:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:20:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:20:51 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:20:51 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:21:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:21:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:21:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:21:08 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:21:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd6831257ebca43ed98b0bc5312b3224ffc537289690c095bc6bfa31ab52d14`  
		Last Modified: Fri, 19 Jun 2026 02:21:24 GMT  
		Size: 91.5 MB (91542251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c1b60b441cbd7157fa7d76f2a9fdcf894cb945ed46c4c35c068f2a06816d46`  
		Last Modified: Fri, 19 Jun 2026 02:21:29 GMT  
		Size: 82.3 MB (82338408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083b43a8ed7dca6c13a1fe2f51c656b21799800b5da498c8af111acd7a572e97`  
		Last Modified: Fri, 19 Jun 2026 02:21:27 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0cc32078e459b774c045881a94038fb8b1412f7f645117b02e281c69cf3383`  
		Last Modified: Fri, 19 Jun 2026 02:21:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:69a3009229121f85f89d815e76974d64b8a8542c2c28e073dabb120b482d095e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7459958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf6690dccaac2af9913c2ec9e8cdbc33eefc7eba84a3bd45cb3a13e345faf9d`

```dockerfile
```

-	Layers:
	-	`sha256:d6b6b59ed3ad47a118fa815b0d155588aefa25e26367807f831c2ed2fbfcd7c2`  
		Last Modified: Fri, 19 Jun 2026 02:21:27 GMT  
		Size: 7.4 MB (7443247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f82d68bee4db0bea8f75a582a8e45f36ad2ba58e6ec878b036e2f8e73c2fee1b`  
		Last Modified: Fri, 19 Jun 2026 02:21:27 GMT  
		Size: 16.7 KB (16711 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:1a5748ce25d787f5a4a65cc9deba9c0ec8e13398f0509efe4cb0b6c06796295c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232991829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f0ea65af34064c0018a5e87f16b2b601d3effff7ebb91241b7df2f51c91498`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Wed, 17 Jun 2026 00:11:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:11:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:11:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:11:00 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 17 Jun 2026 00:11:00 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:57:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:57:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:57:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:57:24 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:57:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc6e91230e9fcb06c48eef2eae63696efc222edfdf9387e828c0e8a79c0a8c9`  
		Last Modified: Wed, 17 Jun 2026 00:14:23 GMT  
		Size: 91.9 MB (91914030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fd2ce2c5230c73f60af8ac611358a33b4fe74d9ef1830889699154ebb9fcbe`  
		Last Modified: Fri, 19 Jun 2026 02:58:08 GMT  
		Size: 87.9 MB (87938816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883e6b6818e19c2852900cb591fc9c74724fab16868f9d3583ea685c17a0343a`  
		Last Modified: Fri, 19 Jun 2026 02:58:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581295f39de808b033d973be2852580bf9d22141d3ee406fbb78acb59eb07f91`  
		Last Modified: Fri, 19 Jun 2026 02:58:06 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f4936f6935d3d90f841f4c2c212b9a63fde929214af24ae30bcbb2d9b8edc872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d90e8320d1bfa507abc41f764e40f909bd32a21b69edee5d94d9cd3db923af9`

```dockerfile
```

-	Layers:
	-	`sha256:3980d91e1cd0f1fc9218d5bb37c2cf3f8853131a01bf6c81bad3efb6d7f047b2`  
		Last Modified: Fri, 19 Jun 2026 02:58:07 GMT  
		Size: 7.4 MB (7424578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:751e6219fea6f9cc2f7ecfc3cb382ccd3003850f7eb3e208611e78b7a4be50f8`  
		Last Modified: Fri, 19 Jun 2026 02:58:06 GMT  
		Size: 16.6 KB (16628 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:dbaa2c080bd9c7623370ba6527daf4cc5a602f048e4cf2831bec9f2f8a4b36f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.3 MB (221308432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ff2df44e9c40ae464cbcc5f5c2785838e77b61ae5514fb590bbae49dd91254`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:21:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:21:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:21:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:21:14 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:21:14 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:22:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:22:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:22:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:22:34 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:22:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61adec2576be28516842462114579539904738dc16abf2591b21445e78b04e67`  
		Last Modified: Fri, 19 Jun 2026 02:22:47 GMT  
		Size: 88.4 MB (88420353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33b4780b95a4e3e93b5e3bf9762058a0b36c6382ac0de39b296e9b49b522090`  
		Last Modified: Fri, 19 Jun 2026 02:23:00 GMT  
		Size: 83.5 MB (83501142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fddc6852125ff0ed2545c9d42f711c29b6f71dfb3d06a85a790eec2dfb6e54`  
		Last Modified: Fri, 19 Jun 2026 02:22:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8ed8140484898c57c6ffa801b4a35173e0c61081e4f212a85286ba06d3c0fe`  
		Last Modified: Fri, 19 Jun 2026 02:22:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0e3ffd07bef4d331afa235123c3fed754e05f364a7ece1f5c0dd26756cbe48ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7032215eb28b0c142ced7f7864653455490182aa5bc27f3fc4fc963a0dbbbde3`

```dockerfile
```

-	Layers:
	-	`sha256:b9f4a555297fc2f44e28735fabb8933883134909e225c248ada398387865c52b`  
		Last Modified: Fri, 19 Jun 2026 02:22:59 GMT  
		Size: 7.4 MB (7417317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd8d5c58d2307ec8cc0c1816e8d01f40ae8677481e5d0be55d9ede3d1f2283bd`  
		Last Modified: Fri, 19 Jun 2026 02:22:59 GMT  
		Size: 16.6 KB (16569 bytes)  
		MIME: application/vnd.in-toto+json
