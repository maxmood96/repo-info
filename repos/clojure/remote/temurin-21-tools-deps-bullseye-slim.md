## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:97a993cdefc1e26a3cb01794f704c2ae3bc543d2e796b26912dd7fa5658c892f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

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

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9a480910419c9550d2883dea418d2d284379acb1db650fdaf55b5cd1be8f5501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.8 MB (244762950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fcd75d63684cdc8f92812560a7fa436f6c20556c5f4ca1b913218ae400d873c`
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
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418be6d64130070ac147f4a2a6cb7282411caa2ea235d5c8d6dba69a77f275ca`  
		Last Modified: Wed, 13 Nov 2024 01:28:32 GMT  
		Size: 155.8 MB (155793082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a2257fcb0cb31321d52971cb60403802fdda0ff29655436d961a73f4ea25e0`  
		Last Modified: Wed, 13 Nov 2024 01:32:10 GMT  
		Size: 58.9 MB (58877226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa610b2c052fc609027f589b88cdd36bab37e7f87aad0fbe7e593f6ceef6c056`  
		Last Modified: Wed, 13 Nov 2024 01:32:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59384873769f54ed457291c5437ad3fb69564efc3c747441f4230bd9cac1a9c2`  
		Last Modified: Wed, 13 Nov 2024 01:32:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:43161f02f3892162049ec172e08a10b73265bcd4098b81ce91c97707c3a44d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5151633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eab2e8b6831cdb6e9d246a8a425439b0b211f8a2a0881c1d2fcf39d51b8bd60`

```dockerfile
```

-	Layers:
	-	`sha256:aa47f49039bf8c3f793541342afe8ff631e1efc6d159f60846562ba6df4ce646`  
		Last Modified: Wed, 13 Nov 2024 01:32:09 GMT  
		Size: 5.1 MB (5134916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4561d9ddc19d0d9607d2de76bee72f512b8db9111dde186fd806c9223af6e479`  
		Last Modified: Wed, 13 Nov 2024 01:32:08 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
