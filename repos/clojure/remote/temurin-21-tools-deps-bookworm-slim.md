## `clojure:temurin-21-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:4b30fa889ed6037926e978e15e9854809353bf7691821631c796610c1007a2cb
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

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5304fbce366032666e8adaf702c4b6ee560e28b1ce713bb6a28212c14dbfe4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256138957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019e8c93a71b9029c42fedc8812c4728530aa32214baa79861e9007d4f8bb13c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:00:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:00:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:00:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:00:01 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:00:01 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:00:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:00:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:00:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:00:14 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:00:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39783e15b20e015213f35f6f733c7a136aff3618fb2c8100e4cbc10327e9ce69`  
		Last Modified: Wed, 20 May 2026 00:00:40 GMT  
		Size: 158.2 MB (158166940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c26e877c494a4225877b97cc2d6960b17b62e9aa544cc090786cf8be8dccf2`  
		Last Modified: Wed, 20 May 2026 00:00:41 GMT  
		Size: 69.7 MB (69737430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7a2b6e9389183105ee3890acb1100ccef7e9fc9120421a562bed98cda07274`  
		Last Modified: Wed, 20 May 2026 00:00:36 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be7b97a91e63a26050bed532ff6d526e66e71b65ac06d3ca602af324ba17725`  
		Last Modified: Wed, 20 May 2026 00:00:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d20d041cdaad494ccecd02c6957c5bebc476c90a6ee6ef542075f62e41dfb0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90dc445c3697980febe5c375600355dfbf79c0caabe3488cbcc39e98ab6ac715`

```dockerfile
```

-	Layers:
	-	`sha256:55403730a9a1665d7ed3b93d1ef325bda4d046023244856ef2e0972987f341b3`  
		Last Modified: Wed, 20 May 2026 00:00:37 GMT  
		Size: 5.1 MB (5118666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a7173d4156f293465d30c10027abb9e716e469db61c7b0dd44e9fb1cf564700`  
		Last Modified: Wed, 20 May 2026 00:00:37 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:be81e3d0353496b88121aed3934ae1a1ff9da2ad135fdf17017894675bf1e82f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254308954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c3ac616e2cb0cc91f20c5f75917dd8796749e7a817507f998f7cc30fe4c2eae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:07:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:07:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:07:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:07:03 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:07:03 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:07:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:07:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:07:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:07:17 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:07:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09fbeb681e10d28b6baa1189254cd9f99ffd8e33cda886a54fa2327da296b9c`  
		Last Modified: Wed, 20 May 2026 00:07:40 GMT  
		Size: 156.5 MB (156461273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2607f0aeda9ac64c248cfc0288993f8593f0ad48632adf4d9e9bf833d283d56`  
		Last Modified: Wed, 20 May 2026 00:07:39 GMT  
		Size: 69.7 MB (69731597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bac874721195de7433a6770230d05f627cfba591e7b6b2bead2f59a29e8c14e`  
		Last Modified: Wed, 20 May 2026 00:07:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d3b0d9e1e3ed03093084a0a51835b0d07fd3f9b5652b3d9cd292d55d68fc59`  
		Last Modified: Wed, 20 May 2026 00:07:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8bab7f690e81c2db3cd9c2a275cc1c4171cc462919facfd52e762fc5fa632ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5140535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbc29aecdc394a21822648c0b805bead26d68bb6f9635ead99a2b585efb7eac`

```dockerfile
```

-	Layers:
	-	`sha256:010d7bdb842b4778623f63f78c4b341f617bb88a7f406e27370fdf2215a25664`  
		Last Modified: Wed, 20 May 2026 00:07:36 GMT  
		Size: 5.1 MB (5124427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2499eb01f28598291f7fb638b30b030f043653084860b6004162ede9e391c8e`  
		Last Modified: Wed, 20 May 2026 00:07:35 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:271970a47af2222d50c90aef678a3ea9d0bfc34522f0e58bbf22c791f6487ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.0 MB (265988781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00f32881a45d4bdbd020d9d0cab62d2b16b7b2a92d22f16657022fd226c06b6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:36:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:36:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:36:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:36:33 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:36:33 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:27:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:27:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:27:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:27:56 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:27:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa7fc9485b4fb59cd58fcb71fcd4db3dba936648eb297bdcd72a79d669b2338`  
		Last Modified: Sat, 09 May 2026 02:37:42 GMT  
		Size: 158.3 MB (158343237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0cd2adb362d11fcb1a5e086f0216518896c0f40e2ab8dad4184852febefe456`  
		Last Modified: Fri, 15 May 2026 20:28:32 GMT  
		Size: 75.6 MB (75566047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9ff3944e4c3a67b9cb75c35e428baef88d7ea051db4c83e3f70f456de15118`  
		Last Modified: Fri, 15 May 2026 20:28:30 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95a83443dbf2bc863fa6949281046762768a9445e2ab8511fbe40056303c87a`  
		Last Modified: Fri, 15 May 2026 20:28:30 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:27841ee5d83e3330a40f3fa9de66a3cac7590a33593fbef3957ffb7c0ae32ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ef6a74ec0249b3cbcd6d092a662e56f9188f3845b25623963a0437bc35506f`

```dockerfile
```

-	Layers:
	-	`sha256:441a05a5d4f0a9bbeace70a107821df6723d3e65b56b4dae4abef6c02b8f65fa`  
		Last Modified: Fri, 15 May 2026 20:28:30 GMT  
		Size: 5.1 MB (5123802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abafa2deaade04965746f905176966b875477bcfb3b7422056662d3e513ff04a`  
		Last Modified: Fri, 15 May 2026 20:28:30 GMT  
		Size: 15.1 KB (15083 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:ac01a6ae0abd6f953f79010d12e3b67e279cab14fba9594edb0d1c1a04d1d405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242816914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fde0227a7a9470b7fc0e2b0189a98776cf2d1f79c2bd6a0f08a8ca7885e7d5d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:45:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:45:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:45:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:45:30 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 01:45:30 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:46:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 01:46:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 01:46:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:46:41 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:46:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f59c7ebea2b6007773062b922180dc57776e79bbece633a441c340904337864`  
		Last Modified: Wed, 20 May 2026 01:46:11 GMT  
		Size: 147.4 MB (147388338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0276640c6c8e55511e25d5b28a39736536d2e778962ba0b9e9cb24f87bd84b`  
		Last Modified: Wed, 20 May 2026 01:47:04 GMT  
		Size: 68.5 MB (68538938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62634ba3147ea4df071a349aec49784ac8e2d8fde7e24bc833f4711c12d69cfd`  
		Last Modified: Wed, 20 May 2026 01:47:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a122a0d4b3e9b5116d2492b1d31259b95f11a6630da66ca97e19b38d4c2a3cc`  
		Last Modified: Wed, 20 May 2026 01:47:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b89c98c0839efb72dd5ff21502a37e11fe7d8993862afee2ef779d88c1d6bda6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c4667d8b9acdc47c20d192c4080ae574de8582e0905daa15f8ba6450ed2e47`

```dockerfile
```

-	Layers:
	-	`sha256:7cf1f42c6c0c76a12db5fcd38b5cad25869fcdbaf501d32fbb1c16e16b250626`  
		Last Modified: Wed, 20 May 2026 01:47:03 GMT  
		Size: 5.1 MB (5109987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:823f420c0d5c0280619ef13e77a36118eac032a0398923e521dcfc93cb70ac51`  
		Last Modified: Wed, 20 May 2026 01:47:02 GMT  
		Size: 16.0 KB (15989 bytes)  
		MIME: application/vnd.in-toto+json
