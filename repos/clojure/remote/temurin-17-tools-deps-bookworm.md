## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:bed6ac187a805da07fc2864973788810f436153d548c381d64e88a01d42245f1
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

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:7d543bf8aeaf1c5c85a1870b2346410de7028cd19d1d4f902634506ce51955b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274321931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08916dd71ff14638b26b76a059ffbce15d77367a19c085247f0b9d303591fdff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:54:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:54:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:54:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:54:50 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:54:50 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:55:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:55:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:55:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:55:05 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:55:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5832d65904243398aad345596edbc0bc26466b9736ff159b5ec0b8c634ea308f`  
		Last Modified: Tue, 04 Nov 2025 11:56:57 GMT  
		Size: 144.7 MB (144693306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fdc900bde6396af36dc30e3e3971a0ef479fae248cc521b403134de8529406`  
		Last Modified: Tue, 04 Nov 2025 00:55:45 GMT  
		Size: 81.1 MB (81146530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81680e41985f0e506fea4c3ee1423593606634cd2da2a4b9f4611ec8fe3b7aad`  
		Last Modified: Tue, 04 Nov 2025 00:55:34 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4e2ccd34c02ff8727d568efdae6d085199a9a89a0cdc61a31857cbbe52ffef`  
		Last Modified: Tue, 04 Nov 2025 00:55:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:cf947e98256e8526379986d4871150aa301c9f4ae48073ea5e47c14c76b54e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7390668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d6f6e2d5e63b103d4ba1e66a44937508cbbfd55aa4948dadd87c64e06d4d02`

```dockerfile
```

-	Layers:
	-	`sha256:7e2358b27eb923dbb4d00861e8d9a076bc24df091e477e7868b7ef007f686dc1`  
		Last Modified: Tue, 04 Nov 2025 10:38:57 GMT  
		Size: 7.4 MB (7374890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f124b9a45a10e399e93b695ebf34b9398e2a9f7669c8f08d935ad1eec1de49a`  
		Last Modified: Tue, 04 Nov 2025 10:38:58 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e2ba5195763dae7de5e89ce2e18ea238f6747674b82128229eeaa5b9477d2066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.9 MB (272933451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d468e16c56a329f72d1f31173584b40e73f0c5a09d1f9c3b0f20fb67486b23`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:55:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:55:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:55:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:55:46 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:55:46 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:56:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:56:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:56:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:56:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:56:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b2e9b8eafc9ba1492756016746b37c25b6922c8d0c4f599d1b45073e9208e8`  
		Last Modified: Wed, 05 Nov 2025 08:02:45 GMT  
		Size: 143.5 MB (143542093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42083b40210a6b82a97ef2c350b083cb75afd372ad8d0fe2e37c566d3126624`  
		Last Modified: Tue, 04 Nov 2025 00:56:42 GMT  
		Size: 81.0 MB (81030840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3e2b0becf84a94dd9eb0c4747fe3ee07003884883bf59944da6bd6cb583375`  
		Last Modified: Tue, 04 Nov 2025 00:56:30 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77474269849fc6b81db01b01758125f2540f9eadb8ed91426f90b6a44eb2a13b`  
		Last Modified: Tue, 04 Nov 2025 00:56:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6ff40158449b2e23dc572b8ae54124fde8fdc44831860578db570e619ab443d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7396549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d316b6d7f96f11d3282375f1d649123d73a0e7366685237e6c2d6c704a8e4d5d`

```dockerfile
```

-	Layers:
	-	`sha256:b854af020e1d665468a74f7a3c48e7622543182d798aba9af967df5b5882f4de`  
		Last Modified: Tue, 04 Nov 2025 10:39:05 GMT  
		Size: 7.4 MB (7380653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f52b70e8799f85d31ffc6910e1d171cc6e2b37c24324a1acd703e0d73ea52036`  
		Last Modified: Tue, 04 Nov 2025 10:39:06 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:2294fb2f79efc271b8cd6e86742680af4471b9a1138ae6c332b01a247ba1081a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 MB (283687287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18416b082dd6b7a5c99cf9c74a860f902b50cbf7b8dadaab885a676bc7922970`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:49:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:49:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:49:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:49:24 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:49:24 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:51:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:51:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:51:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:51:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:51:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c257dece30c42a17aa7d8816f7bcd89b50ce0a6cd59e500ab2a00137c3cb9e`  
		Last Modified: Tue, 04 Nov 2025 00:50:45 GMT  
		Size: 144.4 MB (144372897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a954d84ea15fa30a6b627eb3c112062f9e9ae2dae5a6f7af53683e37fb57cbf`  
		Last Modified: Tue, 04 Nov 2025 00:53:03 GMT  
		Size: 87.0 MB (86986065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b56958c36e2603d50da52a2fa9a2ca18aa61acb696b4531e165308080f01bc5`  
		Last Modified: Tue, 04 Nov 2025 00:52:51 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20b094eda1824e75fee11c74aa7fd1f7a72a04a90a60d96d35963811d22a10e`  
		Last Modified: Tue, 04 Nov 2025 00:52:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b9d51ebeef1342a274260192bc9d1d642715228128f5a43ea6b37e05592c8eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765eac632604a269f4c09e2bead41a9d8dff1bfba8405a432a2ef598f5125572`

```dockerfile
```

-	Layers:
	-	`sha256:9d7b24792da9f7707247f2ed7cb236268cc066f56af246ada5f23265a767a034`  
		Last Modified: Tue, 04 Nov 2025 10:39:12 GMT  
		Size: 7.4 MB (7380104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfd10afd714520a99cbe8ec658c10dae46a819de40057f7547c56e4d54077eb4`  
		Last Modified: Tue, 04 Nov 2025 10:39:13 GMT  
		Size: 15.0 KB (15025 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:fc011d5bf4aefebc2c0af32eb57a567e92faed2df77d12e57bd2a9334f78dafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261819284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3600d14b786684cb9592e7efed2817f2adfb0e91397dc816c83764e52ff54f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 06:24:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 06:24:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 06:24:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 06:24:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 06:24:20 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 06:27:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 06:27:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 06:27:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 06:27:05 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 06:27:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecd7a018e0c266a5a0e6809aa736e696a3218884910229760148d99332361fb`  
		Last Modified: Tue, 04 Nov 2025 06:25:11 GMT  
		Size: 134.7 MB (134723609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0435e639ea0f3562521d3149d69f8a1be3a5bbadea4d249451406230b0dcd343`  
		Last Modified: Tue, 04 Nov 2025 06:27:50 GMT  
		Size: 80.0 MB (79956541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a00af07be0a129ebeed38f84c7931e590ee83bd6b5000d54abeb246c1997c5`  
		Last Modified: Tue, 04 Nov 2025 06:27:44 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27e984dcef49b9ab79859550a91b4f87add8bdadb7fc08c588820984fcc7a01`  
		Last Modified: Tue, 04 Nov 2025 06:27:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c428d48202fda903992a60cca8b21c6118d6e7b959d3e06226844504bc489da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7381186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c301cb83b59bb9ee342c9a5f1b2de38d49cce7b981fcb94a3206b2730e824d7`

```dockerfile
```

-	Layers:
	-	`sha256:924114491dca886c3b8d8852a6529439f4837e400ae0a727024ac8fa00feb898`  
		Last Modified: Tue, 04 Nov 2025 10:39:20 GMT  
		Size: 7.4 MB (7366209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fadd094223b863faf8a58508df1435d49e15df00b9e3883a0bf23292ece486c`  
		Last Modified: Tue, 04 Nov 2025 10:39:21 GMT  
		Size: 15.0 KB (14977 bytes)  
		MIME: application/vnd.in-toto+json
