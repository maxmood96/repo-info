## `clojure:tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:b2c2a9035332e285bd02ce2203ba77474dea6af8bac9b9b7a544b42771cd319e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a7ad48da8b6a3f67d5bfe18964dbcf58a39ed7ff1c2bdfb659bbbe1edcca1715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.8 MB (247761494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf885a9454c53ac79b3a3cb9894e410a4be0f162a0a10a3a42034f4689fb2fc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fe5f8f24900611529379b093c73b603ab06248d2cc8865e95595ebb6cb3043`  
		Last Modified: Tue, 12 Nov 2024 02:49:34 GMT  
		Size: 157.6 MB (157568701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c2130fcd2c550acd6e7ac7c4e4530aa9e8f266b132173282bd27bfd07119b3`  
		Last Modified: Tue, 12 Nov 2024 02:49:34 GMT  
		Size: 58.7 MB (58740199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e82a7b61c60ed41a10923f763564de6fb421a44f8d4d5dc42684d6d1f005592`  
		Last Modified: Tue, 12 Nov 2024 02:49:31 GMT  
		Size: 608.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a1941f9228a6240d8963c88b7d41749a6f613e85f271d5419d7816798a1e20`  
		Last Modified: Tue, 12 Nov 2024 02:49:31 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dd6d2af8716b569807f4e6fe57c04915a809936664d7bb529733655005e0ebc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5145730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9820f8e08299fed3b729b458c915f05e31b66b6ea0ea6d982c7684902d8ed74`

```dockerfile
```

-	Layers:
	-	`sha256:d698aec99216ced2894b8ded79121c4348c02067c3ff648eb3c2de33a4cfa488`  
		Last Modified: Tue, 12 Nov 2024 02:49:31 GMT  
		Size: 5.1 MB (5129155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9bf5376f0fa65338a50f1642cd8c5c4cb02caaaf8dc479d6b714fd3a43389f5`  
		Last Modified: Tue, 12 Nov 2024 02:49:31 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bf8d56c8fb4f97c84317991d5972a89a2f969f3da8259246bb65960bd2217152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247166678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf5b31200ac081c4c1ef726b0aae4c9accfd5e35b5a22e92570d291c1bf657e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cdc35f8305a192807fb33aedd2b7a354b336ed58f1b2833dab6105e7715666`  
		Last Modified: Thu, 24 Oct 2024 09:27:50 GMT  
		Size: 155.8 MB (155793065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cbae495c0ee313b3f322c3fc555c1b22996516df56037f6e38caca4b53fdfb`  
		Last Modified: Thu, 24 Oct 2024 09:33:17 GMT  
		Size: 61.3 MB (61296815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb7e69df2721f488eb4cb6836f73c33071b08c0195cffd4e92358e4a165f093`  
		Last Modified: Thu, 24 Oct 2024 09:33:15 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f856694939e4c6197cc0e02451217ed752f26cfc6108557a387a983fd4565ba`  
		Last Modified: Thu, 24 Oct 2024 09:33:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3d3d8919ef4ac0a31ebc7503582373766047b870bc959e747a2ed1c378677a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5151431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5451436cd9a0afb94a70ee2fd0d73cf5ab656199ad6d706c4c0643d3516340d3`

```dockerfile
```

-	Layers:
	-	`sha256:4acbff6a2b76d696c17182604749d33f621c70f4c323437db47fe2a6d72be69d`  
		Last Modified: Thu, 24 Oct 2024 09:33:16 GMT  
		Size: 5.1 MB (5134880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dec1541f806c5d10e69b5d8db77cd2afaf34ec14c4f2c1f00b7ae42b5647cb8`  
		Last Modified: Thu, 24 Oct 2024 09:33:15 GMT  
		Size: 16.6 KB (16551 bytes)  
		MIME: application/vnd.in-toto+json
