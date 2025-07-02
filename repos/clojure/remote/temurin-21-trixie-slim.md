## `clojure:temurin-21-trixie-slim`

```console
$ docker pull clojure@sha256:064a33845c0e4703be77508097daadbc22f172efd41430f7813557165768ea65
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

### `clojure:temurin-21-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7b6f5c48b17cb0c1e2b0bbcc7e481e94b1de5336a1499ceccd82a086aa2935f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259208522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c66d6732c3e6740ba974e55e082cd217a824e0611e3a165cb02726b5fd0d0de`
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
	-	`sha256:1fbf043a204d12486f78a57a85e3b8c30cae9beadc95c3a9ad6feeac5480e8e1`  
		Last Modified: Wed, 02 Jul 2025 10:48:08 GMT  
		Size: 157.6 MB (157634482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3caebc59988175135dfbc46fcbf2e2196be6a688996a30991c7ffbb2437e0dc0`  
		Last Modified: Wed, 02 Jul 2025 04:17:19 GMT  
		Size: 71.8 MB (71811896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a0dac1d9f7cd5ec78f93c97fcf949d411e0eaf393f179cef85f5b202ba44d7`  
		Last Modified: Wed, 02 Jul 2025 04:17:06 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9853b06964755001923b1ac56cdbd81cfa99c17fa2d15c07acd46437c0055c1a`  
		Last Modified: Wed, 02 Jul 2025 04:17:06 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:38fcaea237c50965f025413cadb5226f2470426e2a1a7b1b6222466b639aad88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049fd943aac8cbc1b977c1f9e3a000a0bef05d678378b32e4e5a3219748fec47`

```dockerfile
```

-	Layers:
	-	`sha256:3ad3e2681522368673a7de68ea0b8a342f4706c11849c1207d3eac70f2e67867`  
		Last Modified: Wed, 02 Jul 2025 06:40:37 GMT  
		Size: 5.3 MB (5256592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd742319ba8681da1aaf5f0570c70bf9f7ccfca9ca42a534a2214560d66cd597`  
		Last Modified: Wed, 02 Jul 2025 06:40:37 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:df41775c3520cc231ae77a1ed18ad09abbf145dad86ddd2147561bc0c7aa252b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257698834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0103ff839f4f0869f5f23d41cb963ad8238f72ba7afad8d5738f4c45c8e1b580`
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
	-	`sha256:21d31faa879a146aae980797b2125120f4100672ca25324e21a59003f7535eaa`  
		Last Modified: Wed, 02 Jul 2025 15:50:35 GMT  
		Size: 155.9 MB (155928828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4e70a1886cd4971495383a36cf1cc25c0017da8c8df1ad6286e75f1caecac6`  
		Last Modified: Wed, 02 Jul 2025 12:55:05 GMT  
		Size: 71.6 MB (71642099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b65c6b11177fa7f070ac8a4eb11bb96f42f77d17d9736d62d9b30a8fa516f14`  
		Last Modified: Wed, 02 Jul 2025 12:54:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ae66797b51bb7714cd452f2b5968eb809435e3a4e1b242fa0fcf458b92d5c7`  
		Last Modified: Wed, 02 Jul 2025 12:54:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e3df874143647dab4a5fb01d7ddd3a24a8291e184ead4160e81d313a8f0ac07f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911831e14c8e6d83b1701bb9d9677163e9774d6eb9a8e69a354e7c532834e7c8`

```dockerfile
```

-	Layers:
	-	`sha256:b3d4b133874ab3e1f46cfae1ad2e408e49b15bc51cd58c1f9c846f4361a59021`  
		Last Modified: Wed, 02 Jul 2025 15:41:19 GMT  
		Size: 5.3 MB (5262385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a43a00edac4f25798fb378f2454cd1f798e35f9ea33d2ea9e9e3b05f764d3d4`  
		Last Modified: Wed, 02 Jul 2025 15:41:20 GMT  
		Size: 16.7 KB (16685 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:eddc3e8b1cd65ad34ee06e416e4519631e93d35763b1872ef16ea48a82137e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268625055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8739816eb50439c3f2a9ce0c78732a1baade8874bf95d7ea519b7555056fac50`
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
	-	`sha256:ed91bc72e61d8832f891aab0bbce5f27ae299c7863f8f1f581b96db6ff4a19af`  
		Last Modified: Wed, 02 Jul 2025 13:59:37 GMT  
		Size: 157.8 MB (157804902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f96318fc15e0706f6f9f70dd906e23aa332eb736dc706194318305c97ef1fc5`  
		Last Modified: Wed, 02 Jul 2025 13:59:36 GMT  
		Size: 77.2 MB (77233075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be17ab3e61ae9d29e34b7c24f3adb0754cdb7c0797bbae2f4b48c7d3205698a1`  
		Last Modified: Wed, 02 Jul 2025 13:59:53 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517b896ce5b3bcb36351b3e67ea077ab013d66edd94199d3a33f7a8e4c93b6d3`  
		Last Modified: Wed, 02 Jul 2025 13:59:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d98a63a16e2638439af78c7870cd248d319e93353149c9d59748506d2661d812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad27c4eaa8b404cd1f37cb134c14d0cbe7901e21cb5d04cd847af9d3becd8487`

```dockerfile
```

-	Layers:
	-	`sha256:c70b27d12269927e11794febb6eff9980340a094d6e2207d7a7ec34016c43a8c`  
		Last Modified: Wed, 02 Jul 2025 15:41:26 GMT  
		Size: 5.3 MB (5260975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4001c44d30a7f046af98b1305f1c18833aa832e28d2fdb0558068881dc7feb9`  
		Last Modified: Wed, 02 Jul 2025 15:41:27 GMT  
		Size: 16.6 KB (16603 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:1ac96ae4f54fea0d36d5896bf440d3b328d8c1ada644912062c57a53d270b220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252413180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2affe77e67b92644603242616424718f2c9f16499bf05040a1a71d09c65be548`
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
	-	`sha256:8616f7bedb56894be7fe53d122ffb03b37e9993aa4c114656ea59dd01cb38176`  
		Last Modified: Tue, 01 Jul 2025 13:21:21 GMT  
		Size: 153.4 MB (153449650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af318ab6a70500e9f73e09addf22a7ee42a01065a08d029534a1d7116e26517b`  
		Last Modified: Tue, 01 Jul 2025 03:25:15 GMT  
		Size: 70.7 MB (70703521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7559d357ed5b8676e56512a4bee290f27190afb11f0e2ea7a4c9ab9adb65bf4a`  
		Last Modified: Tue, 01 Jul 2025 03:24:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fa98c0418182edc7954796ed932dbfe8fbd7710346465e212c4ec40d9cd090`  
		Last Modified: Wed, 02 Jul 2025 09:20:06 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b0a5a033446819e7efb971474d05ea1f14e69ed422d00b7405976c0415584e51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5262671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d5bd4802626b47432cf04fe174e8facc285a8e4ce3cdd3b9d1ae89a5215f44`

```dockerfile
```

-	Layers:
	-	`sha256:81b5631fafb1b62288a6c8e89cfca1ccdab2f288beec75c4a5d9cfb068180b59`  
		Last Modified: Wed, 02 Jul 2025 12:39:55 GMT  
		Size: 5.2 MB (5246068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e83e3acdbcbaacec59ad21270359b6088201512a20de51dd8bb80b5a73f62d58`  
		Last Modified: Wed, 02 Jul 2025 12:39:56 GMT  
		Size: 16.6 KB (16603 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:e7e560ca52226cc68581fa910e16fdd55d6594a11e2c62babf07790676a60b5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.6 MB (249552776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f1cc3d4c5faf90eeeb9dd4aa3ca80afc12ae369c880f9cfb442343918e8066`
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
	-	`sha256:0a3de81f4a29affad19a69c6ea53405aab7b55e447a36696f72bcf8c5ff83f16`  
		Last Modified: Wed, 02 Jul 2025 06:49:21 GMT  
		Size: 146.9 MB (146911007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744d75a25197dc35b5be858fd176b5d2c89d99bb30812a0a5cde2cd7acd5d139`  
		Last Modified: Wed, 02 Jul 2025 06:55:02 GMT  
		Size: 72.8 MB (72802385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accdb3c0b9f6c2e3b93de053b294ebed00037a50b0fa1829ac00529b0d7781d5`  
		Last Modified: Wed, 02 Jul 2025 06:54:57 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a213f6638ae4f3a230c3b203b3e59781b80e01bd39a822e9a216a76dc915ce1`  
		Last Modified: Wed, 02 Jul 2025 06:54:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:664c14df8f2cac3bfa438da6229cd5c89f1a342d9b6b2e421dcffe14236f995d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5269058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36522f84219bba176ad59f3f99839014af59b3a0d56faf57206a4d98c6ee131`

```dockerfile
```

-	Layers:
	-	`sha256:6746f8c8005ba18138207bad45257890566591c39eb68f4d71f68a6fa1348814`  
		Last Modified: Wed, 02 Jul 2025 09:40:12 GMT  
		Size: 5.3 MB (5252516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aad6df8cc155143f8d76de5cd6ac137029dd97ad753e8d2fbe52db146af8ba95`  
		Last Modified: Wed, 02 Jul 2025 09:40:12 GMT  
		Size: 16.5 KB (16542 bytes)  
		MIME: application/vnd.in-toto+json
