## `clojure:temurin-21-bookworm-slim`

```console
$ docker pull clojure@sha256:987c386f2a6f90a410929af6894087c9388528234834eedae902adbb082c4f3e
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
$ docker pull clojure@sha256:85619a49901a0c594d210d296f6a89fcaea67956b2dc99c39ebfc6631b959b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255772341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5716025a6adfd75f547e6b0f1b0fd0de9e7b09066dcbf9669c4e1cc5083f7d98`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:56:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:56:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:56:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:56:10 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:56:10 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:56:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:56:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:56:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:56:24 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:56:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e40e4571c70904209178514181f36961d44e8e46d791612987091441d6091d`  
		Last Modified: Tue, 24 Feb 2026 19:56:46 GMT  
		Size: 157.9 MB (157857058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cba32f6785507dc6624567f13077745cb7181f33911700d8cd089e9802a68e`  
		Last Modified: Tue, 24 Feb 2026 19:56:45 GMT  
		Size: 69.7 MB (69677966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1072c73c8b409af3bf7b91d08483abdf3d74db040efdd9a67fa5758bd57a3ae6`  
		Last Modified: Tue, 24 Feb 2026 19:56:41 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0932ef6c8f5cba627347f6f1572b2e3c434b8d9b01b3e616be77c44768ffc57`  
		Last Modified: Tue, 24 Feb 2026 19:56:41 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a0e20edc9764ac0747323bff7107451d76088bd3753a32c95befb94193b357b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c4d3638192b686f7ac0a1b966fc86eb8017b1c4cb801c4a2097818dc4f4fd4`

```dockerfile
```

-	Layers:
	-	`sha256:e3d2462378979e14735565028046bf5f5a182711c4c6216a0644712bcc586649`  
		Last Modified: Tue, 24 Feb 2026 19:56:42 GMT  
		Size: 5.1 MB (5116506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f861abd975250a1a98b988533ec992b95b4c1b3c27a6af6de488feb9f37cd7c4`  
		Last Modified: Tue, 24 Feb 2026 19:56:41 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:61124f6182eb4a9d0b42189008b8b5a71330a54f00f7de93e64188853f06d4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253923163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64a6eb07d4093beb4cda6ecc485f3cb81ef2ac6d6dc8b012723d294b28d4e37`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:06:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:06:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:06:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:06:56 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:06:56 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:07:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:07:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:07:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:07:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:07:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a120b4061668de1aa4b1ce8b0fa3dcae09c379376546a50773b3d99c1312727`  
		Last Modified: Tue, 24 Feb 2026 20:07:33 GMT  
		Size: 156.1 MB (156133054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7777d4482db8e97255ef7e1bb8b324f3bfe21377f8d6ea8a3069e7aa039d071`  
		Last Modified: Tue, 24 Feb 2026 20:07:32 GMT  
		Size: 69.7 MB (69672990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e1e82c0e0cf687addfca4d21a83d1f47545cbfea4595fb042e053673cfd40b`  
		Last Modified: Tue, 24 Feb 2026 20:07:29 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa9cf12448983006ac240713aeb71a8f8071d4d7572153e60b2f985ac004b8c`  
		Last Modified: Tue, 24 Feb 2026 20:07:29 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2eece11fc57420d6386f23523a6489aa59f0f7a9d34af7f92087fca32637a8da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8cc982469462e4b17a9a9625555e1f07710dbb72157b540453da9f37de1db0`

```dockerfile
```

-	Layers:
	-	`sha256:01df6c429bf471a6316c6d6d26f211ca263ed55d60156a5e7abf2dbcab843734`  
		Last Modified: Tue, 24 Feb 2026 20:07:29 GMT  
		Size: 5.1 MB (5122267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5792e3943227df943c307c09ea04e622b1bdf8eb9267e6f0a766c8394d29135d`  
		Last Modified: Tue, 24 Feb 2026 20:07:29 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ff8bf69316c5a61e28a084a859b62c60c8d3b4445bc9e43ab3970af3c68849d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265561408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e45247d9ae011d5bac4478a8006dc3020e2032a2c132a93257d8216e35b01ed`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Fri, 06 Feb 2026 00:34:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:34:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:34:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:34:00 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:34:00 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:41:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:41:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:41:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:41:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:41:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04686be48d2a894920edac0c0c6434c05a7128013df9522a975b048c103c93d`  
		Last Modified: Fri, 06 Feb 2026 00:36:06 GMT  
		Size: 158.0 MB (157977491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ff8ed03f353a0ece5f58bd3ce03806e34111b0130fe1fac2ba69c56d0e8e2f`  
		Last Modified: Fri, 06 Feb 2026 00:41:55 GMT  
		Size: 75.5 MB (75514159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7265c5180d70ca2c83535214d9fd18f098c2a50781f5aad0b7f5df89b09cee`  
		Last Modified: Fri, 06 Feb 2026 00:41:53 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81e3bbf033fe93b7b083fd05fd6c7bf3ad2317b1c830b56e7b82f3b001ac9ff`  
		Last Modified: Fri, 06 Feb 2026 00:41:53 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6a8ce8c3ecdd6d2f1ce2b344f4d4c8973307b9f992fd6bce75031b915497cd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31dcd4ab30efe6e3a5aaa2ecc8ebaaf33c7771419200ed04f6fe7d48f4802cbc`

```dockerfile
```

-	Layers:
	-	`sha256:9b8aedfaf5c7109d228a7108634c9401ca0fb7628a1779d5b2f8f7b724fdec3d`  
		Last Modified: Tue, 17 Feb 2026 23:59:43 GMT  
		Size: 5.1 MB (5121664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36f5dfeee110634173b5eea3adf60bbf9b91d861b606700c6c2dab519f5700b9`  
		Last Modified: Tue, 17 Feb 2026 23:59:42 GMT  
		Size: 15.9 KB (15883 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:a27cecb9f5fa8ce5d8b2dc85657d0d4ef01f47e2de72c8ebfe95c47639656834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242481210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2732460ae39174a8c83e14cfe992ef71c168f5d5f610e41c06b48d20ec605ea4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 22:13:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:13:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:13:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:13:11 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 22:13:12 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:13:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 22:13:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 22:13:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 22:13:57 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 22:13:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b838670a4f355a1ac037114110d70a67c8c7c1288cea2a0bcf49e74a0f97637`  
		Last Modified: Tue, 17 Feb 2026 22:14:43 GMT  
		Size: 147.1 MB (147105302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d46a41181b95fce21464a8c6075dcb829a6a59ce7605b7ba5be0648c5ca091`  
		Last Modified: Tue, 17 Feb 2026 22:14:42 GMT  
		Size: 68.5 MB (68490479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af4ca1e6d77b67989dcdaa7ff5c8725e45dd4cc2abd1787e50296da24970f3a`  
		Last Modified: Tue, 17 Feb 2026 22:14:39 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618432aefeca4f6d066d9cfd5d19d37e2afdbb4e7195b433fd669dc6a7897c63`  
		Last Modified: Tue, 17 Feb 2026 22:14:39 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:89dccc571eca74bd9ecfd2bab8ad667516aa8e93331ec70419179d75e1298be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8ea6727b283bdd6b1c87e54c6c05cbb9be7572cac74fa6fc7cf7d186be74e3`

```dockerfile
```

-	Layers:
	-	`sha256:78093cb699d13b05b1ba68e67ede3ff5c40c6cd950011efc1d2ea97a09e347c4`  
		Last Modified: Tue, 17 Feb 2026 22:14:39 GMT  
		Size: 5.1 MB (5107827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:014901a333973ac8938e57130a350376dcd1032d803b976256539e5909356635`  
		Last Modified: Tue, 17 Feb 2026 22:14:39 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
