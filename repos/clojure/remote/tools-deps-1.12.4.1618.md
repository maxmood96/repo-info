## `clojure:tools-deps-1.12.4.1618`

```console
$ docker pull clojure@sha256:e0028ed00daa5b469dd674c6dcf056b7f688d9d232c19746e137de97327234ec
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

### `clojure:tools-deps-1.12.4.1618` - linux; amd64

```console
$ docker pull clojure@sha256:7e96f1f16fee669e9693b76cb9a4ddd638852a5bb16c16b633ed052976a585e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221913006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d320c012eca09795c2c11dd1583f1e2226b3926c438f2fefb1f0044c03edac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:14:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:14:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:14:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:14:42 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:14:42 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:20:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:20:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:20:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:20:52 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:20:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a5e93d67c63dae2749e3635a17979b5041562442f7d3b841c14ddfc0f913a3`  
		Last Modified: Wed, 22 Apr 2026 02:15:33 GMT  
		Size: 92.3 MB (92256332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf60f2a7095ee770f3e81d9b25078538375f2ad66d6f78582c789c65911d5070`  
		Last Modified: Wed, 22 Apr 2026 02:21:10 GMT  
		Size: 81.2 MB (81167004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66c6ed5439e2860c12a3b0c4177da524676895dc98f4edbbdfa11df44c4a051`  
		Last Modified: Wed, 22 Apr 2026 02:21:07 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3145cdb68167ef5714a8a6f50d1d6ce6469510b5ce8cd53040eab87688c361d2`  
		Last Modified: Wed, 22 Apr 2026 02:21:07 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:117cfa643671942b097300f6c7f888ac2daf8a55276b35c645470a022c999f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7364672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177da44843897e16b511479b80f14eb93eef68486b9392a44fec3df61f81a78a`

```dockerfile
```

-	Layers:
	-	`sha256:100e7bf120a4d62936d44cd3521007bcc3700b02c4e9cbce9e1870fe45f3f57e`  
		Last Modified: Wed, 22 Apr 2026 02:21:08 GMT  
		Size: 7.3 MB (7347700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc440b1cb97fffe1f12e04f046e0ae1411f4a8ed0bcecf8121fc1c0e52aa5e48`  
		Last Modified: Wed, 22 Apr 2026 02:21:07 GMT  
		Size: 17.0 KB (16972 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1618` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:17974e2af9b4cdc02d14960f09a62d70cf549098796436346b36c2c52035f689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220836604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a987987c5bbe66a371f0866e5a8c0e3bdc5e597a05dbb3e2b44d846da43cc28`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:23:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:23:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:23:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:23:46 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:23:46 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:24:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:24:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:24:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:24:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:24:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530464a312d986a46c66e7165a363e2de523dba1bae0690b86e5705e73976613`  
		Last Modified: Wed, 22 Apr 2026 02:24:23 GMT  
		Size: 91.3 MB (91288310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a044efbc47d8383b9a8d4680629c3958b08c7efd97ac8104760b1bc9d073da`  
		Last Modified: Wed, 22 Apr 2026 02:24:23 GMT  
		Size: 81.2 MB (81174184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1214fa3c3d2486af643a010e2b0fa8dadedb922b426f9ba961085bb79298d96`  
		Last Modified: Wed, 22 Apr 2026 02:24:19 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b157bd29aa34be3f6b9107a8088fc6c6ccc36ec69dbdfd7af5e42a3bf33c85cb`  
		Last Modified: Wed, 22 Apr 2026 02:24:19 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:6d4e9721cd17e940c60ee01683273d41c100e737387e2da96497acde04f4a5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7371493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7027276eb213d6c67e2bee8f8d0db8c54f93ed1cbeba058d96eb9feda96adc1c`

```dockerfile
```

-	Layers:
	-	`sha256:0a1cc2bead94e633a7517462f91a5bfbeab878a068a27832dc1ef9a74b918a20`  
		Last Modified: Wed, 22 Apr 2026 02:24:19 GMT  
		Size: 7.4 MB (7353532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1abda84debebe17b97bfd91d2c2540c6be2da716ef54ea65aa866da208e233ce`  
		Last Modified: Wed, 22 Apr 2026 02:24:18 GMT  
		Size: 18.0 KB (17961 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1618` - linux; ppc64le

```console
$ docker pull clojure@sha256:dfc100757a8adce876845b34fe4c7257317bd54896cb4fe5bd474476bdea8573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (230975102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1fe281ebfef406a79359b62ff9ea2366030944347d3bec17ac33a0850e01aa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 02:29:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:29:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:29:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:29:27 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 02:29:27 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 03:11:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 03:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 03:11:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 03:11:55 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 03:11:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e921237880038077978485833f958f4cb6fe7cf35b55e5d3fcef9da28065c10`  
		Last Modified: Thu, 16 Apr 2026 02:31:28 GMT  
		Size: 91.6 MB (91632998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a51ae4194579d5a7161ca1016385ad82b514d8bb814d1515c99d703e3a66556`  
		Last Modified: Thu, 16 Apr 2026 03:12:31 GMT  
		Size: 87.0 MB (87004124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f978be4cbcc00e56bbe3c2e98d4a456156237c9af145daa47cd369d5d5e8f44`  
		Last Modified: Thu, 16 Apr 2026 03:12:28 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c7edfa947d0634de356562012233caad40f84eb678b691aeb636a08647f619`  
		Last Modified: Thu, 16 Apr 2026 03:12:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:1371147e8c58c448ce88f78ad6f8faf28056eea76f6667bb04910ae8bf2d2ad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7354119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b0e15fc1b33c983ae1d458d6871488992d76f4fe97b622508f039086144a4b`

```dockerfile
```

-	Layers:
	-	`sha256:b150287bfec1fab6a4bd65c7ab4b6136ae50db4600f8b1a8ce85f1c3a27c78b5`  
		Last Modified: Thu, 16 Apr 2026 03:12:28 GMT  
		Size: 7.3 MB (7336264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59000937e45f9161e1429d94e9e26e806c9a24cdf2545311e789f84e037100e5`  
		Last Modified: Thu, 16 Apr 2026 03:12:28 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1618` - linux; s390x

```console
$ docker pull clojure@sha256:428b8f868c2570fa62aa04d4d3402f6a479872c17540662fbc616db84621b035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215362758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2208c13efa23eb2135af3443999a6e6b36e26c6ff4899a4973e9e0590def4e7d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 04:04:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:04:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:04:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:04:56 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 04:04:56 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:06:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 04:06:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 04:06:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:06:06 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:06:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5dad69e7ac6d7de7c487cbd0e07c1a2df656f2bfcdf859fa497ab6b24109cce`  
		Last Modified: Wed, 22 Apr 2026 04:05:35 GMT  
		Size: 88.2 MB (88233835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8220185112ee0c48df3c405a46f7040953fa3619cc6d7587cee666ab891fffc`  
		Last Modified: Wed, 22 Apr 2026 04:06:33 GMT  
		Size: 80.0 MB (79979914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd01d9f41be888c87e3b2c766ab4cdea1e05a11e468c4db45c99b1484f08a46`  
		Last Modified: Wed, 22 Apr 2026 04:06:32 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6f1a9bc544c835e8a1e48ea4113521d63908bcaa7f1b629fc963d489ea3c6f`  
		Last Modified: Wed, 22 Apr 2026 04:06:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:614afd7548ce641994e6feaf8fc6bfc554850b2209a6292f14fa9b3d1ac7a0a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7341352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5958401095a450120458ec6202ad2cbf7e12e67e4139e9ae155336ecc35fac`

```dockerfile
```

-	Layers:
	-	`sha256:d064f87b1cc8cffc302068b2c8455749b3c57d52a0f6918a31660ef3490a5725`  
		Last Modified: Wed, 22 Apr 2026 04:06:31 GMT  
		Size: 7.3 MB (7323581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f62b62fbdbac31bdb9fa3a2d6a45432fd2db9fb27caba87ec9fd3cde665885e0`  
		Last Modified: Wed, 22 Apr 2026 04:06:31 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json
