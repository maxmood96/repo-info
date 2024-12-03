## `clojure:temurin-23-tools-deps-1.12.0.1479`

```console
$ docker pull clojure@sha256:1e299b30d42e6a21642bcab4904733b6c04ab6245bac9dc85e0b0a0da21d475f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1479` - linux; amd64

```console
$ docker pull clojure@sha256:fae319ed005cf8d493c61ff97be1632c6884fecdacb73bcaf92a46b23ca81ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294537393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904d1efc6498ac1db77ae3765c287c7f2cd2a0b61a033ce89f8613fbb464a056`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ebd17a673fc9da8d99cb7f0199f0e2475f6e67e9d2bd0e824d02fc63116fcf8`  
		Last Modified: Tue, 03 Dec 2024 03:26:02 GMT  
		Size: 165.3 MB (165295131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1991dc4564803a64fbc02ab752611a757b58403477e4dafbce175f34f95da442`  
		Last Modified: Tue, 03 Dec 2024 03:26:02 GMT  
		Size: 80.7 MB (80744013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b4bb920de7f788fe81f603a77ca1b8fb96ded53ea68c5dad5ad339037bd205`  
		Last Modified: Tue, 03 Dec 2024 03:26:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063805a6d802d52da1d5df697e81a93fb57ebf55e195595980496281fbe9ea77`  
		Last Modified: Tue, 03 Dec 2024 03:26:00 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479` - unknown; unknown

```console
$ docker pull clojure@sha256:aab2d0a4cae597dbdae0a062912da83da7085c46b5bfeaa90990bc61fd015b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7203376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958cbf90119aa085e781f4834c6126febbc11e35bd42e407a649d61c23921ccd`

```dockerfile
```

-	Layers:
	-	`sha256:10972441f75a9997b8dd24202e320b35fce05d186322a9de9a5386d6be6da84d`  
		Last Modified: Tue, 03 Dec 2024 03:26:00 GMT  
		Size: 7.2 MB (7186872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ddc96c97a0cf21b93c1e67777d79bc6f1764c51d4bebf740298c6599486ecee`  
		Last Modified: Tue, 03 Dec 2024 03:26:00 GMT  
		Size: 16.5 KB (16504 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1479` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cfdb7d04ae1af49781176c0f899a4ea8e4407d26ccdbc8563c2c4a0ebab48482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.2 MB (292214001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd51ab10c15928ab161717c451a98919b6695c3b9b1453aef1ec916036699bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b1613c429db6d1369d575572668a0140513d19368009523d3e28d8ad2b6ca7`  
		Last Modified: Tue, 03 Dec 2024 15:32:08 GMT  
		Size: 163.3 MB (163281815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68debb1b6ff1973cf52cf6c68f71e990b1b38e1847da9fc3b9cbcc8aa46d866`  
		Last Modified: Tue, 03 Dec 2024 15:36:42 GMT  
		Size: 80.6 MB (80605467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cdb65110f1c3e7eff98ce918e3e172b6721ad42f2ce1b3506aaeddc6499d6b`  
		Last Modified: Tue, 03 Dec 2024 15:36:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85590336670f31172947c1533713a3c4a6e86a1422d4d9f07a91c6f8e00ff60`  
		Last Modified: Tue, 03 Dec 2024 15:36:40 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1479` - unknown; unknown

```console
$ docker pull clojure@sha256:bb14db9cb47465b6b1a6a74011edefe3b8b6c9f2995aac018b848e5507ef734e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7208688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794e6282819185472c284f2d8806861858782540fc298f3592d8ec91b02c3281`

```dockerfile
```

-	Layers:
	-	`sha256:448e8f8eb9a983198acafffc752e26b07055335565633e82062a3224dee869f0`  
		Last Modified: Tue, 03 Dec 2024 15:36:40 GMT  
		Size: 7.2 MB (7192042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da3b1ea58f2fca668f492f0f17a4cc32c7cf0c4c6eceae3aedd0aa24114a2eb5`  
		Last Modified: Tue, 03 Dec 2024 15:36:40 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json
