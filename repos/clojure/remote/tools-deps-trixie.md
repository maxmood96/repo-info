## `clojure:tools-deps-trixie`

```console
$ docker pull clojure@sha256:81d69d927d5d93ba4501fbed5c9f6815f9702625c0e0378ba12c858d6614d8ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:be274e1af474b4e9cc80df6ebf697ab1a37802b56d835193af9e2c805ab26326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226862603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc15ca4a67d2564c0362ef697e056af1ccbd15f96ea1d5e872ccbfd4d8312a5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0133f2e42f905f07c4ba353ce2887dc6d871d44eda1653df67ac36b64327159b`  
		Last Modified: Tue, 30 Sep 2025 00:57:36 GMT  
		Size: 92.0 MB (92036048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871ed9045fe70ed40094f46451151538bd49e08cd86a39f0013df649e393081b`  
		Last Modified: Wed, 01 Oct 2025 19:22:42 GMT  
		Size: 85.5 MB (85540887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9cc357aadaf2959bec1cc340040e4e99c7936fc8a7fc80a1f53a8a3c0da0e22`  
		Last Modified: Tue, 30 Sep 2025 00:57:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfd4ce9ab32e8abcd24a377b2c335d6abe27eb32172fd52f174598787634ecb`  
		Last Modified: Tue, 30 Sep 2025 00:57:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fe082f24897acbc90ba2b79e3afb186f30597155d3dc678ff22731e737998b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b12710956155b7f0fccb90c14e744ed19218dabc3767898b1a12f000c860533`

```dockerfile
```

-	Layers:
	-	`sha256:72862a30c611ff768e9df98f048758193ebf27fbd609d632c63261494eab8e61`  
		Last Modified: Wed, 01 Oct 2025 15:43:05 GMT  
		Size: 7.4 MB (7418163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5292f6cde7f26df14036e3a3831873b6c7be85a4b77965462b6243d94133946`  
		Last Modified: Wed, 01 Oct 2025 15:43:07 GMT  
		Size: 16.5 KB (16457 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dff769c40bb4468ed5f76bce4353c645a09849a7517c81ccd6b40ec0aa6e9796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226058468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1092e12159c83224f2e20e76e52d85ffee58828fd32d469fc7aef82291f4aacb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6db19fa452117ade60fcfdff2f0b2c5bcf3c91168e0cc96004fad1220a5de42`  
		Last Modified: Tue, 30 Sep 2025 00:56:18 GMT  
		Size: 91.0 MB (91045236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b254cd070e2cd363e95520f319d6e8052e5357a58e8e7250b98fa5b7c5656ac0`  
		Last Modified: Tue, 30 Sep 2025 00:56:30 GMT  
		Size: 85.4 MB (85363498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2d82ca8daec85eb4f3ebb73e7030a07c600aafdd0aa4342eb0d07e8b54a2bc`  
		Last Modified: Tue, 30 Sep 2025 00:56:08 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4dbcb6cc0a484b688b4af32db586b4588565a728131bcff5392dc4e9f5648c`  
		Last Modified: Tue, 30 Sep 2025 00:56:07 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a069687aeee79544aa0de44f1e04818cd8374fa17cd5b3102f26d6477ada1a07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e375e01ebf2f317ab6c529ae1a8101141978172414fe39dc74e70be62f6f02`

```dockerfile
```

-	Layers:
	-	`sha256:e586e3a6cbbc01226348306f71873de64d12b578648ea4b26e0b09203bbf0d24`  
		Last Modified: Wed, 01 Oct 2025 12:37:16 GMT  
		Size: 7.4 MB (7425214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df77d39204e293691a67e468eb1ed18bdff9a4c8f9f3fa7c19b7f4cfac6b6e15`  
		Last Modified: Wed, 01 Oct 2025 12:37:17 GMT  
		Size: 16.6 KB (16600 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:b539d9d24dc8b13392423f22469c195961ab2410b5feea8c01320bcb90a5c2a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235655576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6290174eb8d12ed46edb47ebee543e30743c1aeb49ea012446d74ad14bf95cc1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cf4ae381b4e7bb5c15181abe64e994932533643478b9004c85a25713722adb`  
		Last Modified: Fri, 26 Sep 2025 18:35:32 GMT  
		Size: 91.6 MB (91601719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8d150849f5b629824b18994694bebd851266b221e785163add4b32fe206466`  
		Last Modified: Fri, 26 Sep 2025 18:42:39 GMT  
		Size: 90.9 MB (90948382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adb89407fcc5784cc09e9368a3d8d14df13f62d30ebc1e1b2eb2699ec38114c`  
		Last Modified: Fri, 26 Sep 2025 18:42:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a837727eff26b61b83c4dc26751c3ce5b6bb33d35e21702b16916e5b077f9d9`  
		Last Modified: Fri, 26 Sep 2025 18:42:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:08bb38313ca6db3c23e09e4686a8e00b1fdbe21e3d4eb7b79b34904f1dd84979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1c5b8ebda4d34ade1c2dd3d424332b4c790f46b767e03b999bed95bfabf95b`

```dockerfile
```

-	Layers:
	-	`sha256:bab6f3113e05e3cd07a0edc27575fba70885a4f275ee828bd84a21a8349dcc13`  
		Last Modified: Fri, 26 Sep 2025 21:42:18 GMT  
		Size: 7.4 MB (7423892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:615b31150fc579ffee7fbac13c48497c0ae43cc0b0c36cdfcc076f7ec5788ec8`  
		Last Modified: Fri, 26 Sep 2025 21:42:19 GMT  
		Size: 16.5 KB (16518 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:d5809dbdecd3dcaa2d1fda8a09bc3d745a1d1bc2232e646eb6d3db7c73047364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 MB (222945719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83dc1a36d45667145c5da13247b2551addabdff56ff2d48706ac128ca1d77b13`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8f913be5ecadf79e3ee9792194aaab366421c7e066487d572f285b293ff78a7a`  
		Last Modified: Tue, 09 Sep 2025 00:25:27 GMT  
		Size: 47.8 MB (47765447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d906c94ffd80ac5b5b080e8a6ba857d4ad76aa0160f09e49e866f4d2bc2962`  
		Last Modified: Sat, 27 Sep 2025 01:24:19 GMT  
		Size: 90.8 MB (90752393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2901c3a8e012ce31bbf7d9c98b5ae6f66ac8fab310ee6c87463906c9d95ab0`  
		Last Modified: Sat, 27 Sep 2025 01:24:13 GMT  
		Size: 84.4 MB (84426834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67fc3c7da6c97e20ac34bd2be62d18f79b8c1ee7710f92cbf623d5b906213e7`  
		Last Modified: Sat, 27 Sep 2025 01:24:03 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a187f4b5a7c132d00bab337e48ae052a43b235962cab6551976d0dda870fbb`  
		Last Modified: Sat, 27 Sep 2025 01:24:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f2f2702db5d4624353eb72521af76e4807ca7c665ad3b910904034bfe0a86119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7422602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9615eb108e42e4bca133583c064e79468f3d53273a342e473ac02f73f414960`

```dockerfile
```

-	Layers:
	-	`sha256:fddcea16304d2d08cf30cb9b1e0c8cf6568b9462c2fea1f95cf9e232e5894044`  
		Last Modified: Sat, 27 Sep 2025 03:38:02 GMT  
		Size: 7.4 MB (7406085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3294d422f87ed5b4a781dee441e5ec42b7c9d8ac6862226a6b2f5c8843b75e57`  
		Last Modified: Sat, 27 Sep 2025 03:38:03 GMT  
		Size: 16.5 KB (16517 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:b8dcba84da60bb0804b3a08d6098f8e1ec02f03ebbfe3e0905af9efa9af93251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224061044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6944b2668fec53290279dbcf1f99826f07e0c21020dac154d0595cf850b91516`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:28eee642962fd09c10ecf87da2d4b65d208f3d5c1bf3fcca21c105c0213f558a`  
		Last Modified: Mon, 08 Sep 2025 21:32:18 GMT  
		Size: 49.3 MB (49346327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182ac8820269436dcc9484ffc51122fcc381e8185984b2a97426f0cdc265d933`  
		Last Modified: Fri, 26 Sep 2025 19:34:05 GMT  
		Size: 88.2 MB (88206458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ac7c31a9ca64f50e065b17c599ded0ea5487cc4a7f934c82ec901c67a126e8`  
		Last Modified: Fri, 26 Sep 2025 19:43:18 GMT  
		Size: 86.5 MB (86507214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07b7b8475464028500117dad358d5065d45ba9c8685b97e8029f8722d5b0d93`  
		Last Modified: Fri, 26 Sep 2025 19:43:11 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0560ab376e619834ba0af76f100af3563c091bda3ed01e8ce947f3bff3508706`  
		Last Modified: Fri, 26 Sep 2025 19:43:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e1b44558d104af8dcda2d56e0bb7caa14599816c537caabd52b59da491c8c3bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd5dace5af8a5bd98cfd27a5ce0a6643875d9930cbc1bb28c1f305617a3a2b4`

```dockerfile
```

-	Layers:
	-	`sha256:8d8acda67303685882ad3145e2ed66b555ad233cff86b5091616de3688791d3f`  
		Last Modified: Fri, 26 Sep 2025 21:42:24 GMT  
		Size: 7.4 MB (7416633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a39eae24059e5d5c7d4e4479478f4a6ce2ec8f8a39de72048bcc669645f5c50`  
		Last Modified: Fri, 26 Sep 2025 21:42:24 GMT  
		Size: 16.5 KB (16457 bytes)  
		MIME: application/vnd.in-toto+json
