## `clojure:tools-deps-1.12.5.1654-trixie-slim`

```console
$ docker pull clojure@sha256:f8b6ecc9cfed124d3704d89add51291a04c3e20f6ec782625cd17f2d7245f927
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

### `clojure:tools-deps-1.12.5.1654-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3c68a45d5b711b7222a3c2faa9dbee22f71f65b54a580785d6c401bc00ed63de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191312759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35d91145f8eceae2f5ff59d4516a9660a12d5b6806c59e269a0728de83ebb2b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:22:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:22:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:22:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:22:16 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:22:16 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:22:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:22:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:22:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:22:31 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:22:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d4dbf52a23cbbf2510a763d58e06fbd6368945cc45e2afe391d5f208d25455`  
		Last Modified: Wed, 24 Jun 2026 02:22:52 GMT  
		Size: 92.6 MB (92574577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b614f9a711e49469fa67228465693dd14784a1f40e830bac760d98bc792ae2`  
		Last Modified: Wed, 24 Jun 2026 02:22:51 GMT  
		Size: 69.0 MB (68951724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4ddee1f848d6b119f0c7104b1caed9c0dd3bd4906521e34dbd34bcf1572090`  
		Last Modified: Wed, 24 Jun 2026 02:22:48 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5845da5585c65618552f8a9b0f5937dc2530f78383974058849a4918307bd8`  
		Last Modified: Wed, 24 Jun 2026 02:22:48 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:351d78a464338494ba51ba142c966d0bfa121b7d477454fd9d79f040a08c76dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5241971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91ff17bd965f7317a85319a614f41ae232da8746057a000440db9e18534e2cc`

```dockerfile
```

-	Layers:
	-	`sha256:b28c154843dd30e769fc8db722a7a630d24ab584114f1f7dc1f84e99a6b1935c`  
		Last Modified: Wed, 24 Jun 2026 02:22:48 GMT  
		Size: 5.2 MB (5225324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1b0449f3a7a573440d088460680baa6d72c369b296d6ddfd278aa884de3243c`  
		Last Modified: Wed, 24 Jun 2026 02:22:48 GMT  
		Size: 16.6 KB (16647 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.5.1654-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b345fbf40e91d0e327334f9038888a9113709ab3a4ebf842eed8126aa18ded25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.5 MB (190469246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a54c279caa17563155ddae8087f31c1b0fc7eb058271b497dd69da9b1107b9b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:28:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:28:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:28:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:28:49 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:28:49 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:29:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:29:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:29:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:29:06 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:29:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6e85dde84c6da473a6b36d6fe5e759f1c3fcaa82cac4f78a827c6372d68595`  
		Last Modified: Wed, 24 Jun 2026 02:29:27 GMT  
		Size: 91.5 MB (91542238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265a456f2ce49e40a73317a4c473ff39bb3baeba2661f2f903ac3d13476a0fe6`  
		Last Modified: Wed, 24 Jun 2026 02:29:26 GMT  
		Size: 68.8 MB (68777416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7319e0fae9c60d36659ca51ab63a37f6c4a34aba591745385938a1292a3d5d58`  
		Last Modified: Wed, 24 Jun 2026 02:29:23 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f506cff295f0622efd8fdaff7b31a2a6580ede4892360ccd96387b090f8c29`  
		Last Modified: Wed, 24 Jun 2026 02:29:23 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0833bd57eeb7d0b4464a8c9665043e712e9ed8e1546a30eb3bf661e7346ad60b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5247895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0738f2c06a97670013ba2e1653254bdd9fb06ae7114f18796ca9658c170b3205`

```dockerfile
```

-	Layers:
	-	`sha256:9f44d00ac94fe2e7471c7e2697ddf359c763e48acc990d5581c06bd84f9d119f`  
		Last Modified: Wed, 24 Jun 2026 02:29:24 GMT  
		Size: 5.2 MB (5231106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61ec32b98eb6d76e728e5be45cbb9979e3edfbc6b5fe27088f6fcd8886425b35`  
		Last Modified: Wed, 24 Jun 2026 02:29:23 GMT  
		Size: 16.8 KB (16789 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.5.1654-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e65010f9b7e1563a7f326f8b99560f66b0f6206b29d1678d3ca5a95f47207c94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.9 MB (199889777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f4699f458ff98bb0d7ea42b23ca11b7d737bda557a78d606851aacde2b3980`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Wed, 17 Jun 2026 00:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:06:39 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 17 Jun 2026 00:06:40 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:57:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:57:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:57:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:57:31 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:57:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d2e9d705b633c31ee18ff0b56f7ec3ad425fb9e720182ee7a6e0f18d85842b`  
		Last Modified: Wed, 17 Jun 2026 00:10:02 GMT  
		Size: 91.9 MB (91914009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f7f8fc02103f298476a67fa95e4222c16a9a40bc5bd802e8e4b8f15b6b0f31`  
		Last Modified: Fri, 19 Jun 2026 02:58:08 GMT  
		Size: 74.4 MB (74368382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d112ee26803c2e58af945a0271c643cac43bc6a5bd16f063a81b9215cd8c9c1`  
		Last Modified: Fri, 19 Jun 2026 02:58:05 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b7447312cd70d5277882aa6225f9aba8af66b0a71e62ba4edd9137b87b7a08`  
		Last Modified: Fri, 19 Jun 2026 02:58:05 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3e97ee93efa00ecf6c11dc7fdf7af2161015d327188bef75969b83ce77fac099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3284749fe82632d3a624f9ed4762b86abce1f1a6043ae94b225d46daa3bb1c`

```dockerfile
```

-	Layers:
	-	`sha256:d5c240f36f7878be52109cdcf7191115783bb4109bc7df07c906dd245bfe4f88`  
		Last Modified: Fri, 19 Jun 2026 02:58:06 GMT  
		Size: 5.2 MB (5213019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1737f21c33197aa93a179668b32f04ac8c64e5a75fea7f84333ab7b43524699a`  
		Last Modified: Fri, 19 Jun 2026 02:58:05 GMT  
		Size: 16.7 KB (16707 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.5.1654-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:ec959d49c6535f05dd99d54d6f88ac7d7238b0ae7c6a5a5c2f30111a5c923799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188205353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce969d00045f9240d56ad33bf3ff3944cb8e9c74cce30cd13d68a11a138c92e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 04:17:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:17:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:17:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:17:39 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 04:17:39 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:19:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 04:19:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 04:19:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:19:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:19:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b6a0af2ceb4b698210b8776157288a3fb06e46aaf75d641139449fcc50ce430d`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 29.9 MB (29851381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da9f34de4476d65de9a6103dc23db503f75ad168097ef1728eb7061fa5665f6`  
		Last Modified: Wed, 24 Jun 2026 04:19:13 GMT  
		Size: 88.4 MB (88420341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792fc598f70e4c38783a7e728b9469e4bb63ab491f71530320aceb69cacc7fb1`  
		Last Modified: Wed, 24 Jun 2026 04:20:10 GMT  
		Size: 69.9 MB (69932590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8290286ec0bbd2f6c71d0277640ba6dff3386f976b228e83f5c976dbdd69a753`  
		Last Modified: Wed, 24 Jun 2026 04:20:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15242e94c5de0282a83550bf8dce829e3e75c30a59e0239826fb2b29a1028ebf`  
		Last Modified: Wed, 24 Jun 2026 04:20:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:52f4ec855c3bae4fc5b84c294facd4ed7c931874d26c8be2068f2d605b7166dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634c1a4a275748016309c30a1bd5ed401e86b1dd5fdb9f4c78a001e629c73a8f`

```dockerfile
```

-	Layers:
	-	`sha256:f1735fd7130f086fdeb5ad5843935a6081d17638bd352ec894215948b5777115`  
		Last Modified: Wed, 24 Jun 2026 04:20:08 GMT  
		Size: 5.2 MB (5205810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:880f9c573f55e5ec2670c68bf0d2111cc360e55033a6d9c9261286f243cfd83b`  
		Last Modified: Wed, 24 Jun 2026 04:20:08 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json
