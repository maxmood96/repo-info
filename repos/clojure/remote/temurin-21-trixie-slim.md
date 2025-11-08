## `clojure:temurin-21-trixie-slim`

```console
$ docker pull clojure@sha256:71f1e14ed9a38b119a979c5fee24537f3646c545dbe29a27087f88f58669da68
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

### `clojure:temurin-21-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ca6df4ca44fa7513fe23e53e45ff679fb05b4289e34a7bf38eddbcf4fab8ad80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259579120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c9f4447a94367ff1450fd38a3114d10d776373fe4b0b222811b43f6845cce0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:31:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 04:31:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 04:31:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:31:28 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 04:31:28 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 04:31:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 04:31:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 04:31:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 04:31:45 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 04:31:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d4d0a7cd3ee10b34b0a8b1c3a8ca04ddb02e8f80b89719b4a627ad44a5208d`  
		Last Modified: Tue, 04 Nov 2025 14:42:10 GMT  
		Size: 157.8 MB (157804745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c18ee14ecd3a05839343c28f055d725e5d37be59e83bad61b63b2c0f64d9b0`  
		Last Modified: Tue, 04 Nov 2025 04:32:18 GMT  
		Size: 72.0 MB (71995232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87e17d6b387d06aad93e1a6d10b9a00067c4a0c570dfe06eefcc54dad5b71d5`  
		Last Modified: Tue, 04 Nov 2025 04:32:12 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd7199c28dfbb92797b01cd23bd3ad92624d8d14193cb1a620553bb062df220`  
		Last Modified: Tue, 04 Nov 2025 04:32:12 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f233a575becb7c25ca42d97676f293a77b4997920f2f04fc2d5e2372250ee9fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172be8e51af996a7b52c807f04485b1257a540f17c06bb5600d1752329ac49af`

```dockerfile
```

-	Layers:
	-	`sha256:82e5795f86a8ebb69b6e7a8a95973d48773e9fce878188303de26c1bd70e7de0`  
		Last Modified: Tue, 04 Nov 2025 10:44:42 GMT  
		Size: 5.3 MB (5259269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:616bca826ed451bca9c0edf50fabe8516adc48b0c1b159f17908641dfe54b47c`  
		Last Modified: Tue, 04 Nov 2025 10:44:43 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d9ff95856fb1351fbc864283961e0932f48ea7f6a4ee5d414f1a17073f3a0271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (258032915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a499c70da2cd64617735d031bbfd4b0744cd82153b7d7970ebf7d6b47f2dc2b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:45:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 01:45:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 01:45:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:45:18 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 01:45:18 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 01:45:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 01:45:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 01:45:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 01:45:35 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 01:45:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fa134ee7f4812ba368741835d72896b409fc9f20146a933419b76b18d0e213`  
		Last Modified: Tue, 04 Nov 2025 21:26:17 GMT  
		Size: 156.1 MB (156081258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae1a306f4bb7d4cae7ccf4fc04c41f4a7d8e68ea4dbac81a956f77550fed49e`  
		Last Modified: Tue, 04 Nov 2025 01:46:13 GMT  
		Size: 71.8 MB (71808318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b66937b8d33b7f69c434ebdd209e3c7ef45ec804199be8473f4d4f2c05765e`  
		Last Modified: Tue, 04 Nov 2025 01:46:06 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe47517d0e889a4f89692b4b799157f677378139fd7ab9d8767eadee5569038`  
		Last Modified: Tue, 04 Nov 2025 01:46:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ca0a5942802da6206e024359fc383645f2c9c2c2abd9df73dfb44f5ee941dee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89ef9476437db504ac898d9742c80ab9c0932c222482742117f8ea3c78c66b2c`

```dockerfile
```

-	Layers:
	-	`sha256:f2f86a38e2413aa2271386a15d2801d8c894fc346dfa4465eb95ba8a9cf5cc33`  
		Last Modified: Tue, 04 Nov 2025 10:44:48 GMT  
		Size: 5.3 MB (5265038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a31848d7f81c7612f8f6048786b8b938215c40916b7203794dcfedcbe99efab8`  
		Last Modified: Tue, 04 Nov 2025 10:44:48 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:a2fc86412cfe7715c5a48f7b24e3f8939b3c882d8a54f822654b616c397f8d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268959764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fafcd33f398f1ca22fb5051dca9eaa11a8630ad6853c3cb226ea56131da3b73d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 13:37:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 13:37:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 13:37:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 13:37:48 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 13:37:49 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 13:43:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 13:43:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 13:43:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 13:43:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 13:43:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3d0c6128d4f756a06ec237219873ec1f9d836855f6fcb4db16fb4c26521fb5`  
		Last Modified: Tue, 04 Nov 2025 13:39:10 GMT  
		Size: 158.0 MB (157963427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c1a23cc9ffe90cdb485031a25b3c9ccf99949211fe902d8151225304903074`  
		Last Modified: Tue, 04 Nov 2025 13:44:54 GMT  
		Size: 77.4 MB (77396648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b501c48b2bab00cdca1a2b695e674e3dfba299e7ac871e4fa81e35ca047f20f`  
		Last Modified: Tue, 04 Nov 2025 13:44:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0df7c533dc6ebbac92c38d9bad46f38e0c04994940777d2f65117d2d6c17ac6`  
		Last Modified: Tue, 04 Nov 2025 13:44:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eb8b77f2e770d4734f8b3d929544778333c2985bf9e5f123ca2e6d7242153242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5278699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0301dafd96031a9b6904748b9e0a09e8c717673e03e61a733ab4719d18e6b256`

```dockerfile
```

-	Layers:
	-	`sha256:1a9827f171b43ddaeb0724099fd0910aa07d80a2f3008b3df0532a51bfd32ec4`  
		Last Modified: Tue, 04 Nov 2025 16:39:03 GMT  
		Size: 5.3 MB (5263640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e188baf7b2482f1bac7e39ed39bf34c0f468e415680f3e795360713766f7bbc`  
		Last Modified: Tue, 04 Nov 2025 16:39:04 GMT  
		Size: 15.1 KB (15059 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:6884b61a8fd5c3a73c741c3886b1f86bdc4055c056be9be8472a7e70be830da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252751298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc42acf94736c8e267bb6bce70efd69ab391bb1bc4db071e485b7031a3a48763`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Fri, 07 Nov 2025 06:39:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 07 Nov 2025 06:39:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 07 Nov 2025 06:39:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Nov 2025 06:39:40 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 07 Nov 2025 06:39:40 GMT
WORKDIR /tmp
# Fri, 07 Nov 2025 06:56:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 07 Nov 2025 06:56:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 07 Nov 2025 06:56:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 07 Nov 2025 06:56:17 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 07 Nov 2025 06:56:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0db3eb8e5337e5bca5167ab6ffe6048420e62d22a7ed6f5b99c7f187ac58dcc`  
		Last Modified: Fri, 07 Nov 2025 22:59:41 GMT  
		Size: 153.6 MB (153593538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e555eede10e0c425221b8e19e5057570bd96805e48a93881fbdac40f95fd8ef`  
		Last Modified: Fri, 07 Nov 2025 07:00:35 GMT  
		Size: 70.9 MB (70880931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caca660f45d19c599cb9c8f5ff5c377ff1fb4cd0ac94fc29962e9d9fe2825049`  
		Last Modified: Fri, 07 Nov 2025 07:00:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69e7f79a4c1c926c0a0bd1636ac29fe5cfb5a1ef0d454c6382bca7a80c77b1b`  
		Last Modified: Fri, 07 Nov 2025 07:00:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d6d580cf8996268c5638078367ca7481dc65280f97e1c9e3dec7d2f63944309c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3d109245c10f2ca9f13269e4262a149d0ee7865acea7b2dcade33e96cb3adac`

```dockerfile
```

-	Layers:
	-	`sha256:1d8e54c73134b3c34f05b343e2a59e69886aeb8653004b46f34c2c393f6cc594`  
		Last Modified: Fri, 07 Nov 2025 10:37:29 GMT  
		Size: 5.2 MB (5248733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8aa55ce256731d714ee9a7137a80a2fb5cef762c49c4f8da05ffc8614479b47f`  
		Last Modified: Fri, 07 Nov 2025 10:37:29 GMT  
		Size: 15.9 KB (15859 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:21c48f74e07d37f49605663fae568d233dd86741979743d13d120df3b4295169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249819040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c77668243f1ddecf94c5ffd5b779cd8d76f957b9e9e0683359c7d19e2f18618`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 13:05:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 13:05:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 13:05:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 13:05:17 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 13:05:17 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 13:07:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 13:07:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 13:07:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 13:07:32 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 13:07:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f927c5338c86d2d275c7f2548392a5c310c20a64640f3b6cf668ab3f7a79af`  
		Last Modified: Tue, 04 Nov 2025 13:05:56 GMT  
		Size: 147.0 MB (147027017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886c5866fff9b4b53afb07fcb8a18b25fe25b3a6c1095bc109800f595c2ba06b`  
		Last Modified: Tue, 04 Nov 2025 13:08:11 GMT  
		Size: 73.0 MB (72953590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad4b37f4578834f6e13f10b17041babf0039fccd55b1b72f5016f97cd22aaee`  
		Last Modified: Tue, 04 Nov 2025 13:08:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b91c0f36d2bc72fcddc0ab7874aca115d3ecc2babfa343f35168d9502aa76ac`  
		Last Modified: Tue, 04 Nov 2025 13:08:02 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b5f09a7b0e81de7f8821744e8db9df6a74ea1c2144fe7f276e46711b0e6454f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2b26de572576d6c460e91d93fc8e40255e45f53e0b6b0500f43535030ead65`

```dockerfile
```

-	Layers:
	-	`sha256:7988015e77e98e5162977a7410af98330a59673dacd920e3bb39f5b52b3772f6`  
		Last Modified: Tue, 04 Nov 2025 13:37:55 GMT  
		Size: 5.3 MB (5255193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c534f1c0f4db75b33f7e01fda7ef5c18b592faa930cc42551cee4c131df35d90`  
		Last Modified: Tue, 04 Nov 2025 13:37:56 GMT  
		Size: 15.0 KB (15011 bytes)  
		MIME: application/vnd.in-toto+json
