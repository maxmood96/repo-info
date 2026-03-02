## `clojure:temurin-17-trixie`

```console
$ docker pull clojure@sha256:5ee51bfb767f8e79b30d840b294d7d35fc143861ecc4598771f8d505b7f5d627
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

### `clojure:temurin-17-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:beddd6264d537965668423c547c671129753bc31a867bee73cf47a8771a8ff5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280477927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c370586d0a187bc815f42680f7a3541397890d42b15c3f420640f38e3120a4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:47:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:47:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:47:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:47:01 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:47:01 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:47:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:47:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:47:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:47:16 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:47:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d18ef2847da214bca2fbf88290beb35008491b24f2b3f10ec7825aabe5793c2`  
		Last Modified: Mon, 02 Mar 2026 19:47:38 GMT  
		Size: 145.6 MB (145628711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f5581edc496f606b3e1434f1abfa99abcb1a8543eadf604f3a3f910b7ae97d`  
		Last Modified: Mon, 02 Mar 2026 19:47:37 GMT  
		Size: 85.6 MB (85555049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60930b9449dfdffd7f92636edb3f8de87421d49d2d9d8e148a4d25ee397092a9`  
		Last Modified: Mon, 02 Mar 2026 19:47:34 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb3c051791e710bb00176a70cac2d5599eaa977ac0130abbbf96f4391f5aff1`  
		Last Modified: Mon, 02 Mar 2026 19:47:34 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:97ac59c6305ad6b3bc64d192b6b72d67ad07fd1a16fd249a1b431b684442a387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f3ff92828dd5cb83aa1ce17267747d3ef0f89db81cb09cf9318b8d07b178cf`

```dockerfile
```

-	Layers:
	-	`sha256:82db9839f142d747d3b193dcfc8de9fe18f1b3acc26076d6b12a847383fabf56`  
		Last Modified: Mon, 02 Mar 2026 19:47:34 GMT  
		Size: 7.5 MB (7470593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:120e0f2c9f880e63cf239a898404a78a6053f0b33c2a20889e9f5cd99c442e49`  
		Last Modified: Mon, 02 Mar 2026 19:47:33 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9affd22c84c747574dfed75e16b92ea12807eace14751cdabb99dde9d26aedaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279467458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:326c6080fba4e796fc6ce370ba7f82665d37eb495e1992d88fce9325666c458f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:46:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:46:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:46:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:46:45 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:46:45 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:47:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:47:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:47:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:47:04 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:47:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f931d66e67eb25139393797578bf4a25b4faa8fc35347d5ca5e3bdff7a7cd7`  
		Last Modified: Mon, 02 Mar 2026 19:47:27 GMT  
		Size: 144.4 MB (144436244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4f125758fbb8937876cdb8c65932663047de27158de98ff1c9d1dfb916d304`  
		Last Modified: Mon, 02 Mar 2026 19:47:26 GMT  
		Size: 85.4 MB (85378004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279593e5b146c0cdea00601aa3d9cd0cb981f7a0f376b0615fd86e317657e9d7`  
		Last Modified: Mon, 02 Mar 2026 19:47:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d32370d0c5af2dc00eb6ed08151cd667e592fbc430341395dd28a953b422d43`  
		Last Modified: Mon, 02 Mar 2026 19:47:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fc8cd278a4515e46311a3ddfd71d3a62a821668a64d4fc8c2d170824225bc4ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f1fd2d6a0ccde54005a09894139d9fcc51f74de8d63392e95a5cd30a2687ba`

```dockerfile
```

-	Layers:
	-	`sha256:81df7c876287bc039d47e7d4c6a101f42f7d978db9818d80d7bfbfa7a586d7ff`  
		Last Modified: Mon, 02 Mar 2026 19:47:24 GMT  
		Size: 7.5 MB (7477623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d494889b2db92364874e6e787b445d3f6819e7e7cf717096cebef75d83bdb4cf`  
		Last Modified: Mon, 02 Mar 2026 19:47:23 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:2401b438729c8bc95f74b3bd1bab3d4a7700ed6cd2ed73c8b1274ea8de36d10e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289525526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d59e3f357ee57eb6b3b555b52b6905ac2dddebcafd6b175226f64f67195fefb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:59:26 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:59:26 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 20:00:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 20:00:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 20:00:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 20:00:26 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 20:00:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638f11e3e8c51f960024a437542fb930078ce0b91c8b3d3ea5b85f3a40326b55`  
		Last Modified: Mon, 02 Mar 2026 20:01:10 GMT  
		Size: 145.4 MB (145438252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5842317e69e8b8d4c3f73c750719c9c01aa4bbeae909c08adcb2e574cc4e1e5`  
		Last Modified: Mon, 02 Mar 2026 20:01:09 GMT  
		Size: 91.0 MB (90973970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebce81ce7e4f1c0363813cb20e3a02997719a8610513e3b4a848e78e95c74a81`  
		Last Modified: Mon, 02 Mar 2026 20:01:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85352e969524f5a32e9234ba7011c3866b1c9fccd0a5ffcd2aec3235cb7707c1`  
		Last Modified: Mon, 02 Mar 2026 20:01:05 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:191e53eacffe415d4343d5eedbc38b9539706a70e5facf3a57ee7e93e72a5933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963b9a0c19f4afdb069de3b819bc69388876f2bcbfa34be8bb12d66a19953d69`

```dockerfile
```

-	Layers:
	-	`sha256:3b8cdea0fe5ab44f45a3f4de6dc472e6636c74392421bbfdbf796da1d29b10e8`  
		Last Modified: Mon, 02 Mar 2026 20:01:14 GMT  
		Size: 7.5 MB (7475014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd329af3246f1c4fc8f6e193f9631ebf426a33217d111293492a0acea7e61b12`  
		Last Modified: Mon, 02 Mar 2026 20:01:08 GMT  
		Size: 15.8 KB (15801 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:e2df82ce084c06bb3f60d36facf579549c8a69bc52c5e8b008c1e6d261fbc578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.9 MB (274865328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9fd40f700b1689e04f8b0f68c85f150ec92eb9a5f45a9d065d6521a00ab245`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Fri, 27 Feb 2026 21:20:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 27 Feb 2026 21:20:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 27 Feb 2026 21:20:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Feb 2026 21:20:56 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 27 Feb 2026 21:20:56 GMT
WORKDIR /tmp
# Fri, 27 Feb 2026 21:36:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 27 Feb 2026 21:36:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 27 Feb 2026 21:36:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 27 Feb 2026 21:36:30 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 27 Feb 2026 21:36:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3be247472b67578a1d05739722d8adeca41098796e5d6210800176db58046fa7`  
		Last Modified: Tue, 24 Feb 2026 18:57:42 GMT  
		Size: 47.8 MB (47776936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f27f4bf7ad939ca2936c66027f77feab15c20528c320fcb92eb833d88b76cc`  
		Last Modified: Fri, 27 Feb 2026 21:27:01 GMT  
		Size: 142.7 MB (142662998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb458e28279666b452fa1a83642b925c284d11c7644b5a9373035d201e9d1ae`  
		Last Modified: Fri, 27 Feb 2026 21:40:52 GMT  
		Size: 84.4 MB (84424346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8ac6abc14fbb5137d1fb9de2666cb1bc844ca379acacf7ba37e75eff968e48`  
		Last Modified: Fri, 27 Feb 2026 21:40:39 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35123d56f3dea28446067705d0f695aba837a357dd6281ce8f3727340f1f923`  
		Last Modified: Fri, 27 Feb 2026 21:40:39 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:cef1e05b187d9ff96c5c7ba6ae74148df432fee28245c5ba1494bd2841b1a507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7470878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2965d86f538abd26602567e8a5f9d5f728d19ff862f90a2b450bbbadecff978`

```dockerfile
```

-	Layers:
	-	`sha256:1e2e2a6eb27ac9b1ff316c383764239adfcafb9da046333f61f06bcbdd32ea9b`  
		Last Modified: Fri, 27 Feb 2026 21:40:41 GMT  
		Size: 7.5 MB (7455076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:974ffffc29c65f86482811b4019ee0df5f26ec7ccff1bc10cf0811e9fcd7ff17`  
		Last Modified: Fri, 27 Feb 2026 21:40:39 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:fb286382085fa44f98d0b4c56aada926b1cf7e6e257d69605fe309cde598291a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271513529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a3a036ab37091f56dbc643262e65a1610e709f14cca61cf5318d1946e492f2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:46:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:46:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:46:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:46:16 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:46:16 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:46:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:46:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:46:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:46:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:46:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04677bee290b0116e28330c00d6d290a6256cb4d2b23929ae5bce501058ad83`  
		Last Modified: Mon, 02 Mar 2026 19:47:05 GMT  
		Size: 135.6 MB (135627117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fe2220f119c109a71d6e5e7def53a8e46287f6b26ee568fbaa0a86fc5acfd5`  
		Last Modified: Mon, 02 Mar 2026 19:47:03 GMT  
		Size: 86.5 MB (86530835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874d805c9c6e1bfaae544e4ccb38ced5a3448260da6a6051332e5ae844f970ed`  
		Last Modified: Mon, 02 Mar 2026 19:47:01 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7eef0b17171edaac3128fb6c60e1efdced52a9db9847c380180c89b762df68`  
		Last Modified: Mon, 02 Mar 2026 19:47:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e4ab9f0acefc8e723b0ad2191d6bae03078b2a64253e45ae1ecb773f71effc37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6737d10693d87ba84abe2c8522200b782a928fb02e2ae04363769aa49ba6a597`

```dockerfile
```

-	Layers:
	-	`sha256:420fd1e567b5c6fad4cc4c9496d19ea2cf70ddbf2090685763a61edb0f1295a4`  
		Last Modified: Mon, 02 Mar 2026 19:47:01 GMT  
		Size: 7.5 MB (7466515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71ff8d97a750aef5f6bf6369e0bcc1f72dd617075d9ebaab8bc08ebe927335a1`  
		Last Modified: Mon, 02 Mar 2026 19:47:01 GMT  
		Size: 15.8 KB (15753 bytes)  
		MIME: application/vnd.in-toto+json
