## `clojure:tools-deps-bullseye`

```console
$ docker pull clojure@sha256:716bb4a366ecb8a85da4bcbab0fbd16a4aa338d7ae4371a2da222d6843030395
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a2cae2747822a5cedf814db39afe744d3df6be41747b99a04bd3d4f31aa3b987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.9 MB (215936494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e60b6800d0b94e46cdb3a37ebf32f55abb98b0b6cfb69b47e876a4c9a23609`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Thu, 30 Apr 2026 23:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:53:36 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 30 Apr 2026 23:53:36 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:53:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 30 Apr 2026 23:53:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 30 Apr 2026 23:53:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:53:50 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:53:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ac264864efc6e224f48927519c232d58db17298271d49eec8ab97f78c33057`  
		Last Modified: Thu, 30 Apr 2026 23:54:11 GMT  
		Size: 92.6 MB (92574623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9004b6562d57ee3494af308fb13557ff1f9cb74cd5fbada438a61c6c5357aa73`  
		Last Modified: Thu, 30 Apr 2026 23:54:11 GMT  
		Size: 69.6 MB (69597679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b651216a89212837ca7a2cd184c62c9b55221ecc7b6eb7f8129185ed76328ae9`  
		Last Modified: Thu, 30 Apr 2026 23:54:07 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13090d588a1ef0e543eb60543f2c23dd9608b6176019d5287b12258572178c5e`  
		Last Modified: Thu, 30 Apr 2026 23:54:07 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:db5382d165d5181ddc641aaeb1779a95c9a226f777ac30ced950af34c8056700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7bf3b4110fef5c1a24ef957dc9456b870b656d0989c0e72752b7530908f295`

```dockerfile
```

-	Layers:
	-	`sha256:bbf00ae76121e6f15a0a4f4cf8331d6b40308ee389d3b0763d5571eef381753b`  
		Last Modified: Thu, 30 Apr 2026 23:54:07 GMT  
		Size: 7.4 MB (7376350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3376c67b4b950ed16db01d6ad0d7de8b862ca1007c086e5c192332632e910b08`  
		Last Modified: Thu, 30 Apr 2026 23:54:07 GMT  
		Size: 16.4 KB (16447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0389533ba705b7f146ce6c642374f392e033b7dd2012413689be2fa167a5e2f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213534955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f06798c03b7c68a2ea62332b668e1fb8fdb3082efbc552778260f04dd66af7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Thu, 30 Apr 2026 23:53:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:53:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:53:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:53:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 30 Apr 2026 23:53:16 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:53:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 30 Apr 2026 23:53:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 30 Apr 2026 23:53:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:53:30 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:53:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0522a9f580b2bdb7623aacdfb52d57b30595e9b585908688fa5718d7b637622d`  
		Last Modified: Thu, 30 Apr 2026 23:53:52 GMT  
		Size: 91.5 MB (91542288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5fd4b92dd110c8f6e5c2bca1e4400a6eb41404186e4a66252044d6ce5f7dee`  
		Last Modified: Thu, 30 Apr 2026 23:53:52 GMT  
		Size: 69.7 MB (69738628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab24f32b915d1312231c45f3ddd8987a1f6602a21f88cf86946aa3f61144054`  
		Last Modified: Thu, 30 Apr 2026 23:53:49 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b8e1e5fccc961f9e5cf9c8e5343c5808c60fa32b36500471974aac5389c741`  
		Last Modified: Thu, 30 Apr 2026 23:53:49 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:8a127422f43fc678a37eea7f428c61e7bea29b9c0cd6c366072b055caf7df4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7398059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cabd245e50a8444426ee77c5083f638edc646c4f0b09603b8f534dc961181e0d`

```dockerfile
```

-	Layers:
	-	`sha256:4fb5efaf81f24883b22ab699fac62d3f06d4b9a169d36803f520bd8ecc8378c4`  
		Last Modified: Thu, 30 Apr 2026 23:53:49 GMT  
		Size: 7.4 MB (7381470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a624e657bb8990b4a4c755590ce0c06831461e1c14b2f6e693e8e2b0cf52c67`  
		Last Modified: Thu, 30 Apr 2026 23:53:48 GMT  
		Size: 16.6 KB (16589 bytes)  
		MIME: application/vnd.in-toto+json
