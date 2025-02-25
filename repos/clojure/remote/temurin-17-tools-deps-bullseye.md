## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:3c36922a9000168fb39b1eb143cc85c19648e38765002a5947c7409bd10b7048
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:0149b8affdf2cc7b7ca7b0a2ddd8ec6cad430c8659eea9432cb82810a19c6766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.5 MB (267496565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9631eb4396954df478fb8375e0efadaf3dd6bd65017fbfb41e292b5eefca2048`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a0b5b32750bef5e9b984a5ed57f72ed0c34a9425246af5b6f8878c390dad91`  
		Last Modified: Tue, 25 Feb 2025 02:33:31 GMT  
		Size: 144.6 MB (144566555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c84365d34a46c0bc25cb912bbfae2e10670f45f734a6c27fef16e971e7adcb1`  
		Last Modified: Tue, 25 Feb 2025 02:33:31 GMT  
		Size: 69.2 MB (69187566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e1700164639782d6298f713b8fe38ec9a33a11292600dd569ce88c7b1e38ec`  
		Last Modified: Tue, 25 Feb 2025 02:33:29 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55928fc44f76c369ef6cbf3fc3f6e72e517cd68ad8623aee143e1f9312f841fd`  
		Last Modified: Tue, 25 Feb 2025 02:33:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:96f32847d1c2a2bdecec0564aae0fda2923ad5397dddeb3b2288ad98cdd0a8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7220375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c39965b2b6b8a846758676f80d455c6eccc735a4ecae32bc1b7e862c408a6fc`

```dockerfile
```

-	Layers:
	-	`sha256:9d20511a47717b1562c18318129dc0721cfd317a2ba5dbdc4db62a83458566d6`  
		Last Modified: Tue, 25 Feb 2025 02:33:30 GMT  
		Size: 7.2 MB (7204555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f017d3c5153967f854729b5c5f706da286df0a18519d9ee6853daa663e0ed4f`  
		Last Modified: Tue, 25 Feb 2025 02:33:29 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1162d9ca57bf6df39db0b4d5cb2130abde00c66ea897e8b0394682bc4b7fa181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.0 MB (265013515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0a7bae7edc64998e07776fb2093677fc4078d54ff6805b8e796effa66ebf84`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7e1cabb756c27ddad3e1de86c2aaf2bca04f012bff531cd99d37f98896026ca4`  
		Last Modified: Tue, 25 Feb 2025 01:31:16 GMT  
		Size: 52.2 MB (52248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205c3a5e7f26c811dd80fe19733e685422351667734280b164c293e5efd676af`  
		Last Modified: Tue, 25 Feb 2025 11:04:31 GMT  
		Size: 143.5 MB (143454729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbec9abbfc81b5c71fc634420221776742f5328964c68b06b0a2b68d0b10f149`  
		Last Modified: Tue, 25 Feb 2025 11:07:31 GMT  
		Size: 69.3 MB (69309100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9901ada6af95726e67812854b724de6bb7a9a6bb07a6551a5e745eb2b0c0f673`  
		Last Modified: Tue, 25 Feb 2025 11:07:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6ff592d9b64f4b34592ef3c4f5105ce1d140e8efc3369bc2b95cc3602c96c7`  
		Last Modified: Tue, 25 Feb 2025 11:07:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:47c389a2d507edf4b82dd4293f4c9434ca5df970b6245b796db0adb749536877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7225593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4444b1b75547bfb54727431b2d735ed2e1c36bc8d8b74898a4966d582b84df3a`

```dockerfile
```

-	Layers:
	-	`sha256:4aeefe849e7db5df9f57f10c936f1c082ebce57f93f89cb329e25e2cbc4c85e2`  
		Last Modified: Tue, 25 Feb 2025 11:07:30 GMT  
		Size: 7.2 MB (7209654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47598ff97fc039c96d9f16d6c3ac28f3652ea70dc8cb48ebfc57c94e3312251a`  
		Last Modified: Tue, 25 Feb 2025 11:07:29 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
