## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:fb1ae2570eb7627c44251d275968c4a77d96f27f90342fe98015810020643718
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d0c89015fb957199f9884dc54d5234f09ee4665b30f6d5487e02e0b51e826fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268993747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d74f24f8f32e4f362da8b5cee804ec708a02892fa8491f5bc6448885d9e808`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:04:12 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:04:12 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:04:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:04:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:04:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:04:26 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:04:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5335b8f1080433f4c9c97ae22e6235ca7679f8bde54d2cbb531f01ac91bbebbf`  
		Last Modified: Wed, 15 Apr 2026 22:04:49 GMT  
		Size: 145.6 MB (145628767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb2910d6288611fc712376d729e62fc68568444268ec13067bb0a12ceba420e`  
		Last Modified: Wed, 15 Apr 2026 22:04:47 GMT  
		Size: 69.6 MB (69601144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c9e3ccbaf22cffc4ab38607cce2b74729950702da1b4c9c73fefdf64eb33a3`  
		Last Modified: Wed, 15 Apr 2026 22:04:44 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b525f775998888a24a55714cd7500ca3e8f94b106eb9fc054a5921b4bfd539`  
		Last Modified: Wed, 15 Apr 2026 22:04:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c3d34ae6756c9a828a076ef9e6f0e783e9ba69c9de26ed6dbce068f1eab24636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7423430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f584b01ebf87f24f55ef1748e4c7ab196018f517350a82fd4ecb918c369b1202`

```dockerfile
```

-	Layers:
	-	`sha256:0cb1edb88ac416adfc3610a83d9464a14b83b8eb371bb59770a5d089e13ddbce`  
		Last Modified: Wed, 15 Apr 2026 22:04:45 GMT  
		Size: 7.4 MB (7407653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b20b99d1347ddc28ed8cd711414e008273e1df061f1bb33140235211b5e5691`  
		Last Modified: Wed, 15 Apr 2026 22:04:44 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4a4844c6a3d754ae99d7e3ef5be9492db0a6915bb83ae6762bdd6c1ce0b52399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266420735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0804f52928a8d134b3ec82a2b3ad9ac6d50b0953e123af0ab35cb9a0dab5bb1e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:15:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:15:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:15:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:15:36 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:15:36 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:15:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:15:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:15:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:15:50 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:15:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94894d71c8e2ac763386e0ba84472a8dec31a6ec07a7adf25d4bf699f527ca28`  
		Last Modified: Wed, 15 Apr 2026 22:16:14 GMT  
		Size: 144.4 MB (144436242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4ab86301e2b1667cd23bbd02a9aa7cbc9e83e27d8d645fe41f2c257e4926c3`  
		Last Modified: Wed, 15 Apr 2026 22:16:13 GMT  
		Size: 69.7 MB (69735836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5f1d07ad79ba88b111846acd679f7df0d5a64e74948181e890d2b38fd3f779`  
		Last Modified: Wed, 15 Apr 2026 22:16:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67ac927f66fac91ec022df4a2aab74e2090e62afbfd79b5876cf21dbda064aa`  
		Last Modified: Wed, 15 Apr 2026 22:16:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:364a50f3ac2360583d321521976c83c5adc7b3b3463c1dca7d2bfa8de5a83f69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7428647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d641155b39234d38a60348cbea12804c3c41df7c8c69193b219c4d9c4b52dd1`

```dockerfile
```

-	Layers:
	-	`sha256:d6b0cd66368c26eaa493fcd2daeb2d3c870aa2df8f0b385d38cddf0221d1875e`  
		Last Modified: Wed, 15 Apr 2026 22:16:10 GMT  
		Size: 7.4 MB (7412752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f251a1ed7f04a6d4f6d08048948304a7ea62485d5e7ce5aa26a76fd8a8d9eced`  
		Last Modified: Wed, 15 Apr 2026 22:16:10 GMT  
		Size: 15.9 KB (15895 bytes)  
		MIME: application/vnd.in-toto+json
