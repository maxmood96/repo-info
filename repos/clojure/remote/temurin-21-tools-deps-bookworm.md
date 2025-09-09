## `clojure:temurin-21-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:e7cf948d290716f863c9190a9168fd1fd1989d7be770fb5eb9d988d2d16559f3
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

### `clojure:temurin-21-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:39c8f64ba8a104e5ae4cb441aa38639492dcfde1276fa34d20100788fb10746f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287424008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:333339678130092110bb23c9d001fd90b08a2a0ddebbdb8633e7ec1a390c9ae0`
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
	-	`sha256:b6b3a8cf4d1c8fa76c9eb090723efb4533874ea219c7950edbc0d4cb85900ac1`  
		Last Modified: Tue, 09 Sep 2025 01:50:04 GMT  
		Size: 157.8 MB (157804796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bf3206203b83632fc471ba3fe0bed57b7e73e80b1e8f16b36271063b52fff3`  
		Last Modified: Tue, 09 Sep 2025 01:50:12 GMT  
		Size: 81.1 MB (81137564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c336c725bb0f06d756aa30dcf981b3c87290d7ab678c5f0837a6f1ee8a1ac27`  
		Last Modified: Mon, 08 Sep 2025 22:58:57 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fdfdb9ed9f6ae5928ec285373b32d34afc549ee802134d90ff959b09e0b5f1`  
		Last Modified: Mon, 08 Sep 2025 22:58:57 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4932e78fcf9b82a62b2a0b1fd8f81de12b230df7b38742f96450da2d85c3e1c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a32457538e914c76aa76d2b06089255773805b5b71f5c1970d64a54738bb67d`

```dockerfile
```

-	Layers:
	-	`sha256:6f46718cf3988ee6b79ccc5c8396f12d7a064095765f308d900a72982f08361c`  
		Last Modified: Tue, 09 Sep 2025 00:39:45 GMT  
		Size: 7.4 MB (7379992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0909125bc1124b41fda3e5abe0640d444ce9f24c1a61ffb29bca2d3330dce6a`  
		Last Modified: Tue, 09 Sep 2025 00:39:46 GMT  
		Size: 17.8 KB (17820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:373a07d0c4045915569b36686482b48a0da1d98c56cd9b5fdbdbe471e041196f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.4 MB (285434164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76dd94f119444627168a4607f46662cac0357357ca12702e2926090aaffd56b2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a7c940a4ab0e7c077b6df48f638094c1e5279248ee3103b5583683e69463287`  
		Last Modified: Tue, 02 Sep 2025 09:47:16 GMT  
		Size: 156.1 MB (156081246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6790206f376d3e868945c9c3577cdbc2e410367f1eb26be1d261c5ad53ea430a`  
		Last Modified: Tue, 02 Sep 2025 08:16:21 GMT  
		Size: 81.0 MB (81009425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b39a17852b321ed6ee836d15a96a795234014cdb6986184891cb506735cb1f0`  
		Last Modified: Tue, 02 Sep 2025 08:16:12 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83be8b43f44c8360003147e1365eac811c8ccb4d515d9e7ed40b61b8942835b1`  
		Last Modified: Tue, 02 Sep 2025 08:16:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:cde2b1ba2df48bddd7b973ef76cf39c4fe0476dc83db0ba9569e1290e34f4152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c5f8af887cffe5d8de8ab75028318b08ee0c5c16dcbf51d664bd5c4a7a3cb7`

```dockerfile
```

-	Layers:
	-	`sha256:d6ecd63eafeaa0484522ce1dc5367268e9eaecfbb23522c2db3e09bcbe4426ff`  
		Last Modified: Tue, 02 Sep 2025 09:40:31 GMT  
		Size: 7.4 MB (7379234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6a2201854678f87531243fde7e76f20ae48a0ee90bfb544ce0fdcc5a5148787`  
		Last Modified: Tue, 02 Sep 2025 09:40:31 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:319dcee1be8c3b39a3e714f3ce2666c8a6b1be8447450f684282fd7e618afb72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297275395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5957af7897f5827bc254a11f22dd1acec48fbd089892c4aecc7722ffe12cdb2a`
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
	-	`sha256:d6dd733126a0f2e946a8bf50a9fefd8e55c3787bf259669bd0eb12f28a79783b`  
		Last Modified: Tue, 02 Sep 2025 10:07:05 GMT  
		Size: 158.0 MB (157963477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc09615ee63f14a85bb0b3b2812d573dbc1929bab99f04c5cea322a3d9265d26`  
		Last Modified: Tue, 02 Sep 2025 09:02:26 GMT  
		Size: 87.0 MB (86972796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81da14f1e93b273e42efcdefb3366750c155ebafdcf12c04022b589d6a5bdd4c`  
		Last Modified: Tue, 02 Sep 2025 09:02:09 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59052a6d6da77d74b37ed231aed65ab460280d9fa0420cdeee1f32014177344`  
		Last Modified: Tue, 02 Sep 2025 09:02:08 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3642c087733d30f58556ac9a420e5381e0756a8cdab19aa00a068c1409931a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7396544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c03fae19575762326672e77b3fd9912fb6c05b9917d659f5c1e938121869aeb`

```dockerfile
```

-	Layers:
	-	`sha256:9d21ece2acc32d461c6dd1fcfc523b97dc4834da0eb5a7e3dd69f91c4ec2fd8c`  
		Last Modified: Tue, 02 Sep 2025 09:40:38 GMT  
		Size: 7.4 MB (7378639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5ca674782ba5b9f1ceb6c0b08f87c238fbd6f8352445166aae7f044a6d9d3ef`  
		Last Modified: Tue, 02 Sep 2025 09:40:39 GMT  
		Size: 17.9 KB (17905 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:765e9875a2a836873907edaa350a7398dde2a5904f3a7c75a8554ca882c3b7cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274131890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38188fbb9f7b990d2ed566dbdc98a14b303bd930cf4cb4f776e06623c260f2a2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c854f0bb2062cb8e3203dbffc406ec501de420643779bca54d79fdb8235d74`  
		Last Modified: Tue, 02 Sep 2025 03:34:47 GMT  
		Size: 147.0 MB (147026994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f77b0a97b6eff2c185af919c492f2c6c8fb346faee6eeb4ccf59dedc16fe4f`  
		Last Modified: Tue, 02 Sep 2025 02:15:16 GMT  
		Size: 80.0 MB (79953989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef6e0368cf551cfcf7881e9a252d8f9f3ffc8f20d98c6273a8b818756bfcc40`  
		Last Modified: Tue, 02 Sep 2025 02:15:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c314b6be9e9c4833ab08f37b8fc0e7fa429db403c66e42ec133a2004e786147`  
		Last Modified: Tue, 02 Sep 2025 02:15:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1639dbf0110dda94ea24f30fb5197f6326d6ab6e3c49931ee181f59e76702c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7382539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a15874f38090797fa3ad1de608a6b5e25738c94e5620d2fecf971c7db06d6c`

```dockerfile
```

-	Layers:
	-	`sha256:91239a485da2ca81b3dc7eaf6e5fd35c3ff625cc14d5a788e0df93cbaacaef0d`  
		Last Modified: Tue, 02 Sep 2025 03:41:07 GMT  
		Size: 7.4 MB (7364718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b4769e83fa9f8bf6a439b82508e3de473ac556953820093756febcd3c4c973e`  
		Last Modified: Tue, 02 Sep 2025 03:41:08 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json
