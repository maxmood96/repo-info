## `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim`

```console
$ docker pull clojure@sha256:f91b03f9cd157c02456eb6010822f5d95852c712dd9584d6d60d8f70fa0e8457
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
$ docker pull clojure@sha256:14aaa942b27d6cf6633910eadaa9009268d161378844e2730d0977b5743809f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 MB (250382998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8608eb3d2f18ab178cba34b5812abffcc69e68448b3ffb4194e589994c3dc6c4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:04:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:04:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:04:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:04:22 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:04:22 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:04:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:04:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:04:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:04:39 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:04:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b8ef79b2db274d32acefb5eec08dc02e862b48a65b007b80d97059ccfb7400`  
		Last Modified: Wed, 15 Apr 2026 22:05:05 GMT  
		Size: 145.6 MB (145628761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5775e7d658d33b8e0610021d10fb02f3c7dfa3a15bda8ba3099a47c33cb2426d`  
		Last Modified: Wed, 15 Apr 2026 22:05:02 GMT  
		Size: 75.0 MB (74977555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c0244e3012ca36a9bfd7ec165766ccf017a0c9af8815f7e4151ad03fa22513`  
		Last Modified: Wed, 15 Apr 2026 22:04:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550cd1b7ebc44529f1c25ecfaeafe183d312f80e60b154322f8ceb28dae002a6`  
		Last Modified: Wed, 15 Apr 2026 22:04:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4a5048217ec398c6fb36436b463191f8f56b66d69e63382b7ac8675c7d290b57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5274950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56fb794bc9c02f58e6c3ab1012d896fa5abcfe89baa21bf30e1309e279f380c`

```dockerfile
```

-	Layers:
	-	`sha256:331b430655b7b620bb96bc0cbb09f9dd003dd3fde06266a6e53735dd7336d759`  
		Last Modified: Wed, 15 Apr 2026 22:04:59 GMT  
		Size: 5.3 MB (5259138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddc137e561bd2edbf79cb75b0d52116ad6a00f4f47a917dec608448d6e625f3c`  
		Last Modified: Wed, 15 Apr 2026 22:04:58 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:632a7fd8554d4857f05f6efa7d5186f74f0ff97cce752824e8585b3360a88c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.7 MB (249725592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08c545e5ca2a056567bae74cb54181951f1313ccab3fb725bcdd1d373c46b3c4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:15:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:15:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:15:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:15:49 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:15:49 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:16:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:16:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:16:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:16:08 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:16:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ad2110f40a93337754cdbe62693384a18ed384a342e7b4764617e29f8e7a36`  
		Last Modified: Wed, 15 Apr 2026 22:16:31 GMT  
		Size: 144.4 MB (144436242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957ddb2d8ae5b614eec4bc17e77b490bc9168fe4faf13ca7af99182a200f34b0`  
		Last Modified: Wed, 15 Apr 2026 22:16:30 GMT  
		Size: 75.1 MB (75149760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a34763c3d41f96092310bb5d0c33994581178c4e750581ed152daf5fb8a2afe`  
		Last Modified: Wed, 15 Apr 2026 22:16:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe02d5ed20cbebc58d4fc67705949fb508a99ff1132ed45e09540c4bfb7bbc6`  
		Last Modified: Wed, 15 Apr 2026 22:16:27 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:55c9ac9dbe8f15d80a766d339b0edeb12cd4d1f4e44fe25b0bb4d7670142a0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f473b15a2c7a2a8af47beb667d0790063330bee02ead570846ac0a01a404a127`

```dockerfile
```

-	Layers:
	-	`sha256:214547bfb702bab96622931a466ad5232731f224954123f742797a91d128c0c5`  
		Last Modified: Wed, 15 Apr 2026 22:16:28 GMT  
		Size: 5.3 MB (5264907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f27863467420d133b0af2a7d05ae326ffc4e64057bb246fce671ebafdb19d18d`  
		Last Modified: Wed, 15 Apr 2026 22:16:27 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f9b293f014000708d0a8e7c84c3946c223026339f639e24754b9ec370f79a133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259643381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1111f1d7a9b1f3fe748a3f843d0f9443c3786a5c0cab04abeeffe4d7b0414b7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 02:51:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:51:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:51:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:51:45 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 02:51:46 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:57:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 02:57:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 02:57:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 02:57:23 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 02:57:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d63fa71f8a08634b0312e1df11dd8fc3363471d8c3e45af52999c7c3ba56e4`  
		Last Modified: Thu, 16 Apr 2026 02:53:12 GMT  
		Size: 145.4 MB (145438287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adee785cb4b2f981419a2dc622c9210cf5d41863a25b7f000daf150541ee234e`  
		Last Modified: Thu, 16 Apr 2026 02:58:10 GMT  
		Size: 80.6 MB (80611032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8766f31590bd4c37b119e329c2b4ccd9e3e9ee28d44129e81ecb1e27a93620dc`  
		Last Modified: Thu, 16 Apr 2026 02:58:07 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd6d6404d14177e8aa7f0522f485449cdc21d9bedff44ac99d5197ddbf9aa2a`  
		Last Modified: Thu, 16 Apr 2026 02:58:07 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:47c6df4b9a68cf4b75748dba7fc51f83d6b91322c0dd6ba96cce25610ff2168d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139ba3975072071fc5548e5d3f50176c13866cfcb9c9b4062f9832cf3701a197`

```dockerfile
```

-	Layers:
	-	`sha256:3b68a706401f501cc21fa4953582689cdc77df726389bd79cc5adb4c72a0d328`  
		Last Modified: Thu, 16 Apr 2026 02:58:07 GMT  
		Size: 5.3 MB (5263509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dd455d244808a5cd9943caf786693e3474765118f81a27cab4e985fff4ef6d4`  
		Last Modified: Thu, 16 Apr 2026 02:58:07 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:5464fa813dbb5c6d536dbf01b8ff31a8fc3cabedddd210b2fb9d3dc61ecae46f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244458673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84288cb688c0423977622f4b653081afd8abe56c5ba09fe4f5f6f486e98c5678`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 11 Apr 2026 21:22:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 11 Apr 2026 21:22:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 11 Apr 2026 21:22:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Apr 2026 21:22:08 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 11 Apr 2026 21:22:08 GMT
WORKDIR /tmp
# Sat, 11 Apr 2026 21:45:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 11 Apr 2026 21:45:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 11 Apr 2026 21:45:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 11 Apr 2026 21:45:09 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 11 Apr 2026 21:45:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627211ea53d67d631f36471af626424406273922e1c797e45253f9483f38b907`  
		Last Modified: Sat, 11 Apr 2026 21:27:49 GMT  
		Size: 142.7 MB (142662927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b09fbf3a9922420534fb327736383544373b3c28e3adb08e4094de77f51440`  
		Last Modified: Sat, 11 Apr 2026 21:48:56 GMT  
		Size: 73.5 MB (73518926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd8d137132560e06f314d2c7f5a26df6300196e6d873ff36bb9c22beed8e008`  
		Last Modified: Sat, 11 Apr 2026 21:48:45 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f960dd86cf1e44b45b02496e3916ab04506d56c861f86d93d5bed7a4d42011`  
		Last Modified: Sat, 11 Apr 2026 21:48:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b333524ea4c031d2c67379cecb70cf311c20a3c826c23e1634b8a29e7d4ce2ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5262543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd65d86c57fc23bb64aa1151bcc70321e0ef466dced7dc23dee0331b44a51d3c`

```dockerfile
```

-	Layers:
	-	`sha256:7f95faa09c1b2eca99b8c28178a440f8bbb88da584cbfbabddc193b6bae088c9`  
		Last Modified: Sat, 11 Apr 2026 21:48:46 GMT  
		Size: 5.2 MB (5246683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41471170482b7713385d113dd8b2da3bfe7d15daba4c608e056d8a5e761fbab4`  
		Last Modified: Sat, 11 Apr 2026 21:48:45 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b42afff3012e9a929d81c5b926c920685f2232fddee70cd0b92d5d7ec7daa2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241062168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9db5548beee3c4cff7740cb9ae8809aa359fa1429e7ef0cb029b8d4f77312a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 00:40:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:40:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:40:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:40:13 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 00:40:13 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:40:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 00:40:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 00:40:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:40:29 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:40:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32da005b43fad81bb2ea36a392cb37891258a2457f0b6848f705c3cc5c016f94`  
		Last Modified: Thu, 16 Apr 2026 00:40:58 GMT  
		Size: 135.6 MB (135626975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36ac352fda95cfb437435ed3abf9f62fcaa0e0db646cfb1339cd12726767393`  
		Last Modified: Thu, 16 Apr 2026 00:40:57 GMT  
		Size: 75.6 MB (75598730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b59a3d65353ceb11e020eec913667d3b2787020ad79d18e0602d9e4812d3a87`  
		Last Modified: Thu, 16 Apr 2026 00:40:55 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71346b3abf90e4c4f477044de1b377c279183d68fe213910f8e29121994028d5`  
		Last Modified: Thu, 16 Apr 2026 00:40:54 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:71f7ea39ab549e4d32bdde64b6a60cb65c80290c516376a4d000ac210a199041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86baf4442c31010b6236ed56e8fe217186d68dd0cbd159ff737f9fb409a9e2b`

```dockerfile
```

-	Layers:
	-	`sha256:ab7947a6f94c47b25161d63eca246b2b68c92a41f13e031506affc48fb7fcaa9`  
		Last Modified: Thu, 16 Apr 2026 00:40:55 GMT  
		Size: 5.3 MB (5255062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8d8e57a037371b1c1f943d88e81806d9c8654e2f6ce3a4b234afacccbadcc31`  
		Last Modified: Thu, 16 Apr 2026 00:40:54 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
