## `clojure:temurin-21-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:d1b3fc1582563a07af7e642dba41a108f825194e0762353caac5a01782dc5473
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

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:119ac769925c656c00f30cff987ea59ddca9a1d8105f4e0778f76dbc9757096f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259651553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63151b7b0576aa86416dc4c7a7ee278d475d2db8247c700d154197063717de87`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:51:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:51:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:51:06 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:51:06 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:51:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:51:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:51:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:51:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:51:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08768d29397cdccbe051190a7a7a1adc99a4306571a471310e3e71e611517119`  
		Last Modified: Wed, 04 Mar 2026 17:51:46 GMT  
		Size: 157.9 MB (157857123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a48b261b4882c3f839063484838a5b1085862c21bad1bc439db38b513f1733`  
		Last Modified: Wed, 04 Mar 2026 17:51:45 GMT  
		Size: 72.0 MB (72014758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8c6a998c9ab0baff8c4dee947b520a4612ec08431aa6871dc14981beceecee`  
		Last Modified: Wed, 04 Mar 2026 17:51:42 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e9ff3c859a9a442abd1c87a404a46d0fc2127363df0a6242635ae96f8ec112`  
		Last Modified: Wed, 04 Mar 2026 17:51:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:801a0c3e9d465153160503fcc19443e23d99de747e97fcc3908ecf2d23f336ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141bb2795e2d7862cea3ccb9b620746b2f3f774edf27f482c9797e16b09a5014`

```dockerfile
```

-	Layers:
	-	`sha256:e78365248b9a32b2a57ae90f0eee4832273aede7e272a74f8298ef3a8594e171`  
		Last Modified: Wed, 04 Mar 2026 17:51:42 GMT  
		Size: 5.3 MB (5260916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99f8f7a2e38292608ffd4076e3998d9519143dc0233d452bf41baaea60b312ec`  
		Last Modified: Wed, 04 Mar 2026 17:51:41 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7e9dd858a571ef74b93c4c221c0fdf96f9e108fd705a7946da09b8e833688d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258105737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a555acc1b2844ad72df3020d3e5a8a53943422869fd6f9a1bcd681f29d8a083`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:50:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:50:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:50:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:50:37 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:50:37 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:50:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:50:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:50:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:50:55 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:50:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bff89f68d7b43582d381b8485667924cfeb11ea4f48b49e2aca0a328e59adca`  
		Last Modified: Wed, 04 Mar 2026 17:51:18 GMT  
		Size: 156.1 MB (156133092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a70fa945b8c7bed372d558bbb0827be9d06482efa86e7d74202fd89e9a2bcaa`  
		Last Modified: Wed, 04 Mar 2026 17:51:17 GMT  
		Size: 71.8 MB (71831503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6950a33bb33565a37aef88aaa917de92589e4d6ba583374870e5d0b53945c8d7`  
		Last Modified: Wed, 04 Mar 2026 17:51:14 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024f18065e94ab4c32453b2fa72dab8fed8b6a1bf34f19b9ca30156b94df860c`  
		Last Modified: Wed, 04 Mar 2026 17:51:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ecc4ccdccae577f35702c4af3626abe60f99eef6d9882d39f8d6aa4c4738fab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5282615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b5a6759bcd304d8f3459677324de342c36c35b5f65c52d691c1b90a856e67d`

```dockerfile
```

-	Layers:
	-	`sha256:ee57316c2bd6e64dd196516e1baf40d680ddde6062270649dba43be867b8f36d`  
		Last Modified: Wed, 04 Mar 2026 17:51:14 GMT  
		Size: 5.3 MB (5266685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbdeae2c6d821d5838117ab354704a9f1f146461aad0cd093635321543abb4a8`  
		Last Modified: Wed, 04 Mar 2026 17:51:14 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:c07adc39f609dc879bc757a0dd27bef66d1512b726f471e0103caa5f73714bf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (269006634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e3082c2adc74ea73a762ae35fe18dceb51e31f9d8c2de8136a092fa986ea27`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 18:06:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 18:06:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 18:06:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 18:06:44 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 18:06:45 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 18:07:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 18:07:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 18:07:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 18:07:28 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 18:07:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c534f15a04304f264cb04db37f2dbea33095d11e7d16b2cbe673e2e526b194`  
		Last Modified: Wed, 04 Mar 2026 18:08:23 GMT  
		Size: 158.0 MB (157977535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3101f88c7e64d44e9c3b6ada3185f04fdf1f25cc2bcad8ce8350b6087bb48fd6`  
		Last Modified: Wed, 04 Mar 2026 18:08:16 GMT  
		Size: 77.4 MB (77427842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0571c57e0facd3a61c8298f797c077f8ee0e6b70d4bbdb0d90a22084c72c85c1`  
		Last Modified: Wed, 04 Mar 2026 18:08:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca72af86f22ce6a357b98e3dc7141d6271d2544ba1927c80bfcdff0bed845fa`  
		Last Modified: Wed, 04 Mar 2026 18:08:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c24622f60bf94a3dccf866316124f392a72840235ffe08b83911e819ad28f1a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5322a049149da3df37c67141373aebfce01cdbfd64046b9a5f5ce4b17890650`

```dockerfile
```

-	Layers:
	-	`sha256:2b4a3ecfaf1104e6b342320a8aafc68fbe8db3d4deb4db46341bdebc3d5982d6`  
		Last Modified: Wed, 04 Mar 2026 18:08:13 GMT  
		Size: 5.3 MB (5265287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dd96960afc8e50f70ee575a61535ea4a4f45c0644d6cef67d9d1836dcc27f1a`  
		Last Modified: Wed, 04 Mar 2026 18:08:13 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:8c6181b8b4c0c64b3e06d9c4e847060b2c32f2e91a67da9e9c91ba480c42ace0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256388401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc47af090bda1fd404b852225616f9abf95b8a9ef399365261d122d465dcfba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 11:23:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 11:23:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 11:23:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 11:23:46 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Wed, 04 Mar 2026 11:23:47 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 11:26:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 11:26:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 11:26:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 11:26:26 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 11:26:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6f2d4c20cb87ce38553ebd9ee153c1d2ba4124eefd89d1277f7fcbaccfbfa3`  
		Last Modified: Wed, 04 Mar 2026 11:31:31 GMT  
		Size: 157.2 MB (157216904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad88cb8b1373f7463a804959d475aa7ecf8a969ba6cfd3c519094ff9b12a011`  
		Last Modified: Wed, 04 Mar 2026 11:31:18 GMT  
		Size: 70.9 MB (70894038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d93039c3954c23198de3b33f7983ed3a3361732414cdf91f6128fddf293e52`  
		Last Modified: Wed, 04 Mar 2026 11:30:57 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d16d63915d7072749c4d610cd21eb6a76425d3677e36c7805998b160b67a6e7`  
		Last Modified: Wed, 04 Mar 2026 11:30:57 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5ea9156e49e9227ccb7e2cab56ca179911b8da88f9fa652e80b5bf7150f8c78a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5266239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a9c4ac64cf16494c849691975d37adba627fd261cf1a7b5069a3fbae6cdb6e`

```dockerfile
```

-	Layers:
	-	`sha256:e6ab3410c54853b4ffd37ade106d235d87fd9914ba6790076b93e00dea9ec42c`  
		Last Modified: Wed, 04 Mar 2026 11:30:59 GMT  
		Size: 5.3 MB (5250380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da2b634da91e1a6aea02af4911a8cc9afdf955ba3507c64b90083e5f31bb1796`  
		Last Modified: Wed, 04 Mar 2026 11:30:56 GMT  
		Size: 15.9 KB (15859 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:685149ca702459005fbd99ff7e1815414036e2f5aad1910d3edf5dccc4175ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.9 MB (249928012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2450dc0acb54bd529595acb873785ef16d095511d867354acc50e4b8e60d5c8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:51:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:51:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:51:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:51:18 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:51:18 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:51:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:51:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:51:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:51:35 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:51:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c848d82b2242adef918e6bda9566b96791d14b8e2608c5457b13a77893e07525`  
		Last Modified: Wed, 04 Mar 2026 17:52:05 GMT  
		Size: 147.1 MB (147105249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:827daf7e1e483748c978c773fb162c8e74594033497c1f8dc7cf8f444e9bd2ce`  
		Last Modified: Wed, 04 Mar 2026 17:52:03 GMT  
		Size: 73.0 MB (72983543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8833f387a4e7028e475db172f357d52673deb65aafba9efb8bd2e2bd42a577bf`  
		Last Modified: Wed, 04 Mar 2026 17:52:01 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8abc1adfb5acf64ed96c758aaba794f15f1f6d25d324277be891466f9513fe`  
		Last Modified: Wed, 04 Mar 2026 17:52:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dd8d369bd63184defa7fa89bc401b2d4a18817e706b5e10372bc401ed2714216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36db91195f272c89d7b7a17a97a06e8919298e0b41e040cd67a0f032cdefd4dc`

```dockerfile
```

-	Layers:
	-	`sha256:1634cc280bd4abb13726fe0c3924faa37ca0f4fee0e167964211bac93bd967ce`  
		Last Modified: Wed, 04 Mar 2026 17:52:01 GMT  
		Size: 5.3 MB (5256840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef9b0acee4bf05b2b665fda2905e02781f5d5245d4b3d9a24f0374e4480efbd3`  
		Last Modified: Wed, 04 Mar 2026 17:52:01 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
