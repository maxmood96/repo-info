## `clojure:temurin-17-tools-deps-1.12.2.1565-trixie`

```console
$ docker pull clojure@sha256:2fe25f09069f6ac5fac34a489e33331c631dc534a8674c2c90d61de4ff941bb4
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

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:97fc8750e400658989b68abe6822422b599720f7b5f2c8c6932ebe4c44f80660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279507350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed0139dae685207648c94980b72ce0770dbf40d2639b700aa6b209cbc1ef1c0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a750bd5f3a22be32fc81adf4bce128e32e4537f4514f76b56c4c2655fcef998e`  
		Last Modified: Mon, 08 Sep 2025 21:43:42 GMT  
		Size: 144.7 MB (144693322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83d0588ae3ffad300d34ccd7be4dd3344810645d944b807fa90174c2e6fb7ed`  
		Last Modified: Mon, 08 Sep 2025 21:43:41 GMT  
		Size: 85.5 MB (85533455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3392930615aaabbe55bc7c19aa681c40bdbc3b5b133cf253f0b280c763717309`  
		Last Modified: Mon, 08 Sep 2025 22:59:08 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764cf20fd8d03092ec87f1be961989a2beaed2adec370fcb2a5862d589b08634`  
		Last Modified: Mon, 08 Sep 2025 22:59:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:60e4b23da0fe257a39d0efebf23949ea79bd1d2e1e70a4b77d5e012910a69320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60fbe49bd821c029488852b36931f0a650c1fe7a69039ad21d0027045f78dd0`

```dockerfile
```

-	Layers:
	-	`sha256:fec296178075feff80196c0e8b74b9ad5527c2001d71af9da621e7de12f92c4b`  
		Last Modified: Tue, 09 Sep 2025 00:39:05 GMT  
		Size: 7.5 MB (7466845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:446009ba92eea641d97ff1546a61db8ac7f9a939cb17cc884007d9981c4ea3f9`  
		Last Modified: Tue, 09 Sep 2025 00:39:07 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:49bc38183f9407005d6cf273d5a3240e9aa4634860a568517e826ea41298bda5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278541482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a0b999f617421cf2a094a2ae2cc664179ec04adfc47ecb347b015ddce28fbbd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2381db314bbe96ae60a85f0b322964e8af3f4237176280548e768f1a3e91889`  
		Last Modified: Wed, 03 Sep 2025 07:59:04 GMT  
		Size: 143.5 MB (143542200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d7e7fa9029c7a48099426c818e929a1568f6771c121f08219e65aa1be9b110`  
		Last Modified: Tue, 02 Sep 2025 08:08:16 GMT  
		Size: 85.4 MB (85356637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74178f2c74bcf7a408ea67503e11b6830f4ce426ac4f5d0bd7a73140bd63a389`  
		Last Modified: Tue, 02 Sep 2025 08:08:08 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fd31c2183bbd15ebc43124c95ffcf4749da6fa033791ee56fc8b51c8d2d349`  
		Last Modified: Tue, 02 Sep 2025 08:08:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:de1bea1cb839d19be7c3f033f8daae5bb382e4eb3569eb44605174d342c54ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7485166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30b287e1c516868184e7df29bf3c0b9d96245bc4bf94147b63954be7871c86c2`

```dockerfile
```

-	Layers:
	-	`sha256:05f73d22c4a27f5b062e44ab40b94f9702cc5f107899a8a91c5404b7394d9237`  
		Last Modified: Tue, 02 Sep 2025 09:40:04 GMT  
		Size: 7.5 MB (7469251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16903b2fdd71144e0ce9af9252b3bedf63a0d9bac970393e119757f41448b05f`  
		Last Modified: Tue, 02 Sep 2025 09:40:05 GMT  
		Size: 15.9 KB (15915 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:8c41f0f481f063d8979ff60e3d876b9869d662f17b697a36c42f152a57a012ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288419046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae093f17a675c9388eec5bffaea3557e436d45dae8575ac25740672f4499487c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c439a99b6ca01e374ea3bed863748e42f80a70a5e99de7c9b05bbcaea58c3032`  
		Last Modified: Fri, 05 Sep 2025 18:48:02 GMT  
		Size: 144.4 MB (144372648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ece5d19519f4dd87993a40f61e01b757b64ed729b8cdc9faa291a16a26af44`  
		Last Modified: Tue, 02 Sep 2025 08:48:26 GMT  
		Size: 90.9 MB (90941971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5afba458b1dbb43d788d63ffd5e7287e1fba88db00cb9950cb81548a9f27f7`  
		Last Modified: Tue, 02 Sep 2025 08:48:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0dfcbb3e27ccb1f8f4994ceb6510d55fdadb3c138987c7b1abb5641bbb192c`  
		Last Modified: Tue, 02 Sep 2025 08:48:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bdc34354dd4ae8ea1613b1a12c10d617f1ebc52e8cfba3077787e62e83b826a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a884b54a5002520e233ebc80315e5063174e9c3b92ccf21e7228abf5cff5d14c`

```dockerfile
```

-	Layers:
	-	`sha256:e511073b7fc41b48df398b75df55ce61985b1aae0e74cc34cbd5d8ad6c6a80df`  
		Last Modified: Tue, 02 Sep 2025 09:40:11 GMT  
		Size: 7.5 MB (7466640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58618e7ac18b847d3fd8129ccf6dc1923e9e908ba4c07e19c716c0f3d33c48ad`  
		Last Modified: Tue, 02 Sep 2025 09:40:12 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:c3caa68630fbe6635b0acc71dc7e1a7fd70cf24615480e8ce5fa1c2d7163a048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.8 MB (270766051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9780c194bcdf56fddf2d852f6e981bc7a0ab01c2a54aa1d58a46eea64cc0051b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:59f3e0adb655cb03f7d489f3cc57e302e249916bbb076c78008f9329238bfb20`  
		Last Modified: Wed, 13 Aug 2025 01:13:55 GMT  
		Size: 47.8 MB (47764303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5c25397d5f3d90fdd1dc2525d97daa82e52a3648f958399f9a8e669a7c93a3`  
		Last Modified: Fri, 05 Sep 2025 18:47:53 GMT  
		Size: 138.6 MB (138575697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc15d01dab5dc8600fd3c90c364a19a545ef6f3a135e1e7328cd558451826a33`  
		Last Modified: Fri, 05 Sep 2025 18:26:32 GMT  
		Size: 84.4 MB (84425005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40dff4b0c2ffb768155fa536333d03a194f33e424ef4215d914dad2a3065e96e`  
		Last Modified: Fri, 05 Sep 2025 18:26:15 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816904286bfbcb70f7c40ceb80ea4f63c7a93487c7b5e7f794b47defcca6b36d`  
		Last Modified: Fri, 05 Sep 2025 18:26:16 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:47e5ff3be489888741852f8dc9e0334714fe102524a6f7c6e0f78dc87cce578b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7464060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef3621e1f0c9d31bfc1c9ee0696cee14bb28ae5cbeae7b3ddada1a0aa720ef6`

```dockerfile
```

-	Layers:
	-	`sha256:291ea69c79f432a4f493996b9c092ab3fa62ffe762fbd9fef080428b05955a3c`  
		Last Modified: Fri, 05 Sep 2025 21:36:10 GMT  
		Size: 7.4 MB (7448215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eabebb77a9e5218c54981fb0cf4e7d97dcd69f86e63c7607ec926117581cbfc1`  
		Last Modified: Fri, 05 Sep 2025 21:36:11 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:edfc6a1f3c76a1e19a641dcda86e2d1f9502349c673ce85d5f41d3740f238998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.6 MB (270568919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d009ae41a224cdc4661b295a05131399231a2d15ad08de9669c11579bcdd32f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ad91519ab3afcb86eb1e7437e5a1429cf6a5c21c2087fabcb2a282473cb2bb`  
		Last Modified: Tue, 02 Sep 2025 02:00:44 GMT  
		Size: 134.7 MB (134724230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a50a94b3529eed0f0d1bb0d95341ab15278de3ba16c625aa9fa5f14ff8afeac`  
		Last Modified: Tue, 02 Sep 2025 02:07:03 GMT  
		Size: 86.5 MB (86498487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1bb02e452edd1a0cf7ebcee35daa1d4e2328d3e04522bd49021ad30bf3c65e`  
		Last Modified: Tue, 02 Sep 2025 02:06:53 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15ef4d8f091bc6400ea52459d5a0ffc0d20fdb8e8a3aa4ef249862d512f150f`  
		Last Modified: Tue, 02 Sep 2025 02:06:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.2.1565-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:812136c17b083d67603110a43e95c2a84743b554f5a1b3222c4ae48f713e1f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7473940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f31ac29a399b9d64f5764f9cd6e7c50ef4cdd79bbb25cbad7f45540f67eedb`

```dockerfile
```

-	Layers:
	-	`sha256:d1d976376a55dc2494ece5175d3de6fdaa64a2390c3df1d99f9578061d5f37de`  
		Last Modified: Tue, 02 Sep 2025 03:40:38 GMT  
		Size: 7.5 MB (7458143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d674c518e42b3e10efedb29e012f038f90fb354faae2104357a284662ff94d2`  
		Last Modified: Tue, 02 Sep 2025 03:40:40 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json
