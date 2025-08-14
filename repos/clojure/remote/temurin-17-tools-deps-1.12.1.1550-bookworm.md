## `clojure:temurin-17-tools-deps-1.12.1.1550-bookworm`

```console
$ docker pull clojure@sha256:0957f46cc7eea78859d225aafc56cb114c124ab644e71d24f4084834ace737e0
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

### `clojure:temurin-17-tools-deps-1.12.1.1550-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:35e09013be8303f5f57a99660a8e5a3d23cb318ff6be484790668b0f923b0081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274182604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f03aadb6150ee49db16d08b3190de63c6ad28af8da5231f397328959b133ec7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ecab08e87d508ee2f55130945a58daf4576b6dec22af5188ed2a1588facf49`  
		Last Modified: Wed, 13 Aug 2025 06:49:10 GMT  
		Size: 144.7 MB (144693300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d639aacb56573140686be135a5f198f78711091ee3703347e7c4e61feeabe655`  
		Last Modified: Tue, 12 Aug 2025 21:37:07 GMT  
		Size: 81.0 MB (80993751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c407486d401d5853d64e62ec5ddcbbfe4dd59ccd98623e89ab7aa9057d749c`  
		Last Modified: Tue, 12 Aug 2025 21:36:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a257f371cc0f26de79fa69fab16800f1932ae69ff3d73857ad842c0845335286`  
		Last Modified: Tue, 12 Aug 2025 21:36:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e306080612a4bdfa0c8b6b7e814d22568df2f1d3f6a38e1e57954e4ab2ce957f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7384088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb315c11042743199ab8234c1649bb3502961e1f3dfeb751b9f0d6f9b1beb76a`

```dockerfile
```

-	Layers:
	-	`sha256:8a12d7e2ce71cd5c90b88d5041d350e2ad22d35a04b4cd350f96edbc74cc3f46`  
		Last Modified: Wed, 13 Aug 2025 00:36:45 GMT  
		Size: 7.4 MB (7368268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5bf9ecca0bac06d25e7dcf6a1c3491bb9dfd46aaba311aaeee1a8753dc722e2`  
		Last Modified: Wed, 13 Aug 2025 00:36:46 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1550-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:503716872254aeb2f04390fd91c5705fed32c3814428a5ae185e37ad5058f89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272754010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88798097838574a79f92a66a75bdda02dacf810ac091b5f3e14b4e61bde38026`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2da76fc655def4e6c69dfbab2bbf51ab3a836e8d3cebd5ca3e88110893fb90`  
		Last Modified: Thu, 14 Aug 2025 07:30:15 GMT  
		Size: 143.5 MB (143542152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0f8c7ed16fe41b1efbaadf5d6f462a28a45dda5d59c0c37cab5c1b8422d0d1`  
		Last Modified: Thu, 14 Aug 2025 07:30:12 GMT  
		Size: 80.9 MB (80868369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef20491fa1a62ff1b331d4275fb919ba4144c92f6b8ea4aefbac8e35b0dd298`  
		Last Modified: Wed, 13 Aug 2025 14:26:42 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f328135c02f663040fa4758855aaba52245799db5743d40887a74ff26c1f1f1e`  
		Last Modified: Wed, 13 Aug 2025 14:26:42 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2357e3dc5be4d2799f7d01471aa176c31a14be350e44092444589956843ff82e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7389969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1067673c9653fcc040eab86418d497a2a846d0550a3f0da7794a717cc5f5199e`

```dockerfile
```

-	Layers:
	-	`sha256:e7601180bb4d40980cef43d1371161efe6cad8511c63557a267bf23c8f3d5ca3`  
		Last Modified: Wed, 13 Aug 2025 15:36:58 GMT  
		Size: 7.4 MB (7374031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca71b61475c63483ff75c46ef03d5390079762fce5ba0b92fa42ddb821ec6d17`  
		Last Modified: Wed, 13 Aug 2025 15:36:59 GMT  
		Size: 15.9 KB (15938 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1550-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:695a3aa40d93dd29b71adb24370c035ed32d95e9ed8f279d701ab4817449246d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.5 MB (283534011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76d955b5fde1a7815242ef57e9a098380a02ab8d4d30b4435a3806b99b22e16`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338f3cf2e89aa00d3573330c028d5fdd8457981c7a4e4125b42fd288974e55a4`  
		Last Modified: Wed, 13 Aug 2025 19:46:41 GMT  
		Size: 144.4 MB (144372823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e4f305441e5cd134223e62e74f2aa7935fa81b0e77b6126824e796b0367d83`  
		Last Modified: Wed, 13 Aug 2025 19:55:06 GMT  
		Size: 86.8 MB (86822068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a066ba578b251272e02dd87fe538e925a661caa4f5c887514034fce1c9faec`  
		Last Modified: Wed, 13 Aug 2025 19:55:33 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fa3840e030e6b29ce9c9bd813cb94d16b5e935ff8cd54a6adc691f70b2dad6`  
		Last Modified: Wed, 13 Aug 2025 19:55:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a6d5a4e1ce2fdb1ee53db098eec1287c7d3f1aa7a0212898084c027a01ead474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7389341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9ec5517ef7d7bd26fd94ae25ad9fdd8c5d87762c374fadebe04a3cb1f1248e`

```dockerfile
```

-	Layers:
	-	`sha256:8eeec8ce38095f689a566f721060672b4dd42b01f7c7413f3880b5a9ba33db02`  
		Last Modified: Wed, 13 Aug 2025 21:36:28 GMT  
		Size: 7.4 MB (7373472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:384816e013ecfb2a61d38207af4719ab5980108c5fa7bfc948d80939a1891150`  
		Last Modified: Wed, 13 Aug 2025 21:36:29 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1550-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:b27ad86b3812c00b569e364b271ed5c55af21adf5725aead9694347f67ff1263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.7 MB (261678440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28bbba6f00c6368da9ae8299f8e68ecdefa16c651d7a09b338a142ba35dd0d8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a098e95cdf3a56fca7c64b00df5d9e7ab42b0c57fa2604af9c414cec99ccdc`  
		Last Modified: Wed, 13 Aug 2025 07:12:12 GMT  
		Size: 134.7 MB (134724396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0895d91e24801f772b155a0487d8286b7b51649a43cc284f2b337fa30cc2ff3f`  
		Last Modified: Wed, 13 Aug 2025 07:16:39 GMT  
		Size: 79.8 MB (79803137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2988552deee22c709f86df20ce7e9ad70de0514cdef7721ebbdbbe7772c980a8`  
		Last Modified: Thu, 14 Aug 2025 18:19:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5643ed32fe7ffc657e26614d3f38fe73d96d342ecf79df02a2a60654936ba1`  
		Last Modified: Thu, 14 Aug 2025 18:35:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3ed521ca2ed03e4a6bd7a3b02d6b9f250996c652637d24de0d3b6c9e5babec4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7375406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9756ef4e1bf658a52c9b555514007935211da552fb5b069b5d69da33e3ce3aad`

```dockerfile
```

-	Layers:
	-	`sha256:b9e28e967ff04a5bee8484ab3d3814218aa11658846723528fb3b100fb77529a`  
		Last Modified: Wed, 13 Aug 2025 09:36:12 GMT  
		Size: 7.4 MB (7359587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69009e9821bce2c7c3d98fc0e634b75c98776dcd474e6bbd5f58823321e63757`  
		Last Modified: Wed, 13 Aug 2025 09:36:13 GMT  
		Size: 15.8 KB (15819 bytes)  
		MIME: application/vnd.in-toto+json
