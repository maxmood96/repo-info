## `clojure:temurin-24-tools-deps-1.12.1.1550-trixie-slim`

```console
$ docker pull clojure@sha256:05330d0971eb7142ac9ec151db1f149259e36d68dc21826f8f8ad1fda457bb4d
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

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f19b62c606cf515548cad7e006404a5e461ce4c36be1fb28888635267badb3ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191526039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514fc135d564137cb07b0cf49fa833a0be9503ea8139464699ae07309a9cd13f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f7f88c6d7f710176d487a3ac59c7790f981832a06bfc197dbe4a74d73b1407b7`  
		Last Modified: Tue, 01 Jul 2025 01:14:56 GMT  
		Size: 29.8 MB (29761106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e264ceac2c88e848475a7ba102a67f9179f454db8cd7506423f58360698d7c1`  
		Last Modified: Tue, 01 Jul 2025 13:23:40 GMT  
		Size: 90.0 MB (89952004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90201b72beff1cc307283df794e53456677d5e31dca01c0a8f9015f776ca552`  
		Last Modified: Tue, 01 Jul 2025 13:28:37 GMT  
		Size: 71.8 MB (71811889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7b6db505b010850a029ba14fb185b60d89c02432678a5ef304a1132ccec871`  
		Last Modified: Tue, 01 Jul 2025 13:28:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dfe38491d62e78258c472f24204a1c9e2c8a46c92710f5e1f2b8978876d4119`  
		Last Modified: Tue, 01 Jul 2025 13:28:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:023f43447efea0c8c9936aa6718c169a39d8bf763e41b25acbd28bcf48ee02af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514b8151879fafd91d355da55a219a3b179c50cab57137e9f703e9042d17f436`

```dockerfile
```

-	Layers:
	-	`sha256:1bf47b92db74db0f7cbb81d7a083a445774f04c2376371fd8fda0d3aadba54ac`  
		Last Modified: Tue, 01 Jul 2025 06:41:48 GMT  
		Size: 5.2 MB (5203448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56485585650c277b86e4472052155cac50b4c4c9d5f17f91b01d8dc9d403b35f`  
		Last Modified: Tue, 01 Jul 2025 06:41:49 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dc32a5ddb6176e4f1628fc0a37e732216b79a939c927ff2b06fd70459bceb35a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.9 MB (190880649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f7aca93ef618f3f1423d8278b601d14e9a1d7e617d8c9e80d3bc1070ab3ed4a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c3306e90503bf56d5d575fca0323e4953fc66cffec788094159d11570a81151f`  
		Last Modified: Tue, 10 Jun 2025 22:53:04 GMT  
		Size: 30.1 MB (30121041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c8750a27004b373ccbbac455cc03e609a08cb23334c213f27833d57177f0b1`  
		Last Modified: Wed, 11 Jun 2025 08:46:33 GMT  
		Size: 89.1 MB (89091271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95773a5d791f45e56ddbe3d339778716df7043ebe37a7f362f089c8fa67ac34e`  
		Last Modified: Wed, 11 Jun 2025 08:50:33 GMT  
		Size: 71.7 MB (71667296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0fe9886938ab5bdde821ea824f9986c0936d337bbbb5fb1fb36f287aac79f2`  
		Last Modified: Wed, 11 Jun 2025 08:50:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad927961fe4b4b0400629b38b59bb301ce543da6dbb154b7d393deaf2d3b942`  
		Last Modified: Wed, 11 Jun 2025 08:50:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:565bb55b0e067eaedec07db58d292a6ca6247fb4082aed7a719527b53b0c1b8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5225176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701667aa75c57901c118c33a60e818796fe6afa830cc3174df3849c5c014914e`

```dockerfile
```

-	Layers:
	-	`sha256:f422e820354549a7363e4f2a0ba22c3a294be5b5d4aad2e1e6f19f6bb101b812`  
		Last Modified: Wed, 11 Jun 2025 09:42:19 GMT  
		Size: 5.2 MB (5209210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07a5060b37762fc8a783de71eca89fbf9d60a21fb68a2f5396313162a8aadc1a`  
		Last Modified: Wed, 11 Jun 2025 09:42:20 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:8a439e01d5c90e5ad04de16c536a1977e25850293774efa0e83b1d298c04f5c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.7 MB (200740408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94dcd63bb78bc3a168b6f6769430417dd2560e0a879ee8009e1d731d30bd4daa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2adebcab7d76ecb14ead3f70af8ca34e5abca513c2fcbd9f40e3af1e18442ccc`  
		Last Modified: Tue, 01 Jul 2025 01:19:23 GMT  
		Size: 33.6 MB (33586035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f033aadf173c9e16eb63bfd0af244c1b0e5ad9842fb8f6f31f94cff732b556`  
		Last Modified: Tue, 01 Jul 2025 09:15:10 GMT  
		Size: 89.9 MB (89920248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99ea2ad41d4f1f069be0ab574f8eef41647d93a8fe1c7555cd49b9e81c3fb88`  
		Last Modified: Tue, 01 Jul 2025 09:22:10 GMT  
		Size: 77.2 MB (77233085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37732d867082ed7863c81613cc25da887249c5fdbc382e3a8b2d270cfe070d03`  
		Last Modified: Tue, 01 Jul 2025 09:22:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6796ae5aa5b80e3a55799481ac6c5ea27e7f4085cfe1e850e1dc01b2224aa9`  
		Last Modified: Tue, 01 Jul 2025 09:22:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:432136fc3081f8d793b7925f9dec8eb322cd0ed73f4123eafff8463599787240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5225011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6c1075631c4050d6e9122363ce4b85bf13d6e9b606fbd3dda944804665bd6d`

```dockerfile
```

-	Layers:
	-	`sha256:49f21ce0b61f69d875638a6005c0e69927d5f33e809862be52740400d49460fe`  
		Last Modified: Tue, 01 Jul 2025 12:38:24 GMT  
		Size: 5.2 MB (5209117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e40b03cb315931c8c418a535497a7b6979c53eacb52e8a591396ebd161966691`  
		Last Modified: Tue, 01 Jul 2025 12:38:25 GMT  
		Size: 15.9 KB (15894 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:68d1cedee8717ae2369f003c67fce5a8e8031876b40bff358694bfd5a1212b9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186585242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882d6575bbc8e591bc3b359209f85bafc30142ff1b513d9cc8211d883ce8ca4a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:43faa9a2f25436afce0db8221e3c0e223102f73a33b0cd47eb32294e8033b203`  
		Last Modified: Tue, 01 Jul 2025 01:24:44 GMT  
		Size: 28.3 MB (28258970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e419a52d0b7166273c72df76079f5355fbec04834338cef62e248098795964`  
		Last Modified: Tue, 01 Jul 2025 03:38:20 GMT  
		Size: 87.6 MB (87622190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221ce50f66674be00315dd597a9ba0619b4d03cc4a9e3b0a29b79d72f94fc660`  
		Last Modified: Tue, 01 Jul 2025 13:33:49 GMT  
		Size: 70.7 MB (70703041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbaeb3fe04ed18d59eb78420e9ac30b77b5e4045bcb6837b9664c738c8997f1e`  
		Last Modified: Tue, 01 Jul 2025 03:52:03 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dabc777a78a5a068e556d5d6adb7afcaa304ca650e91659d34b22f4dd36a7b5`  
		Last Modified: Tue, 01 Jul 2025 03:52:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3f0af6e7a201d388eefdf83500ad5d3850a9d9fe7113728c0050be9dbdd22014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5208805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bc083325bcac415bff63eee23ddf0f1ffa89cc4854ef19586c0dd1636f1bf5`

```dockerfile
```

-	Layers:
	-	`sha256:e4f4b3bf72d16c1eb57abb897a9b52e8229a1655e9381d879057752c3ff3d779`  
		Last Modified: Tue, 01 Jul 2025 06:42:09 GMT  
		Size: 5.2 MB (5192909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76a6928eca70166d6d94dfe71dec681e774b5fda5982307410b9772c09dad1b`  
		Last Modified: Tue, 01 Jul 2025 06:42:10 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:5f83466749f1161044fa12d72b8b1eb80b3b831d855a8aed2eece8d6ab56bed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187858474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56d9fad214b27cb173a8523d7c402cb81ad44f22d55e9d24d6a56f02ba483cb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:728fbd29b8599bd56dcb8703b5c428523bcf0f3d48c5e95804f60267a128a3bc`  
		Last Modified: Tue, 01 Jul 2025 01:19:25 GMT  
		Size: 29.8 MB (29838345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a290bfdcf58eb6f2d2c7d07ad715d97e1157ee6787b7f5904dd6e676ef690441`  
		Last Modified: Tue, 01 Jul 2025 08:28:02 GMT  
		Size: 85.2 MB (85216780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682ae7b4371c3d0fe9322d909d17fda576b8b32435f1af02bdc9e53ad3fe3fd8`  
		Last Modified: Tue, 01 Jul 2025 08:32:03 GMT  
		Size: 72.8 MB (72802313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ec984867bc132201090704e1fb4dc4e7dfb98a3bbf2f16188d2b798feb3a44`  
		Last Modified: Tue, 01 Jul 2025 08:31:55 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd66573d0800754510e913e73009deb975c81231bd13a22bd76021cb066f98f1`  
		Last Modified: Tue, 01 Jul 2025 08:31:55 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bfce8b6ba13db40e9d6e1b206cb760b4a8b7d181659c0dddb94ab73843a4f5bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10628516d00f3a229ecfb9e3eee07111401cefa1049852ea2c5ca0faf62113dc`

```dockerfile
```

-	Layers:
	-	`sha256:e37f3bf063d957ebf951e1da65327e3ee007eb58504f653389bec669ebe2eee6`  
		Last Modified: Tue, 01 Jul 2025 09:41:45 GMT  
		Size: 5.2 MB (5201920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39eb6a8566e0de00b8736591a64f37d527604cd6ddd5a07967a7edc0dab12997`  
		Last Modified: Tue, 01 Jul 2025 09:41:46 GMT  
		Size: 15.8 KB (15847 bytes)  
		MIME: application/vnd.in-toto+json
