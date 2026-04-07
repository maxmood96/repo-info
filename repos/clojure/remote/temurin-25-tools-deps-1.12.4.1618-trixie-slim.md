## `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim`

```console
$ docker pull clojure@sha256:b186af068b0e21ed16ad966ca478b65c944aed5cd6c795bd7fe9f1b43861633d
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

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - linux; amd64

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

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

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

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - linux; arm64 variant v8

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

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

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

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:6b0233925b1e79b8167321dee47382e042ce5e58282e22c54e7158d022497e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202656226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32856a47bec76224bbbcf0679a8c61b55fc681ed43d2f11c0f55a57c3d79d629`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 18:46:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:46:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:46:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:46:17 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:46:18 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:51:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:51:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:51:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:51:10 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:51:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210f0f2228872d076d4a64e5b33affbf6841048c0c771e1ab74cea434ead7212`  
		Last Modified: Tue, 17 Mar 2026 18:47:33 GMT  
		Size: 91.6 MB (91632916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31a9b6fbad6cbe437ecc4c4999243aaa8b1e0afb6cfaf91020f48c26e460019`  
		Last Modified: Tue, 17 Mar 2026 18:51:47 GMT  
		Size: 77.4 MB (77429434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96dd93b0c7406116bda93dcfb8fa7a3bbf3584568da5ea6d35befd38ee7c161`  
		Last Modified: Tue, 17 Mar 2026 18:51:43 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4347b9088ac52ed94c1d2d4fd3ae247775049e6350ef2bd0a10cc042fd5c11`  
		Last Modified: Tue, 17 Mar 2026 18:51:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:131ec748e25419ad9888d7953038ac123ff43c61d26e3628eca526d6a882053d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5231472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1447e9d59a271c5dc405d96047a749760c7be0486eb3c243e81bad07568ef842`

```dockerfile
```

-	Layers:
	-	`sha256:ead1844a3b8dfc74706d4585b9f35b75e8ff5e6c62ec92f6c2d399401319853a`  
		Last Modified: Tue, 17 Mar 2026 18:51:43 GMT  
		Size: 5.2 MB (5214919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37f2ea458ed301309656d5402738143204755813bab862908d2b420577eb3b9a`  
		Last Modified: Tue, 17 Mar 2026 18:51:43 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:79e2df3efe93b1e488cc106b268e1c9be7b5d1a89fd91fb07007fc69a1b6f152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (189950616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1fa3030c34cf57cc20b5fabc29e6544409b4a0a43c4aa10bf76af92a72cb51`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Sun, 22 Mar 2026 19:34:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Mar 2026 19:34:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sun, 22 Mar 2026 19:34:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Mar 2026 19:34:05 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sun, 22 Mar 2026 19:34:05 GMT
WORKDIR /tmp
# Sun, 22 Mar 2026 19:56:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sun, 22 Mar 2026 19:56:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sun, 22 Mar 2026 19:56:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 22 Mar 2026 19:56:15 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 22 Mar 2026 19:56:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0b5164900a4737bd8c71921f9d6095f2a9499d5081755c56a4aa46d8f37e9865`  
		Last Modified: Mon, 16 Mar 2026 22:10:41 GMT  
		Size: 28.3 MB (28275636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18130382227055943bc69d00df6af55a8fd9d543ffadeb9c5060d81d2d5b4bfa`  
		Last Modified: Sun, 22 Mar 2026 19:39:25 GMT  
		Size: 90.8 MB (90773437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3075dd3ca6a0fa86b91a37393ad24c1548b83accb50225f49107c9eae9cc999c`  
		Last Modified: Sun, 22 Mar 2026 19:59:45 GMT  
		Size: 70.9 MB (70900499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df24fb90118d79cb71aaabd45ea4d0ed1cb77383f51e85cd1c1252df734e455b`  
		Last Modified: Sun, 22 Mar 2026 19:59:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f068260ca62ca8fb6ae776e9de60ca89b84be7221e59b38fd85496a31828f6f`  
		Last Modified: Sun, 22 Mar 2026 19:59:34 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7890f3e57ff5cafdb5e46593448eb5e2d4840fbb77301b4b4e037b918a9ba373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:941b728f994ae9252212bf3731dfce88ff1c5fb323f1bf845b276f6651481c95`

```dockerfile
```

-	Layers:
	-	`sha256:95273c9de100c3f71a441226c35ddd12d8af32c31723bafdd09d4870dbf1cd3c`  
		Last Modified: Sun, 22 Mar 2026 19:59:35 GMT  
		Size: 5.2 MB (5198711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce12ee560d2c5b9c10aa8dfe0e153f1cb256fd970e329925375aaf41e023b54f`  
		Last Modified: Sun, 22 Mar 2026 19:59:33 GMT  
		Size: 16.6 KB (16552 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - linux; s390x

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

### `clojure:temurin-25-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

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
