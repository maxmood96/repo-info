## `clojure:temurin-21-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:098b8c1e308ebe7605487473765f92623dc10b6df052712b16509b0d746fee92
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

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:410b2f5487365634296aa99327a0d1a575fb59e5d63bf293a769b94222dae076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259565378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:befab883bd9958fb1cedc086610964c2b0b9861c9548bc1d6db4202d236f0c3c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b695e5aef5f41d99e9a31d4fef9c4fbeb20ae3a101322cd2ceddd80c7df13aec`  
		Last Modified: Tue, 23 Sep 2025 06:26:37 GMT  
		Size: 157.8 MB (157804770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad23ad34a49ebd0c8c6a822f1fbf712d71f4e3f4b5d79f25949587881a46bc5`  
		Last Modified: Mon, 22 Sep 2025 23:47:22 GMT  
		Size: 72.0 MB (71986069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7640b775bf5eed05f613403ea63c782f816be75af8cd44244bf04920e473a2`  
		Last Modified: Mon, 22 Sep 2025 23:46:56 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9acb509c8769735d6fa8be6d92610da1b7bf1bd218fb3b7a970ec71e435960`  
		Last Modified: Mon, 22 Sep 2025 23:46:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bc4e9222af57c78f3d1b24388abb069a75e07d309c94d16f8d632d8185eda708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64a74dbf9322565e078aeeb03e13b1030b0073cd989e0716e7dd42d769cf1e2`

```dockerfile
```

-	Layers:
	-	`sha256:7442b64b5c349069fdd2d84d058a472094a2b79d21835c94d4cadc78ac9fef26`  
		Last Modified: Tue, 23 Sep 2025 00:42:59 GMT  
		Size: 5.3 MB (5259903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36b90cb02358238bbe93f3f037ade7f7dd1735c0b730091a4215077c4c4f3e0b`  
		Last Modified: Tue, 23 Sep 2025 00:43:00 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:26baab4fbb7f1ed25c8cb88f68b9edb54b4c0b15d3411f165668777acd91c5d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (258023959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bacff8b5ce8e9def88bb0cbf3db2950636433260d7d9ae872632cd3d3e13215`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f5fc8e5e9d94d8093ab7d1d42fbe4c2df1d9fec9d5a06a6a1861949dd0808e`  
		Last Modified: Mon, 22 Sep 2025 22:20:18 GMT  
		Size: 156.1 MB (156081216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09276133e5d44febb8189a6ce06fae6945b5b53169a8009441d8e113cbc2465c`  
		Last Modified: Mon, 22 Sep 2025 22:20:28 GMT  
		Size: 71.8 MB (71805068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cae076dcf34f7b6638ffc514b6b99078a65c0e3bea460262bab6a8ce90ddba`  
		Last Modified: Mon, 22 Sep 2025 22:20:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573f5588ec10f9a34c6aa4ad775e54cec18f1213f586bd6b37bff04795fa79ab`  
		Last Modified: Mon, 22 Sep 2025 22:20:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c15247bf7a867994dcce68904d1d5a6253d935e8f5370d816ae4733d3a6c46f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5282381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e68ca76ecfc6891a6c7cfac3918c81c3d85ddd711825746060751e7fc8b306`

```dockerfile
```

-	Layers:
	-	`sha256:e70c76f481d596d7808a7d16e4f94c6bad6df65576d441a1059400ca4e3b27ab`  
		Last Modified: Tue, 23 Sep 2025 00:43:06 GMT  
		Size: 5.3 MB (5265696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9470f1bc372885b70a0386cbba9737f7fbfbff368e189d82fa1f311f7bc4f67d`  
		Last Modified: Tue, 23 Sep 2025 00:43:07 GMT  
		Size: 16.7 KB (16685 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:84891f6cea0808a39fe6fd71e9be0176b351061c3e58a23166fbebfe60347221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268964696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b64c9cbb5144beb17f7a672245e12a22679175795ebbde2f135aa1b6ef75df`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961eb7ebf0035f6d398671677d350eb2f03bf73e15b167f039f8bd38980355b5`  
		Last Modified: Tue, 16 Sep 2025 19:34:14 GMT  
		Size: 158.0 MB (157963461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b75776e014be32987403d4a046ba108c65b00a78a2412394f8fdc841eef3ed`  
		Last Modified: Mon, 22 Sep 2025 23:21:19 GMT  
		Size: 77.4 MB (77405840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61879da6b8d71f61dd2e287c3e89e0d08cbff63b3215ec707e97144d29db601`  
		Last Modified: Mon, 22 Sep 2025 23:20:56 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1f2f123d1e4793801fe8db87a0fa44b37fc1747cc3c577362431dcbf4b5f0a`  
		Last Modified: Mon, 22 Sep 2025 23:20:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c648f9ee2dcab8fe8ba7ba2ecc16649c0255f37a97f9f5eb012cb40561c8a6db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4455923f94c1c3dcc1561c285d33d9f1294a46252531d95efeb23eb8713340f`

```dockerfile
```

-	Layers:
	-	`sha256:a62e21976a70e66891b16acda1636f9e00f627ec76b64ee7e37bb3d2bd795cb5`  
		Last Modified: Tue, 23 Sep 2025 00:43:12 GMT  
		Size: 5.3 MB (5264286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8276a65cc03e59f5f8b2ab8a2cf81530a620172963e056d6e1e086a61789f33`  
		Last Modified: Tue, 23 Sep 2025 00:43:13 GMT  
		Size: 16.6 KB (16603 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:677f8ed3cafdf6c4a1abf063ee506ec5c2d836e6fcd07b0f94cab3f0e01af12d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252747590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd40b8eeb9dae56f1e19df7bf6468ab52693c2d7cec9fe92c32bf077bce8200f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
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
	-	`sha256:5dd1c7f45506c73ead226a0873290a4472ab5ccf8fa88d88c86a7a5207960182`  
		Last Modified: Tue, 23 Sep 2025 01:00:24 GMT  
		Size: 70.9 MB (70881680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c1d19779d6c74328135f69849b1ad89b17f3981bc596a8e58dab64700f8d81`  
		Last Modified: Tue, 23 Sep 2025 01:00:15 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540e611d950313cb9731e980a5b5cd1fe003f9c1b62032917de17b565f8c4973`  
		Last Modified: Tue, 23 Sep 2025 01:00:15 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f153dc4982b4fffc7db198cc95f12a07aedcaf2312defb47b9bd9c5168d2eaf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5265982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da306ea88f73de550d270c4d658d5e0ab4dcfe6f238c233946e76fea0ce8bf4`

```dockerfile
```

-	Layers:
	-	`sha256:68b94316903808ac70acba9fb465e58f5b300aea9223c53fb89ae8cfc9f5ebca`  
		Last Modified: Tue, 23 Sep 2025 03:36:52 GMT  
		Size: 5.2 MB (5249379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:218db09220b10b15335430f371e0bd612ed52d4c6afea90f9a50d4099ecc8342`  
		Last Modified: Tue, 23 Sep 2025 03:36:52 GMT  
		Size: 16.6 KB (16603 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:4e588738e8bca38089cb49ab84dbf96a483182e0637bdee989d7e256e65f8988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249816698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be173665a2abc960eb6cc3b4074f4acab106c043cec601d9ed675dc5b7e21911`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4c284aa571e77182f2d698660ed6e8ab6e5fbf5fa1bcbcf0017032e82225f4`  
		Last Modified: Fri, 12 Sep 2025 23:59:48 GMT  
		Size: 147.0 MB (147027059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69032f25d5cc42f7ce45b0c38dadeabbefbe12cf006f2c352508a47bd5e23b18`  
		Last Modified: Mon, 22 Sep 2025 23:18:23 GMT  
		Size: 73.0 MB (72955690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af341e923c70e090ee320a0500c9e69ad4db1897f6bdb02865e28fc86e34a0e`  
		Last Modified: Mon, 22 Sep 2025 23:18:17 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4125e24cccf4dae1d38f47edaaf1a453d1db67879f691c83002718962bf2ae16`  
		Last Modified: Mon, 22 Sep 2025 23:18:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7d5396a856d808fc4d1993c712c7162029a5160a173a8ee6d826b7df3d352835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33b1148f7797b09a06a2b5e1ad5805e0497ae40ae128e1c82a1ad78844b3dfa`

```dockerfile
```

-	Layers:
	-	`sha256:787f12b690d973b96d4c7a5480873a99d830ef8d4dc1bce077da74506b6c937d`  
		Last Modified: Tue, 23 Sep 2025 00:43:38 GMT  
		Size: 5.3 MB (5255827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c138db214ee079a076603e684ad3d46f191b14c770cfe4d5922e3fa276dff3f5`  
		Last Modified: Tue, 23 Sep 2025 00:43:38 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json
