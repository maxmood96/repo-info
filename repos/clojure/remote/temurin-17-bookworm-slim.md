## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:8ec7318b68f1173022f57276d77e1af3268438543be385f5bfb77dfea514470b
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

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1b549b2114a96974fcb877c7b0bb9fc10c5f433a45d0792598290f105a984151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242756916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e50c83c6fd4a17cfd4248a736d9ad8336f33ba02e3dba32cd06645f532a159`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:53:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:53:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:53:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:53:01 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:53:01 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:53:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:53:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:53:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:53:14 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:53:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f1bde766c0f53226a997ec3e31033ec25f005cefe6fdc26cbef5bbf5614dc3`  
		Last Modified: Fri, 14 Nov 2025 03:12:27 GMT  
		Size: 144.8 MB (144847974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623ca35256b5b66282f306bc76d231feed54d8f563b48893cf95b7378bc13d47`  
		Last Modified: Fri, 14 Nov 2025 01:31:45 GMT  
		Size: 69.7 MB (69679334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db66af2f31065fc19f8992092ec5fc2e9e0f15e01f5a9a6f48050db018e588d`  
		Last Modified: Fri, 14 Nov 2025 01:31:33 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e983edafb42288bf705267b2a823d326707b83d085c5148ee3b0e008fb5bf8b`  
		Last Modified: Fri, 14 Nov 2025 01:31:33 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:024a8be9944bb4063d1d978cf0a8a11d34e2a7fcaf0328252c28432d777904bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5129226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0bf8cdd49e8660c64df5ae12e81a9cdd265029ba55eb132c78c11c3fb65cb8`

```dockerfile
```

-	Layers:
	-	`sha256:89098ad7d7dc190e13665ad4d449583220496aa7f5bd33fb9f6ad98802028707`  
		Last Modified: Fri, 14 Nov 2025 01:38:50 GMT  
		Size: 5.1 MB (5113390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11259cf5239c4c53316da0663b88714da9317fb941ff2d16988f011b3a8de3b3`  
		Last Modified: Fri, 14 Nov 2025 01:38:51 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6e605c0f7efcb07d3ec86e0195d4d58aa6694acac19951bbdaa7a7df81dca165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241343850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2217f9bf6393436972dba8a9d03bcbd7f453f62bd04551bc4cc5dff3e64d46dc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:42:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:42:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:42:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:42:26 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:42:26 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:42:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:42:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:42:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:42:41 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:42:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b4a8cf669b443f60fea528c8903ef54f42cc746d80ce9f8604361f417c6429`  
		Last Modified: Sun, 09 Nov 2025 08:52:15 GMT  
		Size: 143.7 MB (143680023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e1846730ff64a1d9b83d4fe5f25d2fc9b6b8d61724b039fa6fabfda7870bda`  
		Last Modified: Sat, 08 Nov 2025 18:43:33 GMT  
		Size: 69.6 MB (69560410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efd8d041f5e4a0d2e3da752a35034635bb577c2de84794b828ef342369a2219`  
		Last Modified: Sat, 08 Nov 2025 18:43:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dfacf23e367ea092af39b2d81ebf7300ebb4672c87a3bda560704b629e6524`  
		Last Modified: Sat, 08 Nov 2025 18:43:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7f4d6b82704591a80c0afb56ef3cd36703711e1bc919e305c00dcf62d925e838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd9c930df978c968514023577106b01f04061a16ff12bdc2e1ca48ce6617cc1`

```dockerfile
```

-	Layers:
	-	`sha256:3ec30c76dae23a7e183c8b20fc6de070a8a44b6660072f7a880ef50ccbdc2920`  
		Last Modified: Sat, 08 Nov 2025 19:35:31 GMT  
		Size: 5.1 MB (5119151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ed2f2c7b1c7119a8f21fb24431253461860635b01e97c55e8b4622711e1e44f`  
		Last Modified: Sat, 08 Nov 2025 19:35:31 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:45de003315e579995de03b2e7e702cc1c114496ab964bf6cac87dc26b1ff28ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252108597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50549e025761d9904d5dbe636ff0db97c6c60681f2d684c52e94d0c4b5095627`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 21:14:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:14:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:14:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:14:55 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 21:14:55 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:23:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 21:23:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 21:23:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:23:30 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:23:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cc3022c7410c457d51287dbb7e81e407dc7badac69c919f9c8b9350ee668d2`  
		Last Modified: Sat, 08 Nov 2025 21:16:18 GMT  
		Size: 144.5 MB (144525137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e3369a986ff7cdca76c5943addc82fde6683645fd44512cc6faa039da737b1`  
		Last Modified: Sat, 08 Nov 2025 21:24:19 GMT  
		Size: 75.5 MB (75513514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa5da15b25fff94598f774842fd7c4e8c4848b4272cdd92973a50484244a03d`  
		Last Modified: Sat, 08 Nov 2025 21:24:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec5efcc9e610cad5f8af2cf287a4abbfde32dcfcd4be6900700ae24bbc3e457`  
		Last Modified: Sat, 08 Nov 2025 21:24:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4636c6554449486dae84992fe75dd1c5da3e094e1fd7f6ab9e7edccb8165e80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4396e685bc0ef987dc0adeed1a308af78e6a7c194110413528b856c4ad5e68`

```dockerfile
```

-	Layers:
	-	`sha256:f46f3cccd4714b0bf8ed8e06f659dfa5beb9a14c5247d390a0ccb8b062e5fda3`  
		Last Modified: Sat, 08 Nov 2025 22:41:17 GMT  
		Size: 5.1 MB (5118548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10b203d12e63d848e32eb8f8bdb99905192e22732d46de23aa4977056b8a5e9b`  
		Last Modified: Sat, 08 Nov 2025 22:41:18 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:fe510506424c2ebe7ef2be121bc39a26a5a4de7b8e5196c7abf38f4a6917d5cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230235514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ecf1482988434b151399a9e22529ae5d9236994bd4e894303d58daad487be1e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:55:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:55:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:55:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:55:27 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:55:27 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:57:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:57:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:57:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:57:40 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:57:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ce5e7df93c7febf25e35259674232a1818f8d088f849e2c5e02b3f099c63d8`  
		Last Modified: Fri, 14 Nov 2025 00:56:03 GMT  
		Size: 134.9 MB (134859063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41645870067fb0d8d14c361ea2f784dfdd85d65b31cb5c16e135ecc15496335a`  
		Last Modified: Fri, 14 Nov 2025 00:58:14 GMT  
		Size: 68.5 MB (68490857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c530424035169c703ddc341d9e6f7d33d492ee87469c71f9d593549df1f62c`  
		Last Modified: Fri, 14 Nov 2025 00:58:06 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa20d2381caca1079bef2c0cf85e91f43e16c6d0ff0963180a1d7edfdba9e9b`  
		Last Modified: Fri, 14 Nov 2025 00:58:06 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:691ac5fe98ec9a210128ba0b0a4c425ea5783c1361637add43fe52fd224d2807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5120547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f1309834b43f21836df89b6ad4b04da01afb91542e63da516df33b083eb988`

```dockerfile
```

-	Layers:
	-	`sha256:0169e6b3ce88d758dad1ae2e88c3b8924ddca370dfde0675541ca1f5894d8ff5`  
		Last Modified: Fri, 14 Nov 2025 01:39:06 GMT  
		Size: 5.1 MB (5104711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:940749e38eac08bdfbadba87b9067664b109486ec32e1f566a3bc4ca30cc7107`  
		Last Modified: Fri, 14 Nov 2025 01:39:07 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
