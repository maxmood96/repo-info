## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:6fa131ab1a91d69ebc8ddb0145500182ab3ec2df0613c25ac81927b32e8ec90e
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

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:f54345ba7193519c647480d8661e437e75012824af32662ff4162f878b7764d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274312654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db157915b65745537955c25bf66f48d8b9426b6ab26f21a73c9ac3a470c00f9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3851daf9f0fb1d81ef79a85782aa226e9ff640b89e7e1c0a1fafc5090b8719cf`  
		Last Modified: Mon, 15 Sep 2025 23:26:21 GMT  
		Size: 144.7 MB (144693569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9faa97f4c6b7d624c7212168420f31d790490dff3aaacde0ac350bb5a2da1cdb`  
		Last Modified: Mon, 15 Sep 2025 23:26:53 GMT  
		Size: 81.1 MB (81137434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b44622ed17ccb174b7f6a60e5b96acb4bcc7ab8ded382facc7b3652a4effe4d`  
		Last Modified: Mon, 15 Sep 2025 23:26:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7923ecde48684daaaaa159c4f2ca84678fe116624ad23a53e89ea1ab0f0711`  
		Last Modified: Mon, 15 Sep 2025 23:26:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9b213d48c1722af947c3ea0515d3cfeca828560972730d96fdd9141f1e81e65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7390711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ad9edd6da9b300c52b7f1756ec4c67cccac7f4d62a02e82eeb9f56cfddf520`

```dockerfile
```

-	Layers:
	-	`sha256:34bd1a6997784d3a670c2c2fa2d7be89d0430405f87497670806bebdecaab657`  
		Last Modified: Tue, 16 Sep 2025 00:38:36 GMT  
		Size: 7.4 MB (7374890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26a726c8992ec40f0a4b1d24c6158ab65114d3158c0ba37af57e392a9c1b490b`  
		Last Modified: Tue, 16 Sep 2025 00:38:37 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cc75bfa81211586c846e0e0f9cb4d414ef586f283f2347df4eb6866129857b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.9 MB (272928071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a9e77065f357da8d3c0c85b8ab8a5441ead6ec52ea4fde1df958c291b18464`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abd40d4ce426ec4143e0c9b84cad9888472f1fbbe6b66ec4e861e96f7d88817`  
		Last Modified: Mon, 15 Sep 2025 23:26:38 GMT  
		Size: 143.5 MB (143542168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bb0eb90d3e5b2c75c48194ef80b265a39bbaa935652612b25844dad089424c`  
		Last Modified: Mon, 15 Sep 2025 23:27:03 GMT  
		Size: 81.0 MB (81025845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5234aea3b8d0888abda3862e30ee49852441dd9f29796c25f8cb092bd6afbab5`  
		Last Modified: Mon, 15 Sep 2025 23:26:58 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23ef925fd72b7c5634aba4fa71fbebfba52bfa90dbcb3757a920113f6628803`  
		Last Modified: Mon, 15 Sep 2025 23:26:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:de51058d25e0dac2b04343d7bbd740a8b2f7fc645cee6cb86d055e4ff06515aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7396592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90974beb78e77cb6b7b38a5e1e1eac38eb71c4fde3b6770a5bcf76c86a696821`

```dockerfile
```

-	Layers:
	-	`sha256:b70c7d0035344a9c2dcf8f303dd09b849b69179bd4f93f57014d724b35975663`  
		Last Modified: Tue, 16 Sep 2025 00:38:43 GMT  
		Size: 7.4 MB (7380653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cabdf12023e36748d2bc485cf1ae9f5491243dbbf549a49c7b6a96444a459051`  
		Last Modified: Tue, 16 Sep 2025 00:38:44 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:e87d83ca9628f684f69fa4e4bc07b94bfc7dfc70241ab2dd0eb78a4a46827ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 MB (283679241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47e7fbcafe521275764f460437094243e87fc4e60b41ef72c95f2bc24a4e3d4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:64b8116dd43c29a2a4aa3131cb4895af0a7267cc5883e3761556e54c369be9af`  
		Last Modified: Mon, 08 Sep 2025 21:22:08 GMT  
		Size: 52.3 MB (52326822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa04790d770a4c6530b1f54473b8359d7d96b09778c91643ceafc820831a8f0`  
		Last Modified: Tue, 09 Sep 2025 19:07:45 GMT  
		Size: 144.4 MB (144372674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a956a14fc99f1a3056e78ab8ad6ee8b7c9d2421f1cc9df59e96fc11fdd9bb395`  
		Last Modified: Tue, 09 Sep 2025 12:27:11 GMT  
		Size: 87.0 MB (86978700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a63d182b86c4b4e392627b3f73d44329a72e3317cc1918d28340a373196a9d2`  
		Last Modified: Tue, 09 Sep 2025 12:26:59 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf555a17752faade478104b97a74dec42d64ccc71b1bfc593087367eb7372c5`  
		Last Modified: Tue, 09 Sep 2025 12:26:59 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9431aee686bac814ab38e752eb418fa0e940cbc01b3f484e75acdeded934cd02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0800c37fef8432f312622518f4ede22685e5b7b1d70d0b5aea4dcd0396ce70`

```dockerfile
```

-	Layers:
	-	`sha256:c112fe08dd18cfbfc4e51abe0adf0f5c60bee12aaf1eef321f4e664baee76d61`  
		Last Modified: Tue, 09 Sep 2025 15:36:13 GMT  
		Size: 7.4 MB (7380104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10eebb9cf353b79dabf085761b23fd002ae6715c5d4b751b4082bbab2bac760e`  
		Last Modified: Tue, 09 Sep 2025 15:36:15 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:107dbfe714518209cab524d62d14801473dcddc3eb4dfa16e9912ed1f96ac01e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261813991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce0c0ef33f2e9e4284c7c6601ba30714ad8815dd9aa8604e77b91a998bded22`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:67e2d91fae4fd9af13e4e364bf8120dcca7856e8273995cc0651acae70b27e8e`  
		Last Modified: Mon, 08 Sep 2025 21:18:01 GMT  
		Size: 47.1 MB (47137539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8843e95de3b1ace4a43d04712dfdc42e0120d2d94fa51587c513edbe44eb405`  
		Last Modified: Tue, 09 Sep 2025 06:24:16 GMT  
		Size: 134.7 MB (134724248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac129a09425a16e432c85cd3e4e51784df57f1bd5204ca81d09767d9740f76d`  
		Last Modified: Tue, 09 Sep 2025 05:39:13 GMT  
		Size: 80.0 MB (79951165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a3b06fd2d1f8638dd0d88950bd343819ad57e4e08ffc4ccddbdb162d6bab8c`  
		Last Modified: Tue, 09 Sep 2025 06:17:22 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e7208be6219365c51e53eef1a8020543c570f987ebc9fd196e227cba2a3398`  
		Last Modified: Tue, 09 Sep 2025 06:17:22 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:89b83e62e50e54ce7bc172fa55806ea978b4a2aaef3169e6b9b45eb0ae5bdc68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7382030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e7a4f834d0003203093cbf2e0df9b166dbee046cd2e554270a02ba2378a280`

```dockerfile
```

-	Layers:
	-	`sha256:659109ceacf140b04bbabb28cca5c551e8b6ab2ee2370c7a32245be5663ca4e8`  
		Last Modified: Tue, 09 Sep 2025 06:36:41 GMT  
		Size: 7.4 MB (7366209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d83a6ffaf5cbfaf422c7552fb4024e772d9bc2bc29ffd37371c8e6903530b3db`  
		Last Modified: Tue, 09 Sep 2025 06:36:42 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json
