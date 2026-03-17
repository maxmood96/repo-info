## `clojure:tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:af1f1586944e0e2614b3c50c600091a96d0408d4359085db2708b24ba6707a86
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

### `clojure:tools-deps-trixie-slim` - unknown; unknown

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

### `clojure:tools-deps-trixie-slim` - linux; arm64 variant v8

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

### `clojure:tools-deps-trixie-slim` - unknown; unknown

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

### `clojure:tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:6b0233925b1e79b8167321dee47382e042ce5e58282e22c54e7158d022497e5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202656226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32856a47bec76224bbbcf0679a8c61b55fc681ed43d2f11c0f55a57c3d79d629`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 18:46:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:46:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:46:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:46:17 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:46:18 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:51:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:51:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:51:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:51:10 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:51:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210f0f2228872d076d4a64e5b33affbf6841048c0c771e1ab74cea434ead7212`  
		Last Modified: Tue, 17 Mar 2026 18:47:33 GMT  
		Size: 91.6 MB (91632916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31a9b6fbad6cbe437ecc4c4999243aaa8b1e0afb6cfaf91020f48c26e460019`  
		Last Modified: Tue, 17 Mar 2026 18:51:47 GMT  
		Size: 77.4 MB (77429434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96dd93b0c7406116bda93dcfb8fa7a3bbf3584568da5ea6d35befd38ee7c161`  
		Last Modified: Tue, 17 Mar 2026 18:51:43 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4347b9088ac52ed94c1d2d4fd3ae247775049e6350ef2bd0a10cc042fd5c11`  
		Last Modified: Tue, 17 Mar 2026 18:51:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:131ec748e25419ad9888d7953038ac123ff43c61d26e3628eca526d6a882053d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5231472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1447e9d59a271c5dc405d96047a749760c7be0486eb3c243e81bad07568ef842`

```dockerfile
```

-	Layers:
	-	`sha256:ead1844a3b8dfc74706d4585b9f35b75e8ff5e6c62ec92f6c2d399401319853a`  
		Last Modified: Tue, 17 Mar 2026 18:51:43 GMT  
		Size: 5.2 MB (5214919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37f2ea458ed301309656d5402738143204755813bab862908d2b420577eb3b9a`  
		Last Modified: Tue, 17 Mar 2026 18:51:43 GMT  
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
$ docker pull clojure@sha256:c655450a7e2b72e8086dab0fa76fd9d7a0b958ce36760ec3fb3ee94449fd2e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191057672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7168e7c1d4178490aeb29462d1f9de4df56fa74b29c70b8ae98181eb16aababa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 11:44:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:44:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:44:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:44:36 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 11:44:36 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 11:47:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 11:47:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 11:47:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 11:47:22 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 11:47:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb62fc097eaac184da503b941c60f97ec5e455a5301ecef6716aa9c41ac21b33`  
		Last Modified: Tue, 17 Mar 2026 11:46:01 GMT  
		Size: 88.2 MB (88233795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de9d30d050a8d2578e03fc8d8f90189d95fd669dd89db85c2db9c67b62f5ad4`  
		Last Modified: Tue, 17 Mar 2026 11:47:59 GMT  
		Size: 73.0 MB (72987570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5f08d675034796a3e512c334496214c4ca6faa03a7828dbd8e434e1f9aa839`  
		Last Modified: Tue, 17 Mar 2026 11:47:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ea4e10b6ba6453fefe4c4b10e165c9d102fa3f6362361057432e24e2fa9e0b`  
		Last Modified: Tue, 17 Mar 2026 11:47:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fac3846590f6d3aa781923373267ab2533177f60373a09280b404580a795e909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983cf1787367462399b609e5aed5f9bb5e9c3e6eb81ad03adcacd0ae5a5d77d8`

```dockerfile
```

-	Layers:
	-	`sha256:b82f0fafc44726b174b9bed3211441f3f7e8834d2bb0794ac6abf33a879202b3`  
		Last Modified: Tue, 17 Mar 2026 11:47:57 GMT  
		Size: 5.2 MB (5207710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f768ff064bc8fd22166384c0dadc3753236658099cc00c4007fc6bf1234dd34`  
		Last Modified: Tue, 17 Mar 2026 11:47:56 GMT  
		Size: 16.5 KB (16493 bytes)  
		MIME: application/vnd.in-toto+json
