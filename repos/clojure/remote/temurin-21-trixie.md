## `clojure:temurin-21-trixie`

```console
$ docker pull clojure@sha256:b203ba6c28c3a0c0138884e5782189ea34d435f5e265e09e86e4f0abb9cad2a3
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

### `clojure:temurin-21-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:ac4ce8be536ed63141e4297c13066530bfe26755a921acb13d6b897779d6dff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292659405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4862996b4f5b7853d5f1ff7bf678e4a830d1595d2c584f187a8bee289bf61a43`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:05:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:05:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:05:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:05:04 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:05:04 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:05:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:05:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:05:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:05:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:05:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72e3ec4704d158d773c7c6963f272bd304884b3a67f95cf16a7d1bc452b9308`  
		Last Modified: Tue, 30 Dec 2025 01:09:18 GMT  
		Size: 157.8 MB (157826042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846ae67910dbec9eedf9d12f9f99a085d4c74a51243f7d9395aca95ddcad37a3`  
		Last Modified: Tue, 30 Dec 2025 01:05:55 GMT  
		Size: 85.5 MB (85542735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccb118ffaf40c336f5c01cae1607568656b46199d92d021cfa1423fe52682a1`  
		Last Modified: Tue, 30 Dec 2025 01:05:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8833b0e2a664f65467de72c5b53fbfb8ba1daa5cddc58104d949071938b3c7c`  
		Last Modified: Tue, 30 Dec 2025 01:05:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:50108dc44fba063194c2497bc7638670c63f3de1ffb7028c26ad44c0ca24f760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7485785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86874a45506061c7e7c35ea00bbe4cb77e9677fb0ff29e65c81bf451568d12db`

```dockerfile
```

-	Layers:
	-	`sha256:ee1382a3019018b0bb759ac0b6cc4051e729b873f36daf04aa34c81308d02f67`  
		Last Modified: Tue, 30 Dec 2025 04:45:08 GMT  
		Size: 7.5 MB (7470033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf2686d1f090e3970bb0a79c630be86f80e847bb9bcc7e9c7027080793df68fc`  
		Last Modified: Tue, 30 Dec 2025 04:45:09 GMT  
		Size: 15.8 KB (15752 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f603e9730d45565798edb533a39daa7e9203aadce6fa58a0dc66fe5b28a24fea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291120186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc77a708a94edc14cc58578326f5792c207e77630de2cb87f5370b267da74e7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:03:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:03:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:03:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:03:56 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:03:56 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:06:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:06:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:06:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:06:34 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:06:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2058710d5556751b2ba12a69abfbf13bfef16193b699613886adf78bbc1f2840`  
		Last Modified: Tue, 30 Dec 2025 01:05:06 GMT  
		Size: 156.1 MB (156107673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b5d328e4639a2c6fb7dfa95e2bb32145272cea6010b84abc5f110d2c7c730c`  
		Last Modified: Tue, 30 Dec 2025 01:07:11 GMT  
		Size: 85.4 MB (85361280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04cfc6cac55aa8f125d195488d173d3bd26c3d9b1c0953b8fa09117349957320`  
		Last Modified: Tue, 30 Dec 2025 01:06:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b6d4eacc616f31a1e19667c8a58473149958de9af5307e0ddc03570b2808ad`  
		Last Modified: Tue, 30 Dec 2025 01:07:00 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8d8f9ddf1bf7ab7ef6947bfd0c91512a814309ba005c405657a984d203bf74db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ca11a93ed70f7533405ba81514a43f3df561e4feebd99829e1fab2a69214bb`

```dockerfile
```

-	Layers:
	-	`sha256:54ee8fd38c143c26071965b96781b4ad06befeae40f0092301d3d36c82cfc9d5`  
		Last Modified: Tue, 30 Dec 2025 04:45:15 GMT  
		Size: 7.5 MB (7477063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:204b15fff3bc7ff62a04b1dfc5af0c8af270dc97cc27264a131f81bd9c476ef9`  
		Last Modified: Tue, 30 Dec 2025 04:45:20 GMT  
		Size: 15.9 KB (15871 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:4cfa19821ade8eb50e482312d5f2a4ecce386c774ee453faded8db40d28a6f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (301997745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:934965411c7e605bf2554a85a637bd056e9c2df8d1b68e3da57eef6b9ba12c0e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:29:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:29:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:29:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:29:48 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Mon, 08 Dec 2025 23:29:49 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 23:02:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 23:02:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 23:02:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 23:02:56 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 23:02:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6a2ef35163b9d4f6648137cf0019838288c6072622a6112548fb68bfe52e18`  
		Last Modified: Mon, 08 Dec 2025 23:35:07 GMT  
		Size: 157.9 MB (157942951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d48eec2b048868ffa1963ddab06d5c0f1a63970b20e0cebbec33703318096d4`  
		Last Modified: Thu, 11 Dec 2025 23:04:02 GMT  
		Size: 90.9 MB (90945275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b7a5a120b43ca1338d6f2978bfeec541d939badbf973999edca77ae936f7ba`  
		Last Modified: Thu, 11 Dec 2025 23:03:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d206bd8d299879a4bde7658d13999e213965769991e4290f1c127720b51c4f`  
		Last Modified: Thu, 11 Dec 2025 23:03:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:635f1c7d861ce33b4fa7406209b24763e23a78d6604a97db7fd0f84cf8622961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684c1efb713f7452914ae3cdf632fbf405ce8f585e81f8c5098615ad03bac356`

```dockerfile
```

-	Layers:
	-	`sha256:e69d3ee15d71873f11dd19f971cd01d8bdd1113922a4e03026ca9e229ab187b1`  
		Last Modified: Fri, 12 Dec 2025 01:42:59 GMT  
		Size: 7.5 MB (7474452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2ff5814ffe3dbabea625bd1cfa401687a639c9bf88d0cba0c3ceaac5a0bf7e7`  
		Last Modified: Fri, 12 Dec 2025 01:43:00 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:b81c5e53248a362114ce160bcc8db629f0e87fde61e3645e2aa54ccb0741ce12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289390649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463f8b64c64769dd897fa8c18d0f75ab53cef4fcbf8b3600b5ecf21377c6f83b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Sat, 13 Dec 2025 18:54:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 13 Dec 2025 18:54:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 13 Dec 2025 18:54:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 18:54:03 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Sat, 13 Dec 2025 18:54:03 GMT
WORKDIR /tmp
# Sun, 14 Dec 2025 16:22:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sun, 14 Dec 2025 16:22:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sun, 14 Dec 2025 16:22:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 14 Dec 2025 16:22:01 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 14 Dec 2025 16:22:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e8961870af39130e72e5dc66bd3574bb074dffc7989fd5e909f55fefadae8a30`  
		Last Modified: Tue, 09 Dec 2025 02:05:05 GMT  
		Size: 47.8 MB (47771135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed9d408f39b2ab7a732bf4d5e03e354bbdfce3313757f6fa643fc0efe046516`  
		Last Modified: Sat, 13 Dec 2025 19:00:56 GMT  
		Size: 157.2 MB (157194311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499af1a9fc2940441cbdc0d8482f4b999e86477dabcf7b973f1dd83a73a7cea6`  
		Last Modified: Sun, 14 Dec 2025 16:26:43 GMT  
		Size: 84.4 MB (84424163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079ca4d426934d0278c4a1cf7a2c45b408cf7d36f6ff092233a69475512fcc7d`  
		Last Modified: Sun, 14 Dec 2025 16:26:37 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7affdc3cc415a1aa3d710de2cc74ab4c2e235077bd050d1ec4a84d414292ec21`  
		Last Modified: Sun, 14 Dec 2025 16:26:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c865842de1c7cf167e80f3a7ec3f30133fbd56cc276c035e0d32a250d8f037d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7473747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c111395105f8ae18d05c2968a3e1d4cb2a646166739ed9e8d0cb19269910d3b6`

```dockerfile
```

-	Layers:
	-	`sha256:1dc7bda8a22e8db158ed065e3017b4d841716ac83c9ae58ba3feba32a9e52b38`  
		Last Modified: Sun, 14 Dec 2025 19:36:31 GMT  
		Size: 7.5 MB (7457946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67f9e8ecb0306948eac073fae7131fbfa51bc2450414fab96d577ad5f2b78a5a`  
		Last Modified: Sun, 14 Dec 2025 19:36:32 GMT  
		Size: 15.8 KB (15801 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:232710a2b2649c13636e627eee9754c3677fd16033de37c03ffd83f1d6ef3c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282924681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6da58b40653d6e7c9114ed7ad704abbc9487019c98c39a5c709d3d30f3358f7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 22:36:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:36:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:36:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:36:19 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:36:19 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:36:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:36:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:36:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:36:35 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:36:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3f8967bef2f6a8ec916f7d3a0d528a6724093176621c5758addeeece50e41dec`  
		Last Modified: Mon, 08 Dec 2025 22:16:15 GMT  
		Size: 49.3 MB (49345908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19963788028b9d5f5835f7bdbd8c2d1662cd8cc960e10e19c24ab41959a24bc`  
		Last Modified: Thu, 11 Dec 2025 22:37:31 GMT  
		Size: 147.1 MB (147069840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acad61172448cb77fa106292431189aa2ab44bfa24cb296a6d2bf8c7f3764666`  
		Last Modified: Thu, 11 Dec 2025 22:37:22 GMT  
		Size: 86.5 MB (86507892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57967675fe48c13d71d46e9e921f0e5819b42466d4bfe249c5d5497f9bb6531`  
		Last Modified: Thu, 11 Dec 2025 22:37:11 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91987d3eb27719fe78af1beab8d179ca8bacecce08965fe5b661cf4b880e43e4`  
		Last Modified: Thu, 11 Dec 2025 22:37:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3a7390528d1a5d7af883f6fe67f1c37d37591c47b179efcdd217ff2954b1f6ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7481709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105a490c98434a4283665eb403a02793c0e06734d25fb3fb2cba3b56f867d9a3`

```dockerfile
```

-	Layers:
	-	`sha256:c5f6417cfdbcc3e29162162a6e19d6340bec6e4f39d5252d21dfd36337fde622`  
		Last Modified: Fri, 12 Dec 2025 01:43:06 GMT  
		Size: 7.5 MB (7465955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e14fff91143759136e555a5d97680de92b7bff52011c4cc0d145ae2af13636b0`  
		Last Modified: Fri, 12 Dec 2025 01:43:07 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
