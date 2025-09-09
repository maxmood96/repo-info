## `clojure:temurin-21-tools-deps-1.12.2.1565-trixie-slim`

```console
$ docker pull clojure@sha256:986b6829d316e1dbf0d688af639a2aefb42476a61bc8dd2503d4b42430f34806
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

### `clojure:temurin-21-tools-deps-1.12.2.1565-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:32212481fbce3572e05af8f2cbc29fc7447793c3d8f45bb7b86f071eb65733a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259561796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c55c9395fe72f39b057a305caefa6b625b40cf1bbe105e483ae817884d71e13`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559896190705fb23106d00c38726f581fcabad9f828241cc879cc49aa1b19869`  
		Last Modified: Mon, 08 Sep 2025 22:40:44 GMT  
		Size: 157.8 MB (157804766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9c7af46d195186f504284204c363a8d3415c1b7b6632494814fefc102c5930`  
		Last Modified: Mon, 08 Sep 2025 22:40:20 GMT  
		Size: 72.0 MB (71982493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c3bd03db826fe9f137fe3e85c72ccf1ed3d0adfd652b6aaed74e769d81b61d`  
		Last Modified: Mon, 08 Sep 2025 22:40:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8656e0df6f1664e16e06b43911e500880024103c7c518f3d9f8ea7f355cfb6b5`  
		Last Modified: Mon, 08 Sep 2025 22:40:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6611afa06bf56cd02b84a49821a5825481a2cc870ab266c708211424cf7e62f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd7d89476eb812f53f885f89bb9095c56212ffe730442dd972e832a67f5a02c`

```dockerfile
```

-	Layers:
	-	`sha256:d3c095f6ffab71280a80ad4221d49a833bf0acabb1d93c1ba8ab7f8a1d7cfdf2`  
		Last Modified: Tue, 09 Sep 2025 00:41:10 GMT  
		Size: 5.3 MB (5259903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49621687e01becdfc49ab63d1849487092b52841931a24893af1a482c2c52b68`  
		Last Modified: Tue, 09 Sep 2025 00:41:11 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.2.1565-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:90494e1cf86710c35d536d6784c1d51da355805697b2db7695dbd0c6367df7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (258022855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907c118abf4878df1ade65459b106da4cdf42f5388c435b55039b13a0fad891d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51324890c60da3f50797bf158ff0345968677e818ac6c7c375cfa6304598eb6`  
		Last Modified: Tue, 09 Sep 2025 00:41:25 GMT  
		Size: 156.1 MB (156081188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82da0a38ce5dc2b7d2b1fb5f4ffd1403cbdd167be64904bafd90f3adca6d6464`  
		Last Modified: Tue, 09 Sep 2025 00:42:10 GMT  
		Size: 71.8 MB (71803992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4aa98c098f5285b640f6721078121c7039924b1c6d46bc3ee423e8277e2234`  
		Last Modified: Tue, 09 Sep 2025 01:21:59 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4f330e377a2116305adbd277dcae3878424053120bf70617c74eb57c6b284a`  
		Last Modified: Tue, 09 Sep 2025 01:21:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7f16c1a512e2069bde6e85e42664ebfd10fd163f974a2f04f208a7da5f4d9b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5282381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ea2d0bf95f405f7952fcdfd34dae3b8d33b1fdeb01ddbdb5736b146c7d2c9b`

```dockerfile
```

-	Layers:
	-	`sha256:f6733874430e4678fe87e97cf89032833c1ecfe8101ad581b40cf0ce8d5c0f78`  
		Last Modified: Tue, 09 Sep 2025 03:40:54 GMT  
		Size: 5.3 MB (5265696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d5dc313bb4052abb360a7d98df85b1ede478e2305d252ede265e08e8a9eed5a`  
		Last Modified: Tue, 09 Sep 2025 03:40:55 GMT  
		Size: 16.7 KB (16685 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.2.1565-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:78a77d0c4ee6b98beb6ac96caeed3f7e4225da0b453805a93daf30ca7e07f305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268947045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293e358ae827ce03f66b2a6271f418f821940b2eba461cb3064ff2cdf95c327a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
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
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7c959eacec6c619834131d38c38895328f95714d0440bb50ea7a7da6a19678`  
		Last Modified: Tue, 02 Sep 2025 09:00:02 GMT  
		Size: 158.0 MB (157963453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8bee27bbd321870fa86988cf57bacb2b9c25b394f8a4cd70d314176e4f3466`  
		Last Modified: Tue, 02 Sep 2025 09:09:59 GMT  
		Size: 77.4 MB (77388338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c210e2d881b68613c2c6c820dd88b24535297540f692fd547192dc9e9d012376`  
		Last Modified: Tue, 02 Sep 2025 10:02:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae5e401c90f6d13cda5413026fb46a0f94e34bc3374498c39f05483a4ea3105`  
		Last Modified: Tue, 02 Sep 2025 10:02:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:01ac8af68dd485965d971e36ba1eea799aba13972c113130fbaed969f01416b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ff188fc6473c45698409e980693a3af6878930432741874390ef70212a9ff4`

```dockerfile
```

-	Layers:
	-	`sha256:e793f3ae6e0ea3d98c4aaa72f854550e7abc9c80ec54c5c7da7f9e54ba5f7607`  
		Last Modified: Tue, 02 Sep 2025 12:36:23 GMT  
		Size: 5.3 MB (5263410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77436a8cd77f41e9a64369630be8d86203b990d1a7721c23a484e4aa3822d0d0`  
		Last Modified: Tue, 02 Sep 2025 12:36:24 GMT  
		Size: 16.6 KB (16601 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.2.1565-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:78dfe05a4a6a2fa1ad12745dca8dbd96b1893677f56a120cc0a523bc5625bf94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252741936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37318ea4bd3953b2c1ed8f4fcac89688d427e26911f221d4fd2a413fe9abff5e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
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
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2109af8ba4d81824f82c809b27d9617a81aacf05dfc1abb6f4c90cbf04297aa9`  
		Last Modified: Sat, 06 Sep 2025 18:50:08 GMT  
		Size: 153.6 MB (153593507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e431ac6a5783fec1c8d739e1c7dc7a2353cf03e2d51607f5ae18482c5bc9c1`  
		Last Modified: Fri, 05 Sep 2025 19:15:54 GMT  
		Size: 70.9 MB (70875762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9723ebbf6b552a150c4bdb6a931d759a8a109498812238a9c277c4bc15d2ec1e`  
		Last Modified: Fri, 05 Sep 2025 19:15:44 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87db0d4ab753e0e4fa58d60d1f5e690239341833b0cce6382ae088bde2d05f44`  
		Last Modified: Fri, 05 Sep 2025 19:15:44 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7271324524d491bf73c73de41852c6a32a31aba09a9312344a3d8aade32e4c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5265106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45bac4b3060ecc9d1d5841662917e8906357007469ba73c3d4b3a825a99ea97f`

```dockerfile
```

-	Layers:
	-	`sha256:b86b5a40b1af3e8eeba4af4595da18ac0242d0224a95d0422684ae258660a72d`  
		Last Modified: Fri, 05 Sep 2025 21:37:15 GMT  
		Size: 5.2 MB (5248503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2b43a50c7ef656c783676f56fec8fece97b71c4e0b4b9e83caf6d9dfa331811`  
		Last Modified: Fri, 05 Sep 2025 21:37:16 GMT  
		Size: 16.6 KB (16603 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.2.1565-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c4a58b971dac95cfd5c5b845033f45814bcc8a2e0ce2e573ac117995bfb435e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249812490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a27c129873753d1112f065ab4cda37496e4d36f48b214d46df3a7b49fcef17f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
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
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fee6c7e1621e3f55ef3d736beb00076551a0d086b09fc104bd238b1fecb676`  
		Last Modified: Tue, 09 Sep 2025 05:50:44 GMT  
		Size: 147.0 MB (147027052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4149e0fcc773d7b7aeccbf775fe77d9c7efa2a09e4539d22841936ab16470636`  
		Last Modified: Tue, 09 Sep 2025 05:54:35 GMT  
		Size: 73.0 MB (72951494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5833186221c1716be98a8846157924446f4e7a6ddf234ceb461597987f8e462a`  
		Last Modified: Tue, 09 Sep 2025 06:02:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682cfdf8dde6c0f833ef58b5020f21fc4d075a54f8cd3df4e6e6fbad3c70e30a`  
		Last Modified: Tue, 09 Sep 2025 06:02:38 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8d5f9355be68e9076eff17523508bb59512edf5e6842bd4d1e83afa8c0f40cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13626637f180eec774bc36e22c98c8f7e77fda2a47cbd23d33b2b38b0ce648b3`

```dockerfile
```

-	Layers:
	-	`sha256:89e787d7ac5fda581b7fcaaeacf7c3b01035bc09a56e99c422fd19379e26fbf3`  
		Last Modified: Tue, 09 Sep 2025 06:39:26 GMT  
		Size: 5.3 MB (5255827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8465056784b7c3c13640f8f8c3356724e322b7ea3715bd7c66f24d18e3c2ab7d`  
		Last Modified: Tue, 09 Sep 2025 06:39:27 GMT  
		Size: 16.5 KB (16542 bytes)  
		MIME: application/vnd.in-toto+json
