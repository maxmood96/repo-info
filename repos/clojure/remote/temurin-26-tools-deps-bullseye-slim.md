## `clojure:temurin-26-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:e1d2986998d9e52de62d29fa2d76a18623ab4f577cd70cbe79febf6e1ec7cbeb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:59a6aa00676d327e20e3b4dc160b5b73e596317d7ff70cc6100821feabe55fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.0 MB (183973231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e70aac388f5112a1df1325ee585dc43d9a24ce4ce77c71c55e7bb01f3d3242`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:03:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:03:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:03:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:03:53 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:03:53 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:04:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:04:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:04:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:04:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:04:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8419f4a27c97b0c111ab0dc77e0159bd3abfadcb948d4a49cf6dd6670703b84e`  
		Last Modified: Tue, 19 May 2026 22:36:35 GMT  
		Size: 30.3 MB (30257598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e18e5a750ed567ab3cdfd62ca694ece9c5ec1e89f0ed25d2d8dfc3555e04f2`  
		Last Modified: Wed, 20 May 2026 00:04:29 GMT  
		Size: 94.5 MB (94524331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be665968bb448f8e572b1b7ca3a5f634155696077612b5df06fecc68cdec7b60`  
		Last Modified: Wed, 20 May 2026 00:04:28 GMT  
		Size: 59.2 MB (59190259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092f3831357776464082d2870b8b33a9ee2d277f77bfc7b35bba982c3d2633fe`  
		Last Modified: Wed, 20 May 2026 00:04:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecacb9352a948ee8bb6b43d8c083af5ef71dc32756db235d41a61649e41f614`  
		Last Modified: Wed, 20 May 2026 00:04:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2edbc72b41e7ed2bfd8afced9ed8ff105e7a0dd7c2a9ed4415ca5e71bec7b823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5301552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc0c4cef5a4b40b928bbb62c780a46b4e3c3ba41d8dfbc3956d80c3f486efd1b`

```dockerfile
```

-	Layers:
	-	`sha256:77a91da5dd0818ffa572ef3bc15aaf6eedcaf2aa1850e562a1fea1a88df237d0`  
		Last Modified: Wed, 20 May 2026 00:04:26 GMT  
		Size: 5.3 MB (5285569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:358630383b5d3e2152699da5d250277732c472186d8024650246976e8e9eeede`  
		Last Modified: Wed, 20 May 2026 00:04:26 GMT  
		Size: 16.0 KB (15983 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6f8fd6868947e0deb35a415a2d3534f8d2500a46c94b685669eaa158e063042b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181608289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc1f3eb84e493b13f91694af7ddd954731774a8b8c55edbecd89071714783ed`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:09:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:09:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:09:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:09:27 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:09:27 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:09:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:09:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:09:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:09:41 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:09:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2b99ba6638377be8e7e1e9a328ebb001513ab9f700c8168d404eed03437c7ce5`  
		Last Modified: Tue, 19 May 2026 22:36:47 GMT  
		Size: 28.7 MB (28742972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09c9f51f74807b717826806de87cb8ccb1e5ad93f4c1f341bdc1ff90375925e`  
		Last Modified: Wed, 20 May 2026 00:10:02 GMT  
		Size: 93.5 MB (93504334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390d045f1dd8d162465e7764ab7bd2f50e62a8ca02d4c911515d94e9d23eb8d8`  
		Last Modified: Wed, 20 May 2026 00:10:01 GMT  
		Size: 59.4 MB (59359940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736d8bbff4958f2d8b1731316f67fc58de919b02e5d9530e977f09e1c3cb31ae`  
		Last Modified: Wed, 20 May 2026 00:09:59 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50a5f4dc535025f057b4912def1cd544ba04a37d61ef7f7db38f3a837bc5e23`  
		Last Modified: Wed, 20 May 2026 00:09:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f1a72d65fa0c0b3722a566ba06da9c9a04cf0b827f57db3e95ac0033d6e68c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5307399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd722a8fbfab0e45552c538d954779169c3ccfcde0f613b07b4b413213d32c6f`

```dockerfile
```

-	Layers:
	-	`sha256:682db2d34017b32c89e353289709de504fa9bb76f967a725fbb84ce87d5df0b5`  
		Last Modified: Wed, 20 May 2026 00:09:59 GMT  
		Size: 5.3 MB (5291298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2fdfad95db82d9262822f421ea06584c1913bca2b074fbedb4cbab1f9e8b58d`  
		Last Modified: Wed, 20 May 2026 00:09:59 GMT  
		Size: 16.1 KB (16101 bytes)  
		MIME: application/vnd.in-toto+json
