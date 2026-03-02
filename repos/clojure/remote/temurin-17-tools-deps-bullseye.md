## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:d49e6e10d7a1ffb563f1479d5f2e0d710cd9afaa9c415a8ec33423e163541ce2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:423ed52c6e0f529b036e1a30f3c342b153e1d092f82a4af44d4604c5618d4d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268971295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a75ef60d8a6f3e63eb44606206232e65be16d1c83a1b4dc2b94b71f496f9af9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Mon, 02 Mar 2026 19:46:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:46:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:46:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:46:49 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:46:49 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:47:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:47:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:47:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:47:02 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:47:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a3631da109e9957a95ce21c6124e202ef7f857ccc599603724b4ff745db39d`  
		Last Modified: Mon, 02 Mar 2026 19:47:23 GMT  
		Size: 145.6 MB (145628702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb827b2c29750a0aa3bb297d482822f319805bf3b56831de752e682cb88b6cd0`  
		Last Modified: Mon, 02 Mar 2026 19:47:24 GMT  
		Size: 69.6 MB (69585115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9506db3d07a9263a50ea0f5900f1a96fe1b35fd0486223369cb0e266002953c9`  
		Last Modified: Mon, 02 Mar 2026 19:47:21 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc4526f95a8c56e46b240954c353f8f7c404c7643e9d4bfe20b7cfcb332d15b`  
		Last Modified: Mon, 02 Mar 2026 19:47:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:99a953924b3781c6ea456d69c5cb9408f324aa2057ca4552f352d26a82d82734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7425055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3932bd7c033ff9c3c2aa5967c3b5b1c663fdeb55ac2b33c9a990b7ea1bd7758c`

```dockerfile
```

-	Layers:
	-	`sha256:394db3916092c3f37ddbef61a97216f3569a81b315477f7c4515ab9daca7e819`  
		Last Modified: Mon, 02 Mar 2026 19:47:21 GMT  
		Size: 7.4 MB (7409277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2d90dea60f6269494a5ef87ec13e0718171bca77649fb5991066dd631bcf484`  
		Last Modified: Mon, 02 Mar 2026 19:47:21 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fad5048ab05e3473f7592aecb9fd5d12fde6168745fda06945fedc42924d380b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266420740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d3a93c869fd721337d2927cde7826e43f67c2555e0401acd400446c4670444`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Mon, 02 Mar 2026 19:46:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:46:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:46:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:46:39 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:46:40 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:46:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:46:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:46:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:46:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:46:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0509053f2cf8072309184287dd2fd397e589dc5db17a1ddc469001be80ea07a3`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 52.3 MB (52258392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00510152fec3abd779c9973b9b953cbc73bcdd24014f5464bd0052c5ffb05035`  
		Last Modified: Mon, 02 Mar 2026 19:47:17 GMT  
		Size: 144.4 MB (144436198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9570dbca691b3df6d5dd5a155629199c36d1381778988cbe39fb0deaabc515c`  
		Last Modified: Mon, 02 Mar 2026 19:47:15 GMT  
		Size: 69.7 MB (69725108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d710d0afb5965c0c63a4cbc6da2f24d48afec93d53e7cc74d6e5b572492f6b31`  
		Last Modified: Mon, 02 Mar 2026 19:47:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2abebdd1d304e77f1dc900412c64bac6889fcbb15efc007e0d9ee46f410502`  
		Last Modified: Mon, 02 Mar 2026 19:47:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c6456acfe36c6e0e6f97f780f11c3a24caef3e7c45d7384b87fc90a9358d9c3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0694d16d79a9c7acaa2584d051bcddd1721b327c98a3dc8c17e754e0f16481`

```dockerfile
```

-	Layers:
	-	`sha256:2c193d1157d00ca3be9164baa83b293f9bc8f8ff272249d8646a2859929d92ab`  
		Last Modified: Mon, 02 Mar 2026 19:47:12 GMT  
		Size: 7.4 MB (7414376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee02a689e902117c0974c1cbaf70cacc628167d5c33ebcaf340d828780e8cb28`  
		Last Modified: Mon, 02 Mar 2026 19:47:12 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
