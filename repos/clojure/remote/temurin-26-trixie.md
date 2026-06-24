## `clojure:temurin-26-trixie`

```console
$ docker pull clojure@sha256:b00f6c7138cd76f1257d9c744e5e0bc4e863465543cea5c2170a2e17ee358dab
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

### `clojure:temurin-26-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:e5ebb5657fd736c3dd6dbb735d7610b4202f17912025a2450e19eeccb7ee19e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226361568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d639d71f4749fe4f2b850581b1405cfc9973909c934976cfe37a0608d58c36e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:23:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:23:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:23:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:23:56 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:23:56 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:24:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:24:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:24:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:24:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:24:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aa3e9ef32f73c30e8b065800ee66429992d3bfea6a1fb8224afdd878ab5b994f`  
		Last Modified: Wed, 24 Jun 2026 00:28:33 GMT  
		Size: 49.3 MB (49317255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f0c90772fc8a120f9d66aee0b56df6d6042b0d670f90605b2147f30e63d2c4`  
		Last Modified: Wed, 24 Jun 2026 02:24:37 GMT  
		Size: 94.5 MB (94524352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f83693e7d3b5553b00b689ef76a053a3038cd131f88366673e5e83f37f6456f`  
		Last Modified: Wed, 24 Jun 2026 02:24:37 GMT  
		Size: 82.5 MB (82518920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e7b6af958107990944622ab9b0c105574267eb8dca8c3ba48402199083be5a`  
		Last Modified: Wed, 24 Jun 2026 02:24:32 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d580b91bea4a3b425e9e2bb0999fe4be5ef87d05ed0f731b44a543befa8c98`  
		Last Modified: Wed, 24 Jun 2026 02:24:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fabf2e7ba6e90e2d5a21c13468ebc04afb2ad9a3b085b3c0693a2f8c2e4cfa0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7449563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6b1b6699e196d9888001e0e1e4d5d8925ba9dd2fbaedac9d2f6d90a4de6bef`

```dockerfile
```

-	Layers:
	-	`sha256:05b392355a989fc50327cad563e18249a7f16164a53c714adfb23f3927c5425c`  
		Last Modified: Wed, 24 Jun 2026 02:24:33 GMT  
		Size: 7.4 MB (7433662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d49d2d92530f2eb90b29bfc64a317f326f3744ee2b6e0bca2ec2903c4e17cb`  
		Last Modified: Wed, 24 Jun 2026 02:24:32 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1eb393e164c5c77cbccafa54c14f2244a746bea77930d8991f41fba1e6171542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.5 MB (225522011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c88f0983e480016bb8fd94059b2f96dc17720c5cee91d77c79bd762a9e295d1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:30:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:30:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:30:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:30:16 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:30:16 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:30:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:30:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:30:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:30:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:30:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c8a311258fd162f6aa0db134045a19154c81a2244ff9ed7620256c95ae5d6b69`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 49.7 MB (49678395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b95e544d6ee236be6b35d07742ab22e118a15e53f5e6261b6b89a026e00ecc2`  
		Last Modified: Wed, 24 Jun 2026 02:30:58 GMT  
		Size: 93.5 MB (93504362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f88f1404f3de841cc1fce5635b8278eb9572d0b5aa0443c2dc5479abbdfce94`  
		Last Modified: Wed, 24 Jun 2026 02:30:57 GMT  
		Size: 82.3 MB (82338212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5bb1d9d33c9e52ea9dcdd3bf4451201cc8420f40714ca8cba64d07bed5b6f8c`  
		Last Modified: Wed, 24 Jun 2026 02:30:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6198643564331cf387dbb62ebed51ed5c2a2d7c9f7a3bb2fd4840e69b4d65f40`  
		Last Modified: Wed, 24 Jun 2026 02:30:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:62a8399d2a68ab1a3e2e7cc9832f4667d151fc1ff8ea7eb3d16c9f7f72b29b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7456071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19e643188f92f1d2a5d39dd3811f46f92f87ba581ee866a82e2000585264076`

```dockerfile
```

-	Layers:
	-	`sha256:b12c566f1100178a5456759da1cc4899b81cdb2b1d9d2081541ddc59005e4b8c`  
		Last Modified: Wed, 24 Jun 2026 02:30:54 GMT  
		Size: 7.4 MB (7440052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66a8030e41b42885197ef5adc73f4170279fded3ec86adece9954750817fe540`  
		Last Modified: Wed, 24 Jun 2026 02:30:54 GMT  
		Size: 16.0 KB (16019 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:b1fbff283e4e78142341de318e3c3db317ee3101696727785d3921fcf54b7253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (234979734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8905fac51090fa8d1f83a7b4e6f07f3a57726bc0c2db65f96d1f5541a046d69`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Wed, 17 Jun 2026 00:14:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:14:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:14:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:14:41 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 17 Jun 2026 00:14:42 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 03:02:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 03:02:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 03:02:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 03:02:07 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 03:02:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328775c3b052bb498a48836eab308724b02180a01e1a5397b2235df60a8765bf`  
		Last Modified: Wed, 17 Jun 2026 00:18:19 GMT  
		Size: 93.9 MB (93902081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856bbc9642d3749f9fafd01caa9367cf6d7cc51aeeda7b5534fec5814a5b6493`  
		Last Modified: Fri, 19 Jun 2026 03:02:51 GMT  
		Size: 87.9 MB (87938672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3aa4058e871053c8acf129884e52b6071d6c57b4fb83fe7c36b5e10416deca2`  
		Last Modified: Fri, 19 Jun 2026 03:02:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9d92cdb44a87d393de81d7cc542d6777b26204448c78557dae01fa7fa11b88`  
		Last Modified: Fri, 19 Jun 2026 03:02:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:380469a20c70685d24bc6c6d29f8fd664bae04f451d9d1d1c38843b953445e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7437968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3236d55dbc39d0524264f553b836537057cccc07bd5473b17f536ceebf2f97f`

```dockerfile
```

-	Layers:
	-	`sha256:3164a02a32f2e0a9199fc150a484ac04f8ea7b090c60c8528fed27f3b742bf85`  
		Last Modified: Fri, 19 Jun 2026 03:02:49 GMT  
		Size: 7.4 MB (7422019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a73fcad800e3be57a1e8524158b865a7e8d8d83306dce121dd2e1b5052bc804`  
		Last Modified: Fri, 19 Jun 2026 03:02:48 GMT  
		Size: 15.9 KB (15949 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:d3d762231d55da365de8efde60c6cd3984fafbc34ead3fd14c9fcb68661f9825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223425843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f24692733f6555c76407a013383bb6a357ccd9717c2bc749d9624e6820aa30`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:43:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:43:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:43:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:43:17 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Tue, 16 Jun 2026 23:43:17 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:25:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:25:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:25:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:25:08 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:25:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4fe075b6dd2f22b2b5ed10e7aa905d6a156ebcea02659f73eed01d90f3f8b4`  
		Last Modified: Tue, 16 Jun 2026 23:50:05 GMT  
		Size: 90.5 MB (90537002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897cd6b9010dacd89ef872b1d7087ae9bd2fc9a41e5da3a2ceff4f88de2f8cc1`  
		Last Modified: Fri, 19 Jun 2026 02:25:37 GMT  
		Size: 83.5 MB (83501906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d09a072d9d3ebec870eda4d7a24ed9b1ba8a57e7a6ab86c1e8be489ec233cc2`  
		Last Modified: Fri, 19 Jun 2026 02:25:35 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d6bd630fe96cc323810ebb6e757f52bf064a046b03c22d05401b3a6c571c22`  
		Last Modified: Fri, 19 Jun 2026 02:25:35 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4d4a43f01ff5138ec01d0d290880bc7f98a5c1273f2155475687a493e321030e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09a5c1209cbbbf3fdbd66b2921c2191f35feb1acdb66972b9699d2ffa7653ca`

```dockerfile
```

-	Layers:
	-	`sha256:8e2aa403d18e3a8fac76d90c3ab8529386588684cf3accd817572068cfbdeee6`  
		Last Modified: Fri, 19 Jun 2026 02:25:35 GMT  
		Size: 7.4 MB (7414770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28b840baa6674e934c8303f07012b329ef7a64d40a79eecae70a2048f3471679`  
		Last Modified: Fri, 19 Jun 2026 02:25:35 GMT  
		Size: 15.9 KB (15900 bytes)  
		MIME: application/vnd.in-toto+json
