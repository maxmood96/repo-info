## `clojure:temurin-8-tools-deps-1.12.4.1602-trixie`

```console
$ docker pull clojure@sha256:9669b6c1f78d15e3d9cd9da2f136d18f6b73877dcda79f0624c517ffc6bd6ccd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:d73beebf2c39e15221c6e3d163a1eb489c36ee64086f9270ab225ddc480bf365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192533421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8331c0b9520f6503bf1b9320b3caec02de91ba7051b3de723e9114eb9b0382cc`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:03:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:03:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:03:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:03:36 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:03:36 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:03:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:03:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:03:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9548ecc800c152d0bbe88e94e84283437063be5a67b7332d1cc9ba28baaad39a`  
		Last Modified: Wed, 28 Jan 2026 18:04:12 GMT  
		Size: 54.7 MB (54733344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7bca3efe05f54eb5d0e949d61ddedb5ef1cf3f787416a76600840072c65731`  
		Last Modified: Wed, 28 Jan 2026 18:04:12 GMT  
		Size: 88.5 MB (88513813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b9d398dab41a565f48f7f27ebb7ac45913d33f342d840b98f4fecd67110a69`  
		Last Modified: Wed, 28 Jan 2026 18:04:09 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:31cea103f094b214b7e13a994ddc9e23252f92643bfadcc4d8c6198b50153fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7603605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4006ebc808a2f8654e0d6128da8448421608e8c86ad9dd926b5c97163f6b569`

```dockerfile
```

-	Layers:
	-	`sha256:27f0682fb12a2cd56ce9a04525eb1581dc708742a1ce84f32b2c84160a344e88`  
		Last Modified: Wed, 28 Jan 2026 18:04:10 GMT  
		Size: 7.6 MB (7589436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bac399ff40d5187dce363f60351cdfb379cd71e860a3aed3afe2b37e3c7f0dc`  
		Last Modified: Wed, 28 Jan 2026 18:04:09 GMT  
		Size: 14.2 KB (14169 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:45372d1c2762f951b95ac3c27188e5a352a3ff31e8ea00ac8ebfaef42f134c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192156246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5660d09b1109b3e768b6a484746acd03bc7e985202743eca7515bb518a5a591b`
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
# Wed, 28 Jan 2026 18:03:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:03:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:03:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990e3ecddedae0802aed2c9cf9d89e6d92207ec8a9b5b38928e3c402fcad6205`  
		Last Modified: Wed, 28 Jan 2026 18:03:41 GMT  
		Size: 53.8 MB (53815013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29b8ebd8de82684591581ac11c54fd68cf769675ac0fc902b08a86a870a364b`  
		Last Modified: Wed, 28 Jan 2026 18:03:42 GMT  
		Size: 88.7 MB (88692505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffaa6bd1a027b1b3146a668990c984e5061d6592d33624532a78d65d0180953`  
		Last Modified: Wed, 28 Jan 2026 18:03:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:415221bb60abf23a29a458db6afbb911f741054e167b4e514e50df289fb58ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7611451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fd44cc54ad76e0bcb29eb3aed485ca7a178ac55f9874490e299eb96575cf54b`

```dockerfile
```

-	Layers:
	-	`sha256:0fa03e954fb5fdf515e2a00c72679f68d70d6b7d4334d0d5bd1ab74e7bb5df0f`  
		Last Modified: Wed, 28 Jan 2026 18:03:39 GMT  
		Size: 7.6 MB (7597164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac57ffef0aa87d5b62a960c942ae9bfc79287070906d43113ff073ff76db5051`  
		Last Modified: Wed, 28 Jan 2026 18:03:38 GMT  
		Size: 14.3 KB (14287 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:7cadb86633446a447681e2edb13c6075812dd472f1721e1ded894973ecad5e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.4 MB (199435286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168ae73cdaa12b1d8e5ef983d277156c6f14d2046010c6dfd34ae2ead35734a4`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Wed, 28 Jan 2026 18:14:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:14:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:14:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:14:15 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:14:15 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:14:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:15:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:15:00 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:48 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b34b5b8592bb3be88a87ba608937e91bc4eafdf037851a2b30c77121302a62`  
		Last Modified: Wed, 28 Jan 2026 18:15:46 GMT  
		Size: 52.2 MB (52175137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb2c40ff1aec727c0b125c7861b896e03f85d1edf46fbf0007d637227e3428e`  
		Last Modified: Wed, 28 Jan 2026 18:15:47 GMT  
		Size: 94.2 MB (94152541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be6c48cf430a1e3f2fbd9c1eeb7275ec878b00294d0a92d41d611b173b0679c`  
		Last Modified: Wed, 28 Jan 2026 18:15:43 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:222f028b68003e40f62fe833ab44cf10382f871190ccbecdfe7280e0b5236e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7608667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b83fba4c4d2415e5ed97311241d193e0b718876c4ef470cdacbcbc1babc989f5`

```dockerfile
```

-	Layers:
	-	`sha256:ad6204332a7c314dbec982ba7caefde24bd63fc2b1238e527c746c114c77d4b0`  
		Last Modified: Wed, 28 Jan 2026 18:15:43 GMT  
		Size: 7.6 MB (7594450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:723c9dcae89fae6eb69743bdd3be9dd893baa1fa0ecb7d8b52d023ff73900cd3`  
		Last Modified: Wed, 28 Jan 2026 18:15:42 GMT  
		Size: 14.2 KB (14217 bytes)  
		MIME: application/vnd.in-toto+json
