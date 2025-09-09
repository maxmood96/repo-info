## `clojure:temurin-24-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:ed00f5fa51887335e05ba979f0d22f539995441e7da38db3a045ed53444278d8
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

### `clojure:temurin-24-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:1b5c7fd48c2d848c7d3eda12bc40d6552d28b5a4c6e330a6cbc9b1e05a2f1c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.6 MB (219594417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2250c41087d890c027b14c3db759fbd74e9f2a2414703bf253af40c18d7003`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aac84086dbbd2b1ef555392c7936c79267a65d2625517d4991acf7b04db2dc1`  
		Last Modified: Tue, 09 Sep 2025 08:26:49 GMT  
		Size: 90.0 MB (89975233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc436de73fc9aacdd52c016ff6247baba897451b171b40234755921da865442`  
		Last Modified: Tue, 09 Sep 2025 08:26:50 GMT  
		Size: 81.1 MB (81137531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5283229997aa6427729b00f83083f49ceced7f6de40524131293b79797b7ef95`  
		Last Modified: Mon, 08 Sep 2025 22:31:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eff07671274ff55367f3a633174b592e6a2b8e801e2b7fb53fd1bc25cdfde22`  
		Last Modified: Mon, 08 Sep 2025 22:31:38 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4a4100038fcc8a50dce28fcc35613c384305c6271a477a2604415eeeb155a61f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7342720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0054727308c6b5a4702e5ed049590ff4740831fa4501b0c493f6b88e319c92`

```dockerfile
```

-	Layers:
	-	`sha256:4e7d6bf66d3a9df03e1a9b55d8336c8e0483bb519cafeb2e633b72773d77df28`  
		Last Modified: Tue, 09 Sep 2025 00:43:15 GMT  
		Size: 7.3 MB (7326222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae3e4f11d4b3fc82c09e4d4780dee640ca9d0b0ca3a6e8a39960c5ac4373a2bf`  
		Last Modified: Tue, 09 Sep 2025 00:43:16 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0b447e480cfbe3422af3f3530183846fe09c06d673b0b861c615af883849c4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.5 MB (218478325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e27133861b32ddb36116540be9700e36f39f62b1d84526eb32ae9aea0487944`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8e3f3fdaf85a9370155eef817c9fb2a753408e2d326f518eb7d725807b9d14`  
		Last Modified: Tue, 09 Sep 2025 06:41:29 GMT  
		Size: 89.1 MB (89092530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffd0f936bd79349d470796d0e68c8dd66f73213e392d569e953c0c95a21529f`  
		Last Modified: Tue, 09 Sep 2025 00:43:24 GMT  
		Size: 81.0 MB (81025735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4097c9e6b54e7471151d9f58b558f42f85f06277b8bc610077f60d90fbe35a`  
		Last Modified: Tue, 09 Sep 2025 00:45:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a277afbb340bf8968e4f84f18557972a6e414b5cf83237cf06974e4b712223`  
		Last Modified: Tue, 09 Sep 2025 00:45:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d77ed6617ddcb6d2779fccd81d8d801a9887d0698b25f151a62b46b6c6f55878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7348646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d68000d59c1dac4b108743414fc4a37c4e8be651ff15c839e2dca19ae65867`

```dockerfile
```

-	Layers:
	-	`sha256:106cb93d230525c038e7a015262750bf810709d821079a0f0c57f3afdd612ff5`  
		Last Modified: Tue, 09 Sep 2025 03:41:21 GMT  
		Size: 7.3 MB (7332006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd0f5d36af6be62128eb6e952334b8df9a804372b45ed535dd40ff74fa29da52`  
		Last Modified: Tue, 09 Sep 2025 03:41:23 GMT  
		Size: 16.6 KB (16640 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:cff21f7ecc693791d9de3fc7531c0e34efa98b18bf99606400a8d0389f77be3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229229991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c005f0782dd12e08b42399944bd46756a6ae4feb3fbd41a2271cba53d619d603`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
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
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf99ae33abe90ac926d583e1bb0999d30f5d908ae09b020378fb9feecd06514`  
		Last Modified: Tue, 02 Sep 2025 09:11:40 GMT  
		Size: 89.9 MB (89918160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0878dcd66ccf213a640a3b3bc2e4f17c77fdf7efdf7665c42140553b7759a0e`  
		Last Modified: Tue, 02 Sep 2025 09:22:20 GMT  
		Size: 87.0 MB (86972710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594a650855b7633a0839606343a7ec4d6ef493449e4fb9222ea447c2bce47c3f`  
		Last Modified: Tue, 02 Sep 2025 09:21:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347cd2beccd1455bfd5bd0d21948ecf202a77ed2d0aa26eafad2b6b446473fa3`  
		Last Modified: Tue, 02 Sep 2025 09:21:58 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:186a2bfa65432af78ef0d7254fec15c2105fdde03232959bf88546258cde51d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7342701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8cf01a342a38dcb190ed56057324d7e78d1c244b1d2d9009a291cd5d38b0b6f`

```dockerfile
```

-	Layers:
	-	`sha256:089587dba854dadff4bc7d53902a2b7dada7e20072710c98f4fbe39d0c41d1e8`  
		Last Modified: Tue, 02 Sep 2025 12:36:44 GMT  
		Size: 7.3 MB (7326143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4531b9db1681bf6affbf61c51a6917d7febe867fd8947a842ade02274fc4944`  
		Last Modified: Tue, 02 Sep 2025 12:36:45 GMT  
		Size: 16.6 KB (16558 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:95f3a802788e6f575411d7662024033c46eefa9425fa038f8b793d5a07f71d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212316092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c82febe487f0931cede22cb3121da1e3d25de576fa69fb2bda421dafb53a11e`
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
	-	`sha256:03b4a24baa0c6ba5b1c6628d50d52ab7cf427dcdd1ea7e424e55b26086ccbbf6`  
		Last Modified: Tue, 09 Sep 2025 06:41:25 GMT  
		Size: 85.2 MB (85226398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692a7616fcb3ac4dbb031bfc7fecabd205f639120e5f9daa39a330bd677b009b`  
		Last Modified: Tue, 09 Sep 2025 06:00:15 GMT  
		Size: 80.0 MB (79951114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f1c3453e7503d1f2b397d98f8b1f1615c18fc6f6e7f4d2f60e80c8d9259a43`  
		Last Modified: Tue, 09 Sep 2025 06:43:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088ebac423e69d21714330212b4a1bd3bde028644729d8cf482ae68069652ce2`  
		Last Modified: Tue, 09 Sep 2025 06:43:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:306f37d1a1c8735126a0d0db2204c368ca7de60c01cfa2809d8f47f71d2c7a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7335788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10cfcaa1dd6382ce6b31ac6fb05b60b46c6adde2b90eb604339dc123c451f374`

```dockerfile
```

-	Layers:
	-	`sha256:194e868cdbbea6259f11a3890a7f98eb909e557b5c3370069b8fa3244677d162`  
		Last Modified: Tue, 09 Sep 2025 06:39:56 GMT  
		Size: 7.3 MB (7320089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:368c9b50e1e1bc7bc8fff705afe2bd9498a057970abe5574a5aa57c0bdb84c1e`  
		Last Modified: Tue, 09 Sep 2025 06:39:57 GMT  
		Size: 15.7 KB (15699 bytes)  
		MIME: application/vnd.in-toto+json
