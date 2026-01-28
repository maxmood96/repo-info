## `clojure:temurin-8-tools-deps-1.12.4.1602-trixie-slim`

```console
$ docker pull clojure@sha256:6152718018dcd3d1b9cbce0fa624eb7c6958ac2aa5f4e59fc057c72dc54ec240
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6bfdab0cd763de5c5d9e8131e174bb6f8e0d6c7d4e9c2fac09381045d6c0eb97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.5 MB (159452302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901dba9ca58e74ac0f6cf7096f37442217e8629f2378dd850bdcb3b1b373df92`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:03:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:03:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:03:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:03:37 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:03:37 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:03:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:03:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:03:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f998188de8ce8cc6ee8fb7880d33199a685681acaa7a2168f01c8c36553b22`  
		Last Modified: Wed, 28 Jan 2026 18:04:12 GMT  
		Size: 54.7 MB (54733371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3467b9df362729f61bbf9505cbd77a1492b2ecf352cf213386cdf812eab3029`  
		Last Modified: Wed, 28 Jan 2026 18:04:12 GMT  
		Size: 74.9 MB (74944601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a35214431be9622186b1c1ca9a1635216d287e5a81cc8b779dfcd481fea6e8`  
		Last Modified: Wed, 28 Jan 2026 18:04:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:adcaa35b9c7ed3bfd84e772d588ff5f08f033d3be38acc731e1fb24edfa60bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5392135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a71c9d665df1ccafb4fbba30be328a5480158b5729b80dc41a4b0a2f66961742`

```dockerfile
```

-	Layers:
	-	`sha256:eeb1a37b77541fe8632cc6a9c46e7955464e2ee333e961aa3ba8172a050a0b3c`  
		Last Modified: Wed, 28 Jan 2026 18:04:10 GMT  
		Size: 5.4 MB (5377907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f59ffd5ac000f63d544fe4451e267bfac492662f31581b616462f21d88bd73b9`  
		Last Modified: Wed, 28 Jan 2026 18:04:09 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:73cbabff371ffe1948c9a19cc32706a836d590ae25d3b8b693118d16ae6878ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159071888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f75c78d9e8d70ad5d163d00c7cb81b1233c805bdf0fe5f75dd2d6fc383711f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:03:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:03:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:03:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:03:01 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:03:01 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:03:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:03:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:03:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:171be5573e58f68c5d82f2cd70e441efd1e7e18681aad89e69e4902a11eded06`  
		Last Modified: Wed, 28 Jan 2026 18:03:37 GMT  
		Size: 53.8 MB (53815013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea51ef9ef9749981265cfa8302793f6675387d949fd5698ebfad58fd19c6c435`  
		Last Modified: Wed, 28 Jan 2026 18:03:38 GMT  
		Size: 75.1 MB (75122187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96947fced286e77ae1ba6e26c79b767883bfc070366ce9e537fcbf6584bbaa76`  
		Last Modified: Wed, 28 Jan 2026 18:03:35 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4e1a9c7d97ac031bf8a8ae3a3f64bfa370edc1dcfa096c27d3a4cc2d0e0d3d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a37bf18683f054e5ce537b1d70b8f3e2454a7837035f32297397259e6f94c80`

```dockerfile
```

-	Layers:
	-	`sha256:8eb3cc50afc68446b2030a75495bd9d3f8ed24560d300c8206b96bbd3d58182f`  
		Last Modified: Wed, 28 Jan 2026 18:03:35 GMT  
		Size: 5.4 MB (5384374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e926096b15c11402f6189dd3d415f885369eb60036591f98b0dc9da29106bf`  
		Last Modified: Wed, 28 Jan 2026 18:03:35 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:951f2e20f8279bb77467315c99a1946e66cd872f6a69fe7bacf8d783003d755f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.4 MB (166362448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6969f07ef105179e5ffb470cd407edb1a0a9126e76c1c8659b3e56bde480bc15`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:16:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:16:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:16:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:16:02 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:16:03 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:17:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:17:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:17:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5faf783503dc7dd62a80622a59f1d7d097ae81140a522e1cc754dfca95c0390b`  
		Last Modified: Wed, 28 Jan 2026 18:17:43 GMT  
		Size: 52.2 MB (52175145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5370dbc603da3d91b0ddc9fcf48a0224b53f74588a50b4a05ea59a54f3e67f8c`  
		Last Modified: Wed, 28 Jan 2026 18:17:43 GMT  
		Size: 80.6 MB (80591059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc44f6629641099f7063fe4f627855e0b0922841a4c31fc5c91bef452c5524a1`  
		Last Modified: Wed, 28 Jan 2026 18:17:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b5e3a9a270d22258f7ad8f0066f9a05bc41a849fe777e7e38ad1117b1fe027c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a324984fbdac1f7b76427beb6321a459a065d490624ddf9a010688d8194c0a7`

```dockerfile
```

-	Layers:
	-	`sha256:2bb3ce332b514a02cf1190781c8a302945d6f9e20ce373a9b2926e8bafe238c6`  
		Last Modified: Wed, 28 Jan 2026 18:17:41 GMT  
		Size: 5.4 MB (5382871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9a51549d9b369970457f3bd4a1f751a7b9db108324265c836fae29e4f768d95`  
		Last Modified: Wed, 28 Jan 2026 18:17:40 GMT  
		Size: 14.3 KB (14275 bytes)  
		MIME: application/vnd.in-toto+json
