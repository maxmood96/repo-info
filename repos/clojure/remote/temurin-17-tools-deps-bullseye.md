## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:7dd40f6fb95e36c938eb1e5972f9391b7c359db13245ccdebfe1d1b98c6cc287
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

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
		Last Modified: Thu, 08 May 2025 17:04:45 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f18bc04cb516bdffa01fdb749730143f45a612fe56297c30b7da02b6cdc272d`  
		Last Modified: Fri, 09 May 2025 14:15:44 GMT  
		Size: 144.6 MB (144634952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:828fd18e1dd0760579c78a28cf7a52306e86837b0b3734b8199c0974152d7d48`  
		Last Modified: Fri, 09 May 2025 14:15:39 GMT  
		Size: 69.4 MB (69397116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4b7f184fcfcdf4317bec6bb12b686084712e3fae087a91e0f681ce815667cf`  
		Last Modified: Fri, 09 May 2025 14:15:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bae2095e4f8696a9d6c40fc1b7f1197e5b4d7e45c4a68461a0a1f72072d730f`  
		Last Modified: Fri, 09 May 2025 14:15:37 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

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

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e6e0b4b911003b256b2b3fd4e81911ef270a5a558057afcf5e51e41e01e74cc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.3 MB (265288767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9a6f585ba1e93fd335fb8f71210ee41e0d20da96a8da08b630088646af8426`
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
		Last Modified: Thu, 08 May 2025 17:08:39 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15db720bb6866c9beb74c234152feba8348255939932f31dcad2f9f22ef4c80`  
		Last Modified: Tue, 06 May 2025 00:34:07 GMT  
		Size: 143.5 MB (143512639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76a3c49a5436ce2b5d381debba4cf53e07ecf9fca04db6ee5e32f4ea768cb3b`  
		Last Modified: Tue, 06 May 2025 00:38:25 GMT  
		Size: 69.5 MB (69529107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6011b55e73cfb60cc22b189febe95d68d73e1fa0d09152e3c6d057e6d918226`  
		Last Modified: Tue, 06 May 2025 00:38:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463b5e4a930035499328dc745c48385c4c2ffa47a52bec35eb17a542d7ccb76d`  
		Last Modified: Tue, 06 May 2025 00:38:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d1c37f40a79b3fcaaf493c4632ea7bfb2b252d31118d0d4b82d966a70c7efd31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7227593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60470ed9213f493822629382639960bda8e1277424de6e27a6854865cdb3f58`

```dockerfile
```

-	Layers:
	-	`sha256:575642bd16db110ba38e5dabba3bd39c4a3b3453178163b7a3a12e46351ed60c`  
		Last Modified: Tue, 06 May 2025 00:38:22 GMT  
		Size: 7.2 MB (7211654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5912b974a8f2e209ae474905e68b0564e88d31a6e8757857a6182eb9d95ed19e`  
		Last Modified: Tue, 06 May 2025 00:38:22 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
