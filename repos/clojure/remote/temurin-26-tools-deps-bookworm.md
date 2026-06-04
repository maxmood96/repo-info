## `clojure:temurin-26-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:4d62e3d8676bf3a57989c0a29d68fc092104618897c4da6a732ef6cbb605f34f
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

### `clojure:temurin-26-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:15ea6b162ac21c13503ee244274109f6a81f0117fed73f793c77ff966b968db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221145853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ef33212ccbd2d6a32be074249df1d2c7d877f41d26da4b159a9af785f68d66`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:47:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:47:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:47:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:47:39 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:47:39 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:47:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:47:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:47:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:47:54 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:47:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5fd384b8216fc2fcbdb9d9283b350d593124e9b713a6712447e5d23b2090b5`  
		Last Modified: Thu, 04 Jun 2026 17:48:15 GMT  
		Size: 94.5 MB (94524311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320bdfab2085de7f742f2a98cd040f8b4493aaf11e725efad2edb060d713a059`  
		Last Modified: Thu, 04 Jun 2026 17:48:15 GMT  
		Size: 78.1 MB (78125067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d86eb0b38f34b04cb731325f8e01133bf83e6439477cbbc29d517c588dc219`  
		Last Modified: Thu, 04 Jun 2026 17:48:12 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880a1345d008f7bd8cce41c0acc6ecece1106fc2baf3068e572284d3f7c93bd9`  
		Last Modified: Thu, 04 Jun 2026 17:48:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7f3609655f12094a6647f9ab625215bd448538af0c530b28d07cda36167d59f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7358299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09805f5405e7425f3ad00e8994a488f17d9268f46f81f68e72ed0f64c331aad7`

```dockerfile
```

-	Layers:
	-	`sha256:d53fe2c5877c47ba731d028457383129c10dcda80e1b4a5497af34ae63109ca7`  
		Last Modified: Thu, 04 Jun 2026 17:48:12 GMT  
		Size: 7.3 MB (7341691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e04a02419f67b5b7efc3ae8f96954bc5a2811699bab1303badc6bb67984f05ec`  
		Last Modified: Thu, 04 Jun 2026 17:48:12 GMT  
		Size: 16.6 KB (16608 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c3da580b0bbabeafd636709e632cde4bc1f50d0bfd0d8409601f39fc46b2a26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (220010334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96cdd17ea97fb5730cf0ef404d8ce3d0942480d93e0b00d7d257a0177a1d8f99`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:47:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:47:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:47:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:47:30 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:47:30 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:47:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:47:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:47:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:47:45 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:47:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5313a10cfa083b51f7251d4ad5a1548184c5be193dd4c1c4fa00efa86d3e29ed`  
		Last Modified: Thu, 04 Jun 2026 17:48:07 GMT  
		Size: 93.5 MB (93504349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5fcb59280ca8b7bc9a0813053e936b46aaa930cec5cc4ef75c57e63ea1bd37`  
		Last Modified: Thu, 04 Jun 2026 17:48:06 GMT  
		Size: 78.1 MB (78125510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bab753d650e30a1f4cfbaf5dfe6a1a00dc3fac87fbe4e3fd44402c48c3caad`  
		Last Modified: Thu, 04 Jun 2026 17:48:03 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7852640db1d3c7b59fbf4b9fab3efea2d57f1ed63266052f77a2a46dacb6dd41`  
		Last Modified: Thu, 04 Jun 2026 17:48:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b2c2fd35ffb7d66eab66dc3b61c2226ab96d15128ce1cbc0667c26c9fa215c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7364225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91fd8ca7f0806473d118fec45e696e3cf2719b7bbf415af596184a5ad3c7c917`

```dockerfile
```

-	Layers:
	-	`sha256:78f4c499b636ac484017666856dc3992b9879025a28e89720b7d52b2f20dd17c`  
		Last Modified: Thu, 04 Jun 2026 17:48:04 GMT  
		Size: 7.3 MB (7347475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb85270b6bc58c6d50896fed19eb9a7e7d3095dab3e7768aeaf0ac1093d3a8e3`  
		Last Modified: Thu, 04 Jun 2026 17:48:03 GMT  
		Size: 16.8 KB (16750 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:fec805bcce2766f3bff3b32a6e5c3cbf02a6177ebfd775bba8bcd9ca32002176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230202622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5531af9950883d39c201984c86299b06afb4041102f1933a4bd47dff75c48f7b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 18:08:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 18:08:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 18:08:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 18:08:45 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 18:08:46 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 18:09:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 18:09:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 18:09:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 18:09:26 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 18:09:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e94f485920d344090fcca9ea01192b3c70780e200856dd0a864b590a8813b4`  
		Last Modified: Thu, 04 Jun 2026 18:10:08 GMT  
		Size: 93.9 MB (93902081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86ae4124a27c44160f05158aad314ec8f7b7d251b06c795671821096e3a8296`  
		Last Modified: Thu, 04 Jun 2026 18:10:08 GMT  
		Size: 84.0 MB (83959297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fef3639ddbde22ab2db1a6e2c4b5423130a53cffb4078467594cd18ade64471`  
		Last Modified: Thu, 04 Jun 2026 18:10:04 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9be047bfbe0e27bc3c93381fc277fd0bf69c89808148af794521df4eca732dc`  
		Last Modified: Thu, 04 Jun 2026 18:10:04 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:aa690b052bea89c18fc5299042762f54f2014e5ba3b4d685167a961274c8376f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7347524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33acb34c62eda15fe79e20c68afe731ec1075b676c9de2be95577c741e1032d1`

```dockerfile
```

-	Layers:
	-	`sha256:ee3493bcccca82e2c39a2c0dbfbfa9348422bae571a62eb35926b36a0cdf5023`  
		Last Modified: Thu, 04 Jun 2026 18:10:04 GMT  
		Size: 7.3 MB (7330855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4155b564021a1da08f0791498fa208cc8d379707cb20f2bbd7abffa6bfca10a9`  
		Last Modified: Thu, 04 Jun 2026 18:10:04 GMT  
		Size: 16.7 KB (16669 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:a44930002d61e0705d241371781faa6093470decf7236b00bdbfacc24154a8ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.6 MB (214620073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3390114b468baeb5887d03726fc44c86307ac66b4034746abcee20a73c965d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:46:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:46:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:46:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:46:40 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:46:40 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:46:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:46:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:46:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:46:55 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:46:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c7481a24cbd89386c2c2d1365479510816dab5bce759a0e403e214360209be`  
		Last Modified: Thu, 04 Jun 2026 17:47:26 GMT  
		Size: 90.5 MB (90536968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6121555d34adf565936a13f09378eb9fb74db4b035b5d244baf246351b5dc0f0`  
		Last Modified: Thu, 04 Jun 2026 17:47:26 GMT  
		Size: 76.9 MB (76926470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3c78722ced5ce174b224714325e3a716ab6615b74044d26e922bb8ec7f0014`  
		Last Modified: Thu, 04 Jun 2026 17:47:24 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d18d6a81fc9f57115f79af670e905c2099d5853d45af1e9d4c638f8227f73dbc`  
		Last Modified: Thu, 04 Jun 2026 17:47:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d1749199e55fc2cd3240df1d06b1ffc1490f6062565e61bb9beefd9cd41739cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7334805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039385bdfd018f70885e6de98abce241a43fa0da5d4c43649e3749332568fb7a`

```dockerfile
```

-	Layers:
	-	`sha256:588b315b7e3b2a51a21f3c2cce566b8f4c139e4d0c1609aafea9c3459d02265e`  
		Last Modified: Thu, 04 Jun 2026 17:47:24 GMT  
		Size: 7.3 MB (7318196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e62775141b019dce915767f2a37510896b00836a8572cf75472fa9f47fb8468`  
		Last Modified: Thu, 04 Jun 2026 17:47:25 GMT  
		Size: 16.6 KB (16609 bytes)  
		MIME: application/vnd.in-toto+json
