## `clojure:tools-deps-1.12.4.1582-trixie`

```console
$ docker pull clojure@sha256:930975cc266044ab73264de5e276b4115141659f97c2543fd4345186aeb84e8c
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

### `clojure:tools-deps-1.12.4.1582-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:143efd87d4a0371c234605f84583e3d037e42a7c4194f7e7e3d4764878d8e1cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226874654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee622916e96bf5fb19e560c49dbeef68e78a77096633e2bad1299fda8739c6a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 02:07:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:07:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:07:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:07:28 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 02:07:28 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c900d30a9a8588c9e2de3ac94d06e07a7f4f1e95ba3a0e2e60126c3ea3fe1d64`  
		Last Modified: Fri, 16 Jan 2026 02:08:22 GMT  
		Size: 92.0 MB (92045322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee86663e9cc46dc50795744a393285134f819d3aeeed6fa4abaaeaf93df78248`  
		Last Modified: Fri, 16 Jan 2026 02:08:09 GMT  
		Size: 85.5 MB (85542668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea3a7cb32d39ee887724ac96aca8f9f51887010f67e39a3d55fa5320afd328c`  
		Last Modified: Fri, 16 Jan 2026 02:08:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920f6870d2b1b1f579debea6f77cd7194ae53cc81533c35bf5cd1fb18dea9825`  
		Last Modified: Fri, 16 Jan 2026 02:08:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1582-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:cc8e0536ecd28437514a2cbac3cc48ee9d04dd1509e97f7041fc5ec54a2c1e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9ba9eae3ac185fec0b6d21b4a70ecd9d6cd7588113f4f40a7246615552f302`

```dockerfile
```

-	Layers:
	-	`sha256:368b577cdb64900ae7f86d10bad839b82c4a6d6039807ea66337746983a5cc09`  
		Last Modified: Fri, 16 Jan 2026 02:08:06 GMT  
		Size: 7.4 MB (7419156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f908bf711d02999da039f536d1c2bc9c2cf8656d94565e90e72094e4616b9ae1`  
		Last Modified: Fri, 16 Jan 2026 04:51:39 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1582-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bd7d50e603091eabfd6581dabde1016ffa236f53f0393c7d184cf8e872faef7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226062813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8939ff8a7e338d114dd5bf5418d750d5be0a298bf095e3e6b60aa585b946bc0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 02:09:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:09:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:09:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:09:57 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 02:09:57 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:13:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:13:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:13:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:13:04 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:13:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d6fa6f7e598bf4a51eec1f2009a61688e75b55c510a2c12ae1a194db9f4a7a`  
		Last Modified: Fri, 16 Jan 2026 02:10:35 GMT  
		Size: 91.1 MB (91052478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57928153e2765a115f992c31ebea450d8b3417b8c64bbec6a1bacb0891e207a6`  
		Last Modified: Fri, 16 Jan 2026 02:13:23 GMT  
		Size: 85.4 MB (85361213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c8e5d64cc9257ed153a8891a9dfc2ed79a9bdb851ee2217851c06a00a77f2d`  
		Last Modified: Fri, 16 Jan 2026 02:13:28 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84563c54282d778e8aabe0c50684c27789e87c39998ad3ccd1aac383d372739`  
		Last Modified: Fri, 16 Jan 2026 02:13:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1582-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9448058a4c016249a4d7e7d593c78e1e17f21c34e8c38fdf6cfc566d3b2f496b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5725ea71d48b085d66844f19210814f1f26aada41f5fc5c4255a335bc7074453`

```dockerfile
```

-	Layers:
	-	`sha256:709bfc21ae002e348443f8456ddba38cd257a0658e1935024c5704242ea35aeb`  
		Last Modified: Fri, 16 Jan 2026 04:51:46 GMT  
		Size: 7.4 MB (7426207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f25b0455563e85ffae768bc63c216a17047c8bdd09f0aa2cceea39750fefa665`  
		Last Modified: Fri, 16 Jan 2026 04:51:47 GMT  
		Size: 15.8 KB (15758 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1582-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:1966c221853f67ea1387a03c5ebeab1d56fd3979c7dd7de5f64db2bcb7515c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235667324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d462079964ca0f53bf79bff4e7b2ca258e2cf993a40be0a9f3a61dd5094416b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 03:44:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:44:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:44:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:44:39 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 03:44:40 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:50:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 03:50:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 03:50:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:50:21 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:50:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:58 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1f64ed71cadbfa0fdd0e4e5f9f9173c20301e99b8d557346b7aeda0ac3389c`  
		Last Modified: Fri, 16 Jan 2026 03:46:40 GMT  
		Size: 91.6 MB (91610765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ce68ebf51014378a6dd59e41ceac83a1778003875ca0932bac6e98ffd3a316`  
		Last Modified: Fri, 16 Jan 2026 03:51:06 GMT  
		Size: 90.9 MB (90948553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863031bef982b418a28444ab796bb94e7a7c69621783f97207c7a62f7cb96bff`  
		Last Modified: Fri, 16 Jan 2026 03:51:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25301834ff6dc698a80cdbd5821f6a17a151df7308f98d1dfc4faeccd21f3d84`  
		Last Modified: Fri, 16 Jan 2026 03:51:25 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1582-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a9ba6370ac651403835904eb29f140c6bb5f8b675ecd43d9b4ec69c167fff74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cbc9127c2b7d3c5722087b5d0aedc90cdd2bfbe921d9e505ad03f8c05296a8f`

```dockerfile
```

-	Layers:
	-	`sha256:b9cb79170a10088573ddecf39f02b0c02bdd446c47d262179e445e4e2411b96f`  
		Last Modified: Fri, 16 Jan 2026 03:51:03 GMT  
		Size: 7.4 MB (7424887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0538851deaef930e7e482cf3e6628e2f8757bc61ed2c4d717067afe9cd86b080`  
		Last Modified: Fri, 16 Jan 2026 03:51:03 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1582-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:a6a5d0f98c26e631bb4334e9e880310aeff370d05ad75046e588eec56618680b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222949113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09972d1ef764c77912b88691c0005f4e7633bd4da7b808bfb412094d41ebabb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Thu, 01 Jan 2026 07:24:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jan 2026 07:24:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 01 Jan 2026 07:24:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jan 2026 07:24:27 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 01 Jan 2026 07:24:27 GMT
WORKDIR /tmp
# Thu, 01 Jan 2026 07:38:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 01 Jan 2026 07:38:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 01 Jan 2026 07:38:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 01 Jan 2026 07:38:59 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Jan 2026 07:38:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aaf3ef12aa0c431a6203a456b21b1e30e26cb56dfc257b8bca2efe1ba7c531de`  
		Last Modified: Tue, 30 Dec 2025 00:51:23 GMT  
		Size: 47.8 MB (47771153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e72db194620f93f57207f61aa544e094761861bb8fbdbf65160d1e1594a9c91`  
		Last Modified: Thu, 01 Jan 2026 07:30:30 GMT  
		Size: 90.8 MB (90752893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcbe9fed58bbc38ac063c5ed091bd1d2c011f14d2040d7f23f5f7a00a577204`  
		Last Modified: Thu, 01 Jan 2026 07:43:18 GMT  
		Size: 84.4 MB (84424021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd9e1ebe2c1d294a974e9167b1fcd28f1c864b86822aabe277361a2c2666917`  
		Last Modified: Thu, 01 Jan 2026 07:43:25 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780b6c87508d36f5c3312f1ba3e4f71c54a8ecd9fbe887c563d50a42f6aeb0c8`  
		Last Modified: Thu, 01 Jan 2026 07:43:25 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1582-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5e78f243e2193bd66297be8360ab94345507f179dbbc2530472e6f6c3956c112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7422658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed80a35ff71b408c1bb2745a157d2ca33450766546b2b8aa8c579a8a74c3112`

```dockerfile
```

-	Layers:
	-	`sha256:ce769fecab3af4f1003225079c4abca8f41f2510f1f71e1f83922668c9748791`  
		Last Modified: Thu, 01 Jan 2026 10:38:09 GMT  
		Size: 7.4 MB (7406183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:749924ae04839adb99dc146b0d9e4a589ff1b416e87fcb8ee21cf5e96ef9d3d6`  
		Last Modified: Thu, 01 Jan 2026 07:43:05 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1582-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:89e9f8c73f0f12130af83e4eed070ebc0f9ccfa60f82efe615c5793d899446bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224069299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b66be9bba6f0dfb909fafa8cbd02842190c750ed1226d1ae5403075209f012`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 23:22:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:22:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:22:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:22:58 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 15 Jan 2026 23:22:58 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:24:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 15 Jan 2026 23:24:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 15 Jan 2026 23:24:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:24:41 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:24:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:46 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9da15375349ed468c4d395178dea5e2fe711fa01064413f4605f3f47af67086`  
		Last Modified: Thu, 15 Jan 2026 23:23:38 GMT  
		Size: 88.2 MB (88210648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611928ed90b666c9de596d9af9a1f9c28c56322d09861807845b37ffd684b100`  
		Last Modified: Thu, 15 Jan 2026 23:25:26 GMT  
		Size: 86.5 MB (86508906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761a62d3e001b9945849464a1f6edbda065a93d4e339e6f37874ab224e3e095a`  
		Last Modified: Thu, 15 Jan 2026 23:25:12 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be681c74bd53a51ecf8f6e450ebb0e71034ff9b6a64a08765cecedfe2a0475b`  
		Last Modified: Thu, 15 Jan 2026 23:25:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1582-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4bd0318bc99dee240496ac8a514d97889c033a183500e81a1ef7b3c2c3c733cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c787c95afb2d42c847825b0552d1a68295b75cec842390684a5d4b970b444061`

```dockerfile
```

-	Layers:
	-	`sha256:94f9507fa0694b19a01c16f9210909ee05f52f7c94398c34ab1225e8d615be7d`  
		Last Modified: Fri, 16 Jan 2026 01:45:07 GMT  
		Size: 7.4 MB (7417626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fe04cd5d4dd9ca9f6fe7b2616715eafe22da6124fa050f1b5fca99b8b0dda73`  
		Last Modified: Fri, 16 Jan 2026 01:45:07 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json
