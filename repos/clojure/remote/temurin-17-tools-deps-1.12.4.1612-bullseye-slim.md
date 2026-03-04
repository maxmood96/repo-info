## `clojure:temurin-17-tools-deps-1.12.4.1612-bullseye-slim`

```console
$ docker pull clojure@sha256:2529568fb5c73169b22d7c602a67f8fd867d46ad0ced50c092fe7904c1437b28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.4.1612-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f6536817875eeaa008cae69c7d826f7852751364d2c20f6b3308d55ceebaa4f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235071604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d339c964c17fcecd9451a33339579336a1db8c6f8b8b33e6d02c177e1a124f61`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Wed, 04 Mar 2026 17:50:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:50:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:50:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:50:11 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:50:11 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:50:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:50:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:50:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:50:24 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:50:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958b3a08b9192579c65ea6d090323403c7344a2f7d01221a07d5dce5d21a1efa`  
		Last Modified: Wed, 04 Mar 2026 17:50:45 GMT  
		Size: 145.6 MB (145628716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bca1b999ca7410dc473debf170a7e29d7b51e65c2e35e8950118532cf2f8314`  
		Last Modified: Wed, 04 Mar 2026 17:50:43 GMT  
		Size: 59.2 MB (59183470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d963c43d0fb3d349c6c513bfe1318bbc1ad9fe0350d8b997515a7bd915346322`  
		Last Modified: Wed, 04 Mar 2026 17:50:40 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3480e840cfe57e0ce52abba192485c0765b7b62157321f678eeaa276d3e22b`  
		Last Modified: Wed, 04 Mar 2026 17:50:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1612-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:26a74cf3ebebbc3700a460cc7af63394c90b543694575f85f360cf6d207c7e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5337513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5533eba97ea25745c81290dbf809afb3fd5e5206af7a6d86de3308699cd06d`

```dockerfile
```

-	Layers:
	-	`sha256:e5e4bc557bca0a13f1a677e892681ad9411b21dce15cb23f6874c8136a61aef8`  
		Last Modified: Wed, 04 Mar 2026 17:50:40 GMT  
		Size: 5.3 MB (5321677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40e90401e918242f898cdd38e7eea20da7cb4d46bcad0d66f61d24df4b5239f4`  
		Last Modified: Wed, 04 Mar 2026 17:50:40 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1612-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:70e594c4e9a7dc23446d751740a46d3f619a23eec941a7171d38adc7a7985209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232505464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f80b478f6537d514735165656bdeedae2029677c06fcb10c96be787175d8615`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Wed, 04 Mar 2026 17:49:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:49:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:49:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:49:47 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:49:47 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:50:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:50:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:50:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:50:01 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:50:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c300a9fd591df37698581bb6907e3de3d30ab16f45c53107c91158a77af1230`  
		Last Modified: Wed, 04 Mar 2026 17:50:23 GMT  
		Size: 144.4 MB (144436198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8a5ac23d7a61f472f8f5254938f964f1548638dbecb8db50ec8875cad15c28`  
		Last Modified: Wed, 04 Mar 2026 17:50:21 GMT  
		Size: 59.3 MB (59323751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d854d6c097452f640d76bc97c2a7e5a3a75e84cac4c18db4159dc6cff6c39e`  
		Last Modified: Wed, 04 Mar 2026 17:50:19 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442b1d1ece3afa001d6ad48102b008c50902b3196c9c92b8e1761eacacd6dc2b`  
		Last Modified: Wed, 04 Mar 2026 17:50:19 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1612-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8b9b9e843c0d2acbecf3632a1c8593376efe42065d3d3b645296f9576eaef92f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5343363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abfdcbcf42cf2e1054533b9795dc1da454a5200b338a21c3a85dc529a435f470`

```dockerfile
```

-	Layers:
	-	`sha256:b3b3d2b94534dad6c6fd78b1e1f051f88d3b15b0b47b1c3f33e76668c9899f12`  
		Last Modified: Wed, 04 Mar 2026 17:50:19 GMT  
		Size: 5.3 MB (5327409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8415751dcef92e2480dcffe3f876cad4073dc3d8c4ff868b1b74fdb7d9bb44b7`  
		Last Modified: Wed, 04 Mar 2026 17:50:19 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
