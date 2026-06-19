## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:ca2ba6f4bbd009301016d21e3379efc822a9009965200be1c1973af1cbd0054f
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
$ docker pull clojure@sha256:45a863f6a78d48a7a14a6f432335480135fe813d6eefa39526f82067eef10ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240787095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb176e9a3a60cfe03ac473c28b2854c1ccc7f7679aee5c4fcdc98b882c2f8d8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:17:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:17:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:17:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:17:27 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:17:27 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:17:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:17:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:17:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:17:42 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:17:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7828dd2cfcf145bd85f23822277d2e4cdb24d6966dc68457c99cb74670ca15`  
		Last Modified: Fri, 19 Jun 2026 02:17:58 GMT  
		Size: 145.9 MB (145905454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde861edd93bc1467ffc4eb9eead87cf1429785e1db8cf0a16a4b870a25a3dc7`  
		Last Modified: Fri, 19 Jun 2026 02:18:04 GMT  
		Size: 66.6 MB (66642974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11df787c9c6a01d738a75bacaa34a6f8a50025770e7af0f79fd11353ac26fca`  
		Last Modified: Fri, 19 Jun 2026 02:18:00 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14a3e3a9d5e1d050bc12ff93bb87df262d7d52e58fd9bfdca8fbf08a97e68c8`  
		Last Modified: Fri, 19 Jun 2026 02:18:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ac6034ab99b4024d3e8c77784829133386ef56199df4812ddc6affe2ac91f4af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5129989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce862b60a2e245b0a4a86ebc87b431c98f3175bcd50695b9cb3815d4b13d3ada`

```dockerfile
```

-	Layers:
	-	`sha256:e760dfd677385f8e52bbb43139aa157fef3d43cf5ec79ef2e079159eefd1d3c8`  
		Last Modified: Fri, 19 Jun 2026 02:18:00 GMT  
		Size: 5.1 MB (5113999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:266c4f1121b30ef568b0529ed6193eba49aab8102388418f9275a2a176767af4`  
		Last Modified: Fri, 19 Jun 2026 02:18:00 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:21776d1725275bbdf9be922799be15b890b38745e3b0dc206c47540bffa33b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 MB (239490714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf940cf12373f1a1eb96f1bd00d128ee04281fb3a28e5ca9cb8478533ddc5ac1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:17:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:17:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:17:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:17:33 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:17:33 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:17:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:17:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:17:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:17:47 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:17:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7d95240c73273e4e6d70e0180a385ee35272d44febe4b42505dd883a0eec52`  
		Last Modified: Fri, 19 Jun 2026 02:18:09 GMT  
		Size: 144.7 MB (144724310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff48157d87169082c77625afc6be8e9d0a167a79b28daa3e42fdff6271d045b`  
		Last Modified: Fri, 19 Jun 2026 02:18:09 GMT  
		Size: 66.6 MB (66643054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abae08e9f9a3a73163af267d70c1c2fa290c7e58fd0769dca2e3813afaf7b08`  
		Last Modified: Fri, 19 Jun 2026 02:18:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1bef0ba2f28478f72bf94b89ffe40b5290f4b0a338a1346f2d68755cb57e7f`  
		Last Modified: Fri, 19 Jun 2026 02:18:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e08aad16aca627b1803e8d486ae6fd31f3b37cdcf2923b002f0c2208f1673d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d116b11035b0eeb5148bfb0c713072022c77d06951cffff0003674bcd19f495c`

```dockerfile
```

-	Layers:
	-	`sha256:fd3326d25ad7f5567a53691ce2db42dd41785946e5ef89680096ddb20a9e77f3`  
		Last Modified: Fri, 19 Jun 2026 02:18:05 GMT  
		Size: 5.1 MB (5119760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7aa62788010dda8b5f72e6cba5ae826a7a785a598150759e9e1fa8934e33120`  
		Last Modified: Fri, 19 Jun 2026 02:18:05 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:c7d994ba488380a414063a4657eab54034fd20e1f2b95497c418652efcda3950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250325569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6f5b15ce15fad3b0a75ee2fd75b3ada54d47ef629c8500a45825bce8296ed5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:36:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:36:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:36:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:36:44 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:36:44 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:46:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:46:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:46:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:46:02 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:46:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011a8b1fe08cbca6cfbf84dcf1035227586f8c0a013a520d08ca8f1bb6f1baa7`  
		Last Modified: Fri, 19 Jun 2026 02:40:33 GMT  
		Size: 145.8 MB (145766212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbf43af0d3048d5fa020f170a5962dd7a7f5cb9f8dab551a3f3d22e60a089c0`  
		Last Modified: Fri, 19 Jun 2026 02:46:43 GMT  
		Size: 72.5 MB (72476374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328d42e99eb0011073e9c9a750f5fa384f379a866b46e24a51f6f104549a3b16`  
		Last Modified: Fri, 19 Jun 2026 02:46:40 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03667bde63913e0892747b56d3a3abbac90e0821912011cd472c66471bc8857b`  
		Last Modified: Fri, 19 Jun 2026 02:46:40 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e1c25687f888fad8ce3543cb4cf7ab2cbb1fc1fe21317ecafeff88a82e200f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990ae71436877cca3ee0f7cd7c7d4b799620a2aaab93c4c368c08aabf5c9071b`

```dockerfile
```

-	Layers:
	-	`sha256:c614da0ca127923df8a30d3b594e9520cd91d0cfdbbbda9aa7277e27dd8b324e`  
		Last Modified: Fri, 19 Jun 2026 02:46:41 GMT  
		Size: 5.1 MB (5119157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13c74f5b9580d8ea1fb4cf7afb91faea5e495a5729de610f686a211409cc369d`  
		Last Modified: Fri, 19 Jun 2026 02:46:40 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:dda7f7b58491a92d916de05ebf9be15d5987ad4f3268741415f041efa9a48e8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228256991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66322df27a7192a9e5f1e4d1c14fd9ccc4ca6cac805c64d87e4f1cf431702a00`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:16:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:16:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:16:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:16:40 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:16:40 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:18:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:18:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:18:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:18:34 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:18:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12de02280ae8885a4001fbd484dbfc1d6554fb904cc661889a6e6ecda0108b20`  
		Last Modified: Fri, 19 Jun 2026 02:18:03 GMT  
		Size: 135.9 MB (135910426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bb7cfed22cee602460bb74a125f636b3bc11e2534983e438dba605d02ab668`  
		Last Modified: Fri, 19 Jun 2026 02:18:57 GMT  
		Size: 65.5 MB (65452018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d8ca75eb62d275af2ba849834ce38d598c1f6f5a543bd0d778696142079705`  
		Last Modified: Fri, 19 Jun 2026 02:18:55 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b0891787dfee78652702f88b3ad022a32bdb69a32c64ae8424f88bc81a1fd9`  
		Last Modified: Fri, 19 Jun 2026 02:18:55 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:35fd9322a3f98de15fb6ee6c63c762082470d51e515f9396df75236a408c4cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5121309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ba1f4e0c319862dc16689befe4bb519843bae82ff70419f8381e889aa0e18c`

```dockerfile
```

-	Layers:
	-	`sha256:780c5948f114eaf4410f7d48c2d4ac523b10e15c628700264cda0e4776de38d6`  
		Last Modified: Fri, 19 Jun 2026 02:18:56 GMT  
		Size: 5.1 MB (5105320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99edab377c85f002a9233cabf68954de415eddb3be07a6a9d7fb1c997e62f1f0`  
		Last Modified: Fri, 19 Jun 2026 02:18:55 GMT  
		Size: 16.0 KB (15989 bytes)  
		MIME: application/vnd.in-toto+json
