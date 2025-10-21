## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:9bd897233a15944b2578b84211d322a55b4b964cf7d304a2517d509c1af1824f
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
$ docker pull clojure@sha256:23638617afbdb6e02d8c3151014122dc22676c6fa895debc9f3da11d7b3b5b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274322461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ce609e0f54fd4f8251729274fc438b15f1517640e6fb104911e154036af54b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:cd01849e3cbdfc6993640303768edbb56372cf9f1ae101d516334c8d462341af`  
		Last Modified: Tue, 21 Oct 2025 00:19:25 GMT  
		Size: 48.5 MB (48480563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e09517f7b7f9525f3793683237f40225ca02dc670753822771ddb77b8c1219c`  
		Last Modified: Tue, 21 Oct 2025 11:45:54 GMT  
		Size: 144.7 MB (144693290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7582d161f763ff16ee002dcd368bdd25c0631fa84297f72fb480c71c66e79cda`  
		Last Modified: Tue, 21 Oct 2025 11:45:50 GMT  
		Size: 81.1 MB (81147568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a7c0e00d17b17e02805fdaccfdb91cc4013c96e3dd339660e2713a69c79a80`  
		Last Modified: Tue, 21 Oct 2025 02:22:15 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb13f0c562eee5c6cc18e13108db8b94878cb153c4dea8830eb1c13b9edaeac3`  
		Last Modified: Tue, 21 Oct 2025 02:22:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9a9b0fb625d828bf41088a91fec76eb7b14ad54da174c9e2fba0d8726cd5b637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7390710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8fd4d9f54c030ae39846dafdaead4b6056f4f3e881e60cc5758a9ef6872f55f`

```dockerfile
```

-	Layers:
	-	`sha256:2e4aeecea833f5dd60769f38c6a9498cffe482fab20ca7fa87930e9aacdbebb5`  
		Last Modified: Tue, 21 Oct 2025 09:38:18 GMT  
		Size: 7.4 MB (7374890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:073bb91b9e2511fffea5f8fdd62308f7b43f48fcd09031576483276466b63f44`  
		Last Modified: Tue, 21 Oct 2025 09:38:18 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:85757da2782828dea325a22890befbc15fd144f8eb2d57476b24c0075c67f9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.9 MB (272930890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29294e3628df424ced7b1841de59e8c049d87b895cd1571292ddd373927d859`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d93f0bbe5063ddbd91732e12245b9dbe969a4a9c250209c056f5a33ebd508c`  
		Last Modified: Tue, 21 Oct 2025 02:27:41 GMT  
		Size: 143.5 MB (143542157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16bd8ea53aff842c787c0c88d182b949865d24b1347d5177fd7c5d2214f8a37`  
		Last Modified: Tue, 21 Oct 2025 02:27:40 GMT  
		Size: 81.0 MB (81028695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186ab1b76837bb5df85dc09a6f35a7d9815606cf05308a49e3a3a4e2727197fe`  
		Last Modified: Tue, 21 Oct 2025 02:27:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fe235b37f306ddbdd38d8c87e599a17108b54e220c5c558ea94f31f1e10308`  
		Last Modified: Tue, 21 Oct 2025 02:27:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f7e2f711aaa2ca92b88d18232ea197df7f1f01dd551057a0187929abc6e7fb29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7396592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8addb3cbf698bc6151ff8d3d7db37bbab372fc5d3898e7c9b45c29838f3580`

```dockerfile
```

-	Layers:
	-	`sha256:c04835b1a56404286598cb9a2b0acac83e2500039c09e1dba5f7e179a2f84729`  
		Last Modified: Tue, 21 Oct 2025 09:38:25 GMT  
		Size: 7.4 MB (7380653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f805ea299ab4eed686e7aa2192b6c70f9c7702acecd8c789f76b612713849d40`  
		Last Modified: Tue, 21 Oct 2025 09:38:26 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:df506dd92b82479529396dac49a3d4fc84cadf044388c4c7394a0c71f4ee86ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 MB (283686316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8dde72f7e34c9c4bfa398ab3c033cab5df07d0c5a817b911df19750a0eb6f94`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
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
	-	`sha256:812b25f785969d275d8c3962568c03f83ccc4df31b95f01c0646d79d6d5069f3`  
		Last Modified: Mon, 29 Sep 2025 23:33:30 GMT  
		Size: 52.3 MB (52326764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003e75ea4489e91030cf1e37f530c1fe9cc693e3ab296c65e9adb60b605fc10f`  
		Last Modified: Fri, 10 Oct 2025 05:15:59 GMT  
		Size: 144.4 MB (144372895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd14004106c6ebf3b8e6b9e3ee627103fc849a673f020136fc44b854ef376ee0`  
		Last Modified: Fri, 10 Oct 2025 05:25:23 GMT  
		Size: 87.0 MB (86985616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd25e7f98f2062018156e49bd6da1bd1b781a40f17dcb8163818620ab3429908`  
		Last Modified: Fri, 10 Oct 2025 05:25:00 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb827d628afe12ce8120790a435b8abd9cc92b16c0b8ed88b6b5dc123494e70d`  
		Last Modified: Fri, 10 Oct 2025 05:25:00 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:52a5201e922826fbab9bbef92c5b81bec9422b1d3ae3038873423e43df55ac29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:641e1d2eadd903ea5e97f46f6b94558f60f4a97773bdac795a18ef13c62a8617`

```dockerfile
```

-	Layers:
	-	`sha256:91295869b8745d3628ef339249e6bd0ad9b8c1c2a53bed81118b9d63122643fd`  
		Last Modified: Fri, 10 Oct 2025 06:39:50 GMT  
		Size: 7.4 MB (7380104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d7c805831dd009b7ef63492a71835bf0cef7ca6e1145c2e8d1f637533344214`  
		Last Modified: Fri, 10 Oct 2025 06:39:51 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:fa892e42e8101d9f9961b6a8681a89aa325ec7f15adffc8439dfd49109e2e6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261818655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acede584f06e6ce66a23a3f53001c78d92df1db6e1d7d5261e351293e6ef3dc9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
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
	-	`sha256:87d1bec83b35277b636c6e05b9418301b2f025752d7539cecae442f0b94d8fbe`  
		Last Modified: Mon, 29 Sep 2025 23:33:26 GMT  
		Size: 47.1 MB (47137446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3afa8bb81ce30bcf13eb0db5dbd6d2b5add61080756bc490e8e5412b5d8260`  
		Last Modified: Thu, 09 Oct 2025 23:08:30 GMT  
		Size: 134.7 MB (134723624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30aa8c44b70e05464954399a13069cc93c9310bd31a40a0e50376ea20db89174`  
		Last Modified: Thu, 09 Oct 2025 23:14:21 GMT  
		Size: 80.0 MB (79956545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54a9b659d7b6b86fb1a86d7a709880f72dc18d00a87406a7ad8ccc05f087491`  
		Last Modified: Thu, 09 Oct 2025 23:14:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668704c839bb49aa0df365047ddef5c2467945903c874806c774cf0f41c15244`  
		Last Modified: Thu, 09 Oct 2025 23:14:13 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1ce04a443e15874923b448dde2edbec12cacc9d4ea00258799262767e0d10efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7382030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea6a3f8492569151287ec59a26407862e08d4607a6ade807be5ba7f3f88e070`

```dockerfile
```

-	Layers:
	-	`sha256:97de74b909dbc06e400809c6cd0bb4e6c6a4f4f80981d2ede6f9b948b6c9e005`  
		Last Modified: Fri, 10 Oct 2025 00:37:11 GMT  
		Size: 7.4 MB (7366209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84ad56b4b0ae2c5847eb87da3652ce00182701e6e185400b2295ba38f52f6217`  
		Last Modified: Fri, 10 Oct 2025 00:37:12 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json
