## `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye`

```console
$ docker pull clojure@sha256:eb3148d33e1ad850864092e38e739b74cd143461046758a579eaab2bfdedbf1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:6fc03793ae7311dd72780d612d6c63c81805cd99a83058e5149bf9e2f3cc97f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267780847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3695c06fdb3e1c37620bf5833f8e653700c2bc664b65c9b73e31e1dec62cbb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f18bc04cb516bdffa01fdb749730143f45a612fe56297c30b7da02b6cdc272d`  
		Last Modified: Mon, 05 May 2025 17:08:23 GMT  
		Size: 144.6 MB (144634952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828fd18e1dd0760579c78a28cf7a52306e86837b0b3734b8199c0974152d7d48`  
		Last Modified: Mon, 05 May 2025 17:08:21 GMT  
		Size: 69.4 MB (69397116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4b7f184fcfcdf4317bec6bb12b686084712e3fae087a91e0f681ce815667cf`  
		Last Modified: Mon, 05 May 2025 17:08:19 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bae2095e4f8696a9d6c40fc1b7f1197e5b4d7e45c4a68461a0a1f72072d730f`  
		Last Modified: Mon, 05 May 2025 17:08:19 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:013f9e5c2b31dbefa2b863de223c15da5e2e1826d53f0a5a9c003c40d21ef9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7222375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68950a144aec11fad1a8c037fb0ba9d4cd19412dda758dc8dedfbc3348a88b89`

```dockerfile
```

-	Layers:
	-	`sha256:9c58a40191ba959b31d242b5e4ed41993478b4eaa485b9d3155bf4d2ea4ff2e1`  
		Last Modified: Mon, 05 May 2025 17:08:19 GMT  
		Size: 7.2 MB (7206555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01db02764c407f6ac174531809ababe398a2491f7663172fb66b30a8d5576ca0`  
		Last Modified: Mon, 05 May 2025 17:08:18 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:95bd7b7514df67ef1a88d908f0e17097e9d7e1b77875801575d0d217715ebc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.3 MB (265289018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5efbd3c247775a8db9e0215646852eafba3fb42ff0f7493bb9b8371e92d30dd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c441d9b4a0e858b97a1d7c29b1a927fdf6f835e7f9d6713307867ec981319cb`  
		Last Modified: Wed, 30 Apr 2025 01:35:05 GMT  
		Size: 143.5 MB (143512607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a931fdf7ba1225445d2a74248590d09d2ec004e5b3ad55a0a1ac202662015a35`  
		Last Modified: Wed, 30 Apr 2025 01:35:04 GMT  
		Size: 69.5 MB (69529394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8a9e30f5a5a48361248340d469ad25ba73834d2f9298c92ccd9f2bb59bc070`  
		Last Modified: Wed, 30 Apr 2025 01:35:02 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaad5e370a36c0656f41d483ffe67652651b2bccf30cdb84b927b63183a5103e`  
		Last Modified: Wed, 30 Apr 2025 01:35:02 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d50c2c458c9132f5c5bbfef0483ce1c8d7f0bf9f8f9b1dc477b6fbc1a15686fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7227593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461dc1f2cf73e680f5215fe3b783de1a69932084dea0acd714b875b4fb5cff27`

```dockerfile
```

-	Layers:
	-	`sha256:712c07cc0de47655331782ffdbd036271c3c66534911e59182664b591fee142e`  
		Last Modified: Wed, 30 Apr 2025 01:35:02 GMT  
		Size: 7.2 MB (7211654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7e907b0214947770c70394ad2be89880ad5e0ad4aff51449b67c310e83ee2c6`  
		Last Modified: Wed, 30 Apr 2025 01:35:02 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
