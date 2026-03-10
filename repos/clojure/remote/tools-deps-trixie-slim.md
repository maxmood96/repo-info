## `clojure:tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:5c88bd4b4cf75ba46a87669c631bebc80fbb91a07393ef89cfd73f49c0230bba
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

### `clojure:tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:fd829a37c6833872889e603ecf5c555a8d7133729253e0ed53d6669edeb3cc09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.1 MB (194050839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41eac7e14bec6214245da776d6eddbf5e36533d25f38eaf80c18fa0dc4b00fd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:36:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:36:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:36:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:36:42 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:36:42 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:36:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:36:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:36:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:36:57 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:36:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b040a31bfbbd8b30e96100245e6836fdd7ebec1f801a5f37e302e1a771056dd9`  
		Last Modified: Mon, 09 Mar 2026 20:37:19 GMT  
		Size: 92.3 MB (92256329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74c6e96857b5436f871f06365b26397595cf53307bee5e348fe1cc01d9c7afa`  
		Last Modified: Mon, 09 Mar 2026 20:37:18 GMT  
		Size: 72.0 MB (72014835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cfc216cdccd39cf2f2980052cdf5db820bdf190817488cc7a318f6a0f78379`  
		Last Modified: Mon, 09 Mar 2026 20:37:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39a007099a649dd8bf3781b08f61da9e28755b6a4220b512515eaf9a25930b6`  
		Last Modified: Mon, 09 Mar 2026 20:37:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3066af90f2670a1fca47af3062ece35862033f04e8294015ea2ac59370663dc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5243643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38a178cb68edfeafabad6087e7fef582ca49e053246bdac43a519d6f8549ef8`

```dockerfile
```

-	Layers:
	-	`sha256:96df13d27b9152db19ea7ba0c89306e7744162fabe1c5a8043d3cbef006e6b00`  
		Last Modified: Mon, 09 Mar 2026 20:37:15 GMT  
		Size: 5.2 MB (5227150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f95680cccbeb7a0c0807b16ae3371c3018d33285ddeff3f7483910f8450cd63`  
		Last Modified: Mon, 09 Mar 2026 20:37:15 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cff388b29ba051c61460da2c7d10cd9a4b78a1963f14d8081da3a84774d14b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193261566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf5dae296c1a2e96643084c7085d202084b44953d596cb65f9539fdb274fde3c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:36:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:36:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:36:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:36:41 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:36:41 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:36:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:36:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:36:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:36:59 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:36:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7457d9723a96ad8cd682a52a0952eabd5a16fa0e241af17eb749c77fcc064f7b`  
		Last Modified: Mon, 09 Mar 2026 20:37:20 GMT  
		Size: 91.3 MB (91288305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a46aa948c0bfdb219664a9bb501dd46e618b5ce83372beb969f252b9129ef34`  
		Last Modified: Mon, 09 Mar 2026 20:37:19 GMT  
		Size: 71.8 MB (71832122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236708136f2650286b2482b2b08e6669914c37451e888278742535c4dc59e04f`  
		Last Modified: Mon, 09 Mar 2026 20:37:16 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622fa9c88b7f4c25bce74a7ce49d44db24ef270ee37065c6a6442bb321fe013e`  
		Last Modified: Mon, 09 Mar 2026 20:37:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e1a6de1656d208813da7e5f74af88c60bcbfa46689e5b858c116d7ffd9ff2d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3498394a9d59149294e5a4dac19822d4c079368b660bd717447c940a4f8bb6bc`

```dockerfile
```

-	Layers:
	-	`sha256:59262ccc275a65a5c735e8cb9c752852254f8db45cf7d768a61569d319cc7fce`  
		Last Modified: Mon, 09 Mar 2026 20:37:17 GMT  
		Size: 5.2 MB (5232940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5464e9b4b7f4e5624c423055e54526bd78d68c8f9d0bf6dd26837c2e3d1a948e`  
		Last Modified: Mon, 09 Mar 2026 20:37:16 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:17ca121728f75302f3b96cf26c1e94d1ca6dc920df7d2cb73248ee772b3b43b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202662508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56485f9163405eb5896c2d5346b46b04fa0e6577ea2a1080452c6042bd242a7f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 21:11:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 21:11:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 21:11:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 21:11:50 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 21:11:51 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 21:12:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 21:12:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 21:12:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 21:12:38 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 21:12:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a150b2575e992e22c7a0c3151954f9f03c2b476a6885828b60eeee36035715e4`  
		Last Modified: Mon, 09 Mar 2026 21:13:32 GMT  
		Size: 91.6 MB (91632868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40197e05387c613270c77afeea73d2ed4866f2eb231a3ab08f483b77edada5e`  
		Last Modified: Mon, 09 Mar 2026 21:13:32 GMT  
		Size: 77.4 MB (77428378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7bb97a4f8d0b4b031fb37280904b617478b853fc80104d0a4569f9826cd0bb1`  
		Last Modified: Mon, 09 Mar 2026 21:13:29 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67cb993baff659e4ef14d3471d68b6e1df6d791b001ee52355f5be7011b57c0`  
		Last Modified: Mon, 09 Mar 2026 21:13:29 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3e1cd7b1051b471b46fcc476dda6d47993bc915192e7b2ad73398bfac552e6b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5231398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51be81c2f1a7f9108106ba7f56ca5d322ee8a2601aa8631a733c4c00856d8e9`

```dockerfile
```

-	Layers:
	-	`sha256:6948324793850ae0434cdc9927ae0e9911cb8a2858edd8ea21591993aec5e65e`  
		Last Modified: Mon, 09 Mar 2026 21:13:29 GMT  
		Size: 5.2 MB (5214845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:686aef4f054e597bafc580267f5e69b7c7d29baf2f71f1dc14ce900f18e5f1cb`  
		Last Modified: Mon, 09 Mar 2026 21:13:28 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:b9ef7e0922214d1f2f52814b7fdb6b333a6ccf93553688c11a654bd391848e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (189950271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a707d180d5eea77c6c002343319273f6071c3c569d4d52b8244ea7046b864fc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 11:46:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 11:46:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 11:46:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 11:46:26 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 04 Mar 2026 11:46:26 GMT
WORKDIR /tmp
# Tue, 10 Mar 2026 02:11:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 10 Mar 2026 02:11:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 10 Mar 2026 02:11:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 10 Mar 2026 02:11:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 10 Mar 2026 02:11:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e473dd55fe7be2200230572f9e970b4d013f0a4eabca3f6f6d67c88b697e1bc`  
		Last Modified: Wed, 04 Mar 2026 11:53:35 GMT  
		Size: 90.8 MB (90773397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72318bd5b63f30bbd9c20ee0dd4d16e84851e608306747b972294cac8c383567`  
		Last Modified: Tue, 10 Mar 2026 02:15:42 GMT  
		Size: 70.9 MB (70899412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4032c84222a0e2a66fad8be39fe94980bab8c6c9bb6924b4073ff3bfc608513`  
		Last Modified: Tue, 10 Mar 2026 02:15:30 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b237321f2edb45daf01c35fa5a8210df6f85e4cea3e904a72311d4c316e08ee`  
		Last Modified: Tue, 10 Mar 2026 02:15:30 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:71e6302de73d43ce860bada2239da1ea6e1e742758e1a1a3a104fbde234b179e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce839e5c7e06f19e0303f15d4e0f2e39c1854154970fd1ae1dc4c4ebbb6711a`

```dockerfile
```

-	Layers:
	-	`sha256:8b49142fb3d56a319d0f6fd095d2a0dd6f64f3c65c25803c9c3323a568ca9951`  
		Last Modified: Tue, 10 Mar 2026 02:15:31 GMT  
		Size: 5.2 MB (5198637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:920b2ffec32c66431dbcc0e969a8a1a908835fef07a0c60cf842918a021fd06c`  
		Last Modified: Tue, 10 Mar 2026 02:15:29 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:237f423dfd0ed603961f4514bb16f94ddd8b5572617104632ca7c6ca65d7eb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191056926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050a6789a9407edd2bcd3855d398b765f98d48e7a2cfb243463b91f45c28d764`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:37:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:37:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:37:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:37:51 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:37:51 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:38:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:38:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:38:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:38:07 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:38:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b4220e4467e5f92bec7764167d60cc3a421bc5cd2f89531c48feec3e93028a`  
		Last Modified: Mon, 09 Mar 2026 20:38:35 GMT  
		Size: 88.2 MB (88233848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2bf6d7a7c9cd1c81c153de5e410b6dd7026f232bd8fd33f5c31d47fd7f3fcc4`  
		Last Modified: Mon, 09 Mar 2026 20:38:35 GMT  
		Size: 73.0 MB (72983856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d6413d629eeff3d59beaf37b5d5b34dadcc57352c24261d6b01328d4275595`  
		Last Modified: Mon, 09 Mar 2026 20:38:33 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0dfd1d6641793f22fea218e5dd9b7689513662544ed9ef9dbbe1529598b9fde`  
		Last Modified: Mon, 09 Mar 2026 20:38:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c0d7d4788837044e6ebeafea00f29aefda33925ea13ee3de3d962f3a8af5904c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d294a1af3909efa47963518f206febd02d0e79091a0f89899e64b73b6769377c`

```dockerfile
```

-	Layers:
	-	`sha256:464cc6ebf929254d67866a47a9b8304cc1f35e51d5fd106e96391755c255b3fc`  
		Last Modified: Mon, 09 Mar 2026 20:38:33 GMT  
		Size: 5.2 MB (5207636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e8498fa6addcdfcd063fd66e772b3814fb35514b03fee215d0a497b0f07cc8e`  
		Last Modified: Mon, 09 Mar 2026 20:38:33 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json
