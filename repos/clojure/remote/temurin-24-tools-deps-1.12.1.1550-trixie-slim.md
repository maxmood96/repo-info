## `clojure:temurin-24-tools-deps-1.12.1.1550-trixie-slim`

```console
$ docker pull clojure@sha256:b4a5c19d86a662a0fab4253f1029c2b1a5a44377df9facc9c40be2ee5f56655c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b621d588ba86070145ec0c1fffa3f87f738e5466c19bf40a2b4f79d39890d10d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191526066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757277edb65025f6d9d65835f3c2fe7a970d271eb7fa8ad86cf7b5e7c5e7adea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f7f88c6d7f710176d487a3ac59c7790f981832a06bfc197dbe4a74d73b1407b7`  
		Last Modified: Tue, 01 Jul 2025 01:14:56 GMT  
		Size: 29.8 MB (29761106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0015bc7fc37f715a18180beaa3086cf2effb579c6c1d51ef9f9d130be1b28b3d`  
		Last Modified: Wed, 02 Jul 2025 04:17:45 GMT  
		Size: 90.0 MB (89952014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871ffa38a1b194cb317be0de83b3acf7b1b2ca01ca7cc0c039e784c259e755d2`  
		Last Modified: Wed, 02 Jul 2025 04:17:43 GMT  
		Size: 71.8 MB (71811904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007bfe5df4af320cb5ba64f6bbfe96810fd1d736303879049b5891725ebf8d4e`  
		Last Modified: Wed, 02 Jul 2025 04:17:32 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec973eeeb72d2d5e7be60f9c06d54cfde59f3771b9b9ffeb2455d49c7527865`  
		Last Modified: Wed, 02 Jul 2025 04:17:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fc211039ac1e1322a93a14a2c73f7f17b2ca040c8bef05f97ab4d733221100d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b2350a926ce4f04e2b5b75f65836e82f16cfd0282ed79056a3032ebf7a909d`

```dockerfile
```

-	Layers:
	-	`sha256:ada113e57443eb08b19e44f2b10ff4a898f75911f90bb339b4fd0f62d666ad43`  
		Last Modified: Wed, 02 Jul 2025 06:42:27 GMT  
		Size: 5.2 MB (5203448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cfa135e6c0a021aac111baec1eccdac2aa2e2978a76099807e924561657474e`  
		Last Modified: Wed, 02 Jul 2025 06:42:28 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9fce3e0fe28cfb73aeea445f43164cba3c6fcafe02df1773d830dae6e587170f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.9 MB (190861642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91cb5370229ebecb6fc04b53820a96cfe2bb68a417cd0e432741a1c20dee2bcb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dfa10e860e0106510a14bae8331a4dd762d3d3737fdba0dbec102458f9853b71`  
		Last Modified: Tue, 01 Jul 2025 01:18:18 GMT  
		Size: 30.1 MB (30126864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92d6d30892453e80a56f796f38e73c496d83fe2671cf897d645f4de27027602`  
		Last Modified: Tue, 01 Jul 2025 12:41:18 GMT  
		Size: 89.1 MB (89091277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df85d80021add32cb5be17f143c9642c369d448f59518fdd4c174b934e7b4ad7`  
		Last Modified: Tue, 01 Jul 2025 12:45:43 GMT  
		Size: 71.6 MB (71642460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521ec431a64c974bc7ba131d9f094df417282614f4f9602f5d310ada9243786a`  
		Last Modified: Tue, 01 Jul 2025 12:45:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59ff7b58cee9e0325b960d8adc2340a08247289f21d9a020db5d4792a1a70e9`  
		Last Modified: Tue, 01 Jul 2025 12:45:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d035bca1f7ee5f18834a3afee5e032fcb7acc4c54ecec1c268c249e8ad24c71d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5225180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7acd1aa8f96fcde2a17ffcc104a69a691f1af8fa6c9b442adfc1f0dab5be7d2`

```dockerfile
```

-	Layers:
	-	`sha256:20e2ee538e72530df4ea25c98c7b4ec82fa7e28c88b080fefd0a2a9469ee9013`  
		Last Modified: Tue, 01 Jul 2025 15:41:16 GMT  
		Size: 5.2 MB (5209214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a67f945ef446f8f3bbc78eef7998d56e7e755bdaad7ab41f436e201d9ecedfa7`  
		Last Modified: Tue, 01 Jul 2025 15:41:17 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:8a439e01d5c90e5ad04de16c536a1977e25850293774efa0e83b1d298c04f5c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.7 MB (200740408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94dcd63bb78bc3a168b6f6769430417dd2560e0a879ee8009e1d731d30bd4daa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2adebcab7d76ecb14ead3f70af8ca34e5abca513c2fcbd9f40e3af1e18442ccc`  
		Last Modified: Tue, 01 Jul 2025 01:19:23 GMT  
		Size: 33.6 MB (33586035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f033aadf173c9e16eb63bfd0af244c1b0e5ad9842fb8f6f31f94cff732b556`  
		Last Modified: Tue, 01 Jul 2025 09:15:10 GMT  
		Size: 89.9 MB (89920248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99ea2ad41d4f1f069be0ab574f8eef41647d93a8fe1c7555cd49b9e81c3fb88`  
		Last Modified: Tue, 01 Jul 2025 09:22:10 GMT  
		Size: 77.2 MB (77233085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37732d867082ed7863c81613cc25da887249c5fdbc382e3a8b2d270cfe070d03`  
		Last Modified: Tue, 01 Jul 2025 09:22:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6796ae5aa5b80e3a55799481ac6c5ea27e7f4085cfe1e850e1dc01b2224aa9`  
		Last Modified: Tue, 01 Jul 2025 09:22:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:432136fc3081f8d793b7925f9dec8eb322cd0ed73f4123eafff8463599787240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5225011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6c1075631c4050d6e9122363ce4b85bf13d6e9b606fbd3dda944804665bd6d`

```dockerfile
```

-	Layers:
	-	`sha256:49f21ce0b61f69d875638a6005c0e69927d5f33e809862be52740400d49460fe`  
		Last Modified: Tue, 01 Jul 2025 12:38:24 GMT  
		Size: 5.2 MB (5209117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e40b03cb315931c8c418a535497a7b6979c53eacb52e8a591396ebd161966691`  
		Last Modified: Tue, 01 Jul 2025 12:38:25 GMT  
		Size: 15.9 KB (15894 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:61df406bdfe3f40f7d40909e776da035183d56e9bfffb80c633aa39f66b02805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186585241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53f4311dc824418883c762c5c5a193bfda25578b4b08be3fbcb6145044c6801f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:43faa9a2f25436afce0db8221e3c0e223102f73a33b0cd47eb32294e8033b203`  
		Last Modified: Tue, 01 Jul 2025 01:24:44 GMT  
		Size: 28.3 MB (28258970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e419a52d0b7166273c72df76079f5355fbec04834338cef62e248098795964`  
		Last Modified: Tue, 01 Jul 2025 03:38:20 GMT  
		Size: 87.6 MB (87622190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221ce50f66674be00315dd597a9ba0619b4d03cc4a9e3b0a29b79d72f94fc660`  
		Last Modified: Tue, 01 Jul 2025 13:33:49 GMT  
		Size: 70.7 MB (70703041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbaeb3fe04ed18d59eb78420e9ac30b77b5e4045bcb6837b9664c738c8997f1e`  
		Last Modified: Tue, 01 Jul 2025 03:52:03 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e01c12d66a779847342407289af9795654f3e4ccde19606d2c996e8319321c2`  
		Last Modified: Wed, 02 Jul 2025 09:42:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1552691c298feef4484782713d7c47eec28fde14751188eb2b2403de438879e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5208805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b8626b3c625df993ddb06d9bcae267e35462e908a44082d62251b41e3189ac`

```dockerfile
```

-	Layers:
	-	`sha256:5f2bf5cf89b4d6304449ba288ed6ea9b78b84507f2d0770acfb1651d17485584`  
		Last Modified: Wed, 02 Jul 2025 12:41:07 GMT  
		Size: 5.2 MB (5192909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e77cd5aa81a384f2e7bfd9885384b9b0124c71e917343a70b5c4523ad7a0e6c`  
		Last Modified: Wed, 02 Jul 2025 12:41:08 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:7e595e132bf8a4dbd02d58e4d6e89115be4ccee87f11679dd36e81ea10383ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187858711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b034417b6a2ad466bdb0e389e61627aa2799cda4609c744486159f80a25bd42`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:728fbd29b8599bd56dcb8703b5c428523bcf0f3d48c5e95804f60267a128a3bc`  
		Last Modified: Tue, 01 Jul 2025 01:19:25 GMT  
		Size: 29.8 MB (29838345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105179baa40c85d8521707990861ebb0b6d40818c639c5026c7c305780a59f4b`  
		Last Modified: Wed, 02 Jul 2025 06:59:58 GMT  
		Size: 85.2 MB (85216920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbe8d94aa1e4e27e56a191778e7abf5a4b11f0c53303cbc029fd2939c30efd7`  
		Last Modified: Wed, 02 Jul 2025 07:05:09 GMT  
		Size: 72.8 MB (72802406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ae8094c12e550ae637b2cdc0182763279cd3c33754387bf5f806c96c897350`  
		Last Modified: Wed, 02 Jul 2025 07:05:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ca1265b158c43561dfdde40b5cf891bf2ec490a3659d0c2a55c4cf35ae4d2d`  
		Last Modified: Wed, 02 Jul 2025 07:04:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:159bb3820a7002731e50aa042a7ab20d29f80be1c931d9b7a210e9e95e4ad70f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c46404e6ba9e1307f9b8d88275bd99d7ef531e302bf41b1097cb13b06051651b`

```dockerfile
```

-	Layers:
	-	`sha256:c1d17f4137475d8239d8003f86976933223ec4202b851443a7926ec4de0515fe`  
		Last Modified: Wed, 02 Jul 2025 09:41:45 GMT  
		Size: 5.2 MB (5201920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb4c63df7519b119bb7d05e0224447fdf772feeff9feb0c6e56d1a79266028bf`  
		Last Modified: Wed, 02 Jul 2025 09:41:46 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json
