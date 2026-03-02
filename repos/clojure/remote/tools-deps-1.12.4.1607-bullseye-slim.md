## `clojure:tools-deps-1.12.4.1607-bullseye-slim`

```console
$ docker pull clojure@sha256:c13b9089a044a2d89688e8c1ace8914ea44340740e54031b026e7d57c6396a2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.4.1607-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:eb33de99a8807c92c32f7413511367a5a47bc464f5e9ce6e19d55076430e4521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.7 MB (181692705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d881d26193d54e57848f55383e13ffe0c4d605c2cc81b2232f8377f81201932a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Mon, 02 Mar 2026 19:48:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:48:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:48:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:48:21 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:48:21 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:48:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:48:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:48:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:48:35 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:48:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ec107b896bc9df45ae39b8e94d00cb1e94db327661115e92fee8de15e5b507`  
		Last Modified: Mon, 02 Mar 2026 19:48:54 GMT  
		Size: 92.3 MB (92256315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a3a35bf86449c910514b266f76e0454f20eef3ba75c8d2d15602e355541431`  
		Last Modified: Mon, 02 Mar 2026 19:48:54 GMT  
		Size: 59.2 MB (59176967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60534eb52e5fc218db929a76cc43d05894590dba59d7bd91e7e8faf1351714f`  
		Last Modified: Mon, 02 Mar 2026 19:48:51 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e578c436485dc6501f438910d10496822b8a9f513417cfd29cc38542947ed0`  
		Last Modified: Mon, 02 Mar 2026 19:48:51 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1607-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6a8a0964f92238818b5650b233da4bb6958d3fba0683049e301d69b0ee8e0f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5306296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:916aaba35228da2841d4a9bb63197ffa9103bf84001774262f37e7122baa6b39`

```dockerfile
```

-	Layers:
	-	`sha256:66ded7844685347c4b603d96c5f50d4a0450e6d285646f366d73256362a2d2eb`  
		Last Modified: Mon, 02 Mar 2026 19:48:52 GMT  
		Size: 5.3 MB (5289771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7ff505f8d6db2c81bc23d19eddf73789e436db872b37e44f4fac690271704ba`  
		Last Modified: Mon, 02 Mar 2026 19:48:51 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1607-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:793fe6b130a3a223b6ebaf8ba79f52f9380acb3e40902497b04900f6af055863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.4 MB (179351152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81718e79b7d77bcb17ce244456a7a307b746b01dc263ec580ed0e4a5bdffec42`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Mon, 02 Mar 2026 19:48:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:48:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:48:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:48:18 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:48:18 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:48:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:48:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:48:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:48:32 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:48:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1290634b624e4bc5ae52971ef13e7d7ad96ab8d54c3bcd0ad2710a6d91ef24`  
		Last Modified: Mon, 02 Mar 2026 19:48:52 GMT  
		Size: 91.3 MB (91288270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da25bb95acac613a1081a0c194ba9c316154109ab784fd25ed7555d8aa4e9947`  
		Last Modified: Mon, 02 Mar 2026 19:48:52 GMT  
		Size: 59.3 MB (59317368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ae9215ce03d3602c1f53eabe2f55921236ca75dc1972d7ed5baab9294cbf16`  
		Last Modified: Mon, 02 Mar 2026 19:48:49 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8882841a7de2e91ecb3a9b6a0288b5a280aa12509ec518f01d8b0ffdd5a2a42`  
		Last Modified: Mon, 02 Mar 2026 19:48:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1607-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c27392b9ab9df07f3978ee8b859ee9fd96dc5ef9dfc151556a9ca4dce5c93122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5312190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f121cd9af4a12ba6da94109a5b833a494eea5179d00fc4cc53b35b96658f9d`

```dockerfile
```

-	Layers:
	-	`sha256:f3ab1982822b73f633bba6693a6fbbffcedb22996f94b15b04eb2530f8213efe`  
		Last Modified: Mon, 02 Mar 2026 19:48:50 GMT  
		Size: 5.3 MB (5295524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a74e0ca2efa7ac9156635b32e2ff24543afbb9cbd2c152eda6b93ac264e1ff38`  
		Last Modified: Mon, 02 Mar 2026 19:48:49 GMT  
		Size: 16.7 KB (16666 bytes)  
		MIME: application/vnd.in-toto+json
