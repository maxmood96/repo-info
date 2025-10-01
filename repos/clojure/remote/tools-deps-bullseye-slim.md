## `clojure:tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:0f0a897bec552f63c250138cdab4296fd2bc6a93872c56ebd6604bf97713d06f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3ac5de14e1f8addfea0d028dbb9f1e7da3223021a555d7aee5030449939e946e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181446219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6393f0e00e0d68293be9802ae97b8c447ac4e32dfc6b601dae00a03e49319fa4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
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
	-	`sha256:4eb1dd59a73886acc6a3cc9d4c8f8e66d1fd6ba6d6195b05ce21c22b0658aab8`  
		Last Modified: Mon, 29 Sep 2025 23:35:18 GMT  
		Size: 30.3 MB (30258363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc542c61f1dd0ffdd82be9c2c1596a358546e706a6b3093c367babdb2029b8b`  
		Last Modified: Tue, 30 Sep 2025 00:57:35 GMT  
		Size: 92.0 MB (92036028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8260af35ede8ee5ba92f6be10a68e39862a78dff11528b2bf03ab24acf2d5066`  
		Last Modified: Tue, 30 Sep 2025 00:57:30 GMT  
		Size: 59.2 MB (59150786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c4f3410c5f97f6f1a94a7323277a45214c1ba457221cdd967f0fbd54348c15a`  
		Last Modified: Tue, 30 Sep 2025 00:57:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016bb9dd14afe9584848cfa4428676c35ff59904746034c8fdd1ac66a105cb46`  
		Last Modified: Tue, 30 Sep 2025 00:57:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:79f529f820d95357802a625c873b1c723bd13262f0cb00f8df2b4ac6a76a5c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7613b2af95b0916f1b359a071dc3ed05393a23a22c28d021f7f15be6cd1313ca`

```dockerfile
```

-	Layers:
	-	`sha256:38e286ec9cf4f28ae8e8b89dc1116356fc0b3c7641605c4f08f897854cb14247`  
		Last Modified: Wed, 01 Oct 2025 15:42:55 GMT  
		Size: 5.3 MB (5259413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5ed107f0b971f84424cdc27fe031d15aa0efce9887ca555af56edd02258a033`  
		Last Modified: Wed, 01 Oct 2025 15:42:56 GMT  
		Size: 16.6 KB (16568 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bca2fa77c1be23d24f87e7c55b34bf0c6dd4d7ffef18ddfb9bf6f2a808f1b21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179082910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986aa85d20964b79967d11e9befd76a8083b32461708e8de9c5047484029b408`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
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
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8512b4d19483aff21cf861d6f0d787b18e6372c56144a87d5cf28fc22e3e95`  
		Last Modified: Fri, 26 Sep 2025 17:57:11 GMT  
		Size: 91.0 MB (91045231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ce619ab4f3ddb1cf7005731fc7f67cdda15bc18c1468d34891e1cf275cbc7c`  
		Last Modified: Fri, 26 Sep 2025 17:57:11 GMT  
		Size: 59.3 MB (59286181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a963c81ea1a424a8b794397f830df3c96abc0983077a261a9acf623033d6ce`  
		Last Modified: Fri, 26 Sep 2025 17:56:59 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb12b37b5f1f02777a785af88652d11c2aab5d25f0b542cf5d4b6af2f206c41`  
		Last Modified: Fri, 26 Sep 2025 17:56:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1a00d2a0932c9e990c62086fc41d27ea853258c22b5b6faa904512f294806b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559dafbdc567374fb6f3e07f8d2003c7f169aa6b8604473a0b608f849ef54444`

```dockerfile
```

-	Layers:
	-	`sha256:4d0ff9cfae2efbe5f850d20cc6720947adab736906be982a6611abc8afb7f1cb`  
		Last Modified: Fri, 26 Sep 2025 18:44:12 GMT  
		Size: 5.3 MB (5265166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5130dc6120c454f9daace4a46ef0a135177547e4238b9d02c45c8130eac7a18a`  
		Last Modified: Fri, 26 Sep 2025 18:44:13 GMT  
		Size: 16.7 KB (16710 bytes)  
		MIME: application/vnd.in-toto+json
