## `clojure:temurin-26-tools-deps-1.12.4.1618-trixie`

```console
$ docker pull clojure@sha256:8905abb18eeefd593cd6f62f1f2b6f6293543d8f2e006173b3b8d2150e5b2902
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

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:d0496b6603665016ac4ab4360fb9fab33ac116a9f30ac3757369c798bd50e9bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.3 MB (229330045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6541b2600e0bd71b94d9d41df4b0d606e6c25eaf18884f29cfcd5817ef3f42d5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:20:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:20:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:20:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:20:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:20:44 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:21:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:21:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:21:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:21:01 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:21:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7f4310083c0e7fd8146fe30b81bd233a1897232746d35d200a873f6f185019`  
		Last Modified: Fri, 08 May 2026 20:21:20 GMT  
		Size: 94.5 MB (94455692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113973e6e2d76d16a7f07bf40417d246eb96080745f3907fb4125d57fb46930b`  
		Last Modified: Fri, 08 May 2026 20:21:26 GMT  
		Size: 85.6 MB (85570996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325fc435e87af856f3d88fdc0b4c344da5b15d12ac13eeaade4fb6f93e541805`  
		Last Modified: Fri, 08 May 2026 20:21:24 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d359f865658a4effffc24480b9d3aa202a3cb747f06189e1aa417ecbe1d0569f`  
		Last Modified: Fri, 08 May 2026 20:21:24 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4d1c30bd59bb8959e5dd64cfeb21a328365ba653a9ca1c3329097f54ddc58955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7451972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:509a2d473923d60d4dd6784a9b02a0bba7b7304e21d346bf93b78692d8aaf8d0`

```dockerfile
```

-	Layers:
	-	`sha256:fb185df010fe16def5a3feadf28a8d687930191bd26de84ab8a8abce81b3c8cb`  
		Last Modified: Fri, 08 May 2026 20:21:24 GMT  
		Size: 7.4 MB (7436225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b18deba44db2c5a65ec4730080580bcc88407dc678b85f6c4e03fd32408dcec`  
		Last Modified: Fri, 08 May 2026 20:21:23 GMT  
		Size: 15.7 KB (15747 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a0015699f5d6887c7cea696b5fbeb77f2dc1fad02fe522aa422a6787a8cc8349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228449176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73be87674a1327f33f304d364f98bcafe5d637da55f6d07f5571aab8602b54ea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:25:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:25:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:25:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:25:10 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:25:11 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:25:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:25:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:25:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:25:28 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:25:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31131f3dfbd3941589dfa47f6054d400d6e0a0837286c97057e82f3d99795b8`  
		Last Modified: Fri, 08 May 2026 20:25:55 GMT  
		Size: 93.4 MB (93395206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3588b8579b1413f4c64c988826188cdbc6fe6d32c7bd0508c27f75a0c15ea10d`  
		Last Modified: Fri, 08 May 2026 20:25:54 GMT  
		Size: 85.4 MB (85383486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18be96bc62de706652b91aeb60a2cf3320f7ad78cf3ee98aa0b9f8b6ee68b718`  
		Last Modified: Fri, 08 May 2026 20:25:48 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7f906673b199f2bf3e9f42caaf12b57988977bec62a71a026a9368f73f9cdb`  
		Last Modified: Fri, 08 May 2026 20:25:48 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:85fba6c514fd149e583d0aededa346b4f4ba54c0d113252b6c4e3835d00c18fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7459117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8d9daefd175a44d0a20380a38ccd91cf2fb8447ebdec08131193bad80a0de0`

```dockerfile
```

-	Layers:
	-	`sha256:dac6538900655bddbe60c24cca90caa855548b292a7d6d3d07c7040b36af9b70`  
		Last Modified: Fri, 08 May 2026 20:25:49 GMT  
		Size: 7.4 MB (7443252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:452fcf0be5a44dcb695c6e1797a1d579812ab9203b5e7988ece34d696572be39`  
		Last Modified: Fri, 08 May 2026 20:25:48 GMT  
		Size: 15.9 KB (15865 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:aeec1b540ebb9374237991207ce650a4beb50d353a954f63853442f3d30f081c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.9 MB (237891836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2808d0812608add2df995a4b1835673293083b1224439a352695c673c489dd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 08:52:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:52:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:52:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:52:10 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 08:52:10 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:56:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 08:56:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 08:56:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 08:56:13 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 08:56:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3799eaf173a8c1b19c1d7144d609dd7a216352b74dacce1a0b09fe51aa79082a`  
		Last Modified: Wed, 22 Apr 2026 08:53:25 GMT  
		Size: 93.8 MB (93781494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d999fd3749111bc21aa8fbd5bc1b4dff49713ffa2f9f59909035f36f21e19c53`  
		Last Modified: Wed, 22 Apr 2026 08:57:00 GMT  
		Size: 91.0 MB (90986318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73767bdf0179879af74de7dc9613e3da6adcf3d603c919e21c32819b6c7bc9e8`  
		Last Modified: Wed, 22 Apr 2026 08:56:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e169badb8c32882b895a0570b296593aeb2f1138fe4bcb65f8e0145bfa70f9e`  
		Last Modified: Wed, 22 Apr 2026 08:56:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:cb569667088bf22fcb7418698756780fc444fd7be9ed8ea1adf52fc3e49db80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fb387885f656aae79c5010b3c883d2debd0dc68d42fb0fdee7dfe56a38370f`

```dockerfile
```

-	Layers:
	-	`sha256:25b91c16a6418b418220a6da51f5d2c473b1277a08c07b2c306782789ff082bc`  
		Last Modified: Wed, 22 Apr 2026 08:56:58 GMT  
		Size: 7.4 MB (7424582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4b1c7da083e76d4c1d15a60bbf8343a1898a6d606de61341d0aa502d8747568`  
		Last Modified: Wed, 22 Apr 2026 08:56:58 GMT  
		Size: 15.8 KB (15795 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:eff0f2bed3f18cad9adad7842429e68f846f25982e559ede6a2b691acbffcee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.3 MB (225267623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247e07597de82150d9cf586f2857808dd060635f311d594dcba29652348b8063`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 19:04:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Apr 2026 19:04:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 24 Apr 2026 19:04:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2026 19:04:05 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 24 Apr 2026 19:04:05 GMT
WORKDIR /tmp
# Fri, 24 Apr 2026 19:19:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 24 Apr 2026 19:19:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 24 Apr 2026 19:19:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 24 Apr 2026 19:19:08 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 24 Apr 2026 19:19:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e518626ae0de2d990c7c66185d308a25cb3affebb6204543438f56fd9f94992`  
		Last Modified: Wed, 22 Apr 2026 02:29:17 GMT  
		Size: 47.8 MB (47798217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d33f3b0d1516a154dea10fb422a41e3746a0c108f2eea69181e9875275fdbe7`  
		Last Modified: Fri, 24 Apr 2026 19:09:49 GMT  
		Size: 93.0 MB (93008124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282bc587e60bb82cdcf5a70f81cde962e290ccdc15646382e51f1bdb46d14bc0`  
		Last Modified: Fri, 24 Apr 2026 19:23:29 GMT  
		Size: 84.5 MB (84460238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4be8ea6f16a834f280fa5bb121b7a48c784197eb51a11d35750d6396dc627f`  
		Last Modified: Fri, 24 Apr 2026 19:23:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac212a08cb269ab0ee3e5ef701ed7da02a1de44644380511f3bf1a95524721d`  
		Last Modified: Fri, 24 Apr 2026 19:23:15 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6b36988ffc136e6a8bf343ffc925803a19c428ef674e6ccaa6faa91fb7fd6337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7422570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c35e9af4d5e58c61fa388b8152edd669efb9d798848d856d5b66e2bb230151`

```dockerfile
```

-	Layers:
	-	`sha256:80bd4fb4053cacd36352094536b91cfcf49f77ee08806f2a2bddd6e8a2083493`  
		Last Modified: Fri, 24 Apr 2026 19:23:18 GMT  
		Size: 7.4 MB (7406775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96aa3bbe74a62855db6e480d2d5a4e3a3ed212651d91b5b772f7e3b51ef2385f`  
		Last Modified: Fri, 24 Apr 2026 19:23:15 GMT  
		Size: 15.8 KB (15795 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:047a2829370e23164ac2d74e2c518903d8f4dc87c68b1d00a1c7851674538617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226466462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949d120b4fc5a6beacad016c2fd013d4a4e37ea2d65257b52747bac186e2d121`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:21:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:21:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:21:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:21:25 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 22:21:25 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:22:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 22:22:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 22:22:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:22:40 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:22:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ea63852b62fa38d78ab507e59ec519d91cb7d1e9a5a2d2372b05f64d7765244`  
		Last Modified: Fri, 08 May 2026 22:22:06 GMT  
		Size: 90.5 MB (90547732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29115b9d465169743fb26c34f2703f3cc2abc14113553aa142a9842774e96a78`  
		Last Modified: Fri, 08 May 2026 22:23:07 GMT  
		Size: 86.5 MB (86545389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92de4afb669dd353b971eec2751079b9922d002695c2cb4ac5063b88ed33461e`  
		Last Modified: Fri, 08 May 2026 22:23:05 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7b456f036b909a386dbeb978f84f0e5a5040fdfde0a1b088e8f18ef144c6ae`  
		Last Modified: Fri, 08 May 2026 22:23:05 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:133db1d5cf53849aa1180d49ddb43267b04ed0caf7524843c8b493a3204cabca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff2d2d3828ad872b4bbca8a29cb92701f6b9d63c307a4f0e75d7f9152d63ce4d`

```dockerfile
```

-	Layers:
	-	`sha256:65766c7a4104d477f3198ed3cccfdf2869197297e56de4750ca2987158334fed`  
		Last Modified: Fri, 08 May 2026 22:23:06 GMT  
		Size: 7.4 MB (7417333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21451cd3c94e47bcebdb88da3201a35c63b104f49c01aef88135dcd6cdfd3afb`  
		Last Modified: Fri, 08 May 2026 22:23:05 GMT  
		Size: 15.7 KB (15747 bytes)  
		MIME: application/vnd.in-toto+json
