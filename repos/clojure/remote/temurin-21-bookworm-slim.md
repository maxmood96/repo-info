## `clojure:temurin-21-bookworm-slim`

```console
$ docker pull clojure@sha256:eed3f72d8d9e7516c95f0f643e20f6b826a58d20e42c4692d28b2052a75cc8a2
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

### `clojure:temurin-21-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2e35d5da8e2971abd187cb06fd90bfac4f15c65bfc1466a10b49f1b4c3baebba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255735178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d12171d05e74566b664e13631b40ba2825d98e719d6307ddd3ab7bbc4d9452a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:44:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:44:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:44:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:44:50 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:44:50 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:45:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:45:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:45:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:45:04 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:45:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a208f7eec0cdce48d6ccc4057e16ee570614c0e29ee999581a0fe64b2b9cdd24`  
		Last Modified: Sun, 09 Nov 2025 04:30:07 GMT  
		Size: 157.8 MB (157825974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2153e354066ebf2c42e5888fd0b055ebad0bdc51e8f857aad4c31fc9e63d61a`  
		Last Modified: Sat, 08 Nov 2025 18:45:50 GMT  
		Size: 69.7 MB (69679594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd362c73c820ba46c0d43b74d30b1cc52e7ca8d05ab8c3c313b212d6d795ed6`  
		Last Modified: Sat, 08 Nov 2025 18:45:44 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2dfae7dd4aeb2f021998b39765441ffe08415de8b1cf908bb47fbcbe94bc2f`  
		Last Modified: Sat, 08 Nov 2025 18:45:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:31a53635f44700d80cd99b2a26a3ed1704537fff6c211a1220443bcb0e8d9a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd68e9f58a5bff72381a25c34c3cee31d9119ab4548354be6b297695456ba36`

```dockerfile
```

-	Layers:
	-	`sha256:66e9eb84caf86e871eef615ffe5123370676ee611b52e32b40984cd154fec25d`  
		Last Modified: Sat, 08 Nov 2025 22:46:09 GMT  
		Size: 5.1 MB (5116492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2a7066ee1db89d31eaf56023507048dd406c2cde089b20be25fb1bf10830772`  
		Last Modified: Sat, 08 Nov 2025 22:46:10 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:49ed955d5dc258d9b248c5a1459ea2c595f87f5786b43cd1cf694d562a8a8911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253771328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44fe78b3f3468d80c02b0fac883db90cd492113b9bcf64c9230f91351b361a43`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:44:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:44:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:44:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:44:15 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:44:15 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:44:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:44:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:44:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:44:30 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:44:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e351ee3325f67ae978822744f1608b970dc8df180579a39566e3ead662746601`  
		Last Modified: Sun, 09 Nov 2025 08:47:33 GMT  
		Size: 156.1 MB (156107649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606f9a1fb2a965b63ac4e3b7da7b3fc32e425c26ee6f12a1f11f840c909ec7b9`  
		Last Modified: Sat, 08 Nov 2025 18:45:19 GMT  
		Size: 69.6 MB (69560256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927c3afaff5b2fe78e1ea3d62b001650515323a76bde5597ccacce01854dcf0d`  
		Last Modified: Sat, 08 Nov 2025 18:45:12 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e79be585354c33f3b74be5bae7d6f8342f30312cdec9c19afb0417c4638c27`  
		Last Modified: Sat, 08 Nov 2025 18:45:12 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:699b820a112eabe39f80c46eb29d0f3a07f8276dfed07d591a1ca06e19c9d06b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68103c67392ecc44f3dfe00013316bf73ccc7e556162044965421dd7a6e4147`

```dockerfile
```

-	Layers:
	-	`sha256:c5d811f27434e7109f4df8f40f15617108d923f5ef32fd62941d7d7891ec73cd`  
		Last Modified: Sat, 08 Nov 2025 19:36:09 GMT  
		Size: 5.1 MB (5122253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e79121cf958c204061c6907155bb3e4d27b9f43ab32039fa8b6c218887722e9c`  
		Last Modified: Sat, 08 Nov 2025 19:36:10 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b12a215bfb8a39c36fb056ed06fb4a5d968bc18488193c685256d82de4954f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265526201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756beb3b3a8e89767bbce8f80d6065ffc5495a1d8e67262eb510501832edfbcf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 21:31:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:31:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:31:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:31:35 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 21:31:36 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:39:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 21:39:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 21:39:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:39:49 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:39:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944218b16390f9d8d7ad4ec3d5e2b435f5ce7651679065a781dd9f5140c7a7e0`  
		Last Modified: Sat, 08 Nov 2025 21:32:50 GMT  
		Size: 157.9 MB (157942933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e922bd26c61ac028a26e9066d9b8301e8240a4b7b170ecff6f3244a3873a21`  
		Last Modified: Sat, 08 Nov 2025 21:40:37 GMT  
		Size: 75.5 MB (75513320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0b93f29b7d504a0aa2630dedd1c1d66f30621b199c8bde5afa7b709eaa2cb8`  
		Last Modified: Sat, 08 Nov 2025 21:40:31 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba724ab1d0fc6b5808a1df80e7eb5aa0bd6ad900be1724b0b9d54429009ef47f`  
		Last Modified: Sat, 08 Nov 2025 21:40:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e1e7020c2c25b67632cee34cc4ec1e92f4c7708f0e7083dd38cd89edc9c7d67d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a221716abf52bc833535f8114b23e835f35767fc6d51eb179dc6c4b0b960dc2`

```dockerfile
```

-	Layers:
	-	`sha256:74a33e6e570fa7f92e52e6ff574b2e2384b68fab57bb9bd35f0afe0637b9ebe4`  
		Last Modified: Sat, 08 Nov 2025 22:46:17 GMT  
		Size: 5.1 MB (5121650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e7cf5f796be7cd009571f2db601073859f28cccd07fd72be29b1fa449b2c747`  
		Last Modified: Sat, 08 Nov 2025 22:46:18 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:0c1e8d9c425e600b5f987a9a4f210238829befce96df23eed39e9117c4bd78d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242446065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282b47036582c0f7de6aa902efeee0a94952892cffb81d7ad34b126b8151b0b6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 20:28:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 20:28:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 20:28:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 20:28:38 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 20:28:38 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 20:33:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 20:33:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 20:33:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 20:33:32 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 20:33:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179ec4598348efb229bf449e5b14947188b3aa2ce7fd6f3f7718376a0bd1679e`  
		Last Modified: Sat, 08 Nov 2025 20:29:16 GMT  
		Size: 147.1 MB (147069879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4420faafe2123c9f322b76140ea344f340517ce136d871fc472f8c03821878`  
		Last Modified: Sat, 08 Nov 2025 20:34:07 GMT  
		Size: 68.5 MB (68490595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9d0387877f927391d60d3906f46c054505b2438ae96245c228b81ad0143ece`  
		Last Modified: Sat, 08 Nov 2025 20:34:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc3f30bfcb0c943998b1acebb87ccd0ee223f65cf94e738eb19a8a49843d8b2`  
		Last Modified: Sat, 08 Nov 2025 20:34:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:362947c037d1d9044111ffb428dbde6d152209e958489740c2576658a7d7c996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf12df7bb604bed7d662adfbc4f0eb01e5f629278d830508df45e7db36e47df`

```dockerfile
```

-	Layers:
	-	`sha256:c05b5f880c1ac8f8b8a77f06190b633902bdc6dc0184fad509db09081774bb8e`  
		Last Modified: Sat, 08 Nov 2025 22:46:22 GMT  
		Size: 5.1 MB (5107813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be70b5f318d6782d4f3d33b4f2ae3a183ae85d46f16ca41fa8783129f41dc856`  
		Last Modified: Sat, 08 Nov 2025 22:46:23 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
