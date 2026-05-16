## `clojure:temurin-26-tools-deps-1.12.5.1645-trixie`

```console
$ docker pull clojure@sha256:d43cd6e81aa1e1adab588473355ec6c692c4974868e5f6c66697f2d9d2c72bcd
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

### `clojure:temurin-26-tools-deps-1.12.5.1645-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:5fecdff3f6a4f1e2bc474ca720ccb543361de6cb0cc1fffea343983e195a862c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229431283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15421371d3a4d704cfb90fb07566f25f435fcd1a26bd6f57d7c528dea20439d8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:37:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:37:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:37:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:37:41 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:37:41 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:37:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:37:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:37:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:37:55 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:37:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef14310deabe016183ae79da32de99aa3c351d1d94130588d3152ae87d9863dc`  
		Last Modified: Fri, 15 May 2026 20:38:17 GMT  
		Size: 94.5 MB (94524372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd105f97c4491407de34fc0bd665d04ff0f79f1c8822486c703d229f66b8684`  
		Last Modified: Fri, 15 May 2026 20:38:16 GMT  
		Size: 85.6 MB (85603547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a21b4e67693637637a963a0e12c9d8a18eb49d82e0cb74d17259593f81723c`  
		Last Modified: Fri, 15 May 2026 20:38:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6df2f02787db55294345dda21ea53362ee74ea28dad326eaf41b07ba96927c6`  
		Last Modified: Fri, 15 May 2026 20:38:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1645-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bf7fe620a731ea200df7d3dc7e9299152074626b806688d2a8b11aca47ad2b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7452174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeba3fd6ef7632cfc25e54494ac9e66dd6b9c227a21192e2ace68c1c1b69490b`

```dockerfile
```

-	Layers:
	-	`sha256:b9ff597e474a45739de6ed522525132c0b340d0d53517eea9f3d92314d452bed`  
		Last Modified: Fri, 15 May 2026 20:38:13 GMT  
		Size: 7.4 MB (7436273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cd5f4fb13e58cf66d5b1d695a0c57b5215f00a8e47b561a26a931edacaf4941`  
		Last Modified: Fri, 15 May 2026 20:38:13 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1645-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4ed8878dd1870e6ef2b58b79baec14c93bbcf4754068f53e63b95b77b58c6e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228590197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eeac33b785db8c8a141138ce30adaf972bae42b86ae7cff1d8d7c40ae8b5209`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:37:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:37:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:37:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:37:22 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:37:22 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:37:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:37:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:37:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:37:39 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:37:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b321991b598ec8169509ec414f43fc373fb362b85afb2af2583bf8ad093d2804`  
		Last Modified: Fri, 15 May 2026 20:38:03 GMT  
		Size: 93.5 MB (93504371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfe9988da8757271cf9093b4970a5c21fd56da41c994dbd82bf1c707cf2687a`  
		Last Modified: Fri, 15 May 2026 20:38:03 GMT  
		Size: 85.4 MB (85415335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8525902afe2a3e972e3592a081fde1f5b5d2bed852c789431c1cc74bb1b0e9`  
		Last Modified: Fri, 15 May 2026 20:37:59 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567b5142a0e74f120dce5bad7bb75ed5f28f2884c0b1879271118dd5fccefc40`  
		Last Modified: Fri, 15 May 2026 20:37:59 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1645-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4a6412c1609a1eb4f4ffd0813117441406eeac469116019961d58d7acc240a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7459319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a35f7bfdd4797d6613285042a15be12149a7111fba58ee11747fc6134b4e8d`

```dockerfile
```

-	Layers:
	-	`sha256:fd84d5d7b0bf3371249b01950af5ddd6f35fae8badc46aa89823555f2518c617`  
		Last Modified: Fri, 15 May 2026 20:37:59 GMT  
		Size: 7.4 MB (7443300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:493599cc179a3c52bbd0dcfed6e163785063c9321367bef9446b3718e9b78f72`  
		Last Modified: Fri, 15 May 2026 20:37:59 GMT  
		Size: 16.0 KB (16019 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1645-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:d209aa38b5f2644d6a51a69f7fc25780671e4562d8834ac3ee37bc311c7d504a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.0 MB (238033808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f619c925c1a20cfbf75015e8843d8d0157b88c3c70bf6a14bffa57afe32dce`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 21:47:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:47:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 21:47:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:47:27 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 21:47:27 GMT
WORKDIR /tmp
# Fri, 15 May 2026 21:53:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 21:53:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 21:53:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 21:53:03 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 21:53:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8ae203a513e0c8b74c981e5684b8f31f4776f60d5e19fb39186eaa7bfba6fe`  
		Last Modified: Fri, 15 May 2026 21:48:46 GMT  
		Size: 93.9 MB (93902122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1a967785e58d08bb2b03c72746aabd821faafa6db72d0848990b73d8fb7a19`  
		Last Modified: Fri, 15 May 2026 21:53:44 GMT  
		Size: 91.0 MB (91007476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818555b814dab8032c5def66098ccb54f92303ceac6b23b2c5b06585ccce915a`  
		Last Modified: Fri, 15 May 2026 21:53:42 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c85d00a28a911795ce2c48657d1fb50e3a901dc881607feda6c27cd093950dd`  
		Last Modified: Fri, 15 May 2026 21:53:42 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1645-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b4887732a51a3b34d167ec96238d374d8440a2392f073260beb2968925d870d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f452357de00624e8c83f2a0529cbe0dfb5a4781ddd246d4fd85dd5ec22dd06`

```dockerfile
```

-	Layers:
	-	`sha256:de38fcbb5aa4569bd1abf1a20bf0b578263e78c26f6d869b3518827b5848cecb`  
		Last Modified: Fri, 15 May 2026 21:53:42 GMT  
		Size: 7.4 MB (7424630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8f6ce14800f2121cbd98f088ba402782f18de8be3633f79a1fe2b1d89d7f663`  
		Last Modified: Fri, 15 May 2026 21:53:42 GMT  
		Size: 15.9 KB (15948 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1645-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:a23f9e63f0b48db5fe5bce0620532a251a8102c194b089811d2c0971c5bca7c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226476529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e7a6de794f8de9a83729ddc069c54ca279897fa8f480784e03c972dcf2a8363`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 21:29:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 21:29:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 21:29:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 21:29:24 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 21:29:24 GMT
WORKDIR /tmp
# Fri, 15 May 2026 21:31:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 21:31:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 21:31:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 21:31:57 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 21:31:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b45323254ce3bd87b7d048e00f69b36859e12f3173f4f96cdebb3ea0b71fbc`  
		Last Modified: Fri, 15 May 2026 21:31:00 GMT  
		Size: 90.5 MB (90536948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fa073431e5895dd3ea1a546bb6e46d3f1749909c8a6c6989ade91e280ca073`  
		Last Modified: Fri, 15 May 2026 21:32:32 GMT  
		Size: 86.6 MB (86566231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52013599350517609da6dfb50baf2617faec67b1977ee0a8a7ad9397b1e13b5c`  
		Last Modified: Fri, 15 May 2026 21:32:30 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c60f353f08b98c932a1ac09f5ecd02f1a43baecc5e7c2ea06339c1ade2628b1`  
		Last Modified: Fri, 15 May 2026 21:32:30 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1645-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:abcb36b6b54fc7e89cf1f073167ba1cb9bbc338c593aef3040aa2b50facf7236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:805e35710e908b3d4304b00ee19e7796f68cfb9b067a27fc79fc1fc855312f36`

```dockerfile
```

-	Layers:
	-	`sha256:54a42308ec6dfc6a325043281158e28cc986e8824003808f12af7269332f8013`  
		Last Modified: Fri, 15 May 2026 21:32:31 GMT  
		Size: 7.4 MB (7417381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77e24a3621e40a06eefa44950264c7968a9f78c778ef787d7b064b40d3ca88c6`  
		Last Modified: Fri, 15 May 2026 21:32:29 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json
