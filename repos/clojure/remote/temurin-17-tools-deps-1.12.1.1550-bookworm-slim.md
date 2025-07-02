## `clojure:temurin-17-tools-deps-1.12.1.1550-bookworm-slim`

```console
$ docker pull clojure@sha256:b2bb2bc30571ea7f7151b18ff5be192f02f6b88fb7c04a4a3cde472c7cf1704d
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

### `clojure:temurin-17-tools-deps-1.12.1.1550-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b86e5ff64c49cfbb3e66002b9545c6676e92ee443ad36cade17d106aebd3d94c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242399705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2901062cb84b0ae22c97c6d061f41ec4931be022857280871389ef4264b26a0e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a45df6d8358f3e431a23633e91a199a1ee5dab564b57bb88c338e506a724c09`  
		Last Modified: Wed, 02 Jul 2025 16:36:37 GMT  
		Size: 144.6 MB (144635025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed0fb610bbad8a869a83c215223ae04ab1cc9f0e4a632aa8296187393d0dcc6`  
		Last Modified: Wed, 02 Jul 2025 04:17:13 GMT  
		Size: 69.5 MB (69533497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d178b02174c37466ea8056b8669c6b7a0d0caf53b778c9296322ddf6681dc8`  
		Last Modified: Wed, 02 Jul 2025 04:17:01 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68183a8ada41f6d765e7450d770a996efbe8772a58bbf492cfe5d829dac73257`  
		Last Modified: Wed, 02 Jul 2025 04:17:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:90fb29453e1d230fd0eca939c0e255a7a7919691d565d07f995a9b8ed0492f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5127123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9865e52ae91205b469a8b6afc37ae24fa13a4178a6cff36685fbe4d7e95051c9`

```dockerfile
```

-	Layers:
	-	`sha256:6ecf744786059f6e56c90578f049e0dfa917d30fc1d9a25a89d8f7d6b42353b7`  
		Last Modified: Wed, 02 Jul 2025 06:37:12 GMT  
		Size: 5.1 MB (5111244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edce24f01d36c4db2614c5b6bfc38e3cdcc30de365aa206dd814cd1970b83984`  
		Last Modified: Wed, 02 Jul 2025 06:37:13 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1550-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:000610b61dc4c480cdea3f42fb37fbbbca873fa802b1e72577b17d73cabfd6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240979990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd8018fc9cfaf8c11c851c1b85ec4c3e966647425963149a75eb899b2784af6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4370cb4e407f51b3e5ccb42a1500ca53f0f4997eca8c4faaba10b2d50835b01`  
		Last Modified: Wed, 02 Jul 2025 16:37:28 GMT  
		Size: 143.5 MB (143512648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7624b4cc1f9fcebee7188430f4944e5b07c873e20b8f812f3ba121fc1bb07b00`  
		Last Modified: Wed, 02 Jul 2025 16:37:23 GMT  
		Size: 69.4 MB (69388626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ad9db1c5ea0e265ad3247fb7958c00408040bdfb8777bf74cc2481bd591309`  
		Last Modified: Wed, 02 Jul 2025 12:37:11 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecae8e9738e2cb21359d15b0c3583dd92eb077eea309353127d97b254f7f1cc8`  
		Last Modified: Wed, 02 Jul 2025 12:37:11 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4d4d5bb65c7ca9070a36d3407f09078f6b268d1092e2044bcb212410b8fed73f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772323965396f5b826e24100014b5218fe6af76f37241a5c1767e4acb4a11a70`

```dockerfile
```

-	Layers:
	-	`sha256:964f3688233f89cf94590a3e1c88866d62883417fccba4ec0ec28c090e645fb2`  
		Last Modified: Wed, 02 Jul 2025 15:37:19 GMT  
		Size: 5.1 MB (5117005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3917eafacc332175cfb7f15b532fe297b18b97082e7c9d66ab3ecde4504c0fa9`  
		Last Modified: Wed, 02 Jul 2025 15:37:20 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1550-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:dff2cb68f41cb698db6e835717b88a75f62fdef9a77d93c5874d0cfbefb7a58a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.7 MB (251711925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90273af22f51158bfddfc08795e27267fb48255803d4c1547e07e2935fa23d74`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d39b5ad0aca1717411c21ec9d19535e2458a542bed0a4b7d353c7a37608838`  
		Last Modified: Wed, 02 Jul 2025 10:28:34 GMT  
		Size: 144.3 MB (144280328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c39e08f1150892503b31e0ed384c02978cf92600bf75e409661a798ca1bbd33`  
		Last Modified: Wed, 02 Jul 2025 10:37:35 GMT  
		Size: 75.4 MB (75357733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbfd9f2e645c17b79085f3f0bed0360f801c6259be1c5dd62a4560f2537dbe5b`  
		Last Modified: Wed, 02 Jul 2025 10:37:32 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47b304c498f23565f892671e4034e4ec8fced9cfb36d02490e1034d5fd69e88`  
		Last Modified: Wed, 02 Jul 2025 10:37:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eee3d4f5f72c47759c929d20aa7a0aec84c97c7137bf5bcd716894b43675da36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:285b938a15da538aaccde577dc076f92d38de87bfd099b52f8ad8956e0e1e274`

```dockerfile
```

-	Layers:
	-	`sha256:8d142403189616523e4362e1d3d67fefb6acae8ac5aad6e1b99009d1986bff26`  
		Last Modified: Wed, 02 Jul 2025 12:37:03 GMT  
		Size: 5.1 MB (5116402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf33934380441cf73d0d931aede370a6c0a62e9fef9443bf53adea0c4107cec4`  
		Last Modified: Wed, 02 Jul 2025 12:37:04 GMT  
		Size: 15.9 KB (15927 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1550-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:0d457096a88032673b995e52fb781fab384e97b127a94243dacf9b8df99d2737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229901254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d3c84cdd7a2a5525203c4299aea8bc4c556bbdf87fd95effb2d1bdfa4a7fc0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c17bf3255034d3ee3075027258632c7f732d2ef9ff7fc7e48f881cfcb6c558`  
		Last Modified: Wed, 02 Jul 2025 06:35:41 GMT  
		Size: 134.7 MB (134673602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf0005f8c569fd06589e54fcc8202c2826bd6113366226051042df97924e5fb`  
		Last Modified: Wed, 02 Jul 2025 06:41:02 GMT  
		Size: 68.3 MB (68338801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe1361670f32c290bdae2461891629ed497230d99d7dcaff11586646a3b00df`  
		Last Modified: Wed, 02 Jul 2025 06:40:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90768993d361e6829ff92fa2897990e5e1e4f6b2517666165dfa0fb7160ee3cb`  
		Last Modified: Wed, 02 Jul 2025 06:40:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:36034b0253821a632f628a018ffd1560b0e447ae2added0d9fdc89144d713117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5118444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37597f937aee124b16a9e56d584ee4b84e60dfe4e2e1cca93c515aad09f1078`

```dockerfile
```

-	Layers:
	-	`sha256:b4702afbe151bff82104e54019f74e35ec2430c15d6af68c585c2ab127490b86`  
		Last Modified: Wed, 02 Jul 2025 09:36:53 GMT  
		Size: 5.1 MB (5102565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:818b1e6b49154d75c0e3ac04714c38700e2c63ee15579df55c1baee09b7dd197`  
		Last Modified: Wed, 02 Jul 2025 09:36:54 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json
