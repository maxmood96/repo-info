## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:e528acae19e494d48a610313e8dd738ab829976f105c49720267b11ad470f840
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:12fcaabb8be2152a174c78560bf50629266962fe24b620aaad61d1ac6b5ecb3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.8 MB (181826908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fdf13167dc7a52f413513110c50186125c821474ab32ec8dae6e116a141c33d`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:14:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:14:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:14:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:14:06 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:14:06 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:14:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:14:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:14:21 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:425befdf76e52426879d2abe42093a00dca59a893e7b4fa2a7679b0180b71d4b`  
		Last Modified: Wed, 24 Jun 2026 00:27:40 GMT  
		Size: 48.5 MB (48502210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45bda0ccae28f8d8d681c0876e47c03dc9f54ebf85850659a1c7698d8605d238`  
		Last Modified: Wed, 24 Jun 2026 02:14:40 GMT  
		Size: 55.2 MB (55198725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a10027d4525d66b86b0c9565fb5637e26d1f114a1d47f7f8037f61faea1b849`  
		Last Modified: Wed, 24 Jun 2026 02:14:40 GMT  
		Size: 78.1 MB (78125329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7335c57a356aa2a29b6baf55d3efa6e7000fc15ca371020b4a8f8ee027bce708`  
		Last Modified: Wed, 24 Jun 2026 02:14:37 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:10591c4141f9acf5ca40b28262a871fce3690d1906d6c3c50d387022ae7b3c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7510842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0656b914231d2dbf569b6a71fb77e1e2cdbe9f656fac8a80dfd627968cab4289`

```dockerfile
```

-	Layers:
	-	`sha256:f25b4c5bf25ad31cc9b1aab4db8db196cd47e826104b0c5adbf5f6df6cb218da`  
		Last Modified: Wed, 24 Jun 2026 02:14:38 GMT  
		Size: 7.5 MB (7496494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0607679bd46a27cccf9f8b1b3325af78b477c9c282e27bad67cba4eba959bba8`  
		Last Modified: Wed, 24 Jun 2026 02:14:37 GMT  
		Size: 14.3 KB (14348 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c36404894154bf91b2fd12ac67abeeb69ff7a4c41a211ed698120ca1acde782c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180792067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4180e1e029344dbf6c1adecbbb779695b004b325c2bc372ed6a354a954f100`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:20:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:20:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:20:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:35 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:20:35 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:20:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:20:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:20:51 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0fb1189398e2e4b474d43aac6502510d0da0318e70137a377c21087f198814db`  
		Last Modified: Wed, 24 Jun 2026 00:27:19 GMT  
		Size: 48.4 MB (48389201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6344b8fbd83722fa592ff8c43b1edad5976887b040f00a2660e619e4835eba9d`  
		Last Modified: Wed, 24 Jun 2026 02:21:13 GMT  
		Size: 54.3 MB (54272911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adaf1362e9be8c9b1775e80371c3ebbbaa2c77fd9a879140bcde0a34256273e5`  
		Last Modified: Wed, 24 Jun 2026 02:21:14 GMT  
		Size: 78.1 MB (78129309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4edfb2286ea69e2da4776744292f0481fbb50a4eb49627b0e450b663ec4b6ec`  
		Last Modified: Wed, 24 Jun 2026 02:21:09 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f62bfe66ae92316594ae99ece55a483759bc8baec3a7e35f571baa93a8e88427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c673ade81e97053c67cb074c97375290065e71d81426656c66743de6cdac316`

```dockerfile
```

-	Layers:
	-	`sha256:27c3a9960ad1ffe2adcaa22009a4f63a63bf7501207082922d5dd2dbaa82bf8f`  
		Last Modified: Wed, 24 Jun 2026 02:21:10 GMT  
		Size: 7.5 MB (7502957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0d916f1c50a716190b038742877fc1f322ccf0ab1f464de4406d562ffb9fe4e`  
		Last Modified: Wed, 24 Jun 2026 02:21:09 GMT  
		Size: 14.5 KB (14466 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:a688cd30099cfd0a553d731d78e6fb7390f9a17b5a98690b53b8adc168708809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.0 MB (188975208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01fb087405b5a489681d37d83083aca408af2a600e6cb987b391eec46700d9d0`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 07:46:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 07:46:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 07:46:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:46:55 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 07:46:55 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 07:47:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 07:47:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 07:47:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:55b0e891f4e8dc14bf4bc7e853254fcf1f3ba5a8e8e3c07c21e7dd5bd6d87882`  
		Last Modified: Wed, 24 Jun 2026 00:27:34 GMT  
		Size: 52.3 MB (52346847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec8720738a231e03a51ab3360b5c340863474851dcb389bcd71e911076d0002`  
		Last Modified: Wed, 24 Jun 2026 07:48:19 GMT  
		Size: 52.7 MB (52669106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbec26a6d37addd9ea2c4ed992e1ebdfdb4decf160c1a955c4fd10ac88b433d6`  
		Last Modified: Wed, 24 Jun 2026 07:48:20 GMT  
		Size: 84.0 MB (83958608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0748f1bc18cc57a454f27510c9be7b5334e88a33b77d37c56ceee758d7ae085b`  
		Last Modified: Wed, 24 Jun 2026 07:48:16 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7e4f32a59db8c34ab3c12c6b5adb7d26244fc91ee7eb3f4da6b7b94c2b88a5a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7516701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68f20f5ca69babff46708460c0634e27ba0544f3ca44dfedcf04166c9126cc8`

```dockerfile
```

-	Layers:
	-	`sha256:d3eca9d1fd1ebf7fe23975ea17c3af671a2d206936152c36a717d9ce1022216b`  
		Last Modified: Wed, 24 Jun 2026 07:48:17 GMT  
		Size: 7.5 MB (7502305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1033f1f392ce6a45ee7f5cfa2d11f02e9b5e3fdef65ac48421c030a3a2b67a0`  
		Last Modified: Wed, 24 Jun 2026 07:48:16 GMT  
		Size: 14.4 KB (14396 bytes)  
		MIME: application/vnd.in-toto+json
