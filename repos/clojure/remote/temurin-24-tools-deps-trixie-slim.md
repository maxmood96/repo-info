## `clojure:temurin-24-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:fcb3b2fe8cbe84204c7168162e3c433dc998f4326dffcaf9fdec3760176d3e24
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

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; amd64

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

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

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

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:743b3b228ba9de87c0f86b13b647e078f79bbc382195bf5a296bac1bc2150b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.9 MB (190861548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aab22fa0fe58851a606b8c73fd7c9e346032934b94d7581a10c320e9ac620d8`
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
	-	`sha256:5e3b7a4767010fa7ce7cd79c35e00c69d2fb559ce69f151a063ef94a08d5a77c`  
		Last Modified: Wed, 02 Jul 2025 13:00:18 GMT  
		Size: 89.1 MB (89091235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385972b9c64e1fc79575103bed0240bb8d5c1cddaf2dd0f8187311a5599b71f5`  
		Last Modified: Wed, 02 Jul 2025 13:05:53 GMT  
		Size: 71.6 MB (71642408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18397e85582c8d2bab8f464575eec1b8d60396b2f430c9bb84dc7e51d97eb097`  
		Last Modified: Wed, 02 Jul 2025 13:05:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16fccd1a1a25546c4f62cc9167bea6fc9c1a599a664f5ec58cde2ec10983ecb`  
		Last Modified: Wed, 02 Jul 2025 13:05:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1f9e21acb221a57697f569d48679720cb6bc12b8671396faac298c31bf5b23ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5225180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d38f4c8d8d1bdc2be515ef61aea7d57afb389025355858e75a0521f3033f821`

```dockerfile
```

-	Layers:
	-	`sha256:26f61509a07e9c95aab871e341a62bad1ad0e1afab404171b11fa10428dd40c2`  
		Last Modified: Wed, 02 Jul 2025 15:43:49 GMT  
		Size: 5.2 MB (5209214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02cdb0901cbb9fa986b883eaedc1036e22b6af20b35845f66c0b26d59622fab6`  
		Last Modified: Wed, 02 Jul 2025 15:43:49 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:7a369bb29af922363e6e8caaad0defa8574e654af131afb8da935562b8c8b18a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.7 MB (200740538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e7b0da39514d4bc0ccfd9a4c5544aa7242df0bd7f37cb3f460ee352970d63f`
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
	-	`sha256:aa7cbb5f9536c9aa24563a8b209f3c1b094fe9b850aa3b8889a2d17239db0d7b`  
		Last Modified: Wed, 02 Jul 2025 14:09:45 GMT  
		Size: 89.9 MB (89920270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9f1e6b22d50aec2da4dbee8cd8c97036807e18b2f24d7b700403c0e0d0c051`  
		Last Modified: Wed, 02 Jul 2025 14:17:39 GMT  
		Size: 77.2 MB (77233193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d476d88b03d7f8a95f4659f08d79b9167addc06c09a29c0c6ba212e39fdd7c`  
		Last Modified: Wed, 02 Jul 2025 14:17:33 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348516db0f78959b2c1b679e8862b660a4a8263932c06ed3c122b401704667b7`  
		Last Modified: Wed, 02 Jul 2025 14:17:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:05c6999e4b3b99b5171495f0eba719ecacdc05452bb537581298b1d886416189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5225013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2669d2692b487fd4c6e0e48a9af8c658a7af39d5d6899e396792f3502fbdf11`

```dockerfile
```

-	Layers:
	-	`sha256:5a27e7bf363e60de6cc345a441008e96641bd33f7b327509907c4cedfd00906e`  
		Last Modified: Wed, 02 Jul 2025 15:43:54 GMT  
		Size: 5.2 MB (5209117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8842ed0e4ed288c138f970aeafaffdf1a5a2cf46708b456d6ecb9ec5c01e0d1a`  
		Last Modified: Wed, 02 Jul 2025 15:43:55 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; riscv64

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

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

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

### `clojure:temurin-24-tools-deps-trixie-slim` - linux; s390x

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

### `clojure:temurin-24-tools-deps-trixie-slim` - unknown; unknown

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
