## `clojure:temurin-17-trixie`

```console
$ docker pull clojure@sha256:96ce7e6c1debd099787a289959b95f81ce7e269f3537123c94772c9ef30f80cd
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

### `clojure:temurin-17-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:f718f5273dbcefe96b8c9f3cae78ed79b10ba102f10ab40f4196a712d4931e53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.5 MB (282477464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a433c33ad6ba8d5193ed2d60e67dcf2089df31e69af32d1887a888277c4c7a12`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f468d8f3423213f3894fece5d145d047cfaa51db26ba948678536c902df5358`  
		Last Modified: Thu, 02 Oct 2025 14:10:58 GMT  
		Size: 144.7 MB (144693589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78f0ff8e60155359cb4913921dd9df80f803fe7e72f3e101c8755142154a574`  
		Last Modified: Thu, 02 Oct 2025 08:59:33 GMT  
		Size: 88.5 MB (88498207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7de4c5377f888f6ce494e486d1dd6a72acf47fe034fa651d06aed06850cbba5`  
		Last Modified: Thu, 02 Oct 2025 08:59:15 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57011202db2686e0c6e9e6c0993cda3e3dda50c594ef586bf9d571d5d0c7d35e`  
		Last Modified: Thu, 02 Oct 2025 08:59:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e7b7ff51df7aba47666ec93d23ee8c27a26f20f8f58b4239fce3bf97759e79d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a9824449f04b7ebef3155ed6a8b802ba462e91ec496bd8738f63c2c697c246`

```dockerfile
```

-	Layers:
	-	`sha256:c6f67e0a4db7ba485ba1214e7939047fc610c5fd6cc3d840d166405b4f69939b`  
		Last Modified: Thu, 02 Oct 2025 12:39:48 GMT  
		Size: 7.5 MB (7466899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b52388052c71a4a1b0d4d3c0336e81a60dc8e64847656b4fa4d855e65c7c8ab`  
		Last Modified: Thu, 02 Oct 2025 12:39:49 GMT  
		Size: 15.8 KB (15796 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:573a5faab0035044199dca839c5bb9a7de700fb0e8cbe9e06b2bfd96b051e0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.9 MB (281882368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d000f54b3ceef1a61c3f1999d63b35207471c98a7dfa265be0bf7f2cec866888`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e38d1930ae6419042590ec372f58de328029c453483a34de0f7aec09ae1d90`  
		Last Modified: Thu, 02 Oct 2025 09:50:44 GMT  
		Size: 143.5 MB (143542162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20eee459f214dcb00cab6b3e37eab4cab9fbada6298a9925772e59eae9b3c6e`  
		Last Modified: Thu, 02 Oct 2025 02:45:12 GMT  
		Size: 88.7 MB (88690471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70cd19b21ca60f8d92ffc23246a95023104813083f6047ec393830842c1e18d`  
		Last Modified: Thu, 02 Oct 2025 02:44:56 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e083e3bb26f263ed75fc982cf17706428be528212f095cfe28b9130f2e2d8d`  
		Last Modified: Thu, 02 Oct 2025 02:44:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:beba15af84640c90a6d415f1ec482696e322ef89eef45918f19b9eac8f9e21a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9aba33ba73ce5ae95c03c3104abc620378c65500f8682cd567fcd18994de95b`

```dockerfile
```

-	Layers:
	-	`sha256:208ed3b9615042adb2b7e6959ad7d45f6ec1e6dd46a796c373b86891e60eb48a`  
		Last Modified: Thu, 02 Oct 2025 06:41:47 GMT  
		Size: 7.5 MB (7473929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:963418b40bd8f8c4db8913ab8ce7e26b3a082d07bdb1acc0f65f989d5bfd1927`  
		Last Modified: Thu, 02 Oct 2025 06:41:48 GMT  
		Size: 15.9 KB (15915 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:d5c760569575f93338f806cac5a1dde0d357a7b6e5419a3bd99fab27be6eac3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.6 MB (291634920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c6800abafd91524b19454a9d47d4e3229ae410c8ac3d52e3129700338e13fc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71fbf24a239310917388930bb043e64907cb532b9ac8f265e44e032dc3bf4409`  
		Last Modified: Mon, 29 Sep 2025 23:41:05 GMT  
		Size: 53.1 MB (53109217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147ef3ed9bf7756639cb71fcdd41937a73c6b055157e28fe7fd302fcde2df556`  
		Last Modified: Sun, 05 Oct 2025 10:29:25 GMT  
		Size: 144.4 MB (144372680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cf10802a773fda7593bb49abed7c460aad147da319a57ea50fb0c9ce9891e2`  
		Last Modified: Sun, 05 Oct 2025 10:29:20 GMT  
		Size: 94.2 MB (94151982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6151cfc513dad6f69929deb25ab217689426f08ea36da5737f1c33f75c0cac`  
		Last Modified: Thu, 02 Oct 2025 09:05:04 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11017b87687d1b8bacbe65685826963fbe47a3dc664594a72a68315959aa5cbf`  
		Last Modified: Thu, 02 Oct 2025 09:05:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2eb691efdc9e62b8a3afe2d6980c51689e4578165cc392fdbe0269d7e54b09a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dcee001209e5ee16b6958050421e5e554fb7b05bbfbe8bfcf5083dcd6b955d4`

```dockerfile
```

-	Layers:
	-	`sha256:58c2841c5e1e2acc572bb056bddc6b97512f19ce84e647332fbf1b22f8114f06`  
		Last Modified: Thu, 02 Oct 2025 09:39:06 GMT  
		Size: 7.5 MB (7471318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fa34fea284deb499d67b59d81a634e62abdf9eddc7efc1585a78916940c6f56`  
		Last Modified: Thu, 02 Oct 2025 09:39:07 GMT  
		Size: 15.8 KB (15844 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:659db45795e9536259212cab1f12162ca7d73715157f7ee64eb911cdf15ae5bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.4 MB (273395914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4aacbf9142f0f5eca094bec70909d262dc447e6211b0aed91e5eecdd560ffc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:913254a25f5e448a50a1e74fa50f037e22f85cfe4d6a3c626f4b7405299b7c1b`  
		Last Modified: Tue, 30 Sep 2025 01:03:38 GMT  
		Size: 47.8 MB (47770009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f17f9c702399c0e35c7e668e85c4461f2fc447422acb765907b33f99b7165d9`  
		Last Modified: Sat, 04 Oct 2025 20:48:22 GMT  
		Size: 138.6 MB (138575692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043a0bac4d0479ed450ba6809562b318fe5034a5bccee62fb155a541fb257363`  
		Last Modified: Sat, 04 Oct 2025 14:11:16 GMT  
		Size: 87.0 MB (87049172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b79798b773be453d82cc58185404249c12ec51379545a68fe48fcabce86ac6`  
		Last Modified: Sat, 04 Oct 2025 14:11:10 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a658a1e6305cd443e18c4eb2017c30b05d6db22f5f96acaffd255fd10e97079`  
		Last Modified: Sat, 04 Oct 2025 14:11:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e90f3bb36ef33005c22b2234d358ef13068b0c2e65561d3e3e1025df7a432ee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7468737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c542a36c00a2b93f676db3f016e3fb928702ab7c95e76e2f0031336ae157533`

```dockerfile
```

-	Layers:
	-	`sha256:a17c8dba286743dc251e97f3c0b299b4f74b998c17db653ef6047078f86eb5b3`  
		Last Modified: Sat, 04 Oct 2025 15:36:21 GMT  
		Size: 7.5 MB (7452893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00b50cee501cf81e3a59b3faef4cdf4c6824e9aa4962521bd315d4fbb43ea10c`  
		Last Modified: Sat, 04 Oct 2025 15:36:22 GMT  
		Size: 15.8 KB (15844 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:71f62cd18412f439017f7e23fabee2912b9edb75f7ef42bb1f66286828406604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.2 MB (273201263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615c89c55b9eb172b0439a1ed3154172d0b8f286e1ef8585197a7365ae5a0e38`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:024d6c344f0b9dbb2baf07e95dfd2abbfadc5c8262ca381f39f6489670cbaff5`  
		Last Modified: Mon, 29 Sep 2025 23:41:06 GMT  
		Size: 49.4 MB (49351442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24133c4045572f740b0ece90f7f2179652d7d347c8e44d8243dbb266de1bf45b`  
		Last Modified: Thu, 09 Oct 2025 23:11:48 GMT  
		Size: 134.7 MB (134723625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0fcd734d423d6a711f30db3c859cabe618ad72b123ddf9b26259968d78660b`  
		Last Modified: Thu, 09 Oct 2025 23:17:34 GMT  
		Size: 89.1 MB (89125157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6c5947ee46730726d8fd35f9b0c999dbd96a4bbc9db0bab5186d7e435e7206`  
		Last Modified: Thu, 09 Oct 2025 23:17:17 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2192f67e181dc3693825a04b68ebb01ca45d515f0f4a4d53b34a4b95b9f0fa`  
		Last Modified: Thu, 09 Oct 2025 23:17:17 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9adf03a728bb79b225cb78cbf6555d5d532ce419c3c0d8bc2982548305a12a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7478617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9312a4cfa24e09ea74844c8c965d94427501d283f5e7c96370275abdfa990553`

```dockerfile
```

-	Layers:
	-	`sha256:b2e680a1bf9ed272929a489dd19af71abfa42e7e1f4f886c8fc958c8a6065e5e`  
		Last Modified: Fri, 10 Oct 2025 00:39:05 GMT  
		Size: 7.5 MB (7462821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de8d850fbbfb292a94b8390563be3d584f801e49a6dc6c74301233ef1f9e5d0a`  
		Last Modified: Fri, 10 Oct 2025 00:39:06 GMT  
		Size: 15.8 KB (15796 bytes)  
		MIME: application/vnd.in-toto+json
