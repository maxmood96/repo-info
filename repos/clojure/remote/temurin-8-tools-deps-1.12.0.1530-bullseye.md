## `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye`

```console
$ docker pull clojure@sha256:aae71ff8997c3ca5013308ea533de75dd89f7140f01cfe3e7b2783130637261b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:4a68aa8b3f5c7b6ba0a90e95af849e764c2bbbd4ce58194cbd25a9e39c36c50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177860572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d55bd5dda9f0ef595341388e01772b2e8f730dda5baec4c440706accb82cb78`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59d89cf3c4d59d95710ee429f2dbbacd4f66a8107d3506ca30726b890163ff9`  
		Last Modified: Mon, 05 May 2025 17:06:53 GMT  
		Size: 54.7 MB (54716178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41dca3c9d69c808e538fba850494f248f11b208a60584ef17728ccc7297d687`  
		Last Modified: Mon, 05 May 2025 17:06:55 GMT  
		Size: 69.4 MB (69396009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc19db0327c63e22b51b5b05926ba89fd626357712698bf7fbebab2866453f9`  
		Last Modified: Mon, 05 May 2025 17:06:54 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:505c131eb0faaf2ab49a1dc443216d2e462f0810cf9ffdf4076b9f979bcd2f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7342402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ad61fb9d341617f3e0718851acaee6115f3a492541095b93431b2e20833200`

```dockerfile
```

-	Layers:
	-	`sha256:688fd09bd89f73d29a91de2513d84d600a985e4b295b7f655c5b6ec7d0680885`  
		Last Modified: Mon, 05 May 2025 17:06:54 GMT  
		Size: 7.3 MB (7328165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da4ec3c5301c0f044775b4afcb3a55dbe85f2b2df77a42fb2cc50fc8e4a5e1cc`  
		Last Modified: Mon, 05 May 2025 17:06:53 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:85edbd79b5576371b2f274375a948eeecb6164ba8ff04a8292dc474dcc27bc77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175606544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ccc1f83c101bcfa59dd1a7aceaec0246550b4ada3f66a3d7dc72d3bd02baf93`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb2f48618bca1674b7b6aa07975908acb6ec1fe86ee6887bac65ee97038b811`  
		Last Modified: Wed, 30 Apr 2025 01:00:11 GMT  
		Size: 53.8 MB (53830504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c26e7b04f99c52caadba553fcd81233a2492476f261a1074e6c733d82af737`  
		Last Modified: Wed, 30 Apr 2025 01:03:00 GMT  
		Size: 69.5 MB (69529418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858e98eeeaf032740cb7e020b8c57695762b31bdab37630402b65926c6c46aa3`  
		Last Modified: Wed, 30 Apr 2025 01:02:57 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6a80cce08c4b5538ec00b5395a59709c0de666f016e65f4fc543c4fc67f47e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7348317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646f6dc3b3c859bf5afb1d2643ade255f50d8a704334d55f0c374dac19a3df5c`

```dockerfile
```

-	Layers:
	-	`sha256:94e49e58324a6cba30093a97778e357e9e2cfc5d9d434efc14b0a8faf7c55169`  
		Last Modified: Wed, 30 Apr 2025 01:02:58 GMT  
		Size: 7.3 MB (7333962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a311930fbc094aaa3be9585a02ca373124b8b757e256b3284208f52e75ca2a41`  
		Last Modified: Wed, 30 Apr 2025 01:02:57 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
