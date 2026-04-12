## `clojure:temurin-25-trixie-slim`

```console
$ docker pull clojure@sha256:dc07fd6655e74ad1e6d15f8789a300993b845f649dbe98cf699705ebfa586789
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

### `clojure:temurin-25-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a08e7d7e124468b4d437182229bb8d8629c9089820e87d4afa548bf615a4dddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (194045076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:115f1427b9fbec33f53baaa6b69f7921b4cd21ec1988557f89b440ed33433f78`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:17:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:17:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:17:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:17:27 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:17:27 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:17:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:17:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:17:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:17:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:17:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae15d0e8ba0530fc0b4ac1aa7dff460c009c8f69d0017fe8b5ddebc6f1ab2eb7`  
		Last Modified: Tue, 07 Apr 2026 03:18:03 GMT  
		Size: 92.3 MB (92256290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf07de4544ebf63e15fb8a27b1e7b28c03aeb2c157cfc6e529f90ad91eda8f1`  
		Last Modified: Tue, 07 Apr 2026 03:18:03 GMT  
		Size: 72.0 MB (72012105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb24c6ffde5eac8877e399965776d5011c1b8a634b96ddada7c98fbd6f12975`  
		Last Modified: Tue, 07 Apr 2026 03:18:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbcb9c9be13f688bba8ef0e4defe937c83c9f52bc6ab8fc1c20fc60673a40fd`  
		Last Modified: Tue, 07 Apr 2026 03:17:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:212ed7d27954887649206416e44e790e28cb0b5d8416e058089d04dd45e98f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5243715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e8a41e79a09eb05a4dd20a06f150bd82b01d51df8d85b825249bec35df557a`

```dockerfile
```

-	Layers:
	-	`sha256:dc094dfed3fe812d1716ceaa94707142d37433846aefb2187e33f6ba824239eb`  
		Last Modified: Tue, 07 Apr 2026 03:18:00 GMT  
		Size: 5.2 MB (5227224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ece133379bcc2b0772e6c07cc798d43c0124e66db4cfae5a07e1917b61204a12`  
		Last Modified: Tue, 07 Apr 2026 03:17:59 GMT  
		Size: 16.5 KB (16491 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2ae67004114c1058e600ac42e3a90ad5efdba08ceefdeeb798d550f7aa1471cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193259858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1862019dfa0c5194774a638fb6b148ab2e09fe481eef5375be869dbd047b5db0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:28:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:28:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:28:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:28:17 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:28:17 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:28:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:28:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:28:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:28:35 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:28:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8083dded165a72423aea7b3184e9193299b557a975451a01c33ba64a80eaee`  
		Last Modified: Tue, 07 Apr 2026 03:28:56 GMT  
		Size: 91.3 MB (91288281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1824f2d2f88a8e23062ed2838220b6ed4382897c2c8049b30bcbf17f184a1e93`  
		Last Modified: Tue, 07 Apr 2026 03:28:56 GMT  
		Size: 71.8 MB (71831985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43420e6741b5d3dd62ff8a88abd4caf6e9ea9b33206472a2871a105644da536a`  
		Last Modified: Tue, 07 Apr 2026 03:28:53 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a345cc8a681b757c4ba2f2ceac6f25ace8ff13744b656490172603ea1077244`  
		Last Modified: Tue, 07 Apr 2026 03:28:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1d1cb97a23d19ad75564104c4917a65a0b9d6209ebec65bdb39452d41a00ca9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c29df26e39183c61a02d25090794f1dd3e5ff497a9aa6dd3ae671b09ca3722`

```dockerfile
```

-	Layers:
	-	`sha256:36e91f95fcf808100f888476207d1caf2760d2877b816d1e9b4eca1265879618`  
		Last Modified: Tue, 07 Apr 2026 03:28:53 GMT  
		Size: 5.2 MB (5233014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4da128696ae38d6e13c600c55065ee305ae42f6ba967ef9879bbe540f6af3d8e`  
		Last Modified: Tue, 07 Apr 2026 03:28:53 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:6203e338743ebadb1fbe468c168159cfbb242fd31fd3b93bf3ec144d34848547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202656223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5abe8ad945d9bb400b4a86937df90baafbc6712e82a88aef90bda0948a72bb1f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 14:57:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:57:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:57:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:57:19 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 14:57:19 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 15:06:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 15:06:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 15:06:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 15:06:09 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 15:06:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674dad765dcc78e0a3938a692ea5b290c37a0c10042e2a743ec14ddef8e6b775`  
		Last Modified: Tue, 07 Apr 2026 14:58:42 GMT  
		Size: 91.6 MB (91633035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3117a1906e5350225d23f3930acda18fcd4628b02646bc3720b97a0c27d4ff`  
		Last Modified: Tue, 07 Apr 2026 15:06:47 GMT  
		Size: 77.4 MB (77429128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35bc6399945036da62d8f683b7adf2588f39c4222cad6dcaa6d333efa4f2cfc`  
		Last Modified: Tue, 07 Apr 2026 15:06:45 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d05fa574ca7779186ee850aa2806530f8617f0a02ffc18bb859701aee47e20`  
		Last Modified: Tue, 07 Apr 2026 15:06:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c8cd81a472e9def126e3a9bb0ae0317a29ad464fad160ad452e6c5f3090f3275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5231472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab105531560379d8e3983f12b0f2c7ceb86161f8e1a4099848d1c9ec4cbae449`

```dockerfile
```

-	Layers:
	-	`sha256:735b6fe2d4eda47532801a616654956c30ffc0d7da150342fa7a968c599096a2`  
		Last Modified: Tue, 07 Apr 2026 15:06:45 GMT  
		Size: 5.2 MB (5214919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:633a1e035c46be5d33398246764ffede662985768f9aca8ddbe3a3194413a20a`  
		Last Modified: Tue, 07 Apr 2026 15:06:44 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:14d4fac3ac2028368ba481310269d2fbb01153a5608d3053c0237ca227ec1eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 MB (192569208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bcfeae71b170c3c97728ff5e892d6dcaff17816ef7961e0ca2a747932b3ce5b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 11 Apr 2026 22:39:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 11 Apr 2026 22:39:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 11 Apr 2026 22:39:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Apr 2026 22:39:28 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 11 Apr 2026 22:39:28 GMT
WORKDIR /tmp
# Sat, 11 Apr 2026 23:01:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 11 Apr 2026 23:01:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 11 Apr 2026 23:01:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 11 Apr 2026 23:01:46 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 11 Apr 2026 23:01:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94187439743d0e4ea744bbf1c65c89e279a7b6b83ff5e8684b3251e143001c79`  
		Last Modified: Sat, 11 Apr 2026 22:44:45 GMT  
		Size: 90.8 MB (90773426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322b958ad857d72246cefaf46e881ac5d44f81da21e7df1c6c1e1227dbf789bb`  
		Last Modified: Sat, 11 Apr 2026 23:05:24 GMT  
		Size: 73.5 MB (73518961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074bb75a180dcf6ed2ed6e3901f2ffcafb1b0c90e734e449b0b8abad36a3590b`  
		Last Modified: Sat, 11 Apr 2026 23:05:13 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad7f1f7e4037a930e852550ee888099424a6f168f92fb296bb9512cb3966717`  
		Last Modified: Sat, 11 Apr 2026 23:05:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ab415598a83312be3af58891888316c92173d8a88f493d2ca76f5aa5ac820aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf7cf26acae4e4bc3058ec53a5b44610f1b944d78d74964d04c82eee8b7378c`

```dockerfile
```

-	Layers:
	-	`sha256:6bdb5f48df99d49a718ef91968b70182a8f4dbbb9247ebeaa5fd886cfd708869`  
		Last Modified: Sat, 11 Apr 2026 23:05:14 GMT  
		Size: 5.2 MB (5198711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ce84a26ab69dff1dde1e609c2565c955487d0b6b76bfbeb4d210323621e3375`  
		Last Modified: Sat, 11 Apr 2026 23:05:13 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:065349a3bc01f9ed4ef1daf60f095f70487063266ffd391a000b56741385788f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191057519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3333e25ba02f5b92740a2998e1edd23358373c75121a2f77669878e103525105`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:47:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:47:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:47:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:47:32 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:47:32 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:48:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 05:48:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:48:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:48:53 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:48:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e393eb59a51f7f19b07da996a340791549db8b4cea273acb62a8663489354f`  
		Last Modified: Tue, 07 Apr 2026 05:48:11 GMT  
		Size: 88.2 MB (88233812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9f589ba4d768c1a3eceb58b1f30a64397f7ad0b356b7cf3400089e7d497315`  
		Last Modified: Tue, 07 Apr 2026 05:49:17 GMT  
		Size: 73.0 MB (72987249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bfab521fdce726b3fc03d41977fe6485396674e508ce9953d8efb009d0d6f8`  
		Last Modified: Tue, 07 Apr 2026 05:49:16 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d9c7553179e6084fd5346990329cee9b4862b9e61a2cdc437ef46feb719efd`  
		Last Modified: Tue, 07 Apr 2026 05:49:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aae8e44f82492e47a7b95706eb989fe0ea79a409f2a3a39bc19ae0d7589e5fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cebb8631ae9d8d8dc37f07a20fa2d1138a18334b198080a130d221e554058d0f`

```dockerfile
```

-	Layers:
	-	`sha256:21330c84fd144b799a787e4ab4d55428d325754a0e22d9584c70bf2694f29b2b`  
		Last Modified: Tue, 07 Apr 2026 05:49:16 GMT  
		Size: 5.2 MB (5207710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43cc674996ae2984143037e926e576f73d7b4b26e89c11aa5c73c70c191f31ce`  
		Last Modified: Tue, 07 Apr 2026 05:49:16 GMT  
		Size: 16.5 KB (16492 bytes)  
		MIME: application/vnd.in-toto+json
