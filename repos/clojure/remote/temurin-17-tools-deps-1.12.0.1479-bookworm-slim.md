## `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:1ca8bc24fce48719b257227d7b6b062632ae52f18b51e9cad655f60a90660bf2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:144aafc38013112e97f0efe50f4c8dbcdbb456a3660843fb34658fd63a6bd704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242062361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939724e1ab9db536953c5d060fa436ca3a083d4bf50a9cb67b0dd7ecc265b1c4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d08c02696597543bcabaec9f4796c32bab3e5b8dec0f5416641d2190c01d1a0`  
		Last Modified: Tue, 24 Dec 2024 22:38:10 GMT  
		Size: 144.5 MB (144536708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f99d307b25a8cb177b840ced0bb93deb1203f2809c32512713d6f9d3cb8faa`  
		Last Modified: Tue, 24 Dec 2024 22:38:09 GMT  
		Size: 69.3 MB (69293034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7f8bf74a727aad5f59c2395a57d5df12d33e28b2353881af8d58ba7fe5c21d`  
		Last Modified: Tue, 24 Dec 2024 22:38:08 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979ceb8c0262f55a43d7a501abdb480af95c5cecd8deb40921b39b2ccdf02bba`  
		Last Modified: Tue, 24 Dec 2024 22:38:08 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e19ad759b012a7e039914a826e8fe051d1595c66ec757a4cad2fb78662273076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c75794777a056c97a67bbd503563125e88a01640996f6747d19ca5a6c17bbf0`

```dockerfile
```

-	Layers:
	-	`sha256:12a2ffc557c3a7eda336d11b3bb8b59608be4fd877403bbb652492a6d31d98bb`  
		Last Modified: Tue, 24 Dec 2024 22:38:08 GMT  
		Size: 4.9 MB (4912507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d46c476bf54bceac93a2bbf23058d6254bdd5cbed32f8cd9edab24bbe08487f3`  
		Last Modified: Tue, 24 Dec 2024 22:38:08 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3c1cef7b8e220cdec4c88bc2d3af38939365c7eed1e3d8505c7d54c0989c9de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240561553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af81a3b9d7bc4f4c31faf412839b3da9533ee5ecfcc6ef7b5ce0c8858c476fc9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db3ce0e9523a9eb5dc5d8c6b79f65c5c8ba65627853d1041da5183adb9a9e5b`  
		Last Modified: Tue, 03 Dec 2024 15:17:35 GMT  
		Size: 143.4 MB (143360979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3cc1cf0a15f2e4f272cc6680feaa571ec8ae03c944ff724c3f6e1aac43ef49a`  
		Last Modified: Tue, 03 Dec 2024 15:21:43 GMT  
		Size: 69.1 MB (69140727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd1b7eff43d0f2e5a3552886ee7296c9ab61cd40772e9400dd4526b3500044a`  
		Last Modified: Tue, 03 Dec 2024 15:21:41 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9917055c57d5a95cc6baba828b190ea0d038251f6b98fac91d8df47172205c`  
		Last Modified: Tue, 03 Dec 2024 15:21:41 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1b7c21959016ed07209d59f625e30b41c91aac759f6ea1c6c349fb01d296549b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4941143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:219a9cb3e1471245ff762f18d89418862d8ff199f7d61ed97e8bde775a16b1b2`

```dockerfile
```

-	Layers:
	-	`sha256:3bf9141f8f34707c23f21c0f1881c5364e83d0e4cd27c7030e21126e5922c920`  
		Last Modified: Tue, 03 Dec 2024 15:21:41 GMT  
		Size: 4.9 MB (4925146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7dcb20920ae5b03d8a6faf1167e871d2d5a8f5e589de87afe54f5afc7431ec3`  
		Last Modified: Tue, 03 Dec 2024 15:21:41 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
