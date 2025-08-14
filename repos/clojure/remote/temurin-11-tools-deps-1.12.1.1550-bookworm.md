## `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm`

```console
$ docker pull clojure@sha256:4d660551f165fd612b192021cb3fe11fcdc76dabd7c407b0af7b5918826d64d2
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

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:d44e53305d60b565677dcb984f521fda9310cb8b650f167014014b392cccb171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275147055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24cab5d29b4b396f0d083365d6ade3cd432b707183ffb5d17a4c9255a95e9e18`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d57971ad6164c388834b030e5d1b581fad1e91cc4afa315abf0622fff5830d2`  
		Last Modified: Thu, 14 Aug 2025 02:15:38 GMT  
		Size: 145.7 MB (145658158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6d0cc319238a3a83c5e1a508c9568725635febaabf99f9fc5fbe4fa57b0643`  
		Last Modified: Thu, 14 Aug 2025 02:17:53 GMT  
		Size: 81.0 MB (80993741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16af47cc03e50eb37d31151d3e72cb88ee2c795240126816167036322d76bbe1`  
		Last Modified: Tue, 12 Aug 2025 23:04:06 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3d8a71cd80da7fe2ced7cf6fef432cc91adfc7b084823c683f6dd44bba7650f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7402661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eaf3a654d191433f7480d138f7e0e7f96bdbe694ff8cd9bc90460c1cf3bc47e`

```dockerfile
```

-	Layers:
	-	`sha256:f16be1dea4840b79ecd0fafa66ee306f9e22f825ce5025b9f42635584e7f8448`  
		Last Modified: Wed, 13 Aug 2025 00:35:09 GMT  
		Size: 7.4 MB (7388409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9b255d9a0b038da108af29a2be01e9dae034a1bb0a06bc5d4fc3234bfe36d7`  
		Last Modified: Wed, 13 Aug 2025 00:35:10 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cce7bbc559bfb0157d54d1a9e3c0def4ed70e7eaab4ea05a805dd43659780451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.7 MB (271671912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:414001e5fd2feaeb8fb85981749b7d914a9da0e849a3b5a2000e847f64e20de6`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5d7a27062f260b5b7635298f357d685443b07c3c074dd5acefdfb8269b58ae`  
		Last Modified: Wed, 13 Aug 2025 14:10:31 GMT  
		Size: 142.5 MB (142460557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b943b67a817c88aadb7120de1226761ad689d7e25a0a0cd51b4f41bbd34c934e`  
		Last Modified: Wed, 13 Aug 2025 14:15:54 GMT  
		Size: 80.9 MB (80868259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae98a57910ee9d4505c53345f41f06334999e384ef4345847107b4b6bbc9a746`  
		Last Modified: Wed, 13 Aug 2025 14:20:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c049db17b350355d338386f8aef689c769c659777d4a6f2d5e4919c8729f5a3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7409160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe6e9bd8a9c33467397051c7ca2c3c728810076adf5b0cba258c4cecff317d0`

```dockerfile
```

-	Layers:
	-	`sha256:6e81b49bccc401cb2cc677ae9555612422f01efac7be715c6a8f9c5e5c53982a`  
		Last Modified: Wed, 13 Aug 2025 15:35:11 GMT  
		Size: 7.4 MB (7394790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70d7de484078d01a5a6cdebabc3abc9bff7517903bd20f221bfa671b20a1303d`  
		Last Modified: Wed, 13 Aug 2025 15:35:12 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:d204a9293a1335f382bba0f3c11a845ab6e1ac9c296bfa40198c66a4ff057b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (272014099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2ff0836330902720e4df3e534caeb7cf7934a9aa351e3872eaa7452017853f`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
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
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5389df55120d593058923b0c2485af85e597dd3191bb47403241a6c5ab379cc7`  
		Last Modified: Wed, 13 Aug 2025 19:31:31 GMT  
		Size: 132.9 MB (132853300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ac0da62b5f4bf929a902c237ccb314d777aa6a29629061a0cebd2c69dc5382`  
		Last Modified: Wed, 13 Aug 2025 19:39:51 GMT  
		Size: 86.8 MB (86822076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d170f38877691df4b1ec51240bebc905266fbe0418b95c4df7173b75f83fc767`  
		Last Modified: Wed, 13 Aug 2025 19:39:46 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:44c95c1d0e92152980af6cfd9161b1bab0e5cd79be2977c04c9d7205505736d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7407298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2cde7aaa9c49513f10cc42e02a71b00e54008d10a2b4ff72f73922bfd092ac9`

```dockerfile
```

-	Layers:
	-	`sha256:f170a362fab7622373b23dc1ae4b891563fcfbd440aa41c3d0cd9290adce6669`  
		Last Modified: Wed, 13 Aug 2025 21:35:12 GMT  
		Size: 7.4 MB (7392998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24655b33d39350263ab8beb8a63ed8c518f2131eddcebad0f03336f9ecc3ea62`  
		Last Modified: Wed, 13 Aug 2025 21:35:13 GMT  
		Size: 14.3 KB (14300 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:57573a851992c14443e9c448ead26545ac1f66ac8939f63f95d58b7cb04d445a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.6 MB (252575728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25b7089370fee1597a5f4040164c1e0f1ed1e34afc993ec7f93939de5345a4f`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be9ec3d8c70183a13f19f7ac429d57435cdc5b4515a8adc177a754e214598a9`  
		Last Modified: Wed, 13 Aug 2025 08:23:47 GMT  
		Size: 125.6 MB (125622100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d7fa9e5063571899b0e690541b958d8867b51aa6f84dea6df07e62a889b30f`  
		Last Modified: Wed, 13 Aug 2025 08:23:51 GMT  
		Size: 79.8 MB (79803117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc42c9a0b49c26120dfcdbff5ee6e02f42ba089db8eb7f4b97e22a46b2981d37`  
		Last Modified: Wed, 13 Aug 2025 08:04:47 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:32994c2cf3681b98625a5f9aab9e144ace66c9fc8c13f9f0c57d810587e9ff29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7393984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66187710089300418b964c8cee2cdfb15aa25b850304468e3cb2b106d4a22480`

```dockerfile
```

-	Layers:
	-	`sha256:aa7df8564c9fcd86f7c992611c533e343c1640ebfa1f9abe33178041fb6d44bb`  
		Last Modified: Wed, 13 Aug 2025 09:35:04 GMT  
		Size: 7.4 MB (7379732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28160da73cdb540eb2a2e9ec8ad6b975be55a0b58714129fc25f73283023e80a`  
		Last Modified: Wed, 13 Aug 2025 09:35:04 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json
