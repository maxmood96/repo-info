## `clojure:temurin-17-tools-deps-trixie`

```console
$ docker pull clojure@sha256:181f92249dd68f1aafbd5aa6aa1cfd38306d74bd89fd2bb90a31863da44be6d0
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

### `clojure:temurin-17-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:4d2687eab7ad6dc5ad1a9a8731c957036b0242d4dc7fae72237c08cac9ee9fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.7 MB (279679873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd0c07eb82c9b584790b7f114b615eba4b050fac0472df284c457cc7452b573`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:53:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:53:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:53:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:53:40 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:53:40 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:53:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:53:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:53:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:53:59 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:53:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13edccefeafc02a9a16f3e687f8ab69c34fd626fdd1dcfdc20f983b7451b6e26`  
		Last Modified: Tue, 09 Dec 2025 06:10:58 GMT  
		Size: 144.8 MB (144847979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036d82d8ae769e07058af36a8e17725c768fa813b59a53f65d4e9ea75fb3aa67`  
		Last Modified: Mon, 08 Dec 2025 23:54:36 GMT  
		Size: 85.5 MB (85541335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377bb4c321e2f0af3ac3cccebd738147565a984e2439eeae923f9fc73b898216`  
		Last Modified: Mon, 08 Dec 2025 23:54:30 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770d72510bab132df232a0440ad4e9be0375277481e63db0214a1aa381516eb9`  
		Last Modified: Mon, 08 Dec 2025 23:54:30 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:28a4fdc6f42426b168642cf923bda67b704857223d83475741bae085af707828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ac2edfaa891f0e152f64df9e5909b5a5b3675ddb4b66ae784c8afd74cfc7a6`

```dockerfile
```

-	Layers:
	-	`sha256:6178ef1a3b0816236e57cd2059890ff7d09ad07407db3080e3fae916545812c5`  
		Last Modified: Tue, 09 Dec 2025 04:41:26 GMT  
		Size: 7.5 MB (7466931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b32c2df22202267c728a4528591de6049e8ee93aa4c3b8b43bc9f2395e4648b`  
		Last Modified: Tue, 09 Dec 2025 04:41:27 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7c7173caf9dd63627483dca47d88008032212dc3c8865b8a8c53143cf59a7e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.7 MB (278696282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43066c2126e3969c9b40c2d4fceaea3b875b855bb8652871b07ad237ad0955e0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:01:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:01:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:01:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:01:17 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 00:01:17 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:01:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 00:01:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 00:01:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:01:37 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:01:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cae8fe60f4430c9d322abf44551ff661105f999531466c85ff4254c85a89e9`  
		Last Modified: Tue, 09 Dec 2025 02:47:22 GMT  
		Size: 143.7 MB (143679920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daed49b708af3d740abc78d00c6b23ef9d2d16f68e7088f409bedf992d9b2eec`  
		Last Modified: Tue, 09 Dec 2025 00:02:16 GMT  
		Size: 85.4 MB (85365095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3ea86813da0bc9485e9b891d6f2cdb056001bf365977f8b78886d962259271`  
		Last Modified: Tue, 09 Dec 2025 00:02:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f14727d2840d77d7c53bdaa4ac550f686117f4531fc325d8450c32eb5b4747`  
		Last Modified: Tue, 09 Dec 2025 00:02:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6ca7496c0b89d464f8a21721c6b8f5a521cd1f9f726e3d7aa1e8c7e8e57a4415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a7cbfd5560a06b78a2aa9e3365a2be34274b67f5f9ac1675d5356d0b01b719`

```dockerfile
```

-	Layers:
	-	`sha256:863bfef1a20ad71cdb60fc6efa5ad3b15b2e1b4012468d9936aeab251bb81e8f`  
		Last Modified: Tue, 09 Dec 2025 04:41:34 GMT  
		Size: 7.5 MB (7473961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:844744646590ad482281e11d179668e88ba725c395b1a449748154f7b122c3ce`  
		Last Modified: Tue, 09 Dec 2025 04:41:34 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:e96d6d985cc4ef80f485208a568e7aebb02862e8f2d25bfcf99ab81dce1f504d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288582315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f7b61e0eecab70175f6f74a535fc4949560c998d9c0cabf51721d868fde6a7f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:27:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:27:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:27:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:27:14 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:27:14 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:28:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:28:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:28:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:28:22 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:28:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a185af1bf60cf57d1da0f13bf5f3a56964ffa7635cc2b99d41cd3ba11696aff`  
		Last Modified: Mon, 08 Dec 2025 23:28:59 GMT  
		Size: 144.5 MB (144525284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4e57b3cbe5f5bd8a0d33160842d72c47e302702c19bf89538a6fb77c181fd4`  
		Last Modified: Mon, 08 Dec 2025 23:29:21 GMT  
		Size: 90.9 MB (90947512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba156be138c44064af7798eeb270c824eed663c6bcdde3cd86fc3fd8e2c9e3f`  
		Last Modified: Mon, 08 Dec 2025 23:29:12 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb23fcd44fb5a8d139e5e538cf9ec611d235e7a54ed7b6ac0d2ddecfa1b6efd`  
		Last Modified: Mon, 08 Dec 2025 23:29:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:22e492776b29d3b23d00b4026097f3fa6111a57a391e72555a844222145f7db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2dd7d02d662ddecdbd560827df1ab11372b0a924f20eacb65f24bbf2cbea54`

```dockerfile
```

-	Layers:
	-	`sha256:cbdf3ff17e0f3543bc9158dbff761fb47fc01a353eb20ddb2898c18af3624125`  
		Last Modified: Tue, 09 Dec 2025 01:37:16 GMT  
		Size: 7.5 MB (7471350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d394ac5bd76668f6728c4f56789775287db6b040978090b7ee760ea0f9dd95ee`  
		Last Modified: Tue, 09 Dec 2025 01:37:17 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:07f420a77124437113d5cf094c73593e96f585d9f946caf614291dec94ea70a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274088332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:203cd3a413686e89de16e97a57b38b76c8327a9cfe47952bbcdd1d5674ab33c3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 17:51:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 20 Nov 2025 17:51:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 20 Nov 2025 17:51:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 17:51:25 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Thu, 20 Nov 2025 17:51:25 GMT
WORKDIR /tmp
# Thu, 20 Nov 2025 18:07:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 20 Nov 2025 18:07:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 20 Nov 2025 18:07:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 20 Nov 2025 18:07:24 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 20 Nov 2025 18:07:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ed0507b92b5f6d1bbf086936336ca6e85b2d0afbbaab333064cc752190ce52b9`  
		Last Modified: Tue, 18 Nov 2025 01:45:17 GMT  
		Size: 47.8 MB (47771195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c945a137e71885488da7cf422518c6c6ad2c6a58a7c3ce93e4735ec87fbd338`  
		Last Modified: Thu, 20 Nov 2025 18:04:59 GMT  
		Size: 141.9 MB (141889553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051c30ac1da2498ce7c09ebf1bd8a6acb13765e1d1ff92fa2e5848b61113d187`  
		Last Modified: Thu, 20 Nov 2025 18:12:07 GMT  
		Size: 84.4 MB (84426542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf04e5470279dc2a1aa5777505f008ed2a82ee2dc04081c02e6498ecc3e6f8c`  
		Last Modified: Thu, 20 Nov 2025 18:12:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327d4047439b3c12ffe462a1b334faff84163e3bf6cfc1141181f2bf2539a998`  
		Last Modified: Thu, 20 Nov 2025 18:12:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:381476698a4d2d2193522f225f7af9ba2e8a84bf21a5d051c491489920731b6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7468727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe156463cb159b1eec24b16e588817284a51b1e3c8fca251df39791066fa2266`

```dockerfile
```

-	Layers:
	-	`sha256:ee377d308003b3cc7c9c1a8e20a97ef7884c31aaf99bbb068afa78107cc7e60f`  
		Last Modified: Thu, 20 Nov 2025 19:36:09 GMT  
		Size: 7.5 MB (7452925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a88d08502be1e6e5c62d0317c1894b90e1a8548de594ddaa3bd5ecea8126b243`  
		Last Modified: Thu, 20 Nov 2025 19:36:10 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:8b6d6129090f6ddd2d0f4a92d9c8f5e4d477fef2ca3433f706d2ec02941fd7d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270717305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09bcd0725d8defc549c515a5104aba22571c1f22eb08b7bd7c9cbee2e8eafdf2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 01:28:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:28:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:28:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:28:41 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 01:28:41 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:30:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 01:30:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 01:30:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 01:30:10 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 01:30:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3f8967bef2f6a8ec916f7d3a0d528a6724093176621c5758addeeece50e41dec`  
		Last Modified: Mon, 08 Dec 2025 22:16:15 GMT  
		Size: 49.3 MB (49345908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58adddff6e60525e3e5935f4cb8d230990cc26cb84b97bd2bab8bf590bd0472c`  
		Last Modified: Tue, 09 Dec 2025 01:29:57 GMT  
		Size: 134.9 MB (134859044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eee60338279821fb1c8f51443afd69c5f846363b7fcb247798e714624115f63`  
		Last Modified: Tue, 09 Dec 2025 01:30:52 GMT  
		Size: 86.5 MB (86511314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3a6e6563f32822fee789b7293d9417be1867e6dc315d87112f49333c9111fd`  
		Last Modified: Tue, 09 Dec 2025 01:30:47 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b88d77bd61c581d1f818e15cfe621839a69ab2ae4c4e973f9b46cb7a579ad1`  
		Last Modified: Tue, 09 Dec 2025 01:30:47 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:eefe905f5024ab6276dbec6855d2938e370ced8ff18243e6cec354736644cb68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7478607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d09b358aec9146fcc4257ff93ef3d7cef436f3cf18f2d7384215cfedac5139b`

```dockerfile
```

-	Layers:
	-	`sha256:7b1c1bef10589813a0332dc06e2f7b1f33904b8e482d4df36c432151b70de567`  
		Last Modified: Tue, 09 Dec 2025 04:41:49 GMT  
		Size: 7.5 MB (7462853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef8e65b2417c588d7da8714505384f9efb7833dfeedd5820d3f257a98d5a418d`  
		Last Modified: Tue, 09 Dec 2025 04:41:50 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
