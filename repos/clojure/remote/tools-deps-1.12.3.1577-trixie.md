## `clojure:tools-deps-1.12.3.1577-trixie`

```console
$ docker pull clojure@sha256:9e42a0ce53c97b268265a552668911559a0d988003837ca5c4a90d732242a6c3
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

### `clojure:tools-deps-1.12.3.1577-trixie` - linux; amd64

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

### `clojure:tools-deps-1.12.3.1577-trixie` - unknown; unknown

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

### `clojure:tools-deps-1.12.3.1577-trixie` - linux; arm64 variant v8

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

### `clojure:tools-deps-1.12.3.1577-trixie` - unknown; unknown

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

### `clojure:tools-deps-1.12.3.1577-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:3695897f3f2cd840a7a995cf8a85b7408793a33c9b0788f54da24a2aae00445e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235660921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a8f0cbc74f4df695934b7d3c568590aebb21a9959740229ae15ca5c6f33ad4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
	-	`sha256:71fbf24a239310917388930bb043e64907cb532b9ac8f265e44e032dc3bf4409`  
		Last Modified: Mon, 29 Sep 2025 23:41:05 GMT  
		Size: 53.1 MB (53109217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766af3812c96cd94fd147ef3d35381aa3bc0b1eaa8a2ce7ec092737d61a36eae`  
		Last Modified: Tue, 30 Sep 2025 14:05:35 GMT  
		Size: 91.6 MB (91601713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc5879c596198e609aae0a8dcebf43b951d8af30ae3ce5dc4598fa75bc6e194`  
		Last Modified: Tue, 30 Sep 2025 14:10:01 GMT  
		Size: 90.9 MB (90948952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763590394798eae107602409fb0d823d684210f1075503f205c90f0b4f81ef62`  
		Last Modified: Tue, 30 Sep 2025 15:07:08 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d57a9d35979597ff9caf42145a2e5eab63a25d8fa47f7f5c24db8dc0e0fec2`  
		Last Modified: Tue, 30 Sep 2025 15:07:07 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1affc23b1b8b9c9b690e7a2a7f8740f14aeb54e974df5ec4d98aee6671d4bb27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7d676232a006c844e9473e3b22d894c3c3c7811da52457b556b6425815c5ab`

```dockerfile
```

-	Layers:
	-	`sha256:ff163611e4de2b9e83affb0d48d5a3bd88af7129846b76575973ff519f78f7df`  
		Last Modified: Wed, 01 Oct 2025 21:46:00 GMT  
		Size: 7.4 MB (7423892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:268fff88acbda77ae4873b94d8d47ba882847c8d2e87ea6251c1cdfe8acf9024`  
		Last Modified: Wed, 01 Oct 2025 21:46:01 GMT  
		Size: 16.5 KB (16518 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-trixie` - linux; riscv64

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

### `clojure:tools-deps-1.12.3.1577-trixie` - unknown; unknown

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

### `clojure:tools-deps-1.12.3.1577-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:a081feff010f4f4bddbdf2853724cab431ef220159e5d59e6479f547b0306385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224065131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5daf2aa1e865a6aae3c4fa43f8ff60f72897ca3217976151fc1a3275c5fd7de`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
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
	-	`sha256:024d6c344f0b9dbb2baf07e95dfd2abbfadc5c8262ca381f39f6489670cbaff5`  
		Last Modified: Mon, 29 Sep 2025 23:41:06 GMT  
		Size: 49.4 MB (49351442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a669222b11adceb6f50de764217862e10002bcbb4b6c255b2073a95e35d751a5`  
		Last Modified: Tue, 30 Sep 2025 13:39:19 GMT  
		Size: 88.2 MB (88206448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9673d1fb6b57a4d10c4c816905c93536eefd08bac9cc418e6d327f9c9f2b9e83`  
		Last Modified: Tue, 30 Sep 2025 13:43:55 GMT  
		Size: 86.5 MB (86506200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e46395f8ea62d3e869506a11381ce5636a1a447ca6a9abc78fa45ee3ef1717`  
		Last Modified: Tue, 30 Sep 2025 14:32:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb4f58bfab4bc93cfa68cc9f16927c3bbc8b6fded5030777f347c573184993d`  
		Last Modified: Tue, 30 Sep 2025 14:32:25 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f5989a244e5a93259b2f7e5f3321395133eb15bf09f2b02c9d6e19f42128c90c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee961c4c16c8888a8dff5a40f10aa97db9b4623f134a29f68096359433e34865`

```dockerfile
```

-	Layers:
	-	`sha256:083649cca6e0a8a149af87c666c438f81458b49ce91884427b4d80c642774da2`  
		Last Modified: Wed, 01 Oct 2025 21:46:12 GMT  
		Size: 7.4 MB (7416633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f89e7c3edfdc32597cfca8b4f13cd49f3b2f3fe7cf82b8289c9cb1e1cd6ba0b`  
		Last Modified: Wed, 01 Oct 2025 21:46:13 GMT  
		Size: 16.5 KB (16457 bytes)  
		MIME: application/vnd.in-toto+json
