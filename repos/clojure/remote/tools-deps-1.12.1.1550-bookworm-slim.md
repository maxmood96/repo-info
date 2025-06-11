## `clojure:tools-deps-1.12.1.1550-bookworm-slim`

```console
$ docker pull clojure@sha256:715c9a75cbdf0e53f13c0af4d836a72f21a94bb6696c5fad597500ab17c6d867
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

### `clojure:tools-deps-1.12.1.1550-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3c17d8de7e3d140689eb0f1bbc6988284485c34cb6887ce701455c46cd83c44a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255395264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81c20f3a06c5a562f5f7ab480cdcbc9990cd4712a2279a566e5e35ec15b7996`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea0841ecb4003d4597efe5a0bedc6ba99c1d194cc4748fbd5ccea042f02cabf`  
		Last Modified: Wed, 11 Jun 2025 03:41:20 GMT  
		Size: 157.6 MB (157634498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b8249b00dce978c98c7d04df061208845e2fe11bb0d3abb776a96fea5bf8bc`  
		Last Modified: Tue, 10 Jun 2025 23:52:46 GMT  
		Size: 69.5 MB (69529594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cad78bb9468faef939bc932b338dfd5106cecc59fc848844639a14dbc11d595`  
		Last Modified: Tue, 10 Jun 2025 23:52:40 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5762cf8c3a3cddd3ebc71172abfde4aaf2ad45ab903ceacc4a48648017599e63`  
		Last Modified: Tue, 10 Jun 2025 23:52:40 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6a121e8a07463e8dcc2496d599fb41c9f5bdb2658caebca87c9d4a60f898f967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5130261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc6089ea1427dab2c0c90ebf0908d95a94aedcd1d1e3b2288da0a6739aeefea6`

```dockerfile
```

-	Layers:
	-	`sha256:39516686d2df83066c66ae94bd1fef0eea5437b2d4a1a88f47026e91dde04660`  
		Last Modified: Wed, 11 Jun 2025 03:38:18 GMT  
		Size: 5.1 MB (5113686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2840dbd42ea9d743011ee8a3554a6452609b6c3ee0fc700c2c57954de798eba6`  
		Last Modified: Wed, 11 Jun 2025 03:38:19 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.1.1550-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:38a66d335df7be3554df3a46757a4ca65c7fcac5ed542c013c71212eec38825e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253387006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51245b163aae234aed0ec7fccac0cc30e85211f5618962f2c8c91c251134ab85`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec03d7eeca89e0760e8dbc23abc005a69970b61d7619400463b7928ff3fe8a3`  
		Last Modified: Wed, 04 Jun 2025 17:10:52 GMT  
		Size: 155.9 MB (155928831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcf2e1809dd898f51c85947a926640f5072ec15e66381436dcc1a2ba4dc5c71`  
		Last Modified: Mon, 09 Jun 2025 17:53:13 GMT  
		Size: 69.4 MB (69391852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f518a34ecf152c8247624dc3ebb9e46af551334001455def14b06d2fc0ffe337`  
		Last Modified: Mon, 09 Jun 2025 17:52:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da160d4233b8a756f494920d167536700225e3fcd5d7d6b51c30bf4a96df593`  
		Last Modified: Mon, 09 Jun 2025 17:52:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:afb8cda7d76552d0fdbd56f305734e9287abc90c6d34eb9e2d7f8ac74213b8dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5136188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c4dd6fc9eeb06dc63a0f1282a7aea041082ba3f7bc41d9597bdf0adf5f5250`

```dockerfile
```

-	Layers:
	-	`sha256:c897fe5056b8c1809b20cd1f8ec6ecc781a4366cc20069623efbc94de5a312d5`  
		Last Modified: Mon, 09 Jun 2025 18:39:12 GMT  
		Size: 5.1 MB (5119471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77203406b9e78f1ec164820cfec25e98b7553ac4abe89cc751de04ade847fd38`  
		Last Modified: Mon, 09 Jun 2025 18:39:13 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.1.1550-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:c7dac1d6ab94bfc8b512a6829064845d19eaf5b03c621311ea74da17ef74587d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265218816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8911b05feb1bb6b6f5b7ba18d267a28d1903d408a938ec344251a4c90eab44aa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d05da02c9fa2302ce040ac6b740be17fb80e4f4da068aaee1ed947b3588ea4`  
		Last Modified: Tue, 10 Jun 2025 11:59:26 GMT  
		Size: 157.8 MB (157804869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fd969c4d62ea705c0105b64f85b1d5a32e277e26735ae8c8ef6cad9b513692`  
		Last Modified: Tue, 10 Jun 2025 11:59:40 GMT  
		Size: 75.3 MB (75345990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9ce1ca915818a55ade9f9ce9a30f659f9d25724a9338285ad14227f9ec4355`  
		Last Modified: Mon, 09 Jun 2025 18:13:37 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d1aa0dfaba9d5d407a7fc877cd972a31e5d3c969f9af778fda80a7439a6997`  
		Last Modified: Mon, 09 Jun 2025 18:13:37 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:37690f0ba53375e212a2228b1af167a78affdb8083d078d6e4d1daf1386bc1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7620e86a5231d68bbde03758f7bb28f7f9e03c245beaa4778b03d54f8968d7f`

```dockerfile
```

-	Layers:
	-	`sha256:d22086e8d4eae0bd4b23558ac9080e697addef421168ed4c550b51d93ced5c9c`  
		Last Modified: Mon, 09 Jun 2025 21:37:33 GMT  
		Size: 5.1 MB (5118856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ba2c0c724b86c82397038fcdb58d143868c97c0d2802d40b362816d4961a547`  
		Last Modified: Mon, 09 Jun 2025 21:37:34 GMT  
		Size: 16.6 KB (16634 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.1.1550-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:fd7fef1ac2157063222a966f6be0b397aad3bb4b8ad10c3418e31252c8f1537f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242128872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e39a76a0762be51fadefd02eac8491ef4f5dc558fa56074af08ef02dfb8bf42`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Tue, 03 Jun 2025 13:31:54 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833ce0de8cf4c008922a20ce0f4a2e515d9892f114fbc6b544b0dc1f28845f2b`  
		Last Modified: Wed, 04 Jun 2025 11:30:49 GMT  
		Size: 146.9 MB (146910974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bb7940c6391605f47b6edce435ced2543aedb59792f9d8ff20530c9b4b5bae`  
		Last Modified: Mon, 09 Jun 2025 18:53:14 GMT  
		Size: 68.3 MB (68334051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c685bc1b9421f81937e6a1f2126dae4de05deebc2faa26fcafa21a0d6d8dfc`  
		Last Modified: Mon, 09 Jun 2025 18:53:08 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2567d07c754187daac41016c0a862a599523932192148aff5be40346197740fb`  
		Last Modified: Mon, 09 Jun 2025 18:53:09 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:026cd32e58cd02a172006fcb29bc4ff78c4537652001b968f1f3feb26c804e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5121582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61f64451bbc68ec98e2d50b995efb4cf8ae6ff79db76ff1876ac8997946e96af`

```dockerfile
```

-	Layers:
	-	`sha256:6bc389ae31d8c132485232d2eff34d1a8851c3a077cb3c5a21c7ae6d02cecb61`  
		Last Modified: Mon, 09 Jun 2025 21:37:38 GMT  
		Size: 5.1 MB (5105007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e3c4aef8805e0024cb0839c7e604d448413932b4ea96ac25ca9f5070457855e`  
		Last Modified: Mon, 09 Jun 2025 21:37:39 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json
