## `clojure:tools-deps-1.12.4.1602-trixie`

```console
$ docker pull clojure@sha256:b2cf02ae436843a3c2d82a9aaf10657b9a8250aac0cad1aa592ebbf7c4faff9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:tools-deps-1.12.4.1602-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:41fe51f439f1cff3a2365d2a67f4afa7ab40cac792100fc66db37f7253820262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 MB (227092350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffc43b878856c69c4a97611f2572e42ea1e44e5d87c9be09e182a407e52356b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:07:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:07:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:07:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:07:29 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:07:29 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92858be8554371333c98873c16df056b7de4306d2cf737c061a2703742d53d0`  
		Last Modified: Thu, 05 Feb 2026 23:08:07 GMT  
		Size: 92.3 MB (92256235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55d851f34a82c0647c5f54dd5e51032c69bd40bb02739c6b9aa4f549935ce3e`  
		Last Modified: Thu, 05 Feb 2026 23:08:08 GMT  
		Size: 85.5 MB (85542122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f964094e3b797db839c1488ef01f31b1f0471dfa02008bb487ba578b40ab58c3`  
		Last Modified: Thu, 05 Feb 2026 23:08:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14fc92374ff1aac2a7ad282623550919de08dc518beb9a20e102879f193593f9`  
		Last Modified: Thu, 05 Feb 2026 23:08:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:266e9bdb7472a3476af3fed58f73adf9944f582c56f0437090626604dcf0c0eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7453561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a0fddebbdc6f33d9d9d66e9ada2c56afabe555cda7454a2eb60dab820d8fc34`

```dockerfile
```

-	Layers:
	-	`sha256:8660ba948feac0258b961e2f545e0785d371647be15b4ccb18ed044289675cbb`  
		Last Modified: Thu, 05 Feb 2026 23:08:04 GMT  
		Size: 7.4 MB (7437146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab0da634baecbbed6a7a8635a83419b72e768431841fe5b6cadbb0c693e300f5`  
		Last Modified: Thu, 05 Feb 2026 23:08:04 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:609e5bf371f6589a611195bae972429225f5890e1a26bd8dd4b740d1e9f74a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226302431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3702da48ddf1a61dc3cbcbef31743f0a65e49268217994dbf154e52edcd1ac7e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:08:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:08:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:08:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:08:51 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:08:51 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:09:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:09:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:09:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:09:10 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:09:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b312c8ee0f5541625c019dd2083b6b6b2513f2e31fb27699630f3ab1c3b2d0`  
		Last Modified: Thu, 05 Feb 2026 23:09:34 GMT  
		Size: 91.3 MB (91288273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9364664c1f9c4d03a0e2429cb06d5faabf04452cc0fdbecafffb1c7518975e1`  
		Last Modified: Thu, 05 Feb 2026 23:09:32 GMT  
		Size: 85.4 MB (85361099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90703644bd61bdb963b5d60210253020352cbe5239efa8aff8be2866251b8ea1`  
		Last Modified: Thu, 05 Feb 2026 23:09:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fd6efbc33d6d8824cb17dadfdb828a32b9f6831224b2d48f2eabb89a120c3a`  
		Last Modified: Thu, 05 Feb 2026 23:09:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e2da6ca47c866f88d7d84ecbd197267fb3407d541a02ec70f522712181558991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7460754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8b2515417d5694f3cd97531cca4a5a8beee96fd0fc45fdd5f761c44bc9d47c`

```dockerfile
```

-	Layers:
	-	`sha256:e70ffa85225bc637204b3d6cdfb35eff1ce47f151a6e07b34a8ffc9f14f4dc7e`  
		Last Modified: Thu, 05 Feb 2026 23:09:30 GMT  
		Size: 7.4 MB (7444197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4eab5695f5183bd5b29c3fcfdbea55477ac162e9f2cb665e721a2f4e3ac826a2`  
		Last Modified: Thu, 05 Feb 2026 23:09:29 GMT  
		Size: 16.6 KB (16557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:0d463731e66b1289462895c7c89249269dc0361584d8873bc4c57656b8675b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235693564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b319f930a00829982ed3c066c41e674dd1aea7f19a1a5421f9771ed5da2318cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Fri, 06 Feb 2026 00:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:48:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:48:05 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:48:08 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:53:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:53:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:53:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:53:29 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:53:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3230ebb877a1444adbcad5521afaffb1c41773004c4324fe65c2c551a9cc1544`  
		Last Modified: Fri, 06 Feb 2026 00:50:07 GMT  
		Size: 91.6 MB (91632873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ef605411196c730ec201e18c625f2cabfc5fb83efd9aa74fadd830038fa9a6`  
		Last Modified: Fri, 06 Feb 2026 00:54:13 GMT  
		Size: 90.9 MB (90947534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f44e46ba657109043e4bd78d3e9efe1f54b96ba06b92d73b3b462d3a1921ef8`  
		Last Modified: Fri, 06 Feb 2026 00:54:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655167cc00123f09c2a88756e426950971b5bfb6f02d958b0054e20f8bdf753f`  
		Last Modified: Fri, 06 Feb 2026 00:54:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:526c8a40fde65cdb79e643ba93cc7c1d5f24263c3015cb2b4f1aae7eba43e9c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72f5adaeff4d06b2f123d62826603269cbf4b2ed3e6128d35b22466567a1e4b0`

```dockerfile
```

-	Layers:
	-	`sha256:c4537acfbea9a2bd7b4785bc81466cac232b5f2d5410fbea4a80e639b6b8c107`  
		Last Modified: Fri, 06 Feb 2026 00:54:10 GMT  
		Size: 7.4 MB (7424891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8223cff37f3ff2f93ab9f019d111aebf466e279cfc1a9cd93b06b0ed73dbd444`  
		Last Modified: Fri, 06 Feb 2026 00:54:10 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:d5569ee77cb3ebcf946dee5a7847aff6c8494794b99bf7b61da8e7a70af95ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222976497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ceb23e150cde9679316e50fb4570cecb5568c47a471d5bac776bde32b78895a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 12:53:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Feb 2026 12:53:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Feb 2026 12:53:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 12:53:52 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Mon, 09 Feb 2026 12:53:52 GMT
WORKDIR /tmp
# Mon, 09 Feb 2026 13:17:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Feb 2026 13:17:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Feb 2026 13:17:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Feb 2026 13:17:05 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Feb 2026 13:17:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:618efd37f74728f7dcba60c231fad7f2d777dc65e4da32d0adae5e032e1fd125`  
		Last Modified: Tue, 03 Feb 2026 07:13:10 GMT  
		Size: 47.8 MB (47776763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b3877762b7849aab190bdd4be4bec0fdbb7a69de6798289c7ab36fcca52b2c`  
		Last Modified: Mon, 09 Feb 2026 12:59:49 GMT  
		Size: 90.8 MB (90773405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7a7bd39b64d0ecb8e2cc915d3c5439746c541601c6300994a66c45379fdcb3`  
		Last Modified: Mon, 09 Feb 2026 13:21:34 GMT  
		Size: 84.4 MB (84425281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9673f630eeaeb35ec8357819cbd1a9dd8ad789789e4529ca630afa2ebac361`  
		Last Modified: Mon, 09 Feb 2026 13:21:20 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085a0895fdda4f397f81a0b372fd0fb6ba827fb6047ee1fd5aebb5aadf429841`  
		Last Modified: Mon, 09 Feb 2026 13:21:19 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6f5eeba02584c02b4ae87e440262e258109157a2f8d652ac931aba174040c5ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7423559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a773f93a951fb71e638fb79235b158d356cc55e99c17628b5965f61ed96227e3`

```dockerfile
```

-	Layers:
	-	`sha256:7b2ba88d4a556718cf507382514a6b77830c14a7a1f7b7582960d7ea5a3c1fb9`  
		Last Modified: Mon, 09 Feb 2026 13:21:22 GMT  
		Size: 7.4 MB (7407084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba9487606bdf153d91e4c66c11380a1195cdd173e0217de6f09d3568f07dd7ca`  
		Last Modified: Mon, 09 Feb 2026 13:21:19 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:ff2d5590a26975b31f7c81b888feeb3aae6eb5d226bf8a9829754889c4a828cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224100729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d07a1ee7045f51f67f43d722b67054273cb6902900f320fb8094d9ef8937ec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:10:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:10:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:10:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:10:02 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:10:02 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:10:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:10:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:10:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:10:19 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:10:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d40740951f761fcf182da5ef2e4beb87519a160e4c4d14aa7d72ad29502c348`  
		Last Modified: Thu, 05 Feb 2026 23:10:51 GMT  
		Size: 88.2 MB (88233801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d88a1607a18a8ebe74bc4f3e5b3fe41b228bd6c2ee2907a7c81488847f58a6d`  
		Last Modified: Thu, 05 Feb 2026 23:10:51 GMT  
		Size: 86.5 MB (86511508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85efbf24b3c4a71bedea861ba59e63d1c9a108b9fc1a2a83931b0e48407452a1`  
		Last Modified: Thu, 05 Feb 2026 23:10:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcc23280333daeb83ca17a9a12022cd3fd97f3092fe75b7eb7ea1df1ebb5a48`  
		Last Modified: Thu, 05 Feb 2026 23:10:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a46534d910512ad2802bddfcbb8d1f74cffcfc3963b64573f9e7bc5ec7ad1274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4484feccc8574034e951686f48e09d2565a3008428415f81780eee6c9ea9c91e`

```dockerfile
```

-	Layers:
	-	`sha256:2bb0833d2cc756ad76e489bd42f1e8ccf4291c4f581c22783e02125246c8116f`  
		Last Modified: Thu, 05 Feb 2026 23:10:49 GMT  
		Size: 7.4 MB (7417630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1bd9dc03726b12e263a74f02bb5680a2490ba0fa5251383d05ed2ad24a1cd71`  
		Last Modified: Thu, 05 Feb 2026 23:10:49 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json
