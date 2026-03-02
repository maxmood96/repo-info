## `clojure:temurin-11-tools-deps-1.12.4.1607-trixie-slim`

```console
$ docker pull clojure@sha256:c1d45ac2f87b51bb2685bcf6082c499fb23ed06371e7b47b3ef5685a7bbdd7e6
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

### `clojure:temurin-11-tools-deps-1.12.4.1607-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e29fd19b117ea2895b97cd5a52aa1c5a8c58bf44759e6787ca71c0c09a9df6b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 MB (247594195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa4d94a567dbabdc79575cb989de3a3c09dd837c0ac33725615f7285d776768`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:46:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:46:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:46:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:46:12 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:46:12 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:46:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:46:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:46:27 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bd5a9876cf7a1c048d772b33537e7e9566b33266ef740b326fbe2d298e62d0`  
		Last Modified: Mon, 02 Mar 2026 19:46:48 GMT  
		Size: 145.8 MB (145806758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb1118410f7d693b5fa14f35efb8779660827693b76a075c2896f9293987e22`  
		Last Modified: Mon, 02 Mar 2026 19:46:47 GMT  
		Size: 72.0 MB (72008158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f8ab16de1e32d6955fc4b89fe613e5fe103932c8bed8e5326f9dd2097d82a5`  
		Last Modified: Mon, 02 Mar 2026 19:46:43 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1607-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0a384b10554e06dc6fed28a59b42734bb989da335995471ee538570d36bb8417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe949a151233386334a5aa22e03fd1acd38480124da3e088ea0009212f603a2e`

```dockerfile
```

-	Layers:
	-	`sha256:2de67d0380478777316b0774b2e73953c470712105eba477c7551672e3d29ad1`  
		Last Modified: Mon, 02 Mar 2026 19:46:44 GMT  
		Size: 5.3 MB (5279205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c8b4bac9f30f00c354c0b4fe3b4366f7a320bf8b0297eda6fbdb46a50b0c068`  
		Last Modified: Mon, 02 Mar 2026 19:46:43 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1607-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a3c0efbe42b12e64c4cc9e067b037489bd12470cec453d56b1c65c070adc1c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244466168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda14b847b9478dda20fa4a31fd47885ec28ffe8555eda2f91496f78221dc845`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:46:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:46:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:46:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:46:12 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:46:13 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:46:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:46:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:46:30 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa0a878973dc016cb258dfd73697b949762a29184abc1d7c187c487e3ecec1c`  
		Last Modified: Mon, 02 Mar 2026 19:48:45 GMT  
		Size: 142.5 MB (142501445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb15c4c98eaa0f573b269dc459d654373e03962b8bcf9dc6b6aa8f6af9454ec`  
		Last Modified: Mon, 02 Mar 2026 19:48:41 GMT  
		Size: 71.8 MB (71823979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44768629634b3b718338e6f12e60c5fe2f51b609a3745f453ae6714885f18e48`  
		Last Modified: Mon, 02 Mar 2026 19:46:53 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1607-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:960ece2ebefe8f21a1e3eb51437954bb816af11cbc7d3001e094e07b1d5a769c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5299953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9691ac4a56216805d6fa31711a7e6ea6ef08e30cb4befdeb0177a1b1b280ba7f`

```dockerfile
```

-	Layers:
	-	`sha256:ccdfb51faf8b14b6eb0976d0cab83f78419e0f12ae322a88e2dcb40f27422518`  
		Last Modified: Mon, 02 Mar 2026 19:46:54 GMT  
		Size: 5.3 MB (5285592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc8cd494a0d5bf0485c2dd5bc7a77b472aa75da7750e7890c24107d65e514d0d`  
		Last Modified: Mon, 02 Mar 2026 19:46:48 GMT  
		Size: 14.4 KB (14361 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1607-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:58a9a966f9577238cdc8fd2e79d8870bd5974462f957a9d640e60ec946b887bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (244017952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c9f356b2529278d6bcd5a7d83fbe4a47017fd0b5a1eef680c41b8b52a8293e6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:54:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:54:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:54:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:54:14 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:54:15 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:55:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:55:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:55:10 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c81c8aadcb615cd354e8b7da93cdcbaa40fecfc9518777bd732e9d07acb8c76`  
		Last Modified: Mon, 02 Mar 2026 19:55:54 GMT  
		Size: 133.0 MB (132997793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73698476d79f411ea31f032b83bc2a0f7f31f96f9b0d68ac4a25c6f29424b65b`  
		Last Modified: Mon, 02 Mar 2026 19:55:53 GMT  
		Size: 77.4 MB (77419298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74722a706af7a603551d0365ce5c929ef4021ab1220296ebecce209df50a86c1`  
		Last Modified: Mon, 02 Mar 2026 19:55:50 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1607-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:760fada479be72a0ed5de90b98569ec912cc41ffc6579a92d2ae1f9f457b361a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8325d4f3dec8ac155638277f54c2918a3f33b69c42174b79a3121220cce0758`

```dockerfile
```

-	Layers:
	-	`sha256:1e574394e383315f16c9496cfa52e088026f8448dca2d7aef62132166466c57e`  
		Last Modified: Mon, 02 Mar 2026 19:55:50 GMT  
		Size: 5.3 MB (5282961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9608107e28054bde8e75c4fb421a692bfd9d789f403466dcb0b056149e86c90`  
		Last Modified: Mon, 02 Mar 2026 19:55:50 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1607-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:a7ce9bd1170b6ebd36a367e9c0ede9580ac8ed526844777e449612808aec6c41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229372951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878066c1fb61f476f4343138320967fe17b0620f444123df9e8b4745a9a01c25`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:45:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:45:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:45:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:45:01 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:45:01 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:45:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:45:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:45:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e96c059048d9112ac42c3a5e75b4774fc6e819b9c98855d5ddd3f48b640051d`  
		Last Modified: Mon, 02 Mar 2026 19:45:53 GMT  
		Size: 126.6 MB (126562037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc11f75e27fbfc67545d9ec299f71ee8ed78ce54ecf312a0274377ae22073f3`  
		Last Modified: Mon, 02 Mar 2026 19:45:52 GMT  
		Size: 73.0 MB (72972086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db56085765fb834fb399944a74719e647a53f0e21fce9223f699a3ddecdbb8ae`  
		Last Modified: Mon, 02 Mar 2026 19:45:50 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1607-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d9ef0d4806c93cb60d9090dd41b629c284baf6e548d1b1e654c83f36dab5e61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf5f69058376a757f8dab2ec33b271afca9f2c9c73ddbc6b7cbb9dcb9e107fc5`

```dockerfile
```

-	Layers:
	-	`sha256:f9b83cba5881d34781a8abcd58fc3047e9d31d7fda0b1a97ac954e0a4e24eb12`  
		Last Modified: Mon, 02 Mar 2026 19:45:50 GMT  
		Size: 5.3 MB (5275133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac9f943222618732d8597eaf05851a9d4bd3e9a0bb0330407f1407fa37218bfe`  
		Last Modified: Mon, 02 Mar 2026 19:45:50 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json
