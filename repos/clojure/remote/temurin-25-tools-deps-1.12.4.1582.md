## `clojure:temurin-25-tools-deps-1.12.4.1582`

```console
$ docker pull clojure@sha256:57156cffb1ffe1312542eb740c335ee49f0f91a78a79c15119456b180b211139
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

### `clojure:temurin-25-tools-deps-1.12.4.1582` - linux; amd64

```console
$ docker pull clojure@sha256:a4ba697977cd4aaea0bb87f54cb2617af30f58d5a8b9385a8ea0f8a03f7c3372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221674268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc2a01c7ead0b7a92296d0f54cd15b8ccf37ca9217fc65b2545f3cfa5f81444`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:07:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:07:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:07:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:07:25 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:07:25 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:07:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:07:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:07:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:07:40 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:07:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d8129465764ea1474241dd51eb3631eeb37cae77af11d5e559c2942302b306`  
		Last Modified: Tue, 30 Dec 2025 01:08:13 GMT  
		Size: 92.0 MB (92045289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8b899c13114ab7cac426e76591177137cb4d7cc894b81a20f9940fd5417446`  
		Last Modified: Tue, 30 Dec 2025 01:08:11 GMT  
		Size: 81.1 MB (81147143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bf80718beb2478d6fa8d074c34ceeaf32fc76d6376e456c33fe8299f06e549`  
		Last Modified: Tue, 30 Dec 2025 01:08:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3109bdfefa67f634a2870e95b188003e8578aab1b7f671f70462e86826d01c`  
		Last Modified: Tue, 30 Dec 2025 01:08:07 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1582` - unknown; unknown

```console
$ docker pull clojure@sha256:370ce047eab105595914c2a1cf679a82d97110daa37eefd995d33fd332c77ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7345325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31872ba2fa9106a21f9de161cc50e795875f354e81e158c10c1116a9436c93a0`

```dockerfile
```

-	Layers:
	-	`sha256:ee48e3a084202736bc0d703c9729c9d1e34c73602d37229cde0f477d56feae31`  
		Last Modified: Tue, 30 Dec 2025 04:45:58 GMT  
		Size: 7.3 MB (7327554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f50e0394c2e501a3acab38d44bdd2a76701a4833308e51ea981ea109482ea422`  
		Last Modified: Tue, 30 Dec 2025 04:45:59 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1582` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b261b22337e24f812d8318e0ec7a0914e6f86c6eb033b10e36a67fd28951b2c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.4 MB (220438267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c030317451b2ce5d7cc854738cd0546dff4b35402d3f90c24cb3609651fdea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:08:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:08:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:08:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:08:58 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:08:58 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:09:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:09:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:09:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:09:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:09:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60bbae022574750d78425baeaa76fcb1763d3d930d478bfb3c0731a9344f0a4`  
		Last Modified: Tue, 30 Dec 2025 01:09:48 GMT  
		Size: 91.1 MB (91052515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a2272bf2b47cee345055c5b00655becb84faeb8d0debbc6dedce3f7b7bb2ee`  
		Last Modified: Tue, 30 Dec 2025 01:09:50 GMT  
		Size: 81.0 MB (81025569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81da5b86a03caae24c42e4c1b739a2ceda0b86b282d82463ef26f7ed70f41b5`  
		Last Modified: Tue, 30 Dec 2025 01:09:42 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105ad17dec328a45c91a96193ad45637205ded75b37d312afdfe385782b98ed6`  
		Last Modified: Tue, 30 Dec 2025 01:09:42 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1582` - unknown; unknown

```console
$ docker pull clojure@sha256:a2e689e84e4fa261eb0a07a26272ddfc92e52cebd9bd7bc8ceb5a9d2a0277d9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7351347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1695e1bb42869700041e2c2e8d998b45bbede15d68197d1bc16a72dff763fcb2`

```dockerfile
```

-	Layers:
	-	`sha256:0fafb9a141142286c87e4fa6df15613780da1b7a3883aca62c563c6c44eee67d`  
		Last Modified: Tue, 30 Dec 2025 04:46:05 GMT  
		Size: 7.3 MB (7333386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a24f989dc3933d8d7c3bebef36f3dfbf1057847b6ba3c6ade1811f9db9705a7b`  
		Last Modified: Tue, 30 Dec 2025 04:46:06 GMT  
		Size: 18.0 KB (17961 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1582` - linux; ppc64le

```console
$ docker pull clojure@sha256:80fcbb4b415929fae8eff46a85502f12c6c5a7ccb9569787c67be8c411fcb363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230920743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a39bd0b575289f91ae528bd688271e5c1d7d0a785dd9717e6848e4b6af67aa3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:34:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:34:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:34:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:34:56 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:34:57 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:47:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:47:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:47:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:47:22 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:47:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:48e256c4119c0ad256492d6a930e99d2b2d7f8d7920d619aa2de4f616c37076e`  
		Last Modified: Mon, 29 Dec 2025 22:25:39 GMT  
		Size: 52.3 MB (52326998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9547de7380c379be8e2439a1f5f5648ea7e4adf222d1cde7b039d2d494b72f2`  
		Last Modified: Tue, 30 Dec 2025 01:37:19 GMT  
		Size: 91.6 MB (91610788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32a90e548f23480ddc21a8e3f6bfe0dde5613d9976d0ec1fecd437501326ca0`  
		Last Modified: Tue, 30 Dec 2025 01:48:18 GMT  
		Size: 87.0 MB (86981916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4b6a0da4decb1e8dbdec4bb841111c380833358fb682348cb624daa187ef46`  
		Last Modified: Tue, 30 Dec 2025 01:48:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a28502f58bf093629faa2e21c50dd6dd243bf9d119c4b4e9def0a5540c1a59`  
		Last Modified: Tue, 30 Dec 2025 01:48:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1582` - unknown; unknown

```console
$ docker pull clojure@sha256:b19ed4ca74a12ef3f50d65436609b85984d0540854d3b0ea1c2c6206b5ec217e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7351957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cdc313e2c018cf7eaa292eea65103771f207c871b6d60d5610abdae7cc8acda`

```dockerfile
```

-	Layers:
	-	`sha256:34f86ee036b30841b0f56b7d8d824ce7582b91e0ea3de7312a4a76f4d72ceb5b`  
		Last Modified: Tue, 30 Dec 2025 04:46:12 GMT  
		Size: 7.3 MB (7334102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eaa3ef5e11754286ae148539124b758757cd960df48df71a180738ade675989`  
		Last Modified: Tue, 30 Dec 2025 04:46:13 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1582` - linux; s390x

```console
$ docker pull clojure@sha256:e024024e3a5a4ea48bd15e38a52bd5dde5ccaa9a3f1683d97d345f795191839c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215304522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1b4df99708a96e3a68e228969e00baaba122601c04f624f150e35bdfe05ed4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:58:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:58:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:58:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:58:35 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:58:35 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 02:07:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 02:07:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 02:07:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 02:07:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 02:07:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ce8a6983b315f7ccc96b582192afffde7bfdc0a45f357f2cd098b4f88aab2be4`  
		Last Modified: Mon, 29 Dec 2025 22:25:37 GMT  
		Size: 47.1 MB (47137727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c3793451cba2767589ed9770691f86a45615390c5ab745970385d6c38ac674`  
		Last Modified: Tue, 30 Dec 2025 01:59:45 GMT  
		Size: 88.2 MB (88210732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158e36aed98a9b5a5c4464a90a742f697d6f337ec3d678cfdd0e7aad5f4531fb`  
		Last Modified: Tue, 30 Dec 2025 02:07:44 GMT  
		Size: 80.0 MB (79955023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb30b61fd8cecc778f7d41643279cdcb34320fb531ec84a1effd11bdf12995a`  
		Last Modified: Tue, 30 Dec 2025 02:07:36 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7e8c4ab3794a6216b15af38d52921b2d009052f37af1c0e6905847705b925c`  
		Last Modified: Tue, 30 Dec 2025 02:07:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1582` - unknown; unknown

```console
$ docker pull clojure@sha256:9f8bb418d2d2b9547bacc5d4ca35310aac57f35d4939d55cef5ce923cf6dd52a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7338393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f2370d53edbcc8f2746f11325e0663445349871f0a8c7a87f05c2f74d2e2c9`

```dockerfile
```

-	Layers:
	-	`sha256:7b2834e731bbbea1b2ffd43d326e5fbb18dc12e1b0348a27f995fe98c5628740`  
		Last Modified: Tue, 30 Dec 2025 04:46:21 GMT  
		Size: 7.3 MB (7321421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b25e5b89ad777b9febf9e023aa438b0d47696d9ffcfb31411f8e9147f182b091`  
		Last Modified: Tue, 30 Dec 2025 04:46:22 GMT  
		Size: 17.0 KB (16972 bytes)  
		MIME: application/vnd.in-toto+json
