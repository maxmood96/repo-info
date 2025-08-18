## `clojure:temurin-21-tools-deps-1.12.1.1561-trixie`

```console
$ docker pull clojure@sha256:885ad5413605acf87f22f67feb16002a16bcd8e70cd85fc4fa4c6cbb26317a3e
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

### `clojure:temurin-21-tools-deps-1.12.1.1561-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:2a09548e0ce86cf8c5822eb0d33d2ad4814126a8335281a39bed0c67e15b983f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292519609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bcbb2ac5b800f528c5ac44f10c93672cdfd29fb6fea9ce36f988c243e355e29`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a29c3788040f717956aca636848653c50a422fb82d52ed29b23320805db928`  
		Last Modified: Mon, 18 Aug 2025 16:52:51 GMT  
		Size: 157.8 MB (157804771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b7932b70969afe5422f34a5dbd52470b1d5bc92cca1fef09d7ab593d698551`  
		Last Modified: Mon, 18 Aug 2025 16:52:49 GMT  
		Size: 85.4 MB (85435516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e343ed467f16adf2bd8eac2dd80b0aacfe1ed39c73168fd2d57092be879cad`  
		Last Modified: Mon, 18 Aug 2025 16:54:05 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da47f98e86be17d1d6e15b9da48cf4c7c0ae85c75935700fda034254f41afe23`  
		Last Modified: Mon, 18 Aug 2025 16:54:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1561-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:51f11703a879ed96fcc76722261a4a09dea6214a2f768a2ab9e91fbfccc2f4f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3877793b41f862a707e700f99d87e288a7787a5c31a1ce02a293c1eea662071d`

```dockerfile
```

-	Layers:
	-	`sha256:a03001e82aad1560e9cefda6db7eaf87960ae6fc506207b5bbf08664a80263d4`  
		Last Modified: Mon, 18 Aug 2025 18:41:33 GMT  
		Size: 7.5 MB (7465991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45eccefba70ca28b266eaa078ecf61f0abf297f36168414db9f3465ed127008a`  
		Last Modified: Mon, 18 Aug 2025 18:41:33 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1561-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d757fd6b0779964faff9f766f02215bfcb60ab792bf230e0150c767d74f0a99c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (290979904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f1a08ba988a0a0cd95e1f998306811272c71206b3effa3e240f1209d5d0e9f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7dffd1770ccc7064c174de1d859e06dacb9263f4c3b5b48d7ee5c92344915b6`  
		Last Modified: Mon, 18 Aug 2025 17:17:42 GMT  
		Size: 156.1 MB (156081252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68e33629426396a82d59ca975c4ff13f4f51ec47130596f4eb54e3e4c4b3d29`  
		Last Modified: Mon, 18 Aug 2025 17:18:07 GMT  
		Size: 85.3 MB (85256008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc63161ec1362b86ea56f647a591ca0c7f08981da5a2ebbbb9d6270069f485d1`  
		Last Modified: Mon, 18 Aug 2025 17:18:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c490542d8eae26caad28e98d7c71aad8bba593274e038e4eac057165131389e7`  
		Last Modified: Mon, 18 Aug 2025 17:18:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1561-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:19c9da22110aa1594c9190cb40fcf1825f494c714607f89b80bdcec7a0de0ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8982d22ee5252087610199f9395536d513406fcba6e05ac9ce0792535f7194`

```dockerfile
```

-	Layers:
	-	`sha256:3125f0aa7d53bf46a496ad9e793138af2d22ecd3ec1435894d3f5e96f2118bbe`  
		Last Modified: Mon, 18 Aug 2025 18:41:39 GMT  
		Size: 7.5 MB (7473045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:768a3b121f04c8d2d2682d06646ab32b191619843ad09ac2747526d7705b8d98`  
		Last Modified: Mon, 18 Aug 2025 18:41:40 GMT  
		Size: 16.6 KB (16607 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1561-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:b4c639265edb13409de9debf1121e42f001bbbc50e4f7b44474524b9760425fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.9 MB (301908627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa0246e75283d0fc47c6d85526888c6858e4d9dffdf3449773b0e4d3d131a1a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d990776a519a48cfd9f76c1a1eb9307ce4a16a3ce460aaa1ddd5616cf2ea8d`  
		Last Modified: Mon, 18 Aug 2025 17:31:43 GMT  
		Size: 158.0 MB (157963439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a8601ce29ebad13bf18cb01cb1d91a334a3ed88bdb97739ada105570dea39e`  
		Last Modified: Mon, 18 Aug 2025 17:32:07 GMT  
		Size: 90.8 MB (90840761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa4a997855cb7a0613623019631d8a73f65eb01ebb8b0759a420245eed7b339`  
		Last Modified: Mon, 18 Aug 2025 17:31:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed886a054a10b83da8d9232de353aaa46e4698cc6c8d7495e57d9879b85eb33`  
		Last Modified: Mon, 18 Aug 2025 17:31:59 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1561-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:59d7bf42ddeba890cd1078e9f9f52f31017c1b2dcfb23e7df313ffa0f73cc469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07932e3a7e7e2506a38ce90897325c65e186f89bd0408efa2908557c53c69232`

```dockerfile
```

-	Layers:
	-	`sha256:f3201ddf15f507846acaaa4ee877f70964e007436a070e87525d5ad8cbbcf814`  
		Last Modified: Mon, 18 Aug 2025 18:41:46 GMT  
		Size: 7.5 MB (7470422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a0267ffe05f822c72b64315e8db31daf2d0c6bbed49a05e2252640cc9faca6a`  
		Last Modified: Mon, 18 Aug 2025 18:41:47 GMT  
		Size: 16.5 KB (16524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1561-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:9f275320369eaf68b4ca9df2a792cd77487970ccf7ba1b42942a7cc513210607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.8 MB (282776409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd48ecd1bcaf5377049592d1a1c97849c679f932330ebae8f02e27d204eb334f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f10f6fabddb898b27af6c47bb359e1bfac1271c2bccd5a6c9dbce1d92c1b29`  
		Last Modified: Mon, 18 Aug 2025 17:58:12 GMT  
		Size: 147.0 MB (147026960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebeba6afaed07ac30cf550368692462c12218201e4be6ce21b478658549ff2a2`  
		Last Modified: Mon, 18 Aug 2025 17:58:46 GMT  
		Size: 86.4 MB (86403244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43298269ca2f2f3add39cc5d45d8498ea2af1afcd818d9ab230346a3909a7be0`  
		Last Modified: Mon, 18 Aug 2025 17:58:36 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576e6bd34ff70e71608de6b34e2b8dd48cc29fcdf479b41a1e5aaadc968e68a5`  
		Last Modified: Mon, 18 Aug 2025 17:58:36 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1561-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:02041de065e693a1bedf2c7e7a356f8aadcf741d10b731b732bf4e013ee510e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7478378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fc28889947b32f5c5ea4ec8b47b465acad429275aca734999c413316eb79bd`

```dockerfile
```

-	Layers:
	-	`sha256:59f84aff29310aea52e99311bdd80475b8bc277ba09b00fe6c6870ebdb69871c`  
		Last Modified: Mon, 18 Aug 2025 18:41:53 GMT  
		Size: 7.5 MB (7461913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6beacab459f04f9739f719d1b27c9d2432b774cd31c25c11b5296ce199f391f7`  
		Last Modified: Mon, 18 Aug 2025 18:41:54 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json
