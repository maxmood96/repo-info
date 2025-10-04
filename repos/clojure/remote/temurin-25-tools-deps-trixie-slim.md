## `clojure:temurin-25-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:d3d0dc2d89e15fd456ca003263b9e64bac42ac9188737beb9c6044c97d2761df
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

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a7799c5529d6bfc8ddf841f4b4e4539e34e1602d97f59477e813114350815b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196753326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54b7fa367346e47ec3cfb77171118cb0355199806e74fd5e242103a15ee228f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
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
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0327c0d19787f0057ea8ce23dc2100ecd313f3ebdc93f7335614ef048938a48`  
		Last Modified: Thu, 02 Oct 2025 13:08:17 GMT  
		Size: 92.0 MB (92036036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d870013e7a1ea27f31438379a9954198b25e6a16b82b11d7717982b3432590`  
		Last Modified: Thu, 02 Oct 2025 09:56:29 GMT  
		Size: 74.9 MB (74938484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3176100d3e8470acf2ce825b9b65530e36c1380d3ea800932434b0430f0054a`  
		Last Modified: Thu, 02 Oct 2025 09:55:32 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1989d02dbefabd772d864177c3de30c6ee762de9b46ad52065264095397f7bfe`  
		Last Modified: Thu, 02 Oct 2025 09:55:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3c9d05d89dfeae1a9d8b3d5ce2abd21408b10c7848ecffb681c7ce3858c56309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5620b52a33b316dcdd441c574856e19bd42462bc87eeb8d4c30ff4a4cad75c53`

```dockerfile
```

-	Layers:
	-	`sha256:dd7121c8fe79dc76d45806618af4ad8366326201ecbafb5297d808994ad78750`  
		Last Modified: Thu, 02 Oct 2025 12:45:47 GMT  
		Size: 5.2 MB (5207505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14ff89503fba21ca22700089cbeaed849de474098f2385854b12c5c050ce8513`  
		Last Modified: Thu, 02 Oct 2025 12:45:48 GMT  
		Size: 16.5 KB (16536 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bedca12edbc9e574be1a623f96378a071fe4ba1ed1bbe618e67463e6f9e9739f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196311483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57241717a136fd66a2a1374e57bd56eb706fb35b644987a2f0fd737e38f11d4c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
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
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea40a9217b210e0eb65fcfb862b5c68efbe7ac2ef62ae297c1d189974d1e3a5`  
		Last Modified: Thu, 02 Oct 2025 02:47:12 GMT  
		Size: 91.0 MB (91045277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d006c7cb877977438caa28b3a7f22ffec6f11222e5b029cf955d60c37434b29`  
		Last Modified: Thu, 02 Oct 2025 20:43:35 GMT  
		Size: 75.1 MB (75124322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109cbbe633d40d06867b2759eaf3633de6c634616d69fa11885a230efcb4c4a5`  
		Last Modified: Thu, 02 Oct 2025 02:56:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cb21cfed6c8fde4c0e05de6c544c98d82af6d02ec855bff16d08321ff41445`  
		Last Modified: Thu, 02 Oct 2025 02:56:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c085e953d0805fd27d561456601fe1c8031832b9a40fe1067bfca20f986ddaca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ab7031e99b04a58f8ea1c5e9eab2808f3686f935822f1c49490811bf0c8369`

```dockerfile
```

-	Layers:
	-	`sha256:31a977cfc1d44206ff742c61975d59b20b7c07dacdf85fef448139e0793f213c`  
		Last Modified: Thu, 02 Oct 2025 06:47:52 GMT  
		Size: 5.2 MB (5213295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d904b13bac537c3e39f2b7069ea8d2006b5e3c166bd86bebb96772c75da5551`  
		Last Modified: Thu, 02 Oct 2025 06:47:53 GMT  
		Size: 16.7 KB (16678 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:4e112e134a3257b409753fec7179d11c6098615d6e95dc2eac16d59987c2ac02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.6 MB (202593820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0cc7b6fd039532e8c6b7de231439bc2aa1c02ddbfec6729fe6a722248e9504`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02aec982c14ce5979fd1cc3346d4a14cfe11350bfa7072f1c053674be3e6c39`  
		Last Modified: Tue, 30 Sep 2025 22:44:21 GMT  
		Size: 91.6 MB (91601754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9276019b6c4ac8b3419434459e3ae55e86d5b9544a3ee6b9414889f2af5ee36`  
		Last Modified: Tue, 30 Sep 2025 22:44:15 GMT  
		Size: 77.4 MB (77392571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7c0eba35bbc8505a8caebdbc185ca2d527718ae8ea4addf21b426b50693541`  
		Last Modified: Tue, 30 Sep 2025 22:44:11 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5f92e9b0e07a5f5df4970b8a19b1293885b2aa8939ce363523008a4c8fcbdb`  
		Last Modified: Tue, 30 Sep 2025 22:44:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:01779a26fa6c6959149c3c25855aa66bc459b362618cfe8c2a02741c8fd81641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5197fb24085fa98422ccc456d88bc0b353a592a6b8c9b09fbe309795e063fdda`

```dockerfile
```

-	Layers:
	-	`sha256:b3bf0cc31b21c58f2435da1571be92435ddd48378eb0d56333bd1c096d5d757e`  
		Last Modified: Thu, 02 Oct 2025 12:45:56 GMT  
		Size: 5.2 MB (5213132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcdf55534b650a72f0c31502e03fd1bf42d8771772256194914c05e15a732f77`  
		Last Modified: Thu, 02 Oct 2025 12:45:57 GMT  
		Size: 16.6 KB (16595 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:387804d3d26037c5cec35e495592fb0a341dc2a1ef528f733c9aea24030bcd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192517408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64c2cd4762369b2a8e137141ea6be982a1d646ffadae948e26cbb1e9b7f77c53`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
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
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c14210b2e55dc8f2234b49ef3d00fb3fb7050255e8655721e57688e1998fbe2`  
		Last Modified: Sat, 04 Oct 2025 15:14:08 GMT  
		Size: 90.8 MB (90752390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4438d0f363f4565da6530f109ef302236815051d87464be61ffde4cfb72ac549`  
		Last Modified: Sat, 04 Oct 2025 15:34:19 GMT  
		Size: 73.5 MB (73488471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab18a0cb8769f03320f1e3f5277d1e49ba37f13d11cf63e41ae22d291becc89`  
		Last Modified: Sat, 04 Oct 2025 15:34:14 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ca9046d86ebf60ffb21d5efe45960e286772373845da239482012a40582b3d`  
		Last Modified: Sat, 04 Oct 2025 15:34:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a053f21f1476f0fe8e9f3daa40da051898eb772beb07b6a58968f0942c2a57af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814a2ad9cbcf637200799cbc9dc7e6f63a8f7b4ad19f5b3db845c719952bdfc5`

```dockerfile
```

-	Layers:
	-	`sha256:f63483b7f5a293c1e4afd9ec7f02f9ee66796335fd85511232a8a9fc5fa9ec6a`  
		Last Modified: Sat, 04 Oct 2025 18:37:02 GMT  
		Size: 5.2 MB (5196978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef3a24526c1cea1b9eb63268bc03b64f199ec64b94079115b13be081dfc78cd1`  
		Last Modified: Sat, 04 Oct 2025 18:37:02 GMT  
		Size: 16.6 KB (16596 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:8c015ec70ccab65807a2c967d1afec4b8d700280385ece8ea6c15a4d73d0ce01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (190998421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8518ea48742ecc8349099c76010075ac4aef75068a78d796de9b8c2df53a6641`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
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
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42948e38dfef62917f0e859531aad0c12af86cbc4d41c161cc293ff4019a52f4`  
		Last Modified: Thu, 02 Oct 2025 20:36:48 GMT  
		Size: 88.2 MB (88206411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06b98ecfc528bbfe44cd8d7e556cae89348ab45163db3536faa5ddc02c72b62`  
		Last Modified: Tue, 30 Sep 2025 19:31:40 GMT  
		Size: 73.0 MB (72953740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599ca3bc2712ae3d8176b332787bc52c741f8ccf5654ac1ec71e9fbb27522ef2`  
		Last Modified: Tue, 30 Sep 2025 19:31:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d46c753cd594e5fdfa025ac55e82bf869cc572cd4ddb4e3bc4d38131189de3c`  
		Last Modified: Tue, 30 Sep 2025 19:31:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8234a743115002b7677e5cabb79584de74d3eca9bbd82c884a52e50241c92e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc36008b63646c9a0e0dbbefaba3a2d026f790a71b208a71a78e096e12364e5`

```dockerfile
```

-	Layers:
	-	`sha256:4b960eb947fc0c63153f96ad25ec28c90a733f6e018fdfa6581f2a57cfcfb196`  
		Last Modified: Thu, 02 Oct 2025 06:48:04 GMT  
		Size: 5.2 MB (5205923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f90ef2ca826746d74ae4ad852d3c0e9ef6682a0955c668065759e8f1b57ba82`  
		Last Modified: Thu, 02 Oct 2025 06:48:05 GMT  
		Size: 16.5 KB (16536 bytes)  
		MIME: application/vnd.in-toto+json
