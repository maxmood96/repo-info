## `clojure:tools-deps-1.12.4.1618-trixie-slim`

```console
$ docker pull clojure@sha256:4edc1deb2346c41f4f488d2c57be889de137271fffe7e3ecda7337d9ae5526d3
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

### `clojure:tools-deps-1.12.4.1618-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0b7d73572c4e58a36b0cf77d985580ffcce20fdeabe4a2f0b5dee6deb69078b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (194045021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef2f096455eecf0f57ff03576bf219ff764806902d70f9a938b0385657a1c77`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:01:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:01:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:01:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:01:37 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:01:37 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:01:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:01:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:01:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:01:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:01:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8be5df6f510a2090a16bb63e839751aae33c9a15f60a7a123f787f5dc26b6607`  
		Last Modified: Tue, 17 Mar 2026 03:02:18 GMT  
		Size: 92.3 MB (92256290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6e6727e2a7d085f6eff7c732c65674a3d07c38a1ca930d320b55465d53ef72`  
		Last Modified: Tue, 17 Mar 2026 03:02:18 GMT  
		Size: 72.0 MB (72012196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad49c11a18097dabc3b1ff7ca9359becc526dce9646e975edf7da6d79407f54`  
		Last Modified: Tue, 17 Mar 2026 03:02:14 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad0296c152faadcadf03439bb488d55b2c746b00cfcd30089e0548333f313b80`  
		Last Modified: Tue, 17 Mar 2026 03:02:14 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:02d5591fbfca08ae44dd64c8b4ccf5ab92d28e728756a102d69360e44342fe53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5243717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cbe7c0842dcae8b97fb65b5bc88e8b8aba817d327d117974e34ee51aa13f2f0`

```dockerfile
```

-	Layers:
	-	`sha256:1adfcb0c48993fc7665be9027ef18d5e801eccc0345820ea2ad3175bf7ddeee6`  
		Last Modified: Tue, 17 Mar 2026 03:02:15 GMT  
		Size: 5.2 MB (5227224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eddfbeb2e72ab2c43971974982e1c635192880c443a493d08a5b67a2cd699f0e`  
		Last Modified: Tue, 17 Mar 2026 03:02:14 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1618-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:748c4558dd875d53dc7b84b5130f99cf77fd949a51cea7ee173e34966340a212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193259318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1022997d82eb0fdd0421c738e92fa92ceee35ee41a93a37bbc7337b2c7540809`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:06:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:06:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:06:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:06:04 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:06:04 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:06:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:06:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:06:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:06:23 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:06:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21354101ca9267107aacb707f22ae6c57d6c6032cf97fa0e1d12bfbb029aba3f`  
		Last Modified: Tue, 17 Mar 2026 03:06:40 GMT  
		Size: 91.3 MB (91288272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc6f4d5ea6a34bbb12a0d2cb31d94409adf8964029bd13924bdba899430bce6`  
		Last Modified: Tue, 17 Mar 2026 03:06:44 GMT  
		Size: 71.8 MB (71831590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4505afb7237359359f2165c38835d82e0876d45a376eca935e78ddc51bee30df`  
		Last Modified: Tue, 17 Mar 2026 03:06:41 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c1be3d40e4577b160d5e8c98c5d8b1d2413e142305dea9bebb8ca9a6db089a`  
		Last Modified: Tue, 17 Mar 2026 03:06:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ee431f85fecd1124b193518d3189217ee90ab75cba9ffd5d9c402110ef079c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c364eec2ac5a3f6b39ad8fe53c98087191dc596dd9692fb21f7abce7e2ad63`

```dockerfile
```

-	Layers:
	-	`sha256:ca0464309c2854fb9036ab4ca40a808105820b7247d12195d6c064181c1babea`  
		Last Modified: Tue, 17 Mar 2026 03:06:41 GMT  
		Size: 5.2 MB (5233014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12414c4f6624874e33163374debd8b96f68b8864a67b1a2a18c63c7101a23965`  
		Last Modified: Tue, 17 Mar 2026 03:06:41 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1618-trixie-slim` - linux; ppc64le

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

### `clojure:tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

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

### `clojure:tools-deps-1.12.4.1618-trixie-slim` - linux; riscv64

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

### `clojure:tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

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

### `clojure:tools-deps-1.12.4.1618-trixie-slim` - linux; s390x

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

### `clojure:tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

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
