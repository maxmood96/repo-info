## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:3d88e2170d93baf782bee481b0ae366c1769c0fd5f133b86531c7bb43151ba85
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:93038409acbc2fca2bbc4a4adec3e6ca0c1d0d378e595c008e3ab03f4888dc51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184204090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965ba19a71dc64d4e3d7462729cdeefe49f78b44166827ec3a9edccd93b4cee8`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c32239774341a019c02247fc1d1b12148b23ab0de67d3646f332b880fb9cf1`  
		Last Modified: Wed, 02 Jul 2025 04:15:56 GMT  
		Size: 54.7 MB (54716198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67a3f1ab8d00c4f4982129ddd608e5bad6f641538af2e44d28973f311021ca0`  
		Last Modified: Wed, 02 Jul 2025 04:15:57 GMT  
		Size: 81.0 MB (80992964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d3661b4ece01d9d674b26693eba5a795d37e372a322efb058dd5502605eee9`  
		Last Modified: Wed, 02 Jul 2025 06:12:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7663f4bbffc6b729d36f85103497ec7ad64b7cf5de6d7cc1a371b189a57aaaef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7504113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5da904ba5346a7b39e9c0074fdfe3d4d9fe9f732fd3d2519176b3a31b9ff011`

```dockerfile
```

-	Layers:
	-	`sha256:a8266c27c0ecf802ec941bc0707cff532a69cd89407e68f8d342edc9deac788a`  
		Last Modified: Wed, 02 Jul 2025 06:42:52 GMT  
		Size: 7.5 MB (7489878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2336a9b0d43ba170fbcac1cf3b852d6e6a86a5496e8d037bd9645d44d37b3ea6`  
		Last Modified: Wed, 02 Jul 2025 06:42:53 GMT  
		Size: 14.2 KB (14235 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e2cb2431eb4138290ce26a3ca8b3821e23b0a3ac8978ec512d88904fd9ca25f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (183021855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f67d480648ef6a1e8296adf297c0f911803856fdfb1bbe7fbc4d5ef42ff454b`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fa004b17a578fbab709d8ccce7209b0c158bee3d29acad283414b9526ec42c`  
		Last Modified: Wed, 02 Jul 2025 12:04:37 GMT  
		Size: 53.8 MB (53830502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c803fff28c9e2de1181286c180402b9cc530a1efd3a0b03afcd6d80cf6b3b7b`  
		Last Modified: Wed, 02 Jul 2025 12:11:04 GMT  
		Size: 80.9 MB (80851923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6be376b4910e0fb86901c7ec66e71c23db859a5824d371156f1b536258a9e9`  
		Last Modified: Wed, 02 Jul 2025 12:10:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:167f70c25ec8f9a970a63778b6f40dfa42a8c69ce474bd24135d89e68addb77a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7510694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e165da2ae06039d536553726676e7610d11a0100b976d5f74b1e3e2f72f46fc`

```dockerfile
```

-	Layers:
	-	`sha256:b382b08679a76d913e2650b6c02a82ab724552d28c1c157a51d7928777a85a24`  
		Last Modified: Wed, 02 Jul 2025 15:44:11 GMT  
		Size: 7.5 MB (7496339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ad8608fe0972bd9d00776d5b283e5d1d6f1e21f371861a0322a245d25674e9a`  
		Last Modified: Wed, 02 Jul 2025 15:44:12 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:5cd19a132db285c453c58457e8c6262d48b6f29c769e37d015b966c40b13419d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191325291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d2eef33645bfcbfa3da273fd38371731c2f0037745a4a2d053f7850e290d51`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001c5a2b4a804ffd15f3bb4cc7dc5fd44decc310eef36f7e78c41ddc786f461c`  
		Last Modified: Wed, 02 Jul 2025 09:51:52 GMT  
		Size: 52.2 MB (52167961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0426cffa12f603b6e7d8d592c925235211bfe65e42e2cad7159dac8afb99fc`  
		Last Modified: Wed, 02 Jul 2025 10:01:06 GMT  
		Size: 86.8 MB (86819443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491b501fdaf48878df8141a6ca68c47bb32aa09dd5babc4c8e70df703f7d6054`  
		Last Modified: Wed, 02 Jul 2025 10:00:59 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b8834c103ca54321533b99e28e70e300e82ff793f7dce1fbbc01cb0e881eaef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa061bfbf43c53200798ed7b2a3d63b95c30cbf8a4b20fc1f285fc38b994b4d`

```dockerfile
```

-	Layers:
	-	`sha256:c72db524bc6d3dab4baf48df1433bed6040d91d64664224ec01f36f841ae2220`  
		Last Modified: Wed, 02 Jul 2025 12:41:25 GMT  
		Size: 7.5 MB (7495675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3075376abd71a5dc9b7944b5df747012a4383b30e1619d8e6ddd05296722cf07`  
		Last Modified: Wed, 02 Jul 2025 12:41:25 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json
