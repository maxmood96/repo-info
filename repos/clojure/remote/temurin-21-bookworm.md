## `clojure:temurin-21-bookworm`

```console
$ docker pull clojure@sha256:136b0fb222a147183778c41a2e67c7b4dab9bd2d778e6959f4f8d813d9d976a0
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

### `clojure:temurin-21-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:ae0613890ea2fa10ee4f5592bc3563797aaa9d5383d54a72b49591a1e1cfb9d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287508177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26d80f0b8d20e0a424890bea146cb2a7c9084ed95595a608e37a161c5a00817`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:47:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:47:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:47:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:47:30 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:47:30 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:47:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:47:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:47:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:47:45 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:47:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165fa16390016cbfee03a621e23e06246f9110f88040b03d695af7b117fc2c3c`  
		Last Modified: Mon, 02 Mar 2026 19:48:08 GMT  
		Size: 157.9 MB (157857067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b418f60ca5721361fd0c7e7a8506b2cfe8bdaa9908c3b65cb8ebab1d52cb49b`  
		Last Modified: Mon, 02 Mar 2026 19:48:06 GMT  
		Size: 81.2 MB (81161293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668d48373d2e65696d9b976b1f9c64c75703e163f58c4ebf3dbe002a27fdd427`  
		Last Modified: Mon, 02 Mar 2026 19:48:03 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5149d57ccce8f590bf6d9b8a9a78fb09ac8f932fc78a187446f75140380cf06e`  
		Last Modified: Mon, 02 Mar 2026 19:48:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d85becb70fe3887eb1905834fec8ea23567b90011f2e4e3045c179ddee2550c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93866c25411ddd59bbc7fab4f35159a70e1d4b016a8e4d587f11ad3df2935afe`

```dockerfile
```

-	Layers:
	-	`sha256:b9b18dbaa86443f8c119905e651fc0a39787ab796d653261967739886eed382e`  
		Last Modified: Mon, 02 Mar 2026 19:48:03 GMT  
		Size: 7.4 MB (7380838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:788df15ae50f81eb0fa157b4ecb9f2385b8c375d317d7ca507818d8b2869a662`  
		Last Modified: Mon, 02 Mar 2026 19:48:03 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f02c277657e44b2ce529a34d32ebe94d66fce4fcd70aa817b5e89077ac8e4e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 MB (285662361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd6e03cc9bb39ce5eebfe1f6a3b8a250b492012fdc6c938c7e584cdf8a28d36e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:47:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:47:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:47:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:47:23 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:47:24 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:47:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:47:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:47:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:47:39 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:47:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40afa6ae8fb1e2dfb65cb78b8aa0a1ccee54fdbae0e67d45a704df91c54fc3ba`  
		Last Modified: Mon, 02 Mar 2026 19:48:03 GMT  
		Size: 156.1 MB (156133055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f7824b4a7aefef6a2e28925a9dbce8885e6d99a06cfa56fa416555a23d8c6e`  
		Last Modified: Mon, 02 Mar 2026 19:48:02 GMT  
		Size: 81.2 MB (81155053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ca2c07e3086fa3c66ed3fdd4f2c2cfed94b9eb37c7f0cafcd041908846e99e`  
		Last Modified: Mon, 02 Mar 2026 19:47:59 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be2377b042c86d4b0a72fab163fac740811781d65bc433a7e924d9c74ab4a230`  
		Last Modified: Mon, 02 Mar 2026 19:47:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:aad634df5e7789b193596699c90ad40dca90ce0bc9e3aad9f4e168d1e302c737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09db600b90a97a6cbeec55c25c89ec2f815256b3e1170c1ec9579c26c3caa4d3`

```dockerfile
```

-	Layers:
	-	`sha256:0cb63c01a48f0c3adac031d7ac7620ed1014aa9accf067caf8b176668d57675f`  
		Last Modified: Mon, 02 Mar 2026 19:47:59 GMT  
		Size: 7.4 MB (7386625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e87fc6ac6b77077e56d4f65a241a01777adb3a63477d9f8a33f0092af6a8fb0c`  
		Last Modified: Mon, 02 Mar 2026 19:47:59 GMT  
		Size: 16.6 KB (16604 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:d1e0799207dcea3b6566ab7629444b85c8f268a7fc5d2129ee39f965a5a9659d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297318853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53ca9d7172c5d02a9e55751d26ab777f9b5ceb3940c68a596e40f086ed92d79`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 20:01:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 20:01:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 20:01:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 20:01:38 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 20:01:38 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 20:02:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 20:02:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 20:02:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 20:02:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 20:02:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:707f909064f2c92eba706235fb16d4e638f0edff62392500d69d99fae17bc6f2`  
		Last Modified: Mon, 02 Mar 2026 20:03:19 GMT  
		Size: 158.0 MB (157977536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a33c77cd2db5afd893286eae805edad88894fd6989f17ab2738f12e56f7862`  
		Last Modified: Mon, 02 Mar 2026 20:03:23 GMT  
		Size: 87.0 MB (87003475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a463ddbb0a0a9d8f8040c32c17c4aad86fcf4e51ed08ed799f3db0b58c5377f`  
		Last Modified: Mon, 02 Mar 2026 20:03:14 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8637c17355cfaf2278a04173d50fae491ed598b4f24dd2b0ddd54b1a3423e2`  
		Last Modified: Mon, 02 Mar 2026 20:03:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7017c65467bc2219951bd415942357b8a68fdb8f6b70252e0da2e663143343dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7402588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f982e0b8db7309e0b8788c1398c3af56860d5c55d2eca10ecf2f3f9c7dac2b`

```dockerfile
```

-	Layers:
	-	`sha256:f8f6b086bdb6d45c76b78d02aa394c4e9561ee020f367c2c938cada312bca1ac`  
		Last Modified: Mon, 02 Mar 2026 20:03:15 GMT  
		Size: 7.4 MB (7386066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b80571ebb05f2343456efa817e4a35b535d6a76a75ac11d967302c094b8b76aa`  
		Last Modified: Mon, 02 Mar 2026 20:03:14 GMT  
		Size: 16.5 KB (16522 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:9bc7edce73cbf92a632ba6f531a62e2a5ec02d027c965648225c0a0f8392c839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274228967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3aeaa7c480760d94eaf8a3cd548645b00309a05dc37f34fd03f784d0beb83b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:47:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:47:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:47:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:47:11 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:47:11 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:47:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:47:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:47:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:47:26 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:47:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6f63a08a710520100a0c278ef46ab61440421eee50fae9262f4bc544fe5cfd`  
		Last Modified: Mon, 02 Mar 2026 19:47:59 GMT  
		Size: 147.1 MB (147105211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b34400365409cfc30e7cd1289ff216a124bfeaab203af1666996bd617dd77c4`  
		Last Modified: Mon, 02 Mar 2026 19:47:57 GMT  
		Size: 80.0 MB (79974623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6813a6b226c5b98e2ca886f9ab9f13c88d451373463a1a7417677d854296f3bc`  
		Last Modified: Mon, 02 Mar 2026 19:47:55 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3515838cee1b57b29b77ca47e5085df2148fe74326bcb64f70370ac44be1e93b`  
		Last Modified: Mon, 02 Mar 2026 19:47:55 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b71fc8c097634f2be066e30e88afadeef6fd43b5398463629bd0a19fdcf02d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0ad7f914de91eef31cf9a1341c02729bb079c2929553d24939ccb87354d7df`

```dockerfile
```

-	Layers:
	-	`sha256:8f14a4db3e4e91d613ea4da90d98a474a28f18219c088905cedf2592431ebbb1`  
		Last Modified: Mon, 02 Mar 2026 19:47:55 GMT  
		Size: 7.4 MB (7372157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02bd3a10311bc128e6c46c9fac4e76b40394d1f7883dd6e702aefae7cc886401`  
		Last Modified: Mon, 02 Mar 2026 19:47:55 GMT  
		Size: 16.5 KB (16462 bytes)  
		MIME: application/vnd.in-toto+json
