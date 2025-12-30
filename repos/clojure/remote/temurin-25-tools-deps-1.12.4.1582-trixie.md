## `clojure:temurin-25-tools-deps-1.12.4.1582-trixie`

```console
$ docker pull clojure@sha256:b50462011cc07f11a13462c0e29f4caaf47308ccd5fb13026325bb8850fd9e15
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

### `clojure:temurin-25-tools-deps-1.12.4.1582-trixie` - linux; amd64

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

### `clojure:temurin-25-tools-deps-1.12.4.1582-trixie` - unknown; unknown

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

### `clojure:temurin-25-tools-deps-1.12.4.1582-trixie` - linux; arm64 variant v8

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

### `clojure:temurin-25-tools-deps-1.12.4.1582-trixie` - unknown; unknown

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

### `clojure:temurin-25-tools-deps-1.12.4.1582-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:c76078c7fa403786c362c26065e134b18e91a107ddccbd1d0d4b7f02bbfc846d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235665032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1063205c2d8c19fd5bf0f0e89ba0c4dcad982ecb3ad6894cf4364a7b235073c8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 05:29:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 05:29:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 05:29:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:29:25 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 05:29:25 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 05:32:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 05:32:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 05:32:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 05:32:57 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 05:32:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d586c84fb9377f9b3f4030e2c3e1e9ff7b1a23a68b8abc2c48a43163a3589257`  
		Last Modified: Tue, 30 Dec 2025 01:51:01 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0b337200b6e61d16776f5501182cfaee70700993bebbb12367907868e271e3`  
		Last Modified: Tue, 30 Dec 2025 05:30:49 GMT  
		Size: 91.6 MB (91610796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b60e94c27c72e8acf4978d1cf59249b52f71215c6c75e4eff8c221d805b04e6`  
		Last Modified: Tue, 30 Dec 2025 05:33:52 GMT  
		Size: 90.9 MB (90944708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b4985330ddf3abea48c8f0cc9a4918e1e1ec5cf3f39d140e52d8dbc0bc17a1`  
		Last Modified: Tue, 30 Dec 2025 05:33:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bd36e438e7305d95daf4994c9eefbb14f68ea5ab8f43ad03204e844f7f21a1`  
		Last Modified: Tue, 30 Dec 2025 05:33:43 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1582-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3f6c27b7c77cab39d9f9d2f26c1df690f43518fd6a85f002320cca317a7634e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92c2ca2f3affffb2e950d0d5ea1f70215478c64a41889ecdb83557b23b9ced0f`

```dockerfile
```

-	Layers:
	-	`sha256:0b37192238dbb555bc381193d8f70b26013f9cf11affac94ab7861b59b9cf221`  
		Last Modified: Tue, 30 Dec 2025 07:39:16 GMT  
		Size: 7.4 MB (7423990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:398005e9532e74560ce57ae34d8134882524493bdbe93261e7a5fb54eacc8c99`  
		Last Modified: Tue, 30 Dec 2025 07:39:17 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1582-trixie` - linux; riscv64

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

### `clojure:temurin-25-tools-deps-1.12.4.1582-trixie` - unknown; unknown

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

### `clojure:temurin-25-tools-deps-1.12.4.1582-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:a4a16025ead752f1e7cdac3cc98b39b2bfd17b206aaf762ef66cd5b86a97b46b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224066196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b85cdeda6a406d281b4332baccb5709bfbd3d61cb708a8abce1879205f0a82dd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 05:50:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 05:50:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 05:50:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:50:43 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 05:50:43 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 05:51:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 05:51:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 05:51:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 05:51:00 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 05:51:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:85bc4a4d1f4e52a33d42907057e0ab87c5eb2560b332d94f6e9d7da79c0c76b8`  
		Last Modified: Tue, 30 Dec 2025 03:26:29 GMT  
		Size: 49.3 MB (49345959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c3486676761ac84e2d61641ec974a4aa93c05c51fbef9de17494ba193a7f35`  
		Last Modified: Tue, 30 Dec 2025 05:52:03 GMT  
		Size: 88.2 MB (88210730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fdb2de01404fa9dfbde4e9b8c36bc87c221ba6aa9738c62f8544ff94e95feb`  
		Last Modified: Tue, 30 Dec 2025 05:52:00 GMT  
		Size: 86.5 MB (86508466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20a1895c908438bfc38cb134cfd34739277dc4f90672648bbf19436e5c9525d`  
		Last Modified: Tue, 30 Dec 2025 05:51:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac1d508103172db3b5f890246a7b3ebedfa29eaee5e9f901023d46ec7a44363`  
		Last Modified: Tue, 30 Dec 2025 05:51:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1582-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:37a1bf5ababbc0a9fbbbc2d72dbfbae477c2ec98123e3e2a499c160ffc0ea884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64452360d73a9e7c594d7edc1c2da03564299ba1946e8f58768b3ce6fde37597`

```dockerfile
```

-	Layers:
	-	`sha256:d1d164d64a39af21a119784226e7858f343834684c8488f3a8c08f1a065ddf8d`  
		Last Modified: Tue, 30 Dec 2025 07:39:27 GMT  
		Size: 7.4 MB (7416731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d24e1f4b798acac1f2415a579530c9e300db65937f136bc99107024b155c2b3a`  
		Last Modified: Tue, 30 Dec 2025 07:39:28 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json
