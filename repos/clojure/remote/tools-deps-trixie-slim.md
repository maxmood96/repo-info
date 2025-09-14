## `clojure:tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:b8d3c00aafe8e25a86c14d329b987bf36bcab100155da4e50ff44c6ed58102b1
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

### `clojure:tools-deps-trixie-slim` - linux; amd64

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

### `clojure:tools-deps-trixie-slim` - unknown; unknown

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

### `clojure:tools-deps-trixie-slim` - linux; arm64 variant v8

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
		Last Modified: Tue, 09 Sep 2025 16:14:51 GMT  
		Size: 156.1 MB (156081188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82da0a38ce5dc2b7d2b1fb5f4ffd1403cbdd167be64904bafd90f3adca6d6464`  
		Last Modified: Tue, 09 Sep 2025 16:14:45 GMT  
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

### `clojure:tools-deps-trixie-slim` - unknown; unknown

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

### `clojure:tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:4d8da40af2ec357f56e9b5fa4ea57e08371cf48a2c2d184249241126a983cc98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268956850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c14732964bbb377ae3d872867d96ed7cefb6509248689f2c9c0d961989574e2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b14b5ce7c16bc2726163eb9b2d2a77c01ab78c8a69a26de6d23324f5bfe677`  
		Last Modified: Tue, 09 Sep 2025 19:08:15 GMT  
		Size: 158.0 MB (157963447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848fa27797e07b2f7d6b4dedc6e6e024ca6ecbda9c9713ea4c025eeb9767e919`  
		Last Modified: Tue, 09 Sep 2025 12:52:44 GMT  
		Size: 77.4 MB (77398009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28102eb13a239fd1b7084d7956277fee81c988f6624f7574f83b8fe57e8eacdc`  
		Last Modified: Tue, 09 Sep 2025 12:52:33 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea244565f75edf7589f0bead70e250d66b6b5b5ed124c7dd33f3bd016379df9`  
		Last Modified: Tue, 09 Sep 2025 12:52:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:167825bf57f329cdb325af8f2129ff8674564f9acc64a06225f5f7f2da60a7bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5355c2232fe0bb906ef427e9b81376b7d21f734f6cc25652a8a78cfb9b401fd0`

```dockerfile
```

-	Layers:
	-	`sha256:eaa3d56158219fb019eb1b6efec6a9ef958224afb3cfa0741fca9327127dced9`  
		Last Modified: Tue, 09 Sep 2025 15:39:00 GMT  
		Size: 5.3 MB (5264286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32fd96e9d4df864707dbb64fb3cc7b9245919441ef1cd59b0d8264a38d861c7a`  
		Last Modified: Tue, 09 Sep 2025 15:39:01 GMT  
		Size: 16.6 KB (16603 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:441e3b3c954ee8248789566950010c98500b2d4729e15685c72a6e7accbe26cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252745815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320b6d0f3fb0347d795f0905ac43b9b33bcb00806004cf4e3bd081743f4c421d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
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
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25be0a32c196b5e86daa223045b0e32e55940405ffb33be6fe5f6bd48aeeeee`  
		Last Modified: Sun, 14 Sep 2025 19:26:07 GMT  
		Size: 153.6 MB (153593492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de8edfb047643d39d1a8eae5f97a87517988aad5024f669070bbdba01bd39b0`  
		Last Modified: Sun, 14 Sep 2025 19:26:14 GMT  
		Size: 70.9 MB (70879906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757f585b18e2130e580ffd8f796b8b506c887529dd3e482f7d5b5bcec5f4afb0`  
		Last Modified: Sun, 14 Sep 2025 00:30:23 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e6e75f238d5c12884d611331d2baa971d46ebe494d9abc8c46114b281d09bc`  
		Last Modified: Sun, 14 Sep 2025 00:30:26 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:128f7d66f1e936346fddcac20df81d22ae93d24dbb73c88e6871e19af7784018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5265982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d665230282d90060a5d55e6852c4fb7f7d7643c11b1b02f48f6a84410fd1429`

```dockerfile
```

-	Layers:
	-	`sha256:faa71eca617f2ac4e7a31245e64d8b8f225f7e2727b0ef094e7b0fd7dda5c63c`  
		Last Modified: Sun, 14 Sep 2025 03:36:11 GMT  
		Size: 5.2 MB (5249379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1eca6a38b24991ac47d97c16c025bd60740bac9082d2bedced6945e4067f9c`  
		Last Modified: Sun, 14 Sep 2025 03:36:11 GMT  
		Size: 16.6 KB (16603 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-trixie-slim` - linux; s390x

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

### `clojure:tools-deps-trixie-slim` - unknown; unknown

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
