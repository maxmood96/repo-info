## `clojure:temurin-21-trixie`

```console
$ docker pull clojure@sha256:fcb9fd1adaa2ff8e8d43149e95efd077afac00ff8e9c7ceedb78ac9f25c82afd
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
$ docker pull clojure@sha256:642a92241938221e5bf6918a7b9e97c742f1d4046923bd0c16c005779e643fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (301997590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8352f3db9f3f840d77271da729da48b2cfaf9413f33e9f00b452fcd08923ba32`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 05:23:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 05:23:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 05:23:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:23:11 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 05:23:12 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 05:26:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 05:26:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 05:26:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 05:26:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 05:26:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d586c84fb9377f9b3f4030e2c3e1e9ff7b1a23a68b8abc2c48a43163a3589257`  
		Last Modified: Tue, 30 Dec 2025 01:51:01 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda772f725cdfa78e718ae79414865dc7e6adbaabecad3a4b08396e7343aacff`  
		Last Modified: Tue, 30 Dec 2025 05:24:34 GMT  
		Size: 157.9 MB (157942938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cd50b9c3cee63544c14751ad93e3a30023a42e1d179e3c3de3ff57fc6a2c2c`  
		Last Modified: Tue, 30 Dec 2025 05:27:50 GMT  
		Size: 90.9 MB (90945126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9378d56252ee237bfa0a3a3a94f213beb3fbec9747affb51bbf922d6251e308`  
		Last Modified: Tue, 30 Dec 2025 05:27:44 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3127ad26458fd32cf26d7d3f21a6775ff17130a6a52ac194592a4984e78459c`  
		Last Modified: Tue, 30 Dec 2025 05:27:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:71356e988f8ff900233ad94e0b4f4c952b7bc59f0388ddb4690acd3acfb5665a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc577a91170660fb7231a3ea83c327461905c072bac91aebaacf81e310755d0`

```dockerfile
```

-	Layers:
	-	`sha256:bce0d17f02446e0c5e9e8772215a3bf32da76e5a03a0d3de527bd91b75128bf1`  
		Last Modified: Tue, 30 Dec 2025 07:38:13 GMT  
		Size: 7.5 MB (7474452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f704c7f46172e2cd2aaac5cf16b94601f286d78f3e2cc0c2ed1920acbd7132d6`  
		Last Modified: Tue, 30 Dec 2025 07:38:14 GMT  
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
$ docker pull clojure@sha256:a8b67e63e715b8f7ed787e90d4dc46e4f063993e4844aff5d047d70cbb5fe4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282925257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0e7c50794e308461acc8d3d90aadc2bc1434cb9c9de374c93bd68866f5077a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 05:49:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 05:49:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 05:49:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:49:29 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 05:49:29 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 05:49:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 05:49:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 05:49:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 05:49:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 05:49:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:85bc4a4d1f4e52a33d42907057e0ab87c5eb2560b332d94f6e9d7da79c0c76b8`  
		Last Modified: Tue, 30 Dec 2025 03:26:29 GMT  
		Size: 49.3 MB (49345959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813b258f0622e9bf6e7f829414aa194580800b1ef2ef1f3bed15246fd048599f`  
		Last Modified: Tue, 30 Dec 2025 05:50:19 GMT  
		Size: 147.1 MB (147069832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02012752d07ac7f203a48e2ebedbb66d5678168451c213e24189ea2226edd5b1`  
		Last Modified: Tue, 30 Dec 2025 05:50:49 GMT  
		Size: 86.5 MB (86508425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc6570a95d7492d704228d24e556b1158a67297eb165e6a85b99395294999f5`  
		Last Modified: Tue, 30 Dec 2025 05:50:39 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d1b38558599b91cf393ef106cf28c06cae6ff0f3f3ab88626d8de735f9912f`  
		Last Modified: Tue, 30 Dec 2025 05:50:40 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9f66b0519fff9730772704b30c68e28ed45931a5830d14a72371ee082367e1ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7481709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db44176f3276785f5587d0aeb852815d236af258ed8cf341e40bf1b0c0cae6e1`

```dockerfile
```

-	Layers:
	-	`sha256:ae5de2d607b02c6323a583324e4e1dd346c0b68c49cc8dcb8c4fdb117be1f093`  
		Last Modified: Tue, 30 Dec 2025 07:38:26 GMT  
		Size: 7.5 MB (7465955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e11de1e8c7ca440d6a850db1fb7bc1befc5ba9cdbdc940d4b50d0676fad59203`  
		Last Modified: Tue, 30 Dec 2025 07:38:27 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
