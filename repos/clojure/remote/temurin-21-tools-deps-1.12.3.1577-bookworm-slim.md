## `clojure:temurin-21-tools-deps-1.12.3.1577-bookworm-slim`

```console
$ docker pull clojure@sha256:7d9ddc44c5cfed061943a58fe68827b9d02fdf7703decb9168884efea1cc7093
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

### `clojure:temurin-21-tools-deps-1.12.3.1577-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1a7bccad146366f090d35661fb68f017cf7573c14a2239a271375e5889d2deab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255713660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf9e4a9d5c9571368ade66198616b8a2e4853b522a8dd96df96d053b1a0de41`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02b822fb386a92dbe8771a2515c7dec360a00af5a74a7dff37abde2b7874f35`  
		Last Modified: Tue, 21 Oct 2025 12:44:37 GMT  
		Size: 157.8 MB (157804732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0158acb8b9303806301cbaee629b8812d8b294a97b593cce3bea67d37b69c05a`  
		Last Modified: Tue, 21 Oct 2025 02:23:36 GMT  
		Size: 69.7 MB (69679568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09762ae4721657a3275d620b6bf19ae1ca1bd211358474376a2cfd256828411e`  
		Last Modified: Tue, 21 Oct 2025 02:23:29 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c480d8f68872932c1d1fb647e9705b03eae1dcbc1ad9d904730f47330f34496`  
		Last Modified: Tue, 21 Oct 2025 02:23:29 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:905fe9e7355fcd41f950f987adac94ba53025c48c4f5ec06587e13292062c6db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b681c75eec367b0c5221c1bc5a9ae244d6edf2d44c84c90e1968a0b91841a4`

```dockerfile
```

-	Layers:
	-	`sha256:b40549698f4e79ecda5f0f9ee217ab8164b6c85ffdb3a61eab220e6b744c0d4f`  
		Last Modified: Tue, 21 Oct 2025 09:41:15 GMT  
		Size: 5.1 MB (5116490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:044f2e8ed3b0de53d09f0293724206b7eed7491f3e264dd64c6b856e0a246ba1`  
		Last Modified: Tue, 21 Oct 2025 09:41:16 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9f19d1cead1ea27250c37a687d5a0cdc431c162e2e87a1519fc23715863c31ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253744758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de0a1255c0e4652c0ca48f5e776c675fc0e465b40778ca4efc6b4d7abc845231`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd338642bd851db59bb5b5f9089703e11ebe5871d7f48422b4a48e43befd22b`  
		Last Modified: Tue, 21 Oct 2025 21:54:54 GMT  
		Size: 156.1 MB (156081275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ad5db73ab1290b40fdf9340d0af0225afb4309da4135b9944d5f746a3b7d0a`  
		Last Modified: Tue, 21 Oct 2025 21:55:11 GMT  
		Size: 69.6 MB (69560253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0240e5065d2c4929c1450087996c1d42099ef7740a17eaea8ceee3e70dc79f`  
		Last Modified: Tue, 21 Oct 2025 21:55:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6ee18f351520f3d4af529f607cfbeab69fe5526391674262cbc52b14237ebf`  
		Last Modified: Tue, 21 Oct 2025 21:55:15 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a722fd6b59c3083184728a332b63c315b45a7659021f5736890e1b5c06a02e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:148fa4a8371b98d938b259dfe06e6dba1bd97307046243d58ea8589f51126963`

```dockerfile
```

-	Layers:
	-	`sha256:314eab37d3fbd9627081dc4aee999f7747c01826b744260933cc8444197d6331`  
		Last Modified: Tue, 21 Oct 2025 09:41:22 GMT  
		Size: 5.1 MB (5122251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60703b2f9150ed885bfdc43ea9c26518e06d127471cd937b68dbe121192069b4`  
		Last Modified: Tue, 21 Oct 2025 09:41:23 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:75151f156f9037ff03db7db66670fd3bba274e5a56119aaddf2c2d2af637e1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265546108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ef5275c5168cdcfe4109b28b44c131b6da1329c84b390dc2370db8bb41ebb1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
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
	-	`sha256:5a28d569c39dc949a4743122d7b5ec2d2e0664f1276c801bf984a711d80f2a1d`  
		Last Modified: Tue, 21 Oct 2025 03:26:43 GMT  
		Size: 32.1 MB (32068780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4de39d3ceb05c0fff8b1118b58bf5502c7dbd9415c253b8957509f09667345`  
		Last Modified: Sat, 25 Oct 2025 01:34:32 GMT  
		Size: 158.0 MB (157963469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b5006614cf14880b72d679c4c58910d5e4758f69588a2bb01b6b1d1fe0ca48`  
		Last Modified: Tue, 21 Oct 2025 16:12:25 GMT  
		Size: 75.5 MB (75512816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2a48bd0b7b53c0183aa67b5b6f32bbb67cb6a299726a0026b9fad9ec2fdcc7`  
		Last Modified: Tue, 21 Oct 2025 16:12:19 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765b161f9ef0ce91b026a24c7c3a96e0ecf17858c000b50b5984f35eed3721d8`  
		Last Modified: Tue, 21 Oct 2025 16:12:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9fe3e335314fdda39a046109db5ed766ea64fc12bd3774ac544099db369959da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2589e6ec1122eacd73549feeecef76ff7af84e21babd0240c18cf3b93fa87d51`

```dockerfile
```

-	Layers:
	-	`sha256:af193f691da4a3489888785d5a332e2c35d99e219947158e8fbc180b16729740`  
		Last Modified: Tue, 21 Oct 2025 18:38:36 GMT  
		Size: 5.1 MB (5121648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:797b5f69ee6cf262c06469c875b484ceab97b69a1fc8164c2aa27ac1aaf85606`  
		Last Modified: Tue, 21 Oct 2025 18:38:37 GMT  
		Size: 15.9 KB (15927 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c8689b2e49d77c0393e59d2835eec64e47e8e040aa6a16d214d1f2f6d8c18fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242403121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa282f1578d7981542e91b3088d1160e30d0b5a4b26dbedd0313d72f59663748`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
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
	-	`sha256:43b0f588b497b17691a3547afa4ae41853829cffde6930e6425ddae4a3f89278`  
		Last Modified: Tue, 21 Oct 2025 00:21:28 GMT  
		Size: 26.9 MB (26884356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2050d29f18bc4af2bcce04cace956b592934350a910fd6a374fc66bd83c725a2`  
		Last Modified: Sat, 25 Oct 2025 01:35:12 GMT  
		Size: 147.0 MB (147026967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c33a9e9ae3308824146371291fc09bdce9851cde96e997f64d4472c86962e622`  
		Last Modified: Sat, 25 Oct 2025 01:35:23 GMT  
		Size: 68.5 MB (68490754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ca2b6e96482cc1bcef733878116ded8b93941d1550be07cd4ab43f224456a7`  
		Last Modified: Tue, 21 Oct 2025 23:23:42 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a8b32cf17471ee49e28acd42c57020e9f089842aa35719d1c968d64515a909`  
		Last Modified: Tue, 21 Oct 2025 23:23:42 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:75c8f718bf2d0be8ea83e6772ac2da7d561084163eb11c3096376bd3b5475efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb91d8945864b9ea5f016a8f39b205a6668d74966e990e81b84f63a7be69c0c`

```dockerfile
```

-	Layers:
	-	`sha256:80a50527c6f75f48ae4b02305ba5c666e7d19a93011774c2f9d8048a7e2640c8`  
		Last Modified: Wed, 22 Oct 2025 00:38:32 GMT  
		Size: 5.1 MB (5107811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4aa90234a4d03588e663bde0b03fd873d840d73ffb5e4c9f93bcde3763f9a9b8`  
		Last Modified: Wed, 22 Oct 2025 00:38:33 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json
