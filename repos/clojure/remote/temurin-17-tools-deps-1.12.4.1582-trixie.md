## `clojure:temurin-17-tools-deps-1.12.4.1582-trixie`

```console
$ docker pull clojure@sha256:a1653f7c3ccd399164805ac9627974eba7f372ce859cf7e64004efba703f1866
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

### `clojure:temurin-17-tools-deps-1.12.4.1582-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:15e7721fe7bffeb6e21325e9718d74b751c164dc12d825ee27dd53976d9a716a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.7 MB (279681542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653a42b3c12ec1764bccedab356a9ff7e5ac9bc61fc59dadda3ccde56d382d5d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 22:38:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:38:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:38:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:38:32 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:38:32 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:38:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:38:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:38:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:38:51 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:38:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fdecf58a0f913fd2991e9c16cfa98509d20f867d97eb3a479d9fa49fa7f5e1`  
		Last Modified: Thu, 11 Dec 2025 22:39:34 GMT  
		Size: 144.8 MB (144847947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6a2f828d8910cd0315374b2a4e9837f59128bbc2417111dcbc1610d4c3c5f5`  
		Last Modified: Thu, 11 Dec 2025 22:39:33 GMT  
		Size: 85.5 MB (85543035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf43d4282e4e831ebf268ae7c9bc0283a48c2c0b8b352e2e5343af50c07b727c`  
		Last Modified: Thu, 11 Dec 2025 22:39:24 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948f37e535a1c8dcb1de4505ca4b270b4ca00f8305a97cf1a34f054a695b9888`  
		Last Modified: Thu, 11 Dec 2025 22:39:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1582-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:96295e5c6e34189a34d187d42a7f41837c48eb3b29dfdaccb3267573f8b71912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ab2db0b7e67a13b52322f892c64b63b50424ce6e5f8fdcf5ab6a222e0a476f`

```dockerfile
```

-	Layers:
	-	`sha256:41563d5989b55307e638a91789fc8e6bc65ad8139c1ed2766877d5a5c24fb6bd`  
		Last Modified: Fri, 12 Dec 2025 01:39:39 GMT  
		Size: 7.5 MB (7466931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1a3fd64513628c1cca4cfe71f70adebcd0e70bef1c661c474867f1c302a31ac`  
		Last Modified: Fri, 12 Dec 2025 01:39:40 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1582-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2b3c6709e0d5d82f2d684fa6db3758c7e754344cc6ed47a4cfde74513bf93a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.7 MB (278692692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d7336f7d9a9b6396d2c5821baa453aa5e23a910e9207d13db3d733abb3106ff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 22:39:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:39:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:39:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:39:51 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:39:51 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:40:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:40:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:40:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:40:09 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:40:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d88ef0e7990a7816c9bc9a3a9049927b943030d19695296015586d30659b85`  
		Last Modified: Thu, 11 Dec 2025 22:40:49 GMT  
		Size: 143.7 MB (143679920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e6cdff111b4df2f0c89c8056d90af1252a34358c9ecdbb73cde24f9d80f03d`  
		Last Modified: Thu, 11 Dec 2025 22:40:55 GMT  
		Size: 85.4 MB (85361504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc4bd4118115959df8810ef4874d6f031ead3e2bb4fd6a2b77b14e9369b9b21`  
		Last Modified: Thu, 11 Dec 2025 22:40:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66114c49f25980e37cd625d28b5b427ff024cf7d1b5c873f0d3d1528e35bb80`  
		Last Modified: Thu, 11 Dec 2025 22:40:40 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1582-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:729b5c47646bd9383628e99ced9d514801cec8cf08ab1dfdb4e1e9409969ab8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2ae6dc09513f0c05d1a532bcf18050e4a5821aeb0b65bbb711ff1b9b5fcb5f`

```dockerfile
```

-	Layers:
	-	`sha256:792ceadeae8b02cc911ad99c3403244d641f59bd0c41419dde16732d746ceaf4`  
		Last Modified: Fri, 12 Dec 2025 01:39:46 GMT  
		Size: 7.5 MB (7473961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7d7491f911225fe3470781264ef11fbf632dc7757f3861737d8b8a7906d21d3`  
		Last Modified: Fri, 12 Dec 2025 01:39:48 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1582-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:ce0a2b1d6c5595026848879ecbcf880c447235da88fb9da8398c745e64891991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288579883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4a9dd7baf11793247d6a81efd878edafba93ab6e13800b54d271e5da7dde37`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:27:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:27:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:27:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:27:14 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Mon, 08 Dec 2025 23:27:14 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:57:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:57:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:57:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:57:21 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:57:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a185af1bf60cf57d1da0f13bf5f3a56964ffa7635cc2b99d41cd3ba11696aff`  
		Last Modified: Mon, 08 Dec 2025 23:28:59 GMT  
		Size: 144.5 MB (144525284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1be896c74e771b2d6e11daa36577f763d9e8743e8188a1d49579ce0c567d48b`  
		Last Modified: Thu, 11 Dec 2025 22:58:20 GMT  
		Size: 90.9 MB (90945080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b38e733a4223bbc092fbe4a158ba79b0c5322e3c17530e7733674a12f8dda6`  
		Last Modified: Thu, 11 Dec 2025 22:58:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6240fe52ae5f8041763e20d264295cd49aa7ced7e1f47d85e0c31793807cedb5`  
		Last Modified: Thu, 11 Dec 2025 22:58:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1582-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8f4f4143c7705f673460e5f20a9228ad377a7fb2b7066847d2f9c6f0eb15a85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5179f3390ad00573f52da2fe8940ac26242f159f29040f559c490d6dec7abc13`

```dockerfile
```

-	Layers:
	-	`sha256:f6a123c1f551884fe7de83b2e938cbbe1f5b54327ac99a1505313aba4f230863`  
		Last Modified: Fri, 12 Dec 2025 01:39:55 GMT  
		Size: 7.5 MB (7471350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5338e97e2c2f9ed7cea7e088a3d9d7121fc5be124ec0c9de29fe564027e3a9b9`  
		Last Modified: Fri, 12 Dec 2025 01:39:55 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1582-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:bab7c49da34a444079bd11caeb5e73669660ef6d05087e89ac4ab24076e3d707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270714644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb25736120f15515122ae6320b95b3c62464ca2b823114e6eddbb3c8321faa55`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 22:34:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:34:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:34:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:34:17 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:34:17 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:34:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:34:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:34:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:34:33 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:34:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3f8967bef2f6a8ec916f7d3a0d528a6724093176621c5758addeeece50e41dec`  
		Last Modified: Mon, 08 Dec 2025 22:16:15 GMT  
		Size: 49.3 MB (49345908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefe4efd6cb1fe9f9256fb5ec095ce9fd2d8216620ccdc50d88e73bed4e27035`  
		Last Modified: Thu, 11 Dec 2025 22:35:26 GMT  
		Size: 134.9 MB (134859034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8a4ff9d77bf8924b21c9a591115ea837713dbba4a08edec60f1b40f378b59d`  
		Last Modified: Thu, 11 Dec 2025 22:35:18 GMT  
		Size: 86.5 MB (86508661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5778a17fd6c86e638caa41030020e6597141050f99b38d0f914a8c72871e427`  
		Last Modified: Thu, 11 Dec 2025 22:35:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1422c6868f24b82f6fffd167c838082bb7ac075c202ca1cc31ab923ccd101f5`  
		Last Modified: Thu, 11 Dec 2025 22:35:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1582-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4ee0a5d90e0385de7d636771e94093702e76eabb621f3cc60eff74411119a72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7478607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446d19384d1473cdcabde95ad46cc0fbef2a3f4106f4363518bda6f36e184e48`

```dockerfile
```

-	Layers:
	-	`sha256:d86ecb351b99075f30ed7f7674d291c8a5fcd4899b7c1b70c8d0a31742521e32`  
		Last Modified: Fri, 12 Dec 2025 01:40:02 GMT  
		Size: 7.5 MB (7462853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53cc89ee5cd93c08a1442d041cc5326d08ee36259ceac41cd8b625e19ae998a2`  
		Last Modified: Fri, 12 Dec 2025 01:40:03 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
