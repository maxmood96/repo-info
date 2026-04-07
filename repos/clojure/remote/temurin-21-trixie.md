## `clojure:temurin-21-trixie`

```console
$ docker pull clojure@sha256:20eede318f69c6a5e52d0a947c3a7d33d0f02d91e33358921b8bdfe3bc2bd956
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

### `clojure:temurin-21-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:df31a3d932f78d35ab7fbbd77f832c3467adedfabb6e90dfd2f6720a7b112f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292723497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:909c4dc39491bd29f3e8633c01c021b70f670a2b44b00703702ca76c21c7b5ea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:16:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:16:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:16:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:16:18 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:16:18 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:16:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:16:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:16:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:16:34 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:16:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7262c0cbce49dcff4494fd56231d4ea387966e23b2709a1fb89188e991fa52`  
		Last Modified: Tue, 07 Apr 2026 03:16:59 GMT  
		Size: 157.9 MB (157857094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7d23d69e65c3d78d67c89690430a403137e460d62a451229403237a8c5f879`  
		Last Modified: Tue, 07 Apr 2026 03:16:57 GMT  
		Size: 85.6 MB (85567526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b710e07684f03606781efa22beea876f953d9c0b3c482102688ebc6191fd83d1`  
		Last Modified: Tue, 07 Apr 2026 03:16:53 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad9e0494850141dbf215c1de485d2a466e972b24bad9fc74c2cc96ae884475b`  
		Last Modified: Tue, 07 Apr 2026 03:16:53 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4fc3f860c8295b1884cccc487458a807ce68982204447658d4f54c7e268ac307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7488273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc2b9a925ccab6072df8f24b20e93bd1ac3cdfad47afce51382fb0a57ebb22a6`

```dockerfile
```

-	Layers:
	-	`sha256:255a70f97edcc8cfd2abbe41b7696961e671491f7a2d513af4f85c95472bdc5c`  
		Last Modified: Tue, 07 Apr 2026 03:16:54 GMT  
		Size: 7.5 MB (7472519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b149f9eef2fd5c8843d272117f67649639a5161ea105469960b0484fa95721be`  
		Last Modified: Tue, 07 Apr 2026 03:16:53 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:089ab762abd62f2f932542b67e5bdec9f005700e31ab744acb3683fe7529033b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.2 MB (291182326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b1d1871ddda786203ab5ffda6680a4e6a0f1b036c2edb46f5e5d53ba7deaa3b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:27:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:27:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:27:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:27:12 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:27:12 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:27:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:27:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:27:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:27:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:27:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be062e0978705d16045a19addb58b3e6e02faa1fc21be8b77e86e79726f2617`  
		Last Modified: Tue, 07 Apr 2026 03:28:01 GMT  
		Size: 156.1 MB (156133049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c84aaa759bc30c31e23242cebf759c4ebc9a9098877e32e1a4f413a45f9c7e`  
		Last Modified: Tue, 07 Apr 2026 03:27:59 GMT  
		Size: 85.4 MB (85382979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fec198680cba2583f4f74a92e5794628b8243a51c4d120b8e4d33793e2d1f2d`  
		Last Modified: Tue, 07 Apr 2026 03:27:56 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4043f4f854f1874c44dc3dbc35c9f8d693c069ceba269c614e3e3f7c275006e`  
		Last Modified: Tue, 07 Apr 2026 03:27:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4ee0f7da904ff5c5570f80e868973ce643c3d6959d37e2c6de1893c35f19b9bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7495420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f654b4935ce0d789bf830ea2527adf39f7bf928b384403c69c3d925c2fda8ced`

```dockerfile
```

-	Layers:
	-	`sha256:aaee6156e471618f3be7fc62ea2d8084f5f47b992b3de9564f5496ae8cd6a711`  
		Last Modified: Tue, 07 Apr 2026 03:27:56 GMT  
		Size: 7.5 MB (7479549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a62c11916e2e5d36fd32fc6b15b4798bf662dbc912e8facf74da77d5ead810c`  
		Last Modified: Tue, 07 Apr 2026 03:27:56 GMT  
		Size: 15.9 KB (15871 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:dc4d6ba70fe1ce4073244eb6112948b2c1eaf76b28f229502493d889ff09d80b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302084378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba359c42dfd198bb46eaa2de6a029358cdf01735548f68da1090d94c9875a68`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 14:47:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:47:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:47:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:47:39 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 14:47:41 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:52:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 14:52:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 14:52:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 14:52:16 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 14:52:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dae9dc83e459c0aac03f4da141b2222e67e4c531d619bb7dabf0549311b9fd0`  
		Last Modified: Tue, 07 Apr 2026 14:49:20 GMT  
		Size: 158.0 MB (157977541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a3a6fbf8e1cea2ddfa7fbfbdaf8792bb5c6233ba8d8e72991ebdbe7005aa7a`  
		Last Modified: Tue, 07 Apr 2026 14:52:55 GMT  
		Size: 91.0 MB (90987125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9cc23e218b2fe46246c86817864b79e157f3fdfa70dfaf6a9dbf90019afecd1`  
		Last Modified: Tue, 07 Apr 2026 14:52:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caba1bdd01aac912f391c8916aac4146d6eb947ecaf2dae9220a1b82a9e5900a`  
		Last Modified: Tue, 07 Apr 2026 14:52:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1b9f26dc3cc6add5592bdfe67a71b5cb58329b6b7b2a75c679e6d1d5601a60a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29533c3ec798872d303292fc41f6d0fdd72246f063dde5e2fb87ce49c7b35d6`

```dockerfile
```

-	Layers:
	-	`sha256:489386e3b26e175ea091bda8df0401d3a12e29b6f90c711d758dcb60b5cd5688`  
		Last Modified: Tue, 07 Apr 2026 14:52:52 GMT  
		Size: 7.5 MB (7476940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d88f9359d8d68165b4747ddc9c97059cd37ff77e4c13ea81b44c0ca5ce96a5d`  
		Last Modified: Tue, 07 Apr 2026 14:52:52 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:8b72171adf5c109e15a332384043887cfd4a2d9e24d4c44f963245fa6c1a6a5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289469621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dde1bf549e73320e42ee4b0400669ee72dbf183c677f963915fc91ede7990ba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Sun, 22 Mar 2026 18:48:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Mar 2026 18:48:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sun, 22 Mar 2026 18:48:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Mar 2026 18:48:58 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sun, 22 Mar 2026 18:48:58 GMT
WORKDIR /tmp
# Sun, 22 Mar 2026 19:11:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sun, 22 Mar 2026 19:11:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sun, 22 Mar 2026 19:11:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 22 Mar 2026 19:11:49 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 22 Mar 2026 19:11:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:90acba8ac92ad141ae919a99e64549b2f417e5b2ec79f1a99dbc8efba0fea96b`  
		Last Modified: Mon, 16 Mar 2026 22:09:11 GMT  
		Size: 47.8 MB (47792328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248da4038c4f4bc829cf60fb1b9101715933fefeff01226fdf6e29839b9227b5`  
		Last Modified: Sun, 22 Mar 2026 18:55:14 GMT  
		Size: 157.2 MB (157216869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239cbdff89f65d346fa3eb045bd1961e4fa114edbddb78fab680aa7eeb7ac5d6`  
		Last Modified: Sun, 22 Mar 2026 19:16:21 GMT  
		Size: 84.5 MB (84459382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35434218e51a735f254dcb5e886ecb0502b3c331b3241901590707a8f197a3b5`  
		Last Modified: Sun, 22 Mar 2026 19:16:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df0ef619d67b2eb8840ea844c5ad5bb8ef015fde1db93c8a597dc12e9b00449`  
		Last Modified: Sun, 22 Mar 2026 19:16:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f98cfe7b6da41b1a310acfdf6fe7e8a488608e1148fae110d23badb9003d2a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7476236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d56087e09285e699da63c5d2e1919fb8f4830f4a9991d190f3a5267721a7113`

```dockerfile
```

-	Layers:
	-	`sha256:172609e1e6accf6bd26539a0f293487982310ec65f2f1466df2cd1475ae496ce`  
		Last Modified: Sun, 22 Mar 2026 19:16:10 GMT  
		Size: 7.5 MB (7460434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bdd8d6b351a0fa64248d41faa203b34dfb4d2ee91b3451c364c153c414325a7`  
		Last Modified: Sun, 22 Mar 2026 19:16:08 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:e6a1a4e79feabc01aa73d069982095009cf1280b45904280644046187c108098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (283014553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41f89ca728fa29d3151fd3c95dbbe2a91e465ae5f9ee3575d38683d30a66c5bf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:44:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:44:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:44:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:44:54 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:44:54 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:46:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 05:46:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:46:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:46:16 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:46:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64db56f7965b765f0e39653c084418dd2902ad80e13793882547069cfd06d5d`  
		Last Modified: Tue, 07 Apr 2026 05:45:37 GMT  
		Size: 147.1 MB (147105311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499feb5dcf3c356337de599b5abed8dbadde9a36d400dc0f956b13139ee614e3`  
		Last Modified: Tue, 07 Apr 2026 05:46:43 GMT  
		Size: 86.5 MB (86543101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edeb274f37dfc0e0808cadf73708b44f7189f161dac9a3989e58a1664819616`  
		Last Modified: Tue, 07 Apr 2026 05:46:41 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd09132bc6945afc655574d8636e0de3f1c6db72cd6823d79a19817019ec5df`  
		Last Modified: Tue, 07 Apr 2026 05:46:41 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a33c2cc7144316ab1169064dd2b100fb069060a2fb7069934883c75c9cab2c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7484194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44127ef728ccd7743e3bef9d1e0adb8e63d4b9f0875cfd98505792ca90a20876`

```dockerfile
```

-	Layers:
	-	`sha256:bf9ca8463a325381d8c09d6d45819ead7158bcffded266afa98b39f6c3315abe`  
		Last Modified: Tue, 07 Apr 2026 05:46:41 GMT  
		Size: 7.5 MB (7468441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bb1a6fe3ddb5368d98569b5f7d6cd04edcb3dd906a884b568e07344ca9aae9d`  
		Last Modified: Tue, 07 Apr 2026 05:46:41 GMT  
		Size: 15.8 KB (15753 bytes)  
		MIME: application/vnd.in-toto+json
