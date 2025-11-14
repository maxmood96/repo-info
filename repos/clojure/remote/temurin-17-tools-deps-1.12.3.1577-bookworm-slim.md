## `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm-slim`

```console
$ docker pull clojure@sha256:63f939893ddd711a8ef7b8df13510bc4b89f0ada76edf1b79229e390a4d57f18
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

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm-slim` - linux; amd64

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

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:97f9f75c9616bb0187074dff3c9253a67754bc45501279818fc053d2a8dec4eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241343762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304f8628eeddebd0317fbc476b1fe9966849e0b336af26c3688c4524d6766bec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:54:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:54:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:54:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:54:01 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:54:01 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:55:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:55:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:55:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:55:09 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:55:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad13d2bbd74e011d304ff7750d6f05ff7ca072680cd5f2194a35b57a3ad38263`  
		Last Modified: Fri, 14 Nov 2025 00:54:36 GMT  
		Size: 143.7 MB (143679910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39394462bf6ecc01506d10c94ccbf8e7d71ca922bb3665ba5db097d9c08a17f`  
		Last Modified: Fri, 14 Nov 2025 00:55:41 GMT  
		Size: 69.6 MB (69560433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a8ab84b40a4b9245427a9e7effd9a77dd49ffe00f08af16141b3a7c89db464`  
		Last Modified: Fri, 14 Nov 2025 00:55:32 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bf3103038c4d3aced206342342d9cd24a1c26c2b9c9be13d6a0a843dd7e580`  
		Last Modified: Fri, 14 Nov 2025 00:55:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:104ef05194f80638c2250713eb254d2219d875ffa897a5840575f4a3f19fc847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1daa8105e4528d7399f534fb496d35bb5e3193bd55a0d127005ac4978933c121`

```dockerfile
```

-	Layers:
	-	`sha256:e7df0f51ab7d06f5cf03dee60357f989ffbb02614160948b0d8e6ed2cbf184b6`  
		Last Modified: Fri, 14 Nov 2025 01:44:47 GMT  
		Size: 5.1 MB (5119151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9b7bf8e90a32847fb458ebd748fc35ed62b8388f99b2851795d3b7cf19894b4`  
		Last Modified: Fri, 14 Nov 2025 01:44:48 GMT  
		Size: 15.2 KB (15150 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:7fbacac3ef06b14b8bdb152650a3d09c0ab00577f30f00cecd03f792ea71eafc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252108342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916549d218038584ba5cfb21a21c41b21a5c8a236e94d3c904cc38827ff895a6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 07:00:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 07:00:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 07:00:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 07:00:57 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 07:00:57 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 07:10:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 07:10:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 07:10:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 07:10:01 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 07:10:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b176331cf478c057cf81bcee97bd0229df3da42a81c5204530e734e42ea70f4`  
		Last Modified: Fri, 14 Nov 2025 07:02:08 GMT  
		Size: 144.5 MB (144525224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1615b791d30b85d0b5188fad9bd6cd3ff3f9211c5e3547e64c714d4dd7fbed63`  
		Last Modified: Fri, 14 Nov 2025 07:10:52 GMT  
		Size: 75.5 MB (75513168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cdd72b1194e282db0c82f6eedb9581fa8b88597e8fa5f904d499a8add3a945e`  
		Last Modified: Fri, 14 Nov 2025 07:10:45 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c905305411308bf15c51f4e58e4270d871ed8d706f6a541caf74923fcb43f5ba`  
		Last Modified: Fri, 14 Nov 2025 07:10:45 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9490ed8fe186a8a996205ecee2aa818e1d0473d3e9bcf3f48d2841b946254dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8d4a43008d7a0334f0bdbb8847d4554e173f275a74240acef6dc007c6a29c7`

```dockerfile
```

-	Layers:
	-	`sha256:b811f318a3059ab34c0f229c83dd51d744b3e0df40652dff2205356c4483bc69`  
		Last Modified: Fri, 14 Nov 2025 10:35:48 GMT  
		Size: 5.1 MB (5118548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11d11e72e3dbf6771e96a474ae3f8cd4f7cd184fe24ee090b4a58f4994828d61`  
		Last Modified: Fri, 14 Nov 2025 10:35:48 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm-slim` - linux; s390x

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

### `clojure:temurin-17-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

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
