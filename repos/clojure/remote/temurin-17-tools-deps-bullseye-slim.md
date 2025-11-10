## `clojure:temurin-17-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:156784816fcc678fb277fcbe7aad4fd2489b312b93bc87e3a876977fc839615b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:85bff04fdcf07c7fdda88c8e9c63ed5e0058f83620d9f94cecd534766d5af4c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234259617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f2b691ee7b57b2f958f9e55929ef202ca1b8c728fd4f98f11a3d398c7adf89`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:43:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:43:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:43:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:43:21 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:43:21 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:43:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:43:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:43:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:43:33 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:43:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7da7db74abf9c33ded4c539d1a1aa4ee67dbb1036cdd3678e19141551d6b4c6`  
		Last Modified: Sun, 09 Nov 2025 03:55:25 GMT  
		Size: 144.8 MB (144848032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc771a88d698fcbba976f9a442c475865948aa045d3900bd62cc82510d33c078`  
		Last Modified: Sat, 08 Nov 2025 20:33:06 GMT  
		Size: 59.2 MB (59151944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03930f620a521edb7b847dac0e0f0e52ef6f9742d6b108967f2de34cd251e141`  
		Last Modified: Sat, 08 Nov 2025 19:29:44 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45faadd6e88ed1b7c08e1390e098963dd7d128249c36454266a4df7379287ac4`  
		Last Modified: Sat, 08 Nov 2025 19:29:44 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:62090307c83774eaddfb63fe4f83a4b894e07349e7be0bfb5c31709acdeeb692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5323905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99edcc45a1b3402375eba300112466e3b870cf69f67d1675ec008dfbb98ff133`

```dockerfile
```

-	Layers:
	-	`sha256:e79ca605218338906cfc4cd6ad48ecc527174808882bc8a4ce546e44f25bc1b6`  
		Last Modified: Sat, 08 Nov 2025 22:41:27 GMT  
		Size: 5.3 MB (5308069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c1eeb6ebb86e6e1842a2accabbd7a9337af6b0494bd66d68ba076341226bd16`  
		Last Modified: Sat, 08 Nov 2025 22:41:28 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9dfe7a6a928459a8a95e08140eec2836e76b150f1ca4a158f0c8104244d0d88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231717277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef2fbed22529152d8151b40ede5c34efb1c5eba8d7f3fd0d3a1b59595b89a0a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:42:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:42:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:42:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:42:51 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:42:51 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:43:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:43:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:43:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:43:04 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:43:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3323f4bd0da79f9a813ef17c77bb7ead990baaec81092a7a0481e1be17570c75`  
		Last Modified: Mon, 10 Nov 2025 05:11:32 GMT  
		Size: 143.7 MB (143680053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a649220b9e8877be48ccb7cac3f2d837c832062aa687b42d7a21b02d9b0eebf1`  
		Last Modified: Sat, 08 Nov 2025 18:43:40 GMT  
		Size: 59.3 MB (59287631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c176997f6dce07228ad0919f5b852e33a16f07b1a55f3b3988402aa2e14cf4`  
		Last Modified: Sat, 08 Nov 2025 18:43:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078808b3cf6e28ef38b008ff3c9afc4420164ba8940a73d8960b887f8ba5d18a`  
		Last Modified: Sat, 08 Nov 2025 18:43:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d028ca9ae5b847523a45ee2ab33232079e1fad6292a61a1a936ee9fd2af3344a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5329755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c2c187d599037bf1d7b32fc4781c96d374dd268202e9fdfce1abfba599f2d2`

```dockerfile
```

-	Layers:
	-	`sha256:8b385a4b0e998118ae58abe0af5f5a74c7a1ebf6d261258cbb8513ad1e9e14e3`  
		Last Modified: Sat, 08 Nov 2025 22:41:32 GMT  
		Size: 5.3 MB (5313801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3d01a1f5b6f34780d601bfbdd895d3ade8a88a8742934c62b280492347e0592`  
		Last Modified: Sat, 08 Nov 2025 22:41:33 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
