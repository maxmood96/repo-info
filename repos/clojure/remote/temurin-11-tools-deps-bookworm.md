## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:59569f1f80db2444847ddabe7d6b77cd181d4da77cbce929f930e49975f9c490
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

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:549bd035f467ad6b8054c8b072206071b7932f5f4a46b6672c5c2b97162c39a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275280421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7fe7f2763ac54daff30d79318cfd0b5fdf024c3953f08c5f4f3da3d640e727`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcd211d187c1601195248f150b0dd71185c780cb3536c86d5c49e4f10babbe3`  
		Last Modified: Tue, 23 Sep 2025 01:40:03 GMT  
		Size: 145.7 MB (145658246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc6ca10f890532fe7c72ce24e93a8cb73f25fc7022fecc6bf80187af9c188ab`  
		Last Modified: Mon, 22 Sep 2025 23:45:04 GMT  
		Size: 81.1 MB (81140918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1a4769ce14a8b282cbd3621296315ff74fcd96ad325188d581fc13cdb47b20`  
		Last Modified: Mon, 22 Sep 2025 23:44:56 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:62eee709421beccfe4f4eea467092381eed3c2b373becd989cf0710c190e3424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7409283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a319072a227441988e9cf0715e7184aea12450969d44a4a2a6ddd07b238b89c`

```dockerfile
```

-	Layers:
	-	`sha256:92d5d2b181a22f51b8a1d194a3ac3d6b0678ff72127040f57ee09fdab52ce9ca`  
		Last Modified: Tue, 23 Sep 2025 00:34:57 GMT  
		Size: 7.4 MB (7395031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98ed6a9cafe9422259db2553397cbf40e0107abe6c1ac6a70d1ff73addb138e4`  
		Last Modified: Tue, 23 Sep 2025 00:34:58 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f75e9699802a739bd72b4be81036d14fa5b0d6a93a01ebd900b5d489975b5bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271849737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88dfff6b0829e923340c5d2e39ad5738a25e9789c24d95b1d955c13f196edeb7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3144b04fe9a32ffe6deccc4f96730b8fceea86c3038def943992424cf2dd600c`  
		Last Modified: Mon, 22 Sep 2025 22:16:58 GMT  
		Size: 142.5 MB (142458757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ab3be698e0e59370737adad5e812b65f8111aadb230bbfe082fad35b5855e9`  
		Last Modified: Mon, 22 Sep 2025 22:17:28 GMT  
		Size: 81.0 MB (81031314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a19815c6fb5370d1b0e5914c7fc9e4111774f12a7e728c8dc2664671717454`  
		Last Modified: Mon, 22 Sep 2025 22:17:24 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ead4f14384abffc1e6cd1b49a2c7149d1939622c6c5506d420636f83af15438b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc7f9e4f6236fb19dea9c7ce7e83926fc4f71b69c0eae86fca19ff97a3acb621`

```dockerfile
```

-	Layers:
	-	`sha256:a1a8651c3d00137d2e7c6b11dfd944f506650b6e9dffb990a6cae69c0784fec2`  
		Last Modified: Tue, 23 Sep 2025 00:35:05 GMT  
		Size: 7.4 MB (7401412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6681eb2602af6ff53075b0b63f4cbbcc31b6c8a9bc2021568b34d7e6beb4b82e`  
		Last Modified: Tue, 23 Sep 2025 00:35:06 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:f3f5009d6d62d68e5d147204c02e2b28be0327af5a9385c323afc1d1f5b92a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272163358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dcc10295df900a7b876167ed317e8484fa7c017b505d70e8c074dc44c2f69a7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:64b8116dd43c29a2a4aa3131cb4895af0a7267cc5883e3761556e54c369be9af`  
		Last Modified: Mon, 08 Sep 2025 21:22:08 GMT  
		Size: 52.3 MB (52326822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef13c4ba7a52133e1454df897daa22c7439b0df6eb204c60e2ecd3e616796b9`  
		Last Modified: Mon, 22 Sep 2025 23:10:20 GMT  
		Size: 132.9 MB (132852835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68144cb9a3a2f7e80e4010db821554cfc4812241664e062aae090f546254c69`  
		Last Modified: Mon, 22 Sep 2025 22:47:28 GMT  
		Size: 87.0 MB (86983055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c4993504b929fc6e9e2be8730f0a7d10f4604678bc7b39bcbce7890be84569`  
		Last Modified: Mon, 22 Sep 2025 22:47:23 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d73e638abe7e83280b34334cde0b67562aecc965d35dd5a2ac2c66885a077e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7413929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e0a741fce0e7bde1ceeba51e19158f34e0923cd2e9e468858d940a5a94adee0`

```dockerfile
```

-	Layers:
	-	`sha256:1855f44c12240fc966cf3a38bf1715f91f6de08be16668c6f47e59f8705dbf49`  
		Last Modified: Tue, 23 Sep 2025 00:35:12 GMT  
		Size: 7.4 MB (7399630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c280b55a313f4b7ce241f3bf56f235a3b00072ad50317c98b66e2dcda47830e5`  
		Last Modified: Tue, 23 Sep 2025 00:35:13 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:5d3fea089b7c81d8866cd3bb072e106777c2e093f73a9e3fdb72265472191c54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252718236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6eec23e6aa686014a0711500550e46c98739fc0fd6b1f6ce8183a6a0fd7d24b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:67e2d91fae4fd9af13e4e364bf8120dcca7856e8273995cc0651acae70b27e8e`  
		Last Modified: Mon, 08 Sep 2025 21:18:01 GMT  
		Size: 47.1 MB (47137539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72069f8f4220851a584759cf319dda1df252a01a6128f74b28d99dcc4423cd99`  
		Last Modified: Tue, 16 Sep 2025 00:16:15 GMT  
		Size: 125.6 MB (125622201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47fcbf2a5269112e5086a9b9c12488d462fd3194297d5a09c551101a5c547d2a`  
		Last Modified: Mon, 22 Sep 2025 22:59:21 GMT  
		Size: 80.0 MB (79957853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86918f615c83458ed107d554c64ea197c1d6e04d058ae089d2da89e99b983540`  
		Last Modified: Mon, 22 Sep 2025 22:59:00 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6566b95c414a41423d4a8b8670eed4bbdd7bd0671212bf1a069033c1957126c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2e88b4d272ef9dfacda19fea8a411ff57a96d8039b70580296d2b870a3d9b0`

```dockerfile
```

-	Layers:
	-	`sha256:2d509d726527c65d6b9b3456d814e6d223d35552ef6077dc54aed0185ff21ba8`  
		Last Modified: Tue, 23 Sep 2025 00:35:19 GMT  
		Size: 7.4 MB (7386354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7b2c03b0042009eb2b301c3d7e48744c80372989e0b3ba0dd80e98ec46aa1ff`  
		Last Modified: Tue, 23 Sep 2025 00:35:20 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json
