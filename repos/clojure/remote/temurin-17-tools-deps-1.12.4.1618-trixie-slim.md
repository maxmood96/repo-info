## `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim`

```console
$ docker pull clojure@sha256:37d7c5c291bdb071842559951cec5820b0713e63099447a88179e7fd1b8b6c49
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

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f99ec8dea70d36243133debdf0811df4674970136a8de6984c0b1316016eec09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247421013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f362002255d6634afd9b421896e3e9a000c984ada9b89dfb600a9c08616f3555`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:18:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:18:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:18:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:18:52 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:18:52 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:19:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:19:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:19:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:19:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:19:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71ff1afcbafc953e75a5e4564936c1e0f61a3fae4f3bba2db4a79d483d9184d`  
		Last Modified: Wed, 22 Apr 2026 02:19:30 GMT  
		Size: 145.6 MB (145628775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0a6ec1a70c7816d699cf6089674b421f36bc8f03dfd9971184e829cc47d36b`  
		Last Modified: Wed, 22 Apr 2026 02:19:28 GMT  
		Size: 72.0 MB (72011029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc35c694370f9469e256a54d24e1c5fc91c5198e6daa59100c4b08b15c5bbfd`  
		Last Modified: Wed, 22 Apr 2026 02:19:23 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913c2b11c3e31e6f2ddc149d36ec39d617c7991da482257612a607caee4b7899`  
		Last Modified: Wed, 22 Apr 2026 02:19:23 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f5efca7b1c8626aa2486bb11470748f11dbdc4992da3c5616033182db69dd57a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81993397e5c342d79b88d18ecc015b777309024fde58b56820c25a1329b5aa70`

```dockerfile
```

-	Layers:
	-	`sha256:9a38a4c9e446356eca65716cf2eababdc2ebac9165c072921f00048e086a0d73`  
		Last Modified: Wed, 22 Apr 2026 02:19:23 GMT  
		Size: 5.3 MB (5259192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27ad6707b27451be2e14f6de0d2c0b253248c701c7462239bc31b62380d7d0b5`  
		Last Modified: Wed, 22 Apr 2026 02:19:23 GMT  
		Size: 15.8 KB (15811 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2051d6cb85acf35e69cd1acb438a48b701e44de9ea4120e81bc61fb9657182cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246411822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de45cfd09cf4dbf3aa671973985c4eb45b131799d61edc213f74e114761619a6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:22:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:22:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:22:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:22:02 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:22:02 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:22:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:22:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:22:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:22:20 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:22:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4465b23c6e58d5a1a05042311f4685ead7d9047e0131e81387bf48019dd8045b`  
		Last Modified: Wed, 22 Apr 2026 02:22:42 GMT  
		Size: 144.4 MB (144436188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a472be38af607ae6be4edb01a1c70f52a53b3319458d77a3a89ea9c5c3bf7a`  
		Last Modified: Wed, 22 Apr 2026 02:22:40 GMT  
		Size: 71.8 MB (71830991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ffb346ea9c4a2fb56f7bc49cee9a53d7b29316404d3e0b173c8d8d14f58bd6`  
		Last Modified: Wed, 22 Apr 2026 02:22:37 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f717d86f6e89cad1393481616e3cffb1593a9e6d54c1b928ead75cb124993e4`  
		Last Modified: Wed, 22 Apr 2026 02:22:37 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cc4a273a1f38a83e1ff870c67096e7d35357be63d7d6078c4ed902bf03d689db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67e0eeb4cbe39650f1a45f8f9e67999fb920efc0364f19b28c1f521d88bb3e5`

```dockerfile
```

-	Layers:
	-	`sha256:420e9d7d693ac18bc52ddce585f67358d8573f98eaee92335d761399f4d6acfd`  
		Last Modified: Wed, 22 Apr 2026 02:22:38 GMT  
		Size: 5.3 MB (5264961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3058b0a5f9a21c5eb0d67efe11d6d4cc17857844f9bf7e0bc05aee694cba5dc4`  
		Last Modified: Wed, 22 Apr 2026 02:22:37 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:1571e170315d57d3980b45372983ae2ebda860c2a83539d19e9b07e47c7f577a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.5 MB (256466275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b40c8b7b215e1bc42e1d9e28563a0fe83a468750923390ce7270318d116c4b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:30:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:30:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:30:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:30:50 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 08:30:51 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:35:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 08:35:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 08:35:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 08:35:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 08:35:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8050bc2d6ceb1ba93f1bc7881f5152d6617c5ae147bbcf177968cb01c684519`  
		Last Modified: Wed, 22 Apr 2026 08:32:22 GMT  
		Size: 145.4 MB (145438281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3a8031277899b3ffe5bd06bb13e571901d7dad046086ad4d80ab2e4c5491d2`  
		Last Modified: Wed, 22 Apr 2026 08:36:35 GMT  
		Size: 77.4 MB (77428925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb31f78e1cb953cc38d2d2b16e30ee1fac7e82fb15bec9f8652f530bbd2e171f`  
		Last Modified: Wed, 22 Apr 2026 08:36:33 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a057ab225692a259e3d0eca05eff8e9dc73691a711c693417ed24ba7fd0a709`  
		Last Modified: Wed, 22 Apr 2026 08:36:33 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aeb0a71a88718d1b11532bf5ac66cad94ffa76f83429f1d015ce552769e04af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e0a7db7e8a85f132a7285231dddf6a17ea6d4a41983294583176d23239c89d5`

```dockerfile
```

-	Layers:
	-	`sha256:c380f34e91a54af6cd9a4b5eeaa9ae59de2468ee4078c26a272b8dc554147723`  
		Last Modified: Wed, 22 Apr 2026 08:36:34 GMT  
		Size: 5.3 MB (5263563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bffa8bdf182b0516c7c24530e4b09a9467724677b02d3a264718a147d6b5e34`  
		Last Modified: Wed, 22 Apr 2026 08:36:33 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:fda268f2fcf1f52d6b4da382777d6bde19b7a53eab96e64eddad3a72ce2c7f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241844799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca98f4052e745619c647932ade947765d291464cef7425175f75b0a30ed7782`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 17:48:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Apr 2026 17:48:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 24 Apr 2026 17:48:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2026 17:48:07 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 24 Apr 2026 17:48:08 GMT
WORKDIR /tmp
# Fri, 24 Apr 2026 18:05:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 24 Apr 2026 18:05:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 24 Apr 2026 18:05:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 24 Apr 2026 18:05:15 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 24 Apr 2026 18:05:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839a829e8fec6662efa3cab7ad2470690879a00890c2cd0f31b7ec868d89805f`  
		Last Modified: Fri, 24 Apr 2026 17:53:53 GMT  
		Size: 142.7 MB (142662943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914e5777c69f98dbff6809d04c36a53b6f6ce0985215d06f9ff3afa6034b9063`  
		Last Modified: Fri, 24 Apr 2026 18:08:54 GMT  
		Size: 70.9 MB (70900618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6102cb1b86fa4e2d79aa3d441bbb465ec05520a3c193df1725a9205d66ca0a`  
		Last Modified: Fri, 24 Apr 2026 18:08:44 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4a64cf61225ece717217cc9ac4ee192e5daf83b11cd4c2515f3088534274a0`  
		Last Modified: Fri, 24 Apr 2026 18:08:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3f3a37f8172863b6916c44cefb6f5da891135bb527da542feaf808c78d4538c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5262597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72d9b61a8e858e0439c3f1d70221f7852c5d1d0539912ea8b827ee52b192951`

```dockerfile
```

-	Layers:
	-	`sha256:1717073c0fd98c52768d838d5ad5298a84c54c15ff5942df263b1887fb7ea2d3`  
		Last Modified: Fri, 24 Apr 2026 18:08:44 GMT  
		Size: 5.2 MB (5246737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dde60a45455ecb9c13cecc3a49e924765b2c19b0c1118da5205b80f1f52d28a9`  
		Last Modified: Fri, 24 Apr 2026 18:08:43 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:52b5e17a373a04d89d7beee3805b9c9fb6aead449086bc5a769a7c2e5548df53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.5 MB (238455422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55cb4472130ba3d5f63dcfdc4585e5a8dbc3e073f9577c688f6df2f3b65c3bdd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 04:01:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:01:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:01:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:01:03 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 04:01:03 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:02:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 04:02:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 04:02:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:02:25 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:02:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150332b9769a3e50f47d036c734faa3f383f8ddacfb44d5dcc29fa64b02ecdae`  
		Last Modified: Wed, 22 Apr 2026 04:01:47 GMT  
		Size: 135.6 MB (135627000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed07a87de185171280320c8bb7216ba61fd3e71db135ce5537da4a19f2bbea67`  
		Last Modified: Wed, 22 Apr 2026 04:02:51 GMT  
		Size: 73.0 MB (72987082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873213f0ba4721a51f43092b62ecb6315412a423d5ec7151cc2a1d9320057d9f`  
		Last Modified: Wed, 22 Apr 2026 04:02:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8967983ac424ebaa33dfb9ae561201e64c011368a583177a19fab59b3e3c5e1a`  
		Last Modified: Wed, 22 Apr 2026 04:02:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0db0673300dd5f4eca88f1a355610596a691391d214a357f7f894d2d93a54486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ada69889849da62564b6d52e611d161cb0dbc64b492a4d94a39756291526c1`

```dockerfile
```

-	Layers:
	-	`sha256:4f86e969552116e6bf82f6e1846a21a4c5d611a715bc0851182151c013df02be`  
		Last Modified: Wed, 22 Apr 2026 04:02:50 GMT  
		Size: 5.3 MB (5255116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69e742f00a8496439e92785f33745bf8f4a1e2a072f0f0ca211338c981d07711`  
		Last Modified: Wed, 22 Apr 2026 04:02:50 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
