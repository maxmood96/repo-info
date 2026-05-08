## `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm-slim`

```console
$ docker pull clojure@sha256:dd510781673b77125cc72de6e89c1a1baf11769642b28a7d31ccaf03cd5479df
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

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:37ecee0710b9f3a5765df0b39e38a88465afc347b6310092c008b3daed91b4c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256103005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89886e2fe18b2a02a5ae842364757c9929aff61a1f295e5df3b3efe2849d470`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:27:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:27:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:27:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:27:09 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:27:09 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:27:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:27:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:27:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:27:21 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:27:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a26795cbca3210a0aad7c67b560345c46c3ddbca0db0821d613a22dd856587`  
		Last Modified: Fri, 08 May 2026 00:27:43 GMT  
		Size: 158.2 MB (158166935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1db0cb99b27d64196a031d44ccfbed5e7643d6d2f29a520144415e5017221f`  
		Last Modified: Fri, 08 May 2026 00:27:41 GMT  
		Size: 69.7 MB (69698777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f562769c4f449c9ef8c6ead433376bdfc31530ac60c380477d0f14feba45e5`  
		Last Modified: Fri, 08 May 2026 00:27:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a5d152888aff23cc1eb9bb88f457dca8d8be583faaca378fc906eed5b7b672`  
		Last Modified: Fri, 08 May 2026 00:27:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4426ae1ba33aa30706a0718421b347343773592af7542e77fa03b9ad98c1337a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfecd501a0bc53aa5b597c2e9b777c38cf7f4ccc31188d99e9bac4723a95c98a`

```dockerfile
```

-	Layers:
	-	`sha256:847b839eee8690fccf76b38a0405df9ad90eb204ea76cb0e70d73ca000c09950`  
		Last Modified: Fri, 08 May 2026 00:27:38 GMT  
		Size: 5.1 MB (5118646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0af8ebcdb70fdc8fdec59a975e877e497452a2f697ffd279de3e4ba2d29d9402`  
		Last Modified: Fri, 08 May 2026 00:27:38 GMT  
		Size: 16.0 KB (15989 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6d0ba62c4b18a1943e03ca8db761930defef6b36a8136af32ae129cd4f408a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254270940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90438ca799d2f90025421b36a7952071ba25566be2928de1ab60034c099daedb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:26:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:26:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:26:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:26:47 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:26:47 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:27:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:27:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:27:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:27:02 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:27:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6badff8b9b46adac2cc2e8d4a5e4989572eb70344ecf613b0fc73e33ea382d`  
		Last Modified: Fri, 08 May 2026 00:27:32 GMT  
		Size: 156.5 MB (156461225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d7099a19ae42911dfb0ebd622ed48d25029a661253ca4164acb1fe31381014`  
		Last Modified: Fri, 08 May 2026 00:27:26 GMT  
		Size: 69.7 MB (69692560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f29210673221f725721dfce462ace436925b2288524656ccc8a636346a811ac`  
		Last Modified: Fri, 08 May 2026 00:27:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36d74e810f03a6993c3503f85112bfbe0cb3f960c269b7310d9e6de474b5cd1`  
		Last Modified: Fri, 08 May 2026 00:27:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8cefc62e391b490fef42594431e6ffaa47d8f93290f72a4d307d2c4ed4bb0619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5140515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2682375245d26cefdc02d365dd9c8539dfd0bb4cd8f194ee3615c5a37791810a`

```dockerfile
```

-	Layers:
	-	`sha256:f0de446f90b935afd17700c6ac3b654daf6c19bf81fb0fc29cbc259b44fd3d44`  
		Last Modified: Fri, 08 May 2026 00:27:23 GMT  
		Size: 5.1 MB (5124407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60545e3928ce164588850f094ec307e0691cf4eb2b9b78d8d5818dcd8cfee59e`  
		Last Modified: Fri, 08 May 2026 00:27:22 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f35f50f26a116a2a08d1b5b394687db4a54e61fa97cf56f77f6278e8015f777d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.0 MB (265952469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66e7f788baca6c0c1a38cde40604310827df150f2c0a83fc81ed6b132d690deb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 01:36:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:36:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:36:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:36:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 01:36:40 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:40:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 01:40:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 01:40:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:40:46 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:40:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0bcb46f6315f7a2c8ddde875fca21de96c94e451046e6692f77a99aca489f3be`  
		Last Modified: Wed, 22 Apr 2026 00:15:02 GMT  
		Size: 32.1 MB (32078402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030929f85e28291d6f68f9b323b1a7234dec490966f0e6af5276563600fd14f1`  
		Last Modified: Fri, 08 May 2026 01:37:52 GMT  
		Size: 158.3 MB (158343282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd4c649dbfd5874fb49573edf84abf3545338d12691d37a569cad388740ae02`  
		Last Modified: Fri, 08 May 2026 01:41:20 GMT  
		Size: 75.5 MB (75529746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eea4d0f9c8ccf81385714840b40457056a9c7fb0e533520ba5348cb37d8dfd5`  
		Last Modified: Fri, 08 May 2026 01:41:18 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d4e0c8e3e411f236b2aa567d8d1621464a527a75688f57d97c0f1134521982`  
		Last Modified: Fri, 08 May 2026 01:41:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cab38418b9b2283d77f389b620b8be7bfd863dd611911ad3c724be8010ae950c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b326d5410337da71971c58adbc2971c0d0508df4471664ab6261497095698c0`

```dockerfile
```

-	Layers:
	-	`sha256:86d43a25ecd68073b12ee2799624dcdf89167e0afbd9671267c61ee304cbd380`  
		Last Modified: Fri, 08 May 2026 01:41:18 GMT  
		Size: 5.1 MB (5123804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1d8b43923e135e94982b50bd02c6e3ab9457ff04af59c4ac149739b6da9ec1b`  
		Last Modified: Fri, 08 May 2026 01:41:18 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:cd0bededc6c5a7e98e3dccb70de2e2d9d9990477e384a302e33ccf4499c3294e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242793695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f3b8d0518bde273261e8e9046f6f013c8422a891627f31674c3fc6bfffd5f2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:38:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:38:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:38:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:38:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:38:16 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:38:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:38:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:38:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:38:30 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:38:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0646e5b0bf16518381b73f55d914a66db6bc8944180ee94f3163776b9de2ffc2`  
		Last Modified: Fri, 08 May 2026 00:39:04 GMT  
		Size: 147.4 MB (147388333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f90844e68ece6295df0df9e48a9643491b226ce275c525970263b07624a2dc6`  
		Last Modified: Fri, 08 May 2026 00:39:02 GMT  
		Size: 68.5 MB (68512757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc96984fd62c0ffd5dd4eae1b9e3ca67c45e92bddc614a641c53bf65e7a8c72`  
		Last Modified: Fri, 08 May 2026 00:39:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9c0813f4273720f56788696ed1142a809619214d1564c3e6715e88dae59391`  
		Last Modified: Fri, 08 May 2026 00:39:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7c739466188f8508a8e468899f44506d3b4c39d8b66af16548d60603aced2e07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bb1f75a6974232efae9c369348f5604ed5b0e1aaa763820e01208f54008ea4`

```dockerfile
```

-	Layers:
	-	`sha256:14cd4b4f97156ae93bd559c63752db06b019bde16aae132781889f9acdc913f3`  
		Last Modified: Fri, 08 May 2026 00:39:00 GMT  
		Size: 5.1 MB (5109967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab522758a7c4748306221edd55b9f638dbd77ba8b6e547a39fa2caaf47cd37cf`  
		Last Modified: Fri, 08 May 2026 00:39:00 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json
