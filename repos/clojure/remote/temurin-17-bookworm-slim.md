## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:05e5cf79609b854047bf968e251fca879fc87db78507d3533a07dbb4af4c3f74
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

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:df933c2f29f706325bade1859a08812dd21ba28f56b13708ff9aa05ea9a9e07e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242592896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a00de5acc3762cc45ee2a92cd95fa1c01ea34141b24550a4519eeeeb56ddf677`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab3dfcaaa44f104a4a0e8fe39fb668eaea5430a31c155c98cb494b4a310dfa3`  
		Last Modified: Tue, 16 Sep 2025 21:34:56 GMT  
		Size: 144.7 MB (144693592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc65c39b31d66697231f0d5c9378b6a48ead9e107fbaf3d15f1eeb2e33711c5`  
		Last Modified: Mon, 15 Sep 2025 23:27:00 GMT  
		Size: 69.7 MB (69669916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbac48463f377933f741e803e946cf438fefec70998370f298b3c4a45d11caaf`  
		Last Modified: Mon, 15 Sep 2025 23:26:52 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1683796d5a680399e4697544820ba3c382602f8c6c1b611abb08870456f4d799`  
		Last Modified: Mon, 15 Sep 2025 23:26:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:efff964367afd5896ac86a73b02e8317f9f140572bd460f23d4cde023c1bfcc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5129267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8822aef32b46cbe01fd62dc79003eb05284f6e4edd4d9896304cef6a506403ec`

```dockerfile
```

-	Layers:
	-	`sha256:3745aebe9c0adebcdf6715d1113911f3595c417d91833baf9925b3e7d34cab66`  
		Last Modified: Tue, 16 Sep 2025 00:38:42 GMT  
		Size: 5.1 MB (5113388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4eedd17eeb9fc8d9ef74f11b2ec2242b07dffff2402bcd03d44a1674e2a7f307`  
		Last Modified: Tue, 16 Sep 2025 00:38:43 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:112c65dc5f75f0c53568aa50bd8f4a1707679b807016e84e3d5c73020ce67373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241204546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6785da0a4cf6b2a7d6bb04b286d6fb6db9746da1de2aad747ca21a00bf8eba47`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb5cd0278c696d58574078f711aed2f6eb3089ae5af0cfcefffba74a97bbf4d`  
		Last Modified: Mon, 15 Sep 2025 23:26:41 GMT  
		Size: 143.5 MB (143542168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f3002e75762c3d1bec230420ee8cdb70a7e74b3ad95757da60af4081df96bf`  
		Last Modified: Mon, 15 Sep 2025 23:27:09 GMT  
		Size: 69.6 MB (69559240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6daf6ef476a7215121ae17c9a2bd1c22517725544c1008306da0d9f1be799b5b`  
		Last Modified: Mon, 15 Sep 2025 23:27:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009397bbe83b223ee2f10933576054e74fe1e522aadc414b605971e60a4a3596`  
		Last Modified: Mon, 15 Sep 2025 23:27:00 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2c25c9d96aec5bf0f55bfd3f014dc29b5fc1b5e57045f669e1c3352c3cf1fd3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f1c35f23f4254b437d80086925553bbcceb8589d8974743f75c7123d695db8`

```dockerfile
```

-	Layers:
	-	`sha256:64b30f1215ced1e0dcf53967e37b2dfd45f825a2378747d62cdf728f51b6dd6e`  
		Last Modified: Tue, 16 Sep 2025 00:38:48 GMT  
		Size: 5.1 MB (5119149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1b1c3bc4a85eb9705362c7e477630912b5c5efe2ca72a271016fc333b130413`  
		Last Modified: Tue, 16 Sep 2025 00:38:49 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:c4ffebb6889cff3b3bfc0e60fe1f6f3cf543e22b8b7c5d70a9c8d1e79b5164aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251953051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a7429bf6c9c067c5d3319e9c57394bbd20ea8879a26bb47859b17f0fc99a31`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a438293490bbc2af66661166949a4d86358eeb39f9fadd5b0146666f05b9b9ac`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 32.1 MB (32068762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b0b9ad4e2e08bb92699318cb0d261070a8cfd1ce9528efce75a25d890288e3`  
		Last Modified: Tue, 16 Sep 2025 00:59:42 GMT  
		Size: 144.4 MB (144372818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4731383666cb82b9247b745253de74eb0217d4682782f13878954d78780cb8e`  
		Last Modified: Tue, 16 Sep 2025 01:08:12 GMT  
		Size: 75.5 MB (75510425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba8eb874de8eaea5081e1910687e7c0718c1b70a4c9ca125250f67d066fa373`  
		Last Modified: Tue, 16 Sep 2025 01:08:02 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca5efe56a65764522db855398d81f3dfd7903484d20aaca580a250b11be67f3`  
		Last Modified: Tue, 16 Sep 2025 01:08:02 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ae2d1d83f7824075177e0815ccc1c50ff62f6fe50d9aa503ed0eeda1c17f50f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d8b25259ac44de2b1954d6976b13b5a78cf12fea1311ecf21e16bf5d866dea`

```dockerfile
```

-	Layers:
	-	`sha256:693f1587dd10432491aa653f6abbcff0d88443415375d4cd33210c4919ed381e`  
		Last Modified: Tue, 16 Sep 2025 03:37:52 GMT  
		Size: 5.1 MB (5118546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:774b0d244f22c2a126b5c9d613b0ff1788296572e3b898832f36ab1b99802577`  
		Last Modified: Tue, 16 Sep 2025 03:37:53 GMT  
		Size: 15.9 KB (15927 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:5a9b45f3cf0bdabfb0947270eb9a8bae84c653176c55b29f5b812f712dd356ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 MB (230095154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac601a7872bf41b418d5c2aa258f76d2b2d52feece233ef3cd314886573ae375`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2602c23d719124d8d19e0e56c4a779006fdf8ce799d6cb00b3e1ee7041789491`  
		Last Modified: Tue, 16 Sep 2025 00:32:24 GMT  
		Size: 134.7 MB (134724380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e440dac3a9c3071c2d874905332ca502a49d97204ebd0e0ac00e1699ea5c0d9`  
		Last Modified: Tue, 16 Sep 2025 00:41:57 GMT  
		Size: 68.5 MB (68485433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f791c6cf380b3a857a87ff3a18ad3599b4e9cbf77775ccf11eb7d674f3508a1e`  
		Last Modified: Tue, 16 Sep 2025 01:35:38 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fef2fdc83608161fa80fd85645749e2e94994b16e4ce4e6d948dacad9c9fe93`  
		Last Modified: Tue, 16 Sep 2025 01:35:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:876ddf5bcd67f3c2fcaba519a51c94096bc506af40808b00c247420eec82c9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5120588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9247ec10812b212832522cab3ceb140f950183c2dc2108d11e0f1c0ce0d3e66`

```dockerfile
```

-	Layers:
	-	`sha256:459f9332bf266e197563f7716e2603f54e89fe0bf6acc93a120eb378f5fdd0c8`  
		Last Modified: Tue, 16 Sep 2025 03:37:57 GMT  
		Size: 5.1 MB (5104709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8642d927e29564c37e1efc4c5c8f071653bf73f3c2c8a85ff6db048a24907c0`  
		Last Modified: Tue, 16 Sep 2025 03:37:58 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json
