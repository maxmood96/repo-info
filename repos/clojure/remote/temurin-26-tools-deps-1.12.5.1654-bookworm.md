## `clojure:temurin-26-tools-deps-1.12.5.1654-bookworm`

```console
$ docker pull clojure@sha256:9debba1102e4f94cd69f79975fdabadd8606aa6adeaed1158bf17a7df9ce6d3c
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

### `clojure:temurin-26-tools-deps-1.12.5.1654-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:3b0eadf890b2b85b01489d116ec81f7e821c1152d817fb538102d4f4dc969553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.2 MB (221152809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5d32a321b5185181e958828650a24bdebbb9a87a234127ad8ec8ec0d734c1c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:21:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:21:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:21:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:21:54 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:21:54 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:22:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:22:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:22:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:22:08 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:22:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e33ef5925879f00c9f19dede1e8ba41e8b446b2f29023751ee4661b7a5242e0`  
		Last Modified: Thu, 11 Jun 2026 01:22:30 GMT  
		Size: 94.5 MB (94524364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b89c4031491841230c2516b2e064ed36dbae64aae49ac57c9cc1d2870a0e9f8`  
		Last Modified: Thu, 11 Jun 2026 01:22:31 GMT  
		Size: 78.1 MB (78125363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75cb6f3903b324caa6258a61f7c04b48e266ead7d768c240266564aea3a80a2`  
		Last Modified: Thu, 11 Jun 2026 01:22:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d04e3c643388411d52797c384bb1eaa11afbb9f9c8e585f22ff84ea5851552`  
		Last Modified: Thu, 11 Jun 2026 01:22:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8ce74063c353d4e75c4ed62a1603e9a712c730daa7e7325033226905ad3028ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7358318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7979f7b1f6480d4c19837c3a216b442afba5f7656b8202e95d915c6ca7bb06a7`

```dockerfile
```

-	Layers:
	-	`sha256:7ea904eb83d470b81ffd964a03940927e15ee8bec18923893c83b5cd31612a11`  
		Last Modified: Thu, 11 Jun 2026 01:22:27 GMT  
		Size: 7.3 MB (7341709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee666d664a6c244baea36734d81170bad1abed69bd9dabfb8e7213ffb528ddef`  
		Last Modified: Thu, 11 Jun 2026 01:22:26 GMT  
		Size: 16.6 KB (16609 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1654-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3d5741d23ea01f8cd0519624cd6dadaf1e4328f618aefc482fd41919ae727ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (220024174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5042442db661b1a355e0c0a4f49761bebaccb8944ec8239acc726e762120a849`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:26:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:26:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:26:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:26:19 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:26:19 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:26:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:26:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:26:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:26:32 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:26:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750786772ca2ccb838203dfa2fd668ba3d06c4db633eeb0f0321d2e02e3d6feb`  
		Last Modified: Thu, 11 Jun 2026 01:26:55 GMT  
		Size: 93.5 MB (93504348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db06e0750f48fdfc14a0c7ed5eab4eb37ee1ac1e97375cf7fc55a8fb7c9a3a63`  
		Last Modified: Thu, 11 Jun 2026 01:26:55 GMT  
		Size: 78.1 MB (78129770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45832af340b14486a2eddb50a3c7db4500b5fe46255451c94a7cf484e0fefeb`  
		Last Modified: Thu, 11 Jun 2026 01:26:51 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e569d8b5186845dd75404321ae7107288dbcc1efcea3284abafb362babc51a5`  
		Last Modified: Thu, 11 Jun 2026 01:26:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:89604c969184daf6eff3cd8d11211d95702113cb50a7c30091eb9f9178cb6d6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7364244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c248ececf8f72dbd669dfc5b8c67c621e3bd0a83e21a20a027332e628c2a233`

```dockerfile
```

-	Layers:
	-	`sha256:0f3142a9689102841e39d42b3ec26f507b4c8d9ccf9c37caeb2774a1ad567d09`  
		Last Modified: Thu, 11 Jun 2026 01:26:52 GMT  
		Size: 7.3 MB (7347493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:406282f95bc10e75caefcb4395d7abf98345164403e86db486829a9fb71d0654`  
		Last Modified: Thu, 11 Jun 2026 01:26:52 GMT  
		Size: 16.8 KB (16751 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1654-bookworm` - linux; ppc64le

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

### `clojure:temurin-26-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

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

### `clojure:temurin-26-tools-deps-1.12.5.1654-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:a5a2beb4eb0492a7ee7fe878ddce9118110850ef2bc88bcb2f9bfc0869219820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.6 MB (214628962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:161b7239a981fa6e6357a6b21a6b129a23f168eef901c9d110180eafd7ca6026`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 03:15:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:15:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:15:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:15:20 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 03:15:21 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:16:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 03:16:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 03:16:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:16:40 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:16:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9599dc914187bd0773e9a9bfca693b301ec556e0366d3639bd6b7023bafb8e5`  
		Last Modified: Thu, 11 Jun 2026 03:16:07 GMT  
		Size: 90.5 MB (90536968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a10346c89c9ed6fbe07b2cc2074d823effb736c8b332c0543a24acc02d46629`  
		Last Modified: Thu, 11 Jun 2026 03:17:06 GMT  
		Size: 76.9 MB (76929457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87cc7e51d978380c12f27404ac2d6eea446f21c38bd77fc84a9aa8bc0d0b2a0`  
		Last Modified: Thu, 11 Jun 2026 03:17:04 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc75299de3fc6bd09bf67bc38b12f1dcfd20b8206fbdda7a92489cdcea64ed7`  
		Last Modified: Thu, 11 Jun 2026 03:17:04 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8d854c3cb6737f292c2d2dd334687fefef156c17d97b6801a415ad33068d03aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7334823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0245263033f33c320fbd23da56374fa75c9859c2caa5df7644899240b15b1ee6`

```dockerfile
```

-	Layers:
	-	`sha256:754ba6ead2edc9cd2768b0f3a72152862dc891c5f088ec7ce2ee8933c4dc8cbc`  
		Last Modified: Thu, 11 Jun 2026 03:17:04 GMT  
		Size: 7.3 MB (7318214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d9763802e6c36a25340876c98b6a8a4ef77addc8623ceb8c20ddcd59953f2de`  
		Last Modified: Thu, 11 Jun 2026 03:17:04 GMT  
		Size: 16.6 KB (16609 bytes)  
		MIME: application/vnd.in-toto+json
