## `clojure:temurin-21-tools-deps-trixie`

```console
$ docker pull clojure@sha256:e1eb2a7eb0241af5e25bc35ed7ab3656f649ae2804ded3814d8105472f15d0c3
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

### `clojure:temurin-21-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:e934a8da4b016ff5aac58f241c02f47779b4404c565256bcb7d4a690c56c5ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.0 MB (290003944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d316ec456ef35bf3d384b2cc891109df489d06f1a1120b03f2b81b5a4d948da6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:20:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:20:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:20:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:20:03 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:20:04 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:20:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:20:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:20:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:20:20 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:20:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28bf929f7aad80732116fa0b6cb9dc96d54a2866fe1ea1fb35f2ad9a1ed2af9c`  
		Last Modified: Thu, 11 Jun 2026 01:20:45 GMT  
		Size: 158.2 MB (158166940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08ca26b9c070e7ae8c1e5905fcedfed6252319d6b0d7c2c504895a7138db069`  
		Last Modified: Thu, 11 Jun 2026 01:20:44 GMT  
		Size: 82.5 MB (82518843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56fd061de487cb0b8f034e79f80872d42f6cf958eb5c4e1d67f5b6ea10e12f08`  
		Last Modified: Thu, 11 Jun 2026 01:20:40 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc46f0f5e5a4ce17e0d1c09896b132ee460de866a3530af78cced84c0b518344`  
		Last Modified: Thu, 11 Jun 2026 01:20:40 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:875f79d5aeb99f96300b48c2bb345879e4a905d8fae00f82277e8088739f080e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce7125478dc6068b2895251af2d4fb9d89ae1a07d6dd09b5b6708ba1c453c7b`

```dockerfile
```

-	Layers:
	-	`sha256:d8ce6515d3fdb0e5db28f0612a67b65cb48f7dc79c7ab9f4977de01ddeb52157`  
		Last Modified: Thu, 11 Jun 2026 01:20:41 GMT  
		Size: 7.5 MB (7470623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bec6935125454a05ec0ca705587dbd29d3c80ef9fc5f1228d21cb66af2b588b7`  
		Last Modified: Thu, 11 Jun 2026 01:20:40 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:70401872d33506fdc910a8806265a17bc707d3d4e162c7de13c029b6b1ff1992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 MB (288479048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc75d27fb0a29888ce588d5d609ed667ec4dbe94df6b85b9812d11bad77e3289`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:24:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:24:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:24:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:24:23 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:24:23 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:24:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:24:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:24:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:24:39 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:24:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679134f5748a52b18a915a7211c9eb6302c4063ac1b7f17bdd65f6147854be0e`  
		Last Modified: Thu, 11 Jun 2026 01:25:05 GMT  
		Size: 156.5 MB (156461323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f0c366dba1d15a35b1790d520fd0de01bd751e0b73f676640d93ee64258498`  
		Last Modified: Thu, 11 Jun 2026 01:25:04 GMT  
		Size: 82.3 MB (82338516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69156b790f1e6cff563b8e8a21acab144a1d0f94e80e98f47874bc48dbdf7668`  
		Last Modified: Thu, 11 Jun 2026 01:25:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0cb181377b16affd40f07c67b65aea5d66fdc5bad2981d03716c55b52c30526`  
		Last Modified: Thu, 11 Jun 2026 01:25:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:df23c813070a717846b45d3998ae2e4d8c9fd7b8b1b243a74d56bc217e61ab33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada000e4d1f4269fe6bea8626748e7d4917e054fbf4719b1d51bae2e338e0bd9`

```dockerfile
```

-	Layers:
	-	`sha256:5ceb6c7e9b971f0194e3a7f54980f84b96a602d3b310c1eb744a1de20d9292a6`  
		Last Modified: Thu, 11 Jun 2026 01:25:01 GMT  
		Size: 7.5 MB (7477016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2b410fab7d576eeee89c0eeb2c9d1d0ab8cbc2680e90b029e723928e650f40e`  
		Last Modified: Thu, 11 Jun 2026 01:25:00 GMT  
		Size: 16.0 KB (16026 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:8c7683e0e8ef4e20a2afb7c017b2d8d90cf5bfaea6d31f8f36463b0f51d5406a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.4 MB (299414763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd654ed1dc439ed3b05e8cbffc2231fb261e8f05d5d91203b964b6d5da1aa39a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 18:02:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 18:02:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 18:02:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 18:02:28 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 18:02:29 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 18:03:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 18:03:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 18:03:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 18:03:18 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 18:03:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f96ab628163acfc4a897a60446de4136b4548cd3582a46ae52f4ea4f52f11fa`  
		Last Modified: Thu, 04 Jun 2026 18:04:09 GMT  
		Size: 158.3 MB (158343238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a1e1cb8580ac4268a3c4e3a37b203da55014fee78fa783d37bd4af826a9571`  
		Last Modified: Thu, 04 Jun 2026 18:04:07 GMT  
		Size: 87.9 MB (87938298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b5199c2bae3aab160dd46ffe25d545bd5592f984308090666887c2dcf252f5`  
		Last Modified: Thu, 04 Jun 2026 18:04:03 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea57d62e98e2e672ad6a830b006e5a8298b3d5091337d29685a21f131a31a179`  
		Last Modified: Thu, 04 Jun 2026 18:04:03 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a0fc623ada0ab6cdbdc85c6682ba0b13d55967dca234f9efc43857caffa10d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e845b6d1e3f0c65492d623b065308ac48d16b5b0ccd7bd7f639190479e6910f`

```dockerfile
```

-	Layers:
	-	`sha256:4eddc7a4ced7655c1b79615cff0bd27d8759b575aa0f9bb9f44e9c419b5d9cc5`  
		Last Modified: Thu, 04 Jun 2026 18:04:04 GMT  
		Size: 7.5 MB (7475044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bde4ee7d8a1c33acbb573665b3bac085f91850e77fbcc51f071bf1262d752aef`  
		Last Modified: Thu, 04 Jun 2026 18:04:03 GMT  
		Size: 16.0 KB (15956 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:37cb078b0667336830b9eb43813d7b6d9c7cf78bb43367f1cde3ca2184d1a650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.3 MB (280277138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d9670c43d20343509e75965cb2b6368549932999a971adc94c92ead040a177`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 03:11:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:11:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:11:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:11:22 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 03:11:22 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:12:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 03:12:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 03:12:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:12:42 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:12:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d283a83afe454a5e986887cabe845ba92525fe405ba9481c9381d96f0b53ca97`  
		Last Modified: Thu, 11 Jun 2026 03:12:05 GMT  
		Size: 147.4 MB (147388375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efcb7f186669ec9e7baf08bde36040efc2af36636b25ff1386f0e36fcf30732`  
		Last Modified: Thu, 11 Jun 2026 03:13:08 GMT  
		Size: 83.5 MB (83501827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1648815dba058d14219c49731151ec3d3587eae3b54b4401fd949b5f03b6e07a`  
		Last Modified: Thu, 11 Jun 2026 03:13:07 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0321cf3984a714ecabb889b0935268f21b1c3d19333ee42835e5706b01d4878`  
		Last Modified: Thu, 11 Jun 2026 03:13:07 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f780bfc731fe4b57753bfeefaccedb91e38e7d2c3d8f543b0f80f83f7e907e8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74826d081601424b07353daa42ea1ee97cb3280871fcb8909ea0442a5c65b8a9`

```dockerfile
```

-	Layers:
	-	`sha256:0282d5f2ebbd08d5cd3643c5288dae42f0fbaf8dd4672cac95770a8f7a4b869e`  
		Last Modified: Thu, 11 Jun 2026 03:13:07 GMT  
		Size: 7.5 MB (7466545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d926e11bf27b42e4dffa39c9ec4b74cc9205c1332483760f723ba1b73c9928fa`  
		Last Modified: Thu, 11 Jun 2026 03:13:07 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json
