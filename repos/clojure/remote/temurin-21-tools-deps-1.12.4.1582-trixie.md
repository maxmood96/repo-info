## `clojure:temurin-21-tools-deps-1.12.4.1582-trixie`

```console
$ docker pull clojure@sha256:a37b37448fce41e2827f845c0b9f034aaa15194f637406dacaf74f32f10ee047
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

### `clojure:temurin-21-tools-deps-1.12.4.1582-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:069729a445f5abbf625d844d7b88e6d29064d2550706307a7980aad61c3558f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292659410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e0ccb1c47b87baa9edfc4f33d6ef4daea575ad4b67011633ae663676c9db13`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 22:40:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:40:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:40:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:40:10 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:40:10 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:40:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:40:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:40:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:40:28 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:40:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892a5aa64aab184ff797caa5c1436ed59a771f36c7bd54fafd73a798bb30b071`  
		Last Modified: Fri, 12 Dec 2025 10:19:12 GMT  
		Size: 157.8 MB (157825957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5337678d61cb2415a6ef6600ac46bb16e8ae269acbba5b2804ee6c88b641bc40`  
		Last Modified: Thu, 11 Dec 2025 22:41:09 GMT  
		Size: 85.5 MB (85542892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26630fa71e587ea3f8503d439b4edaa8d819cc70414dcc486568d62ab65ed154`  
		Last Modified: Thu, 11 Dec 2025 22:41:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6db5cca8ce1c85ad463a51e14bb0ab20546348547516bb6a819c8096d1e358`  
		Last Modified: Thu, 11 Dec 2025 22:41:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1582-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:dd570cd9051e6001434a14dd0ebafa60cec1130f41589add7a9d7bfb92abb2cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7485787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58aff7453c666fca0cc9b5af451ddab44b6d4fa08620d20baedc973e3dadf0b1`

```dockerfile
```

-	Layers:
	-	`sha256:2c7161639d7b67dbefdb9e42600ae71ca088d3bec05f43f46d890765d7838a64`  
		Last Modified: Fri, 12 Dec 2025 01:42:43 GMT  
		Size: 7.5 MB (7470033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9d24b3b170e43a9131d450ac81ff323213b8f91047fdca8cc5965889ca1e698`  
		Last Modified: Fri, 12 Dec 2025 01:42:46 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1582-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c6e9bf9bd19fa4f8ed510ce400dc43452bf2a9b43572d0d1d26b986fc18d0fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291120236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eacc25ca14835531cc3a58cf0b6afe59acabb060b5a9fdd6fbdffd14169335a7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 22:40:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:40:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:40:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:40:05 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:40:05 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:40:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:40:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:40:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:40:23 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:40:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a384c4fb3cd2bca60628d18532b208969c422446ce4507dc549a18d7f94336`  
		Last Modified: Thu, 11 Dec 2025 22:41:06 GMT  
		Size: 156.1 MB (156107637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638efe6992c5ed4114aff0ea2102863a6477de2a944efa756717ca1f936fc30f`  
		Last Modified: Thu, 11 Dec 2025 22:41:01 GMT  
		Size: 85.4 MB (85361335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9094c68bcffbb41ff053a71186a518a28ce05ef2510586b8450988932c7883d9`  
		Last Modified: Thu, 11 Dec 2025 22:40:53 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454965977a202d9582b6811bdf742371c525968637923567ee921d42dc115b59`  
		Last Modified: Thu, 11 Dec 2025 22:40:53 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1582-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a2fb2f7846c0898086ffa40a474188d57644290022d1d04b86f1e8ee2531944a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80d205c1d1f2c072da3315f8cc688c8744cf084c5d8ef2469aaadfbc50944ee`

```dockerfile
```

-	Layers:
	-	`sha256:f3fc72e87b7522b9cde9ada6e033104d56421c16ee3ff4255e2659aaf29a90ee`  
		Last Modified: Fri, 12 Dec 2025 01:42:53 GMT  
		Size: 7.5 MB (7477063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b95593e185d95b468a2ea8ee398704175d915430220602f9f0f4a38b38cfef8`  
		Last Modified: Fri, 12 Dec 2025 01:42:53 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1582-trixie` - linux; ppc64le

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

### `clojure:temurin-21-tools-deps-1.12.4.1582-trixie` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-1.12.4.1582-trixie` - linux; riscv64

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

### `clojure:temurin-21-tools-deps-1.12.4.1582-trixie` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-1.12.4.1582-trixie` - linux; s390x

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

### `clojure:temurin-21-tools-deps-1.12.4.1582-trixie` - unknown; unknown

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
