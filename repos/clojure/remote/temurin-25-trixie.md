## `clojure:temurin-25-trixie`

```console
$ docker pull clojure@sha256:0e45d5aeecd34d216d79d1947acc0c918e933b1c88e7cbc474aea56574927ede
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

### `clojure:temurin-25-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:cd66e0bb59fb33fd184980653a68c71105108b263c810795a157309db8f6a719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226878777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea22f1d299a9b422cc9f540191ac386a72f47b13a75ad104fd2d2df21bc7ddc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:09:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:09:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:09:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:09:14 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:09:14 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:09:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:09:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:09:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:09:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:09:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a15c0c42d29a4d45d2a10c66f7f6755a9a765092f102f11981a23d42acc1db5`  
		Last Modified: Tue, 30 Dec 2025 01:10:17 GMT  
		Size: 92.0 MB (92045295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687d1cd62511e55f90ff0a315ed60a1d4db73884805b075a879a1cd98f3e2c40`  
		Last Modified: Tue, 30 Dec 2025 01:10:11 GMT  
		Size: 85.5 MB (85542852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25c19d1910bee03242e9820db4aec4ff1e56d64870b57968f9d099b0d05cccd`  
		Last Modified: Tue, 30 Dec 2025 01:10:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5df63aeb2ebd86c2c615b04187a0c1201b8f39224e5b23cd52e57d4c0e47338`  
		Last Modified: Tue, 30 Dec 2025 01:10:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8543967992228376f33972b17af6f6747efd355a58aae2064a147b942cb596bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0fbe1e481c186c54ce733fdbeaad2b4677aef87c49f7fb9cc01b136021a9c48`

```dockerfile
```

-	Layers:
	-	`sha256:ad0eeba0362688e8000246db9fdb7a28315d016e7cfcaf4d6b7e87d1acab7b54`  
		Last Modified: Tue, 30 Dec 2025 04:47:36 GMT  
		Size: 7.4 MB (7418261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b7b9d9c24fe58426b7c688ba814dab4e3a6ebc15710697d466fa49696e72a20`  
		Last Modified: Tue, 30 Dec 2025 04:47:36 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:202edb8056c7cb1ffdf690dea7897c36f3a13675349dd8bf875084cbda5c240b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226064934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68b56c198ec37232f16462ce333762bbff692c25b4ecdd7ecf736981c5d2903`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:10:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:10:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:10:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:10:25 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:10:25 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:10:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:10:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:10:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:10:44 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:10:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd4b4ee6668ea8d591b2b9fc10e48f7128831cc6fa32d71054ea6d8aac33789`  
		Last Modified: Tue, 30 Dec 2025 01:11:23 GMT  
		Size: 91.1 MB (91052515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2eb923b66faa5c7079dd10a1850eafce338400bbcd23f7a768a0729d0543a8`  
		Last Modified: Tue, 30 Dec 2025 01:11:20 GMT  
		Size: 85.4 MB (85361186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971b38f95a97958e98c791e68394ac6eda7a511ab87edd03220dd81e53f627a7`  
		Last Modified: Tue, 30 Dec 2025 01:11:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b20fd946de32d9474e2ba71324ab9daf084c937e659c1409714f4eccde3674a`  
		Last Modified: Tue, 30 Dec 2025 01:11:14 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bbfc8a188047029f2c955d3340380aa403356038207822a8c9056cd6fdb582b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6732c9201b571d06e9cb29850a1114da25e20b4909b568e8ded05dc4baa31f2`

```dockerfile
```

-	Layers:
	-	`sha256:5e68eac60375447b36ef278e4c27fc00986fd78129eb186fbb2556c0a91f7cdd`  
		Last Modified: Tue, 30 Dec 2025 04:47:43 GMT  
		Size: 7.4 MB (7425312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b478fda257437cf51af45bf1da73ef73520f3f74892b0bd7d7a93a69ed12255`  
		Last Modified: Tue, 30 Dec 2025 04:47:43 GMT  
		Size: 16.6 KB (16557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:0351337d6b303ad2fbe1c9e929e9b70ceb517703213d57a6d529e01ef096d2e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235665453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e710f000b02c1182a81e1d883399552196513d68c1aecc1e067b54154d2c04ab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:32:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:32:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:32:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:32:22 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Mon, 08 Dec 2025 23:32:23 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 23:07:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 23:07:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe3513d576a2d4d2badd58f02126058233abf53aea816262c3b7f313a199d32`  
		Last Modified: Mon, 08 Dec 2025 23:34:05 GMT  
		Size: 91.6 MB (91610745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da45ec45f7fa7a8009cd6ce07a814e88d0a24ee721dff3402b8b92096674114`  
		Last Modified: Thu, 11 Dec 2025 23:08:46 GMT  
		Size: 90.9 MB (90945188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75068561fd075272328e2d624a007a2b3aef2d0c6c62a8dd531ae2ba505822b7`  
		Last Modified: Thu, 11 Dec 2025 23:08:41 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5df7221d03aa3e1893c77972de57363465493db030f2b83f4e6bed9f355fb2`  
		Last Modified: Thu, 11 Dec 2025 23:08:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3517fb2180be464df32a80ee194d1083d31038f33b21dd4e8184760dd137be66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dabf913b9543056e283f4ec64ae6af5d9e08f4662f2f45e8399c215ef1c7704`

```dockerfile
```

-	Layers:
	-	`sha256:55282e42f7bb304ee79c05e2e1c58d79f7f2e06be32c7129201808c7aaab5ad9`  
		Last Modified: Fri, 12 Dec 2025 01:45:40 GMT  
		Size: 7.4 MB (7423990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f38cdf47e6dcee61dc3b14357c679c38edd02984bb8e6219feb7d1153988035`  
		Last Modified: Fri, 12 Dec 2025 01:45:41 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:946e2c557eed59a32f2118e1392e4bff4868133f79042ec55a769f64cdd34df4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222949228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d883d57c81d68fa7b1853f3e05e977d160a02677a8a0eb74b2cd9c7952f6e549`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Sat, 13 Dec 2025 19:08:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 13 Dec 2025 19:08:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 13 Dec 2025 19:08:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 19:08:58 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Sat, 13 Dec 2025 19:08:58 GMT
WORKDIR /tmp
# Sun, 14 Dec 2025 16:42:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sun, 14 Dec 2025 16:42:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sun, 14 Dec 2025 16:42:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 14 Dec 2025 16:42:53 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 14 Dec 2025 16:42:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e8961870af39130e72e5dc66bd3574bb074dffc7989fd5e909f55fefadae8a30`  
		Last Modified: Tue, 09 Dec 2025 02:05:05 GMT  
		Size: 47.8 MB (47771135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e7a81485ab6b126c740ed6e6342f4229b7a854be769f1f6488cea63fad4ccc`  
		Last Modified: Sat, 13 Dec 2025 19:14:48 GMT  
		Size: 90.8 MB (90752902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915ab7e794154bf595e52e1db988550cfd9dab6a8c7544a6d282c64de9b59ccf`  
		Last Modified: Sun, 14 Dec 2025 16:47:21 GMT  
		Size: 84.4 MB (84424150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65fcec3825501926e341695eb990000078228b34e274bfcab3725c8e45cfc31`  
		Last Modified: Sun, 14 Dec 2025 16:47:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16152e62b8ac8749e605603a19315b931ef9e376f61d9b3103331a122bb28652`  
		Last Modified: Sun, 14 Dec 2025 16:47:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0ef9a43e68e80475d183a033539dcbead48acada7ee5c9d8de847ab8880134a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7422658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39fb05772fbbe8691e77ab32aa7916baf640f95c19272ebff84583e4356e2abc`

```dockerfile
```

-	Layers:
	-	`sha256:8a4badaf66475c23f844b6de7712d9ea2a048c8e77a90d1775fae6b384864c3d`  
		Last Modified: Sun, 14 Dec 2025 19:37:27 GMT  
		Size: 7.4 MB (7406183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a990656c3116934a145d29e9654e1f3ffa4757fafac532a37e3e5f077af50ec8`  
		Last Modified: Sun, 14 Dec 2025 19:37:28 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:26550c691b8fa8d151856de241a84bb8df27595f4650701290c98c8b05cd51bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224065309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb17aae78e00fc67bb24768ee0725ba897a7b52ea65b42aeaaf2602170e6f68`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 22:37:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:37:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:37:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:37:25 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:37:25 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:37:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:37:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:37:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:37:42 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:37:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3f8967bef2f6a8ec916f7d3a0d528a6724093176621c5758addeeece50e41dec`  
		Last Modified: Mon, 08 Dec 2025 22:16:15 GMT  
		Size: 49.3 MB (49345908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1aea96d74749c960c1f1090f28c52cb64429f8a769bcf18dd21864d5a82ea95`  
		Last Modified: Thu, 11 Dec 2025 22:38:21 GMT  
		Size: 88.2 MB (88210741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0219b4a9c3bcdc5421deece773209ab1a06a22a8bf39e1fde71b2153702d42f4`  
		Last Modified: Thu, 11 Dec 2025 22:38:24 GMT  
		Size: 86.5 MB (86507618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456d25c866039a7cbe80116eabc20f7f4119cb1ecd618b74c6e6b568a3c502f0`  
		Last Modified: Thu, 11 Dec 2025 22:38:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8973d8890d8771d7f739ac471390920e9f4064b3ea1d7d3039c9567fa95a1f`  
		Last Modified: Thu, 11 Dec 2025 22:38:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:759bdfe0112260c6619f72702395bef44dcc1e98170d3727f65255f2441f980f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b623dfdab4f63e1ba0f2626a908cc03d68cf6fe0190e7151dc346aca07fdbb`

```dockerfile
```

-	Layers:
	-	`sha256:0d5389051a13dcf8da5a378369c0fcc874698dfe5295363843d82ea9a696a68c`  
		Last Modified: Fri, 12 Dec 2025 01:45:48 GMT  
		Size: 7.4 MB (7416731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd96911c650bf5a9700916a5a52e2bf4a2ba2119e9e418cb2a1450b1e664c535`  
		Last Modified: Fri, 12 Dec 2025 01:45:48 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json
