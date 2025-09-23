## `clojure:temurin-24-trixie-slim`

```console
$ docker pull clojure@sha256:4cddec2428df22f69f0208b1755b021f22f05f63a71d0bc5e43040177b20ce08
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

### `clojure:temurin-24-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b7e1856ff21aa15181c9ac126d3379ca4fc167ba98745e02f1f38ae863f65f7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191736118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac371264cc09fa69358e5bbe307b1f19b809d3acd392f805720c76214834f218`
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
	-	`sha256:fda7b96e53d3336d914001e0800014788858c916bcb66c417653b7c34f247d17`  
		Last Modified: Mon, 22 Sep 2025 23:47:24 GMT  
		Size: 90.0 MB (89975197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1023bc6906aaf3bc843e122dde32533551068a620a221537e3ef796b653d2c84`  
		Last Modified: Mon, 22 Sep 2025 23:47:06 GMT  
		Size: 72.0 MB (71986386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0741d5a243a237aa45fb3dc4523db8250d13dd38dde8f0cbab6f6041b9620a`  
		Last Modified: Mon, 22 Sep 2025 23:47:15 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0ef89dd2209d99054063d44937fe4de1ee322279dfaf6fdc45a818cb4ed82c`  
		Last Modified: Mon, 22 Sep 2025 23:47:15 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cd2c8a6cacf79ce1fdb5d9198327889a143925d986a546f94209693035222f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5755e8b5d61b7e0bbff3fe6303a80a5016466dd5d2566c130f3c2b0285d12e3e`

```dockerfile
```

-	Layers:
	-	`sha256:d51a6cf0dffa7326728786127642a90f6f5bfe4bb46c05583bda1e9147cb7d9a`  
		Last Modified: Tue, 23 Sep 2025 00:45:37 GMT  
		Size: 5.2 MB (5206761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbbf5803b1349ab99352c8272276669f09e1f78a9e2f42e6a2bf878b1ce93ce9`  
		Last Modified: Tue, 23 Sep 2025 00:45:38 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:43c2147079b414d4b71ff7100ed62615597342b645a529e7488f55acf369aa5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191034866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:385d7dec297fa32beb64ed1a0b9759019516d91db4395b3fb6f0984ac713719f`
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
	-	`sha256:f9397c4684d94db78898aca7144260dd4f5230297f38b9fb31e483031f33103b`  
		Last Modified: Mon, 22 Sep 2025 22:22:23 GMT  
		Size: 89.1 MB (89092538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4437f616387f1b8cdb1b897a52547697835d4f0a23cb9c5911c9a5e30830cf81`  
		Last Modified: Mon, 22 Sep 2025 22:22:20 GMT  
		Size: 71.8 MB (71804653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c0edd0b1fd4ec7ae16e210d34c32029762b81499b7b75f407762d351fc33b1`  
		Last Modified: Mon, 22 Sep 2025 22:21:57 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc66fbaa6a33356c0b4ede63e739f59fda859af4b4b2d8bc608fe325912b7798`  
		Last Modified: Mon, 22 Sep 2025 22:21:55 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:88ce04cf034e1e8495ffec08a03656cba1ef7d9cd96f1e7b96b2f35bc9574285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24415a93baf2eb4a038d4bb485b5b3881677fe1f015c02531d59b4f75722d7a3`

```dockerfile
```

-	Layers:
	-	`sha256:d8ff23d2938353e94b67617aab9e17dc87fbdb60c67bfb635a1c5e9dd8dff26a`  
		Last Modified: Tue, 23 Sep 2025 00:45:44 GMT  
		Size: 5.2 MB (5212527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45a839363c7c9dfae3a09db7b4646c2291e1273c8258078cd25be131295c0dc8`  
		Last Modified: Tue, 23 Sep 2025 00:45:45 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f95008d01d69cdf072ebd99855c9ef8ed4d049baff5c3f6c877328861ad5311d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.9 MB (200921091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23288747b4fbfc9ca2dea95e7294b145a8a46cbeefa28d61fd0f3bd1feb20a30`
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
	-	`sha256:4ab6532f47259b4baefc4644a9d2f6e61e29f5697fdc7617b9491b02a2197399`  
		Last Modified: Sat, 13 Sep 2025 03:55:52 GMT  
		Size: 89.9 MB (89918195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671851d6ae1b77efdfd27a609eb6f71286362843ede1d5ab6f86b91100ce77c9`  
		Last Modified: Mon, 22 Sep 2025 23:31:13 GMT  
		Size: 77.4 MB (77407498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbd40074466c201832d2617179a2a4114601231a2349ca7a956c51e2e1a707a`  
		Last Modified: Mon, 22 Sep 2025 23:31:07 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9745adf868a2e896527fea0b6a09cb8184366e7cf5bfb85bcae98f6f4b89a2ce`  
		Last Modified: Mon, 22 Sep 2025 23:31:08 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:532bf72991e078905eed2dea2a070831a5b6f09ca71a676e5960b15120e37015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5bdc1b3576865aab565ba470e9441cb269cf0b1e343bf969871dc56499baec`

```dockerfile
```

-	Layers:
	-	`sha256:a17f2422bb78e0c06d6d9a854d88f65ebd03e808bc0ba860e948b135dea5f4f4`  
		Last Modified: Tue, 23 Sep 2025 00:45:51 GMT  
		Size: 5.2 MB (5212430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99a0a9cd8eaa53da7cf06a26059593d81601da7bb6ab5413db3fb3ee0e468658`  
		Last Modified: Tue, 23 Sep 2025 00:45:52 GMT  
		Size: 15.9 KB (15895 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:379aac212559f6979c327f4ff74c32639973b72ab773cf6e0f070f0c61c2c70c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.8 MB (186822188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347383b7e448d86a3e8d4b6cf908b70811c57f99a71d0e40a9e8fd83633d9b14`
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
	-	`sha256:21bc3fbdc5bd092ca0af738f65f8ae8ce176945ba88b669c5e80fb9adb3f5eaa`  
		Last Modified: Sun, 14 Sep 2025 00:38:37 GMT  
		Size: 87.7 MB (87670426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f306023afdd4b220c4d8bb52121ecf0e954b280e72f3029805a46753ce81a0c9`  
		Last Modified: Sun, 14 Sep 2025 00:38:33 GMT  
		Size: 70.9 MB (70879348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d6a7e3a7a9d6b0739613cc3645212ee48cada7a5eb61850907b3fb83b845c8`  
		Last Modified: Sun, 14 Sep 2025 00:38:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8044294e53545067b46832278c613fcdf8b9f6fb53c6579ab35e48e700592d`  
		Last Modified: Sun, 14 Sep 2025 00:38:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a73d6761043f54a639532b354557ec4e9ef122a2d1611ff73fb5e4008287a77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0c43cfdc889d95331f13473d49f9e4fc24b1700baccdefc7e1e019721bac754`

```dockerfile
```

-	Layers:
	-	`sha256:0a88c39581c054ee8ba0757eaa171aa6a54ff032ae33e086cd8cdf29becc5749`  
		Last Modified: Wed, 17 Sep 2025 21:39:09 GMT  
		Size: 5.2 MB (5196222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d88de7ee765a81a04d51ed07e7efa440273215676a25e9758a7c39c62ad15ae2`  
		Last Modified: Wed, 17 Sep 2025 21:39:09 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:9483582d7d3df37d91078e01678c7998aabdaac1deeb45384d6695ba5035e14a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188016571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512f5e26b189773e77d8c96ddea6bc95a043aaba05811cf58535c7f3d6832c69`
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
	-	`sha256:001f899a0035f92502563c4bdaed319ad7f7d929742ec096c4bb55d3733e094a`  
		Last Modified: Sat, 13 Sep 2025 03:21:52 GMT  
		Size: 85.2 MB (85226409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5005c6a40d16e921da5e31a49092636ca7d5ffdc6f6dd79bb34e3186b5c2de7`  
		Last Modified: Mon, 22 Sep 2025 23:24:01 GMT  
		Size: 73.0 MB (72956221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09419d53b10fc396294930055dcfbbb14ed0ea62d7b35e8bd3ca1688ce51e50a`  
		Last Modified: Mon, 22 Sep 2025 23:23:59 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99cb7a63ecb2d4af0b4708496ebddea6747700e1fa6d4bc89a75f7879a45052e`  
		Last Modified: Mon, 22 Sep 2025 23:24:00 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a9a326fd7bed583748f562906da6c7c433d9bb61e511c9e4aa326b5da2ba9107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4d8f7331f872c7c7231140a168da763a5888ec093cf43a8bf37307d0cd698a`

```dockerfile
```

-	Layers:
	-	`sha256:2e61fdfd95e657cbe0cb8b4423869112fa299f40352913102378731d02d638f4`  
		Last Modified: Tue, 23 Sep 2025 00:46:00 GMT  
		Size: 5.2 MB (5205233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62198fd008d51e743fe7b67f270520f6d9276b1f60365e4943998e92c99738cd`  
		Last Modified: Tue, 23 Sep 2025 00:46:01 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json
