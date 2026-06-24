## `clojure:temurin-26-bullseye-slim`

```console
$ docker pull clojure@sha256:b5aad00feab78c96bd0dc125e710fce40ce1e01ceedd33e66d30548ff721244f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6856c962ad2f8afb46d1f6954359222bf826329bb67ae8805726d78ff3d10cb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.9 MB (180885155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93276f89e9f9a517e190e85f8f60b8b73690ba329294688b6be6a906115b447`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:23:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:23:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:23:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:23:28 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:23:28 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:23:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:23:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:23:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:23:41 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:23:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0251c4232e4025b51352f0bb7119fd866d4a6a62861f09baea6fe5af4c6eee59`  
		Last Modified: Wed, 24 Jun 2026 00:28:14 GMT  
		Size: 30.3 MB (30259447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7014a988890210f52e194e50cbc0222260ae28cf0bc0216fe2bc003c53ecd2`  
		Last Modified: Wed, 24 Jun 2026 02:24:02 GMT  
		Size: 94.5 MB (94524361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d38bd226c48213e473f4f3800b200559a8940a0abb66d7d78ffeecc7b2aaec`  
		Last Modified: Wed, 24 Jun 2026 02:24:01 GMT  
		Size: 56.1 MB (56100308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1b4759f9fccd3844523d37ce6e9700e3e83bda59a210400c8eb74a57b5bd9f`  
		Last Modified: Wed, 24 Jun 2026 02:23:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781e7c62a98a9bd085f6d4b1ad0768bf012eb709bcd17898056c35ea97f9984a`  
		Last Modified: Wed, 24 Jun 2026 02:23:59 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1acae34fb409eae947285438b977ff1c708a02486463cd6ce88d0ebef739d400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5298722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69da1cb698880ea8f6675a99b99aea9c00961568f89572b24075eda66b325372`

```dockerfile
```

-	Layers:
	-	`sha256:332cdbe36776b46bbe8590f214bd764ed62a87619edeb661602d626a9f9f48c5`  
		Last Modified: Wed, 24 Jun 2026 02:23:59 GMT  
		Size: 5.3 MB (5282740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e72d2e55b921fcfb6117bf456dacaf89f564527e3ad6b3a278db4108e8ad13e`  
		Last Modified: Wed, 24 Jun 2026 02:23:58 GMT  
		Size: 16.0 KB (15982 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9c605422c9e603540df495e0d6f691a9724421d577cd84c4ddee6875781bdd75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178519954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74940ac98a8a654eb8e8e164515bcfba5a12d0a976900113ec3547db7483e45d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:29:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:29:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:29:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:29:39 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:29:40 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:29:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:29:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:29:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:29:52 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:29:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:58009b48fe731a10341c4f5f98dfa280afd10fa34cc71961411d37e306120dd0`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 28.7 MB (28746926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefdb7cd502490d58aaffde8f574d1045925e63bd73e13f12eb295de41690f19`  
		Last Modified: Wed, 24 Jun 2026 02:30:15 GMT  
		Size: 93.5 MB (93504334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3bc805f28ff530b41409fe4716690373c4e34881ad55ef4a7fec11bf4a6cf71`  
		Last Modified: Wed, 24 Jun 2026 02:30:14 GMT  
		Size: 56.3 MB (56267656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e60a8b2d9d3527ea6f2fcb7cecf2a70210dfac09b0fe60917e587df5d4960ad`  
		Last Modified: Wed, 24 Jun 2026 02:30:11 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8891a1299c508521056e66b2621ab31eae416380ec0ad5dd6cc0aaa45ea6461a`  
		Last Modified: Wed, 24 Jun 2026 02:30:11 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:27aaec5430a1883d0673bfbf34b75e943f0ef74646e831dd046ad11464d973ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5304568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701f0b7f65624827aed9f87454226360e9130d7c482353a85cbb9ad88bf15149`

```dockerfile
```

-	Layers:
	-	`sha256:195990e3cf5a92c7daf52c4881bcf6524241e3ba1a7fc1520d895c0d6b69c220`  
		Last Modified: Wed, 24 Jun 2026 02:30:11 GMT  
		Size: 5.3 MB (5288469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87cc6cb4c64b2674ed533246c0716cda6c5a7f71920062bcff303a664d0fcce4`  
		Last Modified: Wed, 24 Jun 2026 02:30:11 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json
