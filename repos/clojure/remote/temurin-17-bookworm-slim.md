## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:160c62e71643a0ceda931d09c782aa8d828f333fd3e5908c9930dca1afdd53f5
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

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:456817f05ab3202931a1f6ca0189505a40325f33dd2fbba90d7607a9feb078f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242756828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6cafccbe2df95383ba75789ce3261eb3b18e1be13cddc9baebb2dbc094e7446`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:53:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:53:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:53:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:53:18 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:53:18 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:53:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:53:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:53:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:53:35 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:53:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305e645085c3164effe0b48a2b1857b21a2e2f6fb982c01572020d858197eab3`  
		Last Modified: Mon, 08 Dec 2025 23:54:31 GMT  
		Size: 144.8 MB (144847947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee606951b28873d808885b135cd2df57c7355f9134059c82ea8c9b4eb85005c`  
		Last Modified: Mon, 08 Dec 2025 23:54:12 GMT  
		Size: 69.7 MB (69679424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af68b95a232afeb17541621085f56298e84f850434e596fa426bb09a79110ae8`  
		Last Modified: Mon, 08 Dec 2025 23:54:04 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d745430c2ddb72df45b5e5339d47afa1ce726478330cd8a3f0b189d650b2834`  
		Last Modified: Mon, 08 Dec 2025 23:54:04 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8744a7ebbfa76e6c32dd5aeb24ac7c68cb95a0dbcf2cc9594c5624e5212db7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5129225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2389b0caa4fa64e50fd132e114123b503bab87d56dd4e639130cad93f703a19b`

```dockerfile
```

-	Layers:
	-	`sha256:fd1802c1ba03067f6ee678a9d31ed58c1e3da23aace0dba20d2576dc3ba6e284`  
		Last Modified: Tue, 09 Dec 2025 04:39:11 GMT  
		Size: 5.1 MB (5113390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42ded708f8cd5642e2d2ad0338acb014465d6d228917259a2c466040bf8786b5`  
		Last Modified: Tue, 09 Dec 2025 04:39:12 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0fa866524f6d5434327ed5ff0a749728bae2a7ed4c1f43c59d6a4d15f9b17b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241343569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd37f933725af1c80bcff6f505236080adeccf10ea8776a4191cc0a8ca8ff9a3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:01:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:01:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:01:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:01:11 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 00:01:11 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:01:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 00:01:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 00:01:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:01:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:01:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b05332f3db7801ed8aae1f570c1c7ced1ee978b260643f0fd49aec6d8a29d4c`  
		Last Modified: Tue, 09 Dec 2025 00:02:08 GMT  
		Size: 143.7 MB (143679920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f690d3607603ee76e98fa78c7dfaaf6f54b5b089e7a47f472fd4a5bc324d5833`  
		Last Modified: Tue, 09 Dec 2025 00:02:00 GMT  
		Size: 69.6 MB (69560383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704a19568a674fdab40f904d103a884c9123450f99ca6c108371034752579b4e`  
		Last Modified: Tue, 09 Dec 2025 00:01:56 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f38da699967096502d942477e9f650e65102e365bd266d4b4b32611d48cce16`  
		Last Modified: Tue, 09 Dec 2025 00:01:56 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5fb8871902a694ff2ccddb5ccf07f7ef908528dec2e8447f6bceec25c8677b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e05847d60c3b3ae2f6faa0e9f754bbb9f29c02c12f39ec0884c8b7e2b96585`

```dockerfile
```

-	Layers:
	-	`sha256:0ab0edc8111064f6589b6927766b975cff76431c36e5b400d87d615c05c7d84c`  
		Last Modified: Tue, 09 Dec 2025 04:39:19 GMT  
		Size: 5.1 MB (5119151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8e31e9b1c3032b7825f70fc80c36683f44a6e7367e73f4694d96e74b360fd63`  
		Last Modified: Tue, 09 Dec 2025 04:39:20 GMT  
		Size: 16.0 KB (15953 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:60794e6d89c9570eb4fabcfb2ec749e6470e82957b40692d6923803ba729bc77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252108437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cecc703660d231625ef0c77f045870e46509a540367bd5aa16306a38e8c50ef6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 06:27:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:27:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:27:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:27:21 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:27:22 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:30:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:30:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:30:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 18 Nov 2025 06:30:09 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 18 Nov 2025 06:30:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ec7a1a15d2a3b24a68856f8ea1e0b4ced75acf51647ebb533587594c649f3a5b`  
		Last Modified: Tue, 18 Nov 2025 01:56:01 GMT  
		Size: 32.1 MB (32068826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172e760286a339898f9ca04793550c307642085dbffc819262542c00d0caf079`  
		Last Modified: Tue, 18 Nov 2025 06:28:44 GMT  
		Size: 144.5 MB (144525254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6f37c30fc46c3732ea9de95f46682fb18beb238e010d37ae1210090781b6f0`  
		Last Modified: Tue, 18 Nov 2025 06:31:03 GMT  
		Size: 75.5 MB (75513321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f368de175d375774d3a29ef8b644659143abf6551c53505a672c79de58c8169`  
		Last Modified: Tue, 18 Nov 2025 06:31:00 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1f445c0f753495af3d7dc2292010b0c9538f50e3c64046fabc374ed7571022`  
		Last Modified: Tue, 18 Nov 2025 06:30:59 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a3f0f16ad7be3756bd725a225acdc758156824a5a9cca27e5073eac026f6750b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5dd7e77a73df58f1b2a91bc999fa602732feb4dff5f450f5a92bc3017e371f`

```dockerfile
```

-	Layers:
	-	`sha256:5c09b6a8d906e1ed1d040b4976eec274497e709fe1b5813cfde3d1c7129c55fc`  
		Last Modified: Tue, 18 Nov 2025 07:40:54 GMT  
		Size: 5.1 MB (5118548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1543b222d70cb2cc1da915ff6e930eec052494fa5e2a837ee231c104400e006`  
		Last Modified: Tue, 18 Nov 2025 07:40:55 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:48e99f56a2634995b23b721baf3fe95e85e456891ac77a6719e0e32add17fb2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.2 MB (230235035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15bd2f8eeefb1fb48e2afa7dc63e4348da5bb4ec50a4ef3beae31832148cc69`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 01:28:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:28:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:28:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:28:38 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 01:28:38 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:29:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 01:29:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 01:29:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 01:29:56 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 01:29:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e50b79de06901b4ac24155509c29afa77758151aad26c6b4026f26a3ea1d70`  
		Last Modified: Tue, 09 Dec 2025 01:29:29 GMT  
		Size: 134.9 MB (134859048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40c1f694790e5fc7ad96aa6851352d9a622b185a94c0cc89310aa4aec07afa0`  
		Last Modified: Tue, 09 Dec 2025 01:30:31 GMT  
		Size: 68.5 MB (68490518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc69494e67ef2d87fb17cf04bd3f3f9403fe7b43447619d8edf3035066b8a162`  
		Last Modified: Tue, 09 Dec 2025 01:30:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12515cd6dc055c178d4b46f65b57d991885c83d21c0046b82fd681e127039dda`  
		Last Modified: Tue, 09 Dec 2025 01:30:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:411514e1a28ae2235a9670e7f4106487381dcc13d3a94990191686f7db4aaf74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5120547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48150e97df0ca624b5dd5513106497da9430d2a1ed5c95c7c4dfc902f2abb7d7`

```dockerfile
```

-	Layers:
	-	`sha256:25e23a92aaa14381fdbd5c054338792f7e178a2b86dee00493873b52d5cf1bae`  
		Last Modified: Tue, 09 Dec 2025 04:39:31 GMT  
		Size: 5.1 MB (5104711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6aa15b20971709f8de334d6d2c64a530d067419cbd77253d1185d3cd5571a6b7`  
		Last Modified: Tue, 09 Dec 2025 04:39:31 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
