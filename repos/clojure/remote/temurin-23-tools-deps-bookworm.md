## `clojure:temurin-23-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:5640e20ea98c771b76e9be9ff3ad7d72c345f56f017f2aae7678a62ec9e46473
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:646fc933d84c047a1f2b98aba9f72b6f57bb12dd9427aba8f74677b388529126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294537441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78e80d0383d209a4e811a80d8cd523d384c9b1a4eff95517d2792d40984b73a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d760ac17e45d3321880494fc84d74adc4e770c4f5a24b2843c41f16eaf54d91`  
		Last Modified: Tue, 24 Dec 2024 22:38:45 GMT  
		Size: 165.3 MB (165295092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e2548782c7de41cb65099b0b180d162799d354bfff070b8dcb9fc2bb638a05`  
		Last Modified: Tue, 24 Dec 2024 22:38:49 GMT  
		Size: 80.7 MB (80744244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b68d62bec92e4765b2f93f117374d9d96b702ed69bda32ea4e833b0f3ef764`  
		Last Modified: Tue, 24 Dec 2024 22:38:46 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc339761a3234fa28c37fdcf3acbf0f5dcbce5b9fbb4c174438bde9c8ef6e002`  
		Last Modified: Tue, 24 Dec 2024 22:38:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f3ce9522fc4bb8cba6aab290925bc154449a9f24ace5a93014d9bb7841a0560d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0018e7a3818aed31f5a6d7fa526f7bc8bc9fbf460fe2a15c8330761053183037`

```dockerfile
```

-	Layers:
	-	`sha256:11b3bc0f9c9df9f1eefddc20ad1cb05d96cb00225e0dd3a8bfe605532ddf4d47`  
		Last Modified: Tue, 24 Dec 2024 22:38:46 GMT  
		Size: 7.2 MB (7176707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4e48ef6cbdb84671e1d1cb1cd4637b69a5997ab2eb112398969330d94154f55`  
		Last Modified: Tue, 24 Dec 2024 22:38:46 GMT  
		Size: 16.5 KB (16504 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bookworm` - linux; arm64 variant v8

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

### `clojure:temurin-23-tools-deps-bookworm` - unknown; unknown

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
