## `clojure:temurin-11-tools-deps-trixie`

```console
$ docker pull clojure@sha256:db2840f841b473f3245b9340c2d8c910a4db74c0dd2326f342025ecc0b8613ab
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

### `clojure:temurin-11-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:c372b8984f9d84362227c3bba658121931720603916e868b6e64df634d08f099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280484150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e70e2077193c94115a8408927a3afbd2a5d2760f9f1700005786e60e00c122b`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4e0be23e579f67249688ecfe2e8c2e5cd8418cb7567471aade1f5319f9dbec`  
		Last Modified: Tue, 30 Sep 2025 00:53:06 GMT  
		Size: 145.7 MB (145658246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb6c0b87415040f770ca91541f3e9859ab90e5f53a518a3697169fdfb612239`  
		Last Modified: Tue, 30 Sep 2025 00:53:31 GMT  
		Size: 85.5 MB (85540634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ba1815ad00e73bcfb1290c55771432e5eb80b72675f259ea8041921c273bb5`  
		Last Modified: Tue, 30 Sep 2025 00:53:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:642c1f2bf2462769b2237209d02d7d9dcf8797abc0293ab3d4d6ef8def0b41fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7501214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709e889ca667213f44decd5a4c296cefb1ff847871825b9a3749bbbad8ad1098`

```dockerfile
```

-	Layers:
	-	`sha256:bc546778f03f4cb3eff57d6fc75bc774eb805a8a52996283214dd71f22aabf51`  
		Last Modified: Wed, 01 Oct 2025 15:36:48 GMT  
		Size: 7.5 MB (7486986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd2bb17d8da21aa6277ee7d8b3aec6f156c2ce7678568015f268aae58a6068e7`  
		Last Modified: Wed, 01 Oct 2025 15:36:49 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ded95c14e376ec0ed0862620ba0a7ae562896edcad013294f73dfb3e2ce87bd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277466569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a803c292e57933cb7b2265710f623d46d74e3889a1bd535208ad452b8413db2`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a271e1eebf6b2154867439bfa0646bebe7ca18e64e8714cdaf77f5bd81a1d374`  
		Last Modified: Sat, 27 Sep 2025 02:57:15 GMT  
		Size: 142.5 MB (142458757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e0e288342cd51b3aba181b3f34395dfcb58b2d5eaf2ee2e3308fb130e426cc`  
		Last Modified: Fri, 26 Sep 2025 17:54:36 GMT  
		Size: 85.4 MB (85363420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296ac655788860521197afabe286ec4e6f341a972ba12e6e8a5591b24a05bb91`  
		Last Modified: Fri, 26 Sep 2025 17:54:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7e8c4283d5770545de38647353afd50752afe22dc9b5d4eaf96031721f3ed989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7508979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed543de271a04182bed409de2ff4635d0a3e5dc0e91bcfee208f5134167f6e1`

```dockerfile
```

-	Layers:
	-	`sha256:7206efa093409f0ca29f163acf8fc7ae2629d24797cfdcd54ee401228855a07a`  
		Last Modified: Fri, 26 Sep 2025 18:37:41 GMT  
		Size: 7.5 MB (7494634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7982894f6cbedee5f084f95eebcbb22b0103dc0035b81aa082d270f602cbe04`  
		Last Modified: Fri, 26 Sep 2025 18:37:42 GMT  
		Size: 14.3 KB (14345 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:e0f757fd6161973597d1666549689609c41c3617166c7961dbb0abb5f54c030a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.9 MB (276906285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c730b75b7ed0fc2daf1eb4263e5c795309b7f79ece11546624234da7f04756f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063b55e192b7cd2b1b8605d164618a1885c56ec5dfaaa0791d24657e692f589c`  
		Last Modified: Sat, 27 Sep 2025 20:13:02 GMT  
		Size: 132.9 MB (132852816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d7928a96de39137c114ba1cf8240df06a8403316651f38385752a292f29786`  
		Last Modified: Fri, 26 Sep 2025 18:10:21 GMT  
		Size: 90.9 MB (90948391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea80f6ff7e06a236adf2ef78645dd2ef6bd38aec800386c705782838792cf505`  
		Last Modified: Fri, 26 Sep 2025 18:10:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b7c4670d14d15a977f35226214efe35b9c23c13fce8677c85a0452845056a05d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7505066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a926957fa3c0e1725de8cb4a62d2e7ab1ea858f81f31569eb55e41ccd93f9467`

```dockerfile
```

-	Layers:
	-	`sha256:d20e722e0d79bae10db17de71e1fa9bb4223d5216335ceace39c36f1bafae031`  
		Last Modified: Fri, 26 Sep 2025 21:36:28 GMT  
		Size: 7.5 MB (7490790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9c646a92f2391d9fec8baa8d3f2d7db0ae3753fccd8f2573eef937646810647`  
		Last Modified: Fri, 26 Sep 2025 21:36:29 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:dd14c5693f9a33099ce7f3b2c9e8b38ca54680c19dd5131adde8bc35ecdd147b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261475800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd010371189244cd769385ebae25179be11a12c5fee20b1514499bf5f57ddcc`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:28eee642962fd09c10ecf87da2d4b65d208f3d5c1bf3fcca21c105c0213f558a`  
		Last Modified: Mon, 08 Sep 2025 21:32:18 GMT  
		Size: 49.3 MB (49346327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a04daa9a30eebb28f66846e414b575847585435ef8632f943b65c4bcba1d2bb`  
		Last Modified: Fri, 26 Sep 2025 18:56:19 GMT  
		Size: 125.6 MB (125622240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e6b58fc251eece597278d9e7a392b8e713d1f726288a193789c8495842ef54`  
		Last Modified: Fri, 26 Sep 2025 18:56:16 GMT  
		Size: 86.5 MB (86506588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039f4918a6ee79ac356dd13821e1b2e6dca130a0bfaec52e8389ec87743f6850`  
		Last Modified: Fri, 26 Sep 2025 18:56:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:938e0ef4899578533394c42173645fb37e1bcc134817a325ef0f9754e9e4bcbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7497139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dae04d6e643edae63c0df1e2f126fed1aaa13c7fb24439ecef564de95412a29`

```dockerfile
```

-	Layers:
	-	`sha256:1e5528dd93d23aaa0c65424f2209a6e42b7e364c09ac5e9f4584d93be6888b22`  
		Last Modified: Fri, 26 Sep 2025 21:36:34 GMT  
		Size: 7.5 MB (7482912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b2ff4de34e6194b03c39ca0c7b97e9fe86ccd3ee3ed528a3c43a67caf221586`  
		Last Modified: Fri, 26 Sep 2025 21:36:35 GMT  
		Size: 14.2 KB (14227 bytes)  
		MIME: application/vnd.in-toto+json
