## `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim`

```console
$ docker pull clojure@sha256:70ac8a4992e5dad8026ca468514d4c1860248385a5fa09e608b8a77aa277ad67
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

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bf6b7827c3d52f1fc4b3f380b649c99aecf8670595a7692ae240220769126978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243567692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f47a62fbdeb724489e23f4d9e5c9a8c8d16aa2c9a21a76b0748e4ceb369925`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:14:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:14:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:14:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:14:53 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:14:53 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:15:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:15:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:15:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:15:07 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:15:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eacf0dd39e7cdc5ea590c025413077c07276ed23d574d79619733175ce62b9d`  
		Last Modified: Tue, 07 Apr 2026 03:15:27 GMT  
		Size: 145.6 MB (145628717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b94dda0fc51dfa9d7055ac603c59412429d7cbeccef45e3e46374e34cfac65f`  
		Last Modified: Tue, 07 Apr 2026 03:15:26 GMT  
		Size: 69.7 MB (69701600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23334b2f30b322c3cc151df90baeffe067e264d8a9d856f367c5bbd594c7b712`  
		Last Modified: Tue, 07 Apr 2026 03:15:23 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01cfab99f2aed70ad29698d218e26d8fb217a91c39920ceac9ca8079c4b81c1`  
		Last Modified: Tue, 07 Apr 2026 03:15:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:68d09f1aa813a651407ffd843278a282420129bf13f348d6a5c58a29796e8cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cbc360ebccabd0e783466c10eaddcaa1399cd99532fb9f58f6f87fd88a931bd`

```dockerfile
```

-	Layers:
	-	`sha256:1fb61686b603518c930bf4775b1b222e107a723def039169e4d90d7d8542b999`  
		Last Modified: Tue, 07 Apr 2026 03:15:23 GMT  
		Size: 5.1 MB (5116167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5517fdfad4bdbf12c6d58234efa3a2e974d4baa2101851e74b3fe2cae1720157`  
		Last Modified: Tue, 07 Apr 2026 03:15:23 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:190c3a77bdff89e210ca8ec26adec0fce8cf36031779e96ee7147cc7f78e5d02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.2 MB (242242369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb671b147d4d304ec963d0948a9e1fa393f009e35149f8c6c977d11d90737928`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:25:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:25:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:25:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:25:43 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:25:43 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:25:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:25:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:25:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:25:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:25:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a5640f6d669bd0b44f1458a8caac2a42f65ba877ec921985b35ea3014b6f49`  
		Last Modified: Tue, 07 Apr 2026 03:26:21 GMT  
		Size: 144.4 MB (144436224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7b76d9244a6d54b979bbb0751f88c7dd4a11383b28367dcc591c2dc6724b44`  
		Last Modified: Tue, 07 Apr 2026 03:26:19 GMT  
		Size: 69.7 MB (69688935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d394a782656b1ad437290f0b5fc555fae47ddda446bfada74675a8eb0887dd`  
		Last Modified: Tue, 07 Apr 2026 03:26:16 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62a29dc67bfc8db429262ee2b3c6e827b949436acc04ffc9baa93086160ae80`  
		Last Modified: Tue, 07 Apr 2026 03:26:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fd102695355f2664f3e5a691a569074ebdf477f8163f1e80cf241021dd2b0f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec50b51312f5068df12e520bdd157ef1fa45878e5b1275377eab850e4f417b2`

```dockerfile
```

-	Layers:
	-	`sha256:e29f4261a14a57578cfbd579e765b81ac732ad1a283a77ef885f3e08d2ee7a74`  
		Last Modified: Tue, 07 Apr 2026 03:26:17 GMT  
		Size: 5.1 MB (5121928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:122cad4e80a699b68eff9aa69fa3f294ab67d4f8ca71d082e2d6e2ade310ec1d`  
		Last Modified: Tue, 07 Apr 2026 03:26:16 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d988d98f63bfd22aa78defd80d9e19c48844c6f08b33c176903388371236cd25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253051041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854d213d8c4ed3d51742997cb3fe9cf3144e28baf13642a43d4a71661302d2a8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:24:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:24:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:24:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:24:41 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:24:42 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:30:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:30:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:30:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:30:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:30:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7705c24a18f6ee8e217698c94ce8917cf545ab215e1af2f67054b8aadf8bc4a9`  
		Last Modified: Tue, 17 Mar 2026 18:25:57 GMT  
		Size: 145.4 MB (145438266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0405cf48aacfe852792e8db2dd763330f6a73ae6f1750d26a1d2c03d07c6687a`  
		Last Modified: Tue, 17 Mar 2026 18:30:56 GMT  
		Size: 75.5 MB (75533368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1db6b7fac07fec680ca092b5be38f1d8b2374f355e66445f9da98cf57505b4c`  
		Last Modified: Tue, 17 Mar 2026 18:30:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f562593312ad2a3a137ba4daba01aa5abe410fafcea2686e6069e54c6e5240d`  
		Last Modified: Tue, 17 Mar 2026 18:30:54 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:327a23e7af8c65c21cdd4fd31d50ad87765e9ca203dd39734283e9ae03ce7576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac8883797b91f362e3d4867817ca8a4f7ebaa5916da127f13d51310f67d8575`

```dockerfile
```

-	Layers:
	-	`sha256:a811c24b7a1ef409414d416fbe0a955a65ab0fc6fcb7a4a7db79b28f126ecf6d`  
		Last Modified: Tue, 17 Mar 2026 18:30:54 GMT  
		Size: 5.1 MB (5121325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7918962a5b756198bddc41ccd09a696b4903794c303126115565fa8ef67fd770`  
		Last Modified: Tue, 17 Mar 2026 18:30:54 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c49bbc8756d5b5196ab0a2e3fbb03442e84432c32f2916a3136aa942105eb68d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231033220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2738466ae56fe12f78ff1da6aac23d61ece6c589bd8d75d30e968384d3aaaf98`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 05:41:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:41:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:41:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:41:51 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:41:51 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:43:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 05:43:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:43:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:43:03 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:43:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5bb5c429c7fc69853b04b7b379880a199d321686ac73dcbc03c18f0876fec8`  
		Last Modified: Tue, 07 Apr 2026 05:42:27 GMT  
		Size: 135.6 MB (135626852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81f953c4f5e6f098875cf19eb3db5ff7d0abfb254428c68de93299b96694c4a`  
		Last Modified: Tue, 07 Apr 2026 05:43:27 GMT  
		Size: 68.5 MB (68513692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7cad3a8df70817bf4981b9ebe26551ccb21cc70c8b26dd30b94797da4d2da1`  
		Last Modified: Tue, 07 Apr 2026 05:43:25 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3745761857dea9e94755cf32032e4a4215a981e608a8d912f33b09cc33cf31b4`  
		Last Modified: Tue, 07 Apr 2026 05:43:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:09063ddd60eef1525e8748509cfff4651cc44b2f07a5b7c4809e7272476eea09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c971cae8112d07562f318b8529eb3503362e15dcb8d3c1c97cb817f91f437e1c`

```dockerfile
```

-	Layers:
	-	`sha256:de5a1f01aac64a7255a51b81341e53932ce7c5c51eccd6edd909a8f9156c875e`  
		Last Modified: Tue, 07 Apr 2026 05:43:26 GMT  
		Size: 5.1 MB (5107488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2c4075fc07f7683aaf788fe5d1e0680958d9409a6b9cd8d0a6920dde10a44c1`  
		Last Modified: Tue, 07 Apr 2026 05:43:25 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
