## `clojure:temurin-17-tools-deps-1.12.2.1571-bookworm-slim`

```console
$ docker pull clojure@sha256:2ddb8e050ee754ea3334e0031c2f44f67502980d2e81927496a06484940c9121
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.2.1571-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:16e4c08e3bd452cab73e0a70b7f17fc106e4da9ec85a74e5e9a1c9cd71679d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242598060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db074e26f07d6e0958a0cb139ecdf07966f781448c5289ad46b9fac78a95e2c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780335342d3c285c2b5cda8b655ed51d315855c88acdf47b742c8e0b94e1b12c`  
		Last Modified: Tue, 23 Sep 2025 01:45:19 GMT  
		Size: 144.7 MB (144693609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a43c7dffacf42f3ff04f22bd8e2395d4e3e0b69d36df6a489849c53f11d7b23`  
		Last Modified: Mon, 22 Sep 2025 23:46:11 GMT  
		Size: 69.7 MB (69675063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41e1b2951f7fc54a31b591faad621671f2ff287e750faa497af7802091cccb6`  
		Last Modified: Mon, 22 Sep 2025 23:46:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259bbb283ed084237a02ee818efecb1ba3143fd3df61f9c95d5e7ae56574d446`  
		Last Modified: Mon, 22 Sep 2025 23:46:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.2.1571-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cc0fb484375baa439b0aeba3fd313d90854db269cff2b7227a16c8eb1d12aee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5129267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55df595d29526d0da8d0b2c1ef76fcf824469b33f923cec8e0c24494a429817b`

```dockerfile
```

-	Layers:
	-	`sha256:4dbec663d51103a8d526e206c79e7576212c9b4ec037bf6acc0dcaa3366e1cec`  
		Last Modified: Tue, 23 Sep 2025 00:37:59 GMT  
		Size: 5.1 MB (5113388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e50db74a2d6dffa265e0c6e1f00b923e49513aa262d5c6c1d2bc57acc356fd8`  
		Last Modified: Tue, 23 Sep 2025 00:38:00 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.2.1571-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:97f33d46c8cd6a8a557d0fe894e52afa366a7c36dab16d1d41a1bddb795e75a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241208798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f803528ab9fc9efe50455391f8fe791304b42ffa5af19b16fa269438703c8b2b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d6161c80ad842947e3efdd0d2da7bc48a8f4b1b33205d6f22f25644724b3fd`  
		Last Modified: Mon, 22 Sep 2025 22:18:08 GMT  
		Size: 143.5 MB (143542128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c004ef9f8798a7b4e56b8d8f62e933032d635e639a1d99f3a126240fda60d8f`  
		Last Modified: Mon, 22 Sep 2025 22:18:19 GMT  
		Size: 69.6 MB (69563525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffac6c6a3004d2867e751e83619d1eed63ad1f4a8be5300c74eeb3235c7d707`  
		Last Modified: Mon, 22 Sep 2025 22:18:14 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f167a4f4066fbdedb1e4e270b6b638e2e0105bb92feaa273774973841d8c1c7`  
		Last Modified: Mon, 22 Sep 2025 22:18:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.2.1571-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:398cf1983c47c363408d0230f78dd2a590aa319fbafe43e44a833aa2df991300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2e988c6578896af99bcdc031131bf5b90849be1ce8fca674486c843d55757c`

```dockerfile
```

-	Layers:
	-	`sha256:30a86674d21255eaec2639d0ef34f3c08c285a2f6b3c3423b7f1ab467f7dc02f`  
		Last Modified: Tue, 23 Sep 2025 00:38:06 GMT  
		Size: 5.1 MB (5119149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dc049ee46f261db02de9eb670e7a21f33be0b8a8a295e6029f39a6df36f4ab9`  
		Last Modified: Tue, 23 Sep 2025 00:38:06 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.2.1571-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:9d2894d58e9074d8c18bd13b1de04bcbed1a9f438341c87dafe34e06610247ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (251955893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3c5d08fd11e821e7b358558d431b45c952298222230e0668cefe927ea492fd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a438293490bbc2af66661166949a4d86358eeb39f9fadd5b0146666f05b9b9ac`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 32.1 MB (32068762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b0b9ad4e2e08bb92699318cb0d261070a8cfd1ce9528efce75a25d890288e3`  
		Last Modified: Tue, 16 Sep 2025 00:59:42 GMT  
		Size: 144.4 MB (144372818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a8f9e4fb03abf657274e9190034deddd5239e670aebdd2c0301086460c0585`  
		Last Modified: Mon, 22 Sep 2025 23:00:56 GMT  
		Size: 75.5 MB (75513270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae67bd6dec4d68f268cf5300f75358698443a319db737473bf317eb1357bb3b`  
		Last Modified: Mon, 22 Sep 2025 23:00:51 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08854dcb1f862500f8f09182ad4f4ed482181d22a9a68517afad60e2e437b51`  
		Last Modified: Mon, 22 Sep 2025 23:00:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.2.1571-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:098293f2e591a8ecbbf26cf6d20c277cb1ce94f7ca64adfd236d2830d8138547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b34fbe75a7e9aef25fde20c31e6eeba176d5e6be2a10cb988dde2ca7b4dd8e3`

```dockerfile
```

-	Layers:
	-	`sha256:19b47e50ea215888c0ef4e41ccc3a2b4c2c637f6cddeba9102d6de68d8141edb`  
		Last Modified: Tue, 23 Sep 2025 00:38:11 GMT  
		Size: 5.1 MB (5118546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:514a0bb8a861b85ffa18a4859624848e543838cea6ba083955f51521e03cd87d`  
		Last Modified: Tue, 23 Sep 2025 00:38:12 GMT  
		Size: 15.9 KB (15927 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.2.1571-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:0278d8ea83e80a4ebf39bb08c063342a7f9bce961f5442c47daf64334c2279d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 MB (230100399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e03c9afd99ffab0624e09871c74c37c6f80174c354537b2f86b79610c5b74457`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2602c23d719124d8d19e0e56c4a779006fdf8ce799d6cb00b3e1ee7041789491`  
		Last Modified: Tue, 16 Sep 2025 00:32:24 GMT  
		Size: 134.7 MB (134724380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821adc3af2191577da7eee61b134f1e88b2eaa0ca3bbe4a81a9c609a34ae0500`  
		Last Modified: Mon, 22 Sep 2025 23:07:23 GMT  
		Size: 68.5 MB (68490681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d72c5bdef50019fcac22d3b811a7ad6c9a6be743052af4b226f6e01bf0f5656`  
		Last Modified: Mon, 22 Sep 2025 23:07:18 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af050b2c4ffb8e557b03b526dab795cda2bfb233feedcc0b340ee3bb0ca9292`  
		Last Modified: Mon, 22 Sep 2025 23:07:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.2.1571-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b1bb7b7f1e699993eec13808ab18fddcf9a250b4634e233f9ad007ff2259c69a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5120588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23a593d8a3c8e3d86de850d11608beb0973bd6ad39cc597b5043181a6a797add`

```dockerfile
```

-	Layers:
	-	`sha256:dcab2851ed71d10f48bbcc47e0d10d29b75221ab56ee83e57ffe15870fc0dd6c`  
		Last Modified: Tue, 23 Sep 2025 00:39:21 GMT  
		Size: 5.1 MB (5104709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c1eb3ba0db47252427b8155028219eb2da0fe136083866f2cae0b079c233b5d`  
		Last Modified: Tue, 23 Sep 2025 00:39:22 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json
