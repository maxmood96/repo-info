## `clojure:temurin-25-tools-deps-1.12.3.1577-trixie`

```console
$ docker pull clojure@sha256:ce771b7f9bb4e1b292b43bd98416d02492ea9df582da1cc337ead0356f4efc3a
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

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:4c669c84519c3220d279e4e9571e6a55c6e0e479fddce37fcf734fa4e00ba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229819930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68fe78864c23b2806f51d3927b016760c5a8fa1d05a6374d52ddaab512d62040`
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
	-	`sha256:f0327c0d19787f0057ea8ce23dc2100ecd313f3ebdc93f7335614ef048938a48`  
		Last Modified: Thu, 02 Oct 2025 13:08:17 GMT  
		Size: 92.0 MB (92036036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0db4511e233681c7764d19259b84d59a23bf0ab17f4bb019886ccc0945d0eb2`  
		Last Modified: Thu, 02 Oct 2025 09:55:03 GMT  
		Size: 88.5 MB (88498228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c9ba517f3546f5395ae123b0ccb2d05088c0f43412dba1c6283556901a508df`  
		Last Modified: Thu, 02 Oct 2025 09:09:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4109a72c822830729d6a8974920f0e18bfb191004ad9ecd7eb0476dbcca7370f`  
		Last Modified: Thu, 02 Oct 2025 09:09:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d51566796ee62aaaa54c92c1d82253f4061d7b47a19c1662154edb65ed019d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17a585445c0937e37e3864f6bb36aaf31f0d2b8ac880bd4b46268675d2528518`

```dockerfile
```

-	Layers:
	-	`sha256:716827cc420d742c50efe5c6394be51e26fd9aa168c39dd10256f903b6ff3a02`  
		Last Modified: Thu, 02 Oct 2025 12:45:39 GMT  
		Size: 7.4 MB (7418217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b300da7bd77bbf9292e789082516957617f0ff279f2ac3e8a34c1e5565f177d3`  
		Last Modified: Thu, 02 Oct 2025 12:45:40 GMT  
		Size: 16.5 KB (16457 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:50b392fb173c41ef295ea81177da7bf9fc6687e213217fa0860d4fe56e0f77db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229385823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6cd3b3f3c23d06c2056c4b948de6995ea4abac01a8d54f8ad0d2ace3e9c5335`
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
	-	`sha256:b8c028b2b2108cd8409d417e0eda1efcb2454ecae68896f94301dfee54401638`  
		Last Modified: Thu, 02 Oct 2025 02:48:20 GMT  
		Size: 91.0 MB (91045286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0913ac11daf6c95529e64022a7265defc32e471d918b0d340677c26e028e6e10`  
		Last Modified: Thu, 02 Oct 2025 02:48:02 GMT  
		Size: 88.7 MB (88690803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1bd56accac022be28e8be903aaab5ae448eb73c4b23b90a9d7cf119598b61d0`  
		Last Modified: Thu, 02 Oct 2025 02:47:56 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8eedac3385e31a48d28e2192438a45a9a9eae32d637e2cd0ea1143c11ef9be`  
		Last Modified: Thu, 02 Oct 2025 02:47:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bad36f4cfaecd1d4794025ea3011e1c7abec6b0b3b08761dbf04723efa1e9e1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac1ea46de22acae28374d4006d13f791f389962f5f48cf92c85d862c977cf75`

```dockerfile
```

-	Layers:
	-	`sha256:533a8094cb9ae1e02ffa0587e3064a44537548ffcd4acb9e9ae6e74df13c3863`  
		Last Modified: Thu, 02 Oct 2025 06:47:46 GMT  
		Size: 7.4 MB (7425268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b2bd08c85a8d3f490beef51f9982285e7674f73692a34912dff9399cbf6d83f`  
		Last Modified: Thu, 02 Oct 2025 06:47:47 GMT  
		Size: 16.6 KB (16600 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:06f5bf8dda2c51a4b8593d7a0bfb2dc952e0d8a00c27754e654a8fdf008a7a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.9 MB (238863625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3ce68bd452022f59a00a9a376c69ed07e5c27716537bea370d12a4ac109ba4`
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
	-	`sha256:26068084d5c0d18ceb5891b6fd4231786726d8ad744810400957e5a91ddb77fc`  
		Last Modified: Thu, 02 Oct 2025 20:36:58 GMT  
		Size: 91.6 MB (91601758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71467a6d07245b31c0eb40aefee7298e6ca1b5ea78e44e930cf023736b74f667`  
		Last Modified: Thu, 02 Oct 2025 09:44:13 GMT  
		Size: 94.2 MB (94151608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03d394bad1b71a3d056ef5856b4c422ade53dc1f89ecb4101484a6a66942543`  
		Last Modified: Thu, 02 Oct 2025 09:44:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41025d47e309196346f935e1818fa741471b70a447e4371806e68a6f105f9c7`  
		Last Modified: Thu, 02 Oct 2025 09:44:07 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4355463c4ef0ba77751bc25176d3c8165c83b3e23438050fa6ea0b0b8a9318e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691ecb78eb58575e16ce7ff0cd310b39baeff8a771ce3632429a487569ddf3b9`

```dockerfile
```

-	Layers:
	-	`sha256:14f455343886a25851bc24c82cc1309bed21535596e114aa1eaa3fe516503367`  
		Last Modified: Thu, 02 Oct 2025 12:45:52 GMT  
		Size: 7.4 MB (7423946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f217cd2b50a670e6135a00ef4899d94c45ce91fc35943d0e987773f903aefc9c`  
		Last Modified: Thu, 02 Oct 2025 12:45:53 GMT  
		Size: 16.5 KB (16518 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:d61c9a2aa777df4704247823a450f423871d76990b166a868e041b4c7a218d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 MB (225572519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48c3298100ea3e805dd4c39f116008271da599071fe2ebde85c613d11d924e67`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
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
	-	`sha256:913254a25f5e448a50a1e74fa50f037e22f85cfe4d6a3c626f4b7405299b7c1b`  
		Last Modified: Tue, 30 Sep 2025 01:03:38 GMT  
		Size: 47.8 MB (47770009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964f0570909b5b1168e8db033d13313402e740c877ecfa3fc939ead46e3f0584`  
		Last Modified: Sat, 04 Oct 2025 15:08:07 GMT  
		Size: 90.8 MB (90752390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b35e41345536e4b39903100ca4cdd3f1cd7acf09e4312b7d1bd2edbe00e350b`  
		Last Modified: Sat, 04 Oct 2025 15:27:29 GMT  
		Size: 87.0 MB (87049079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0487211216114a1f6954e6acfda39f50103b1ffebf9daabf3c33a41ba892926`  
		Last Modified: Sat, 04 Oct 2025 15:27:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ac32d7d681471435a1d1881ed44230a73fa14cec104f93066036b2f34345cc`  
		Last Modified: Sat, 04 Oct 2025 15:27:25 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:92008c106bfe231229294922751bdb06a3db2f5a4bed9f8bb5b5723a25fb33a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7422657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28db29bb06eddeae36b9c6bb627ee5822d542cb22dcae4f5476ecedd03f144fb`

```dockerfile
```

-	Layers:
	-	`sha256:7a07b76996d742927c7fc1d3bc96709946f4c96fce5d5143afffa7e17bee2c80`  
		Last Modified: Sat, 04 Oct 2025 18:36:55 GMT  
		Size: 7.4 MB (7406139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a7e152d4f82a2aa4bce5e3e9159611a2d9e8a86e5b295692d4367e24143de2d`  
		Last Modified: Sat, 04 Oct 2025 18:36:56 GMT  
		Size: 16.5 KB (16518 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:289b9a776834cb9868f225c36ac5fed6e848bca03f3917b95d3431568df6093f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 MB (226684063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6544e1f002257467650a58f2d87759c3f99f4c86fef152c39b03edb239a83d9`
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
	-	`sha256:1c472da08548dcf037f943b616dabad9bb86cbf698dd3af1da4c39e1dc1031b7`  
		Last Modified: Thu, 09 Oct 2025 23:46:04 GMT  
		Size: 88.2 MB (88206430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83036269757bedca8ae87dd13c2e369618f3fd2ed1867c4958e70ab146d3a731`  
		Last Modified: Thu, 09 Oct 2025 23:51:45 GMT  
		Size: 89.1 MB (89125151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca2c9bb8ee0994b08fec82d5fbc151fcfaee47f86b8ab918be05f68ff13a77c`  
		Last Modified: Thu, 09 Oct 2025 23:51:22 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97803e1302231335318fcff0bbf952ab0ffb5a47aeb4b57a7b0d160df90f47a8`  
		Last Modified: Thu, 09 Oct 2025 23:51:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3e6bbf66a2756b999f26e03aa58fa780c302eb5e528b4b36c310727092ccdc0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5228de3b5a12804321d7b7b2a9357aa6e0ba2b3243436fd2c3a12cff3c2384`

```dockerfile
```

-	Layers:
	-	`sha256:83d959366a289e23ced4883c34cc95d6d9c817733a188c0b3df7ab93e04371b9`  
		Last Modified: Fri, 10 Oct 2025 00:40:48 GMT  
		Size: 7.4 MB (7416687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2971deeffbbe67e7927f6cc8b7743c1d0699c305a431237d94a28079d7c7e236`  
		Last Modified: Fri, 10 Oct 2025 00:40:50 GMT  
		Size: 16.5 KB (16457 bytes)  
		MIME: application/vnd.in-toto+json
