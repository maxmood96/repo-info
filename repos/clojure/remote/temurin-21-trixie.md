## `clojure:temurin-21-trixie`

```console
$ docker pull clojure@sha256:543324c63b57b128e57fa085d79c587b60f4fbb4e3ef380be10ece23d8b9c38a
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

### `clojure:temurin-21-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:4eceb87f8fccdb5c4a8525dbf263423ccbd3e75bbfd6a0ab5a6371f2798a8967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292617069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d9db598b5705a393719e6b96a49097e3daaca2febfd852c5ee7bd3a3fc0469`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319b9ed961688aa658d5e726230da53a0f2e5071001891f0c307b5903f47efa7`  
		Last Modified: Tue, 02 Sep 2025 11:02:56 GMT  
		Size: 157.8 MB (157804808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5dbccf0a7914d29642ac596d23541b3dad5e714dc301c8d7c8e55adeb1ee300`  
		Last Modified: Tue, 02 Sep 2025 11:02:41 GMT  
		Size: 85.5 MB (85532938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee7b9616a57b0fc41adea266e990f32dca4d2bdcf3b10d0fe33caba97c01f65`  
		Last Modified: Tue, 02 Sep 2025 02:35:31 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1bd49edf7278b7baf7d304ed28a1429ff3213a59b16860977db3e23af3f795`  
		Last Modified: Tue, 02 Sep 2025 02:35:31 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b6213c9282184833151d44cb3b0f18ddf643df0ae5dc9c94c6509f2da661a45d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a56a79d5270790624216b723d3cfbcd3d22566dc76484a197b35e2941e7c850d`

```dockerfile
```

-	Layers:
	-	`sha256:bb71eadedf6be7aac6ef1c75c0341d01350f17243acc15589b2ac65ed26e05a8`  
		Last Modified: Tue, 02 Sep 2025 03:42:30 GMT  
		Size: 7.5 MB (7465991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5c030fc582a932f717e8ad684d89ecb90b3fa6a532453418030e6b9867fbf90`  
		Last Modified: Tue, 02 Sep 2025 03:42:31 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e261c657d6266004418f3cdef98b9435b67cefa6c52917fca7eb95bd676ca8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291080536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96fc9f4d62238dddf2574761f1cead87fc8bf0bd15c9cdb3da411de6a1c44870`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976fe2678a5c3a0ed2924da3a9b1a2337ec1dd308b187d5161115d86c9392e0f`  
		Last Modified: Tue, 02 Sep 2025 08:14:13 GMT  
		Size: 156.1 MB (156081263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02c642fc6d1dd2cc8cb70e5abdf94a2dfcd54d9857aa81d035171f357622d9c`  
		Last Modified: Tue, 02 Sep 2025 08:20:58 GMT  
		Size: 85.4 MB (85356626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8cf6f0190fbea2af9d87eb6a9527361f5d016a78ff84caed6bffec72a64083`  
		Last Modified: Tue, 02 Sep 2025 08:20:49 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3e7274beae844edc12c6ff70afbaf15f4c937f1b51962ea6479d32e4c25de5`  
		Last Modified: Tue, 02 Sep 2025 08:20:50 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f890a6ad06f005caf555e2c07930860cbd95dbd4137a945453b487ce84a24da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f741d7ac59b88222c39689b33832ed2c7a68694e4f159173bcb6d3235bb669a4`

```dockerfile
```

-	Layers:
	-	`sha256:dc476fd9a084963fc54c75ed6cc7ab45782490d4ab45b16239a51606d9ff2a8f`  
		Last Modified: Tue, 02 Sep 2025 09:42:03 GMT  
		Size: 7.5 MB (7473045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ab186891ef04a6c4327d51b79c177bf0b6273e30955dd0c4ec9fb788b6a40b7`  
		Last Modified: Tue, 02 Sep 2025 09:42:04 GMT  
		Size: 16.6 KB (16606 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:ce907cf371a4224f3c2a0308aaac8467ae36613ccf05b7e38fb3df166f7fa084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (302008727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87103d8bab2f73aea89594eb4d1baab26e9be6d73dd08efca8da6e0f37174541`
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
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d990776a519a48cfd9f76c1a1eb9307ce4a16a3ce460aaa1ddd5616cf2ea8d`  
		Last Modified: Tue, 19 Aug 2025 18:06:40 GMT  
		Size: 158.0 MB (157963439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f24945a7c512ed79b894e68df488ebb968a0126123da75a0685b050dbac0ae`  
		Last Modified: Tue, 26 Aug 2025 18:12:17 GMT  
		Size: 90.9 MB (90940858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87e331b9641fa7afa7d22ffbfd7ec9439c275c5773deaf6e7cf4424c31770b4`  
		Last Modified: Tue, 26 Aug 2025 18:12:07 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16dee6090998c3b39235ba4e69943c390cb78741ee97cd8b9a312974fd46e5ea`  
		Last Modified: Tue, 26 Aug 2025 18:12:07 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:cccbfdc87ea9408320088eae7a907a8fa03579f5240def6fdfba7a6fd05cc4d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc49b9ecf204b296bd9286f4e57679452d92a55c0a1e89ea8023a63a3afbb8a`

```dockerfile
```

-	Layers:
	-	`sha256:9b1062e94cf09b401c0b65f462eb5549b15ab998763d8ce04dba4d299850d06e`  
		Last Modified: Tue, 26 Aug 2025 21:37:36 GMT  
		Size: 7.5 MB (7470422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1502997d8e89a31b74561aaa949154d9887b735720816f282098f0ddff46f67d`  
		Last Modified: Tue, 26 Aug 2025 21:37:37 GMT  
		Size: 16.5 KB (16524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:69a762fbcc07f22304c8e4c47b16cd37962a365960eb2930f4425caa87e23122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285783881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9d94aaaf54029b94cd4d21a3ecbb1372213b2a5fb06e493024b6c95b5990b0`
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
	-	`sha256:59f3e0adb655cb03f7d489f3cc57e302e249916bbb076c78008f9329238bfb20`  
		Last Modified: Wed, 13 Aug 2025 01:13:55 GMT  
		Size: 47.8 MB (47764303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bffae3a33fbf86c821fef106b632710dc7ec1e7ca68bbba90801f6da94b28e2d`  
		Last Modified: Sun, 24 Aug 2025 00:20:19 GMT  
		Size: 153.6 MB (153593530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8082f6858a52a4a05a82821c9a8b69dc1315c5c2b533e66b1ec592ecb2b58219`  
		Last Modified: Wed, 27 Aug 2025 09:27:32 GMT  
		Size: 84.4 MB (84425002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67dccd8bcdfac6a7fded0fab61a6da52c243bfe2336c414af7ea6efc3cb77b34`  
		Last Modified: Wed, 27 Aug 2025 09:27:25 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a80e2b4dc8e3dd01ddf5c44abf90eef3d22550f8d031c84c0a1d5361379a171`  
		Last Modified: Wed, 27 Aug 2025 09:27:25 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b81147c2007d7b98b26fab86a2ce5665353501daee36c785e9f93d39378e3196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7470441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7390bfa6ba286cdb85325a26739a7ca924594ff1643f6fed5d9f9bee315cda58`

```dockerfile
```

-	Layers:
	-	`sha256:eed1291a39e8f6209ac7b991943f4d53954503515965ac97c7e94ace72b56aa1`  
		Last Modified: Wed, 27 Aug 2025 12:36:36 GMT  
		Size: 7.5 MB (7453916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a610ddccc6201691911e18c2dbdab41fd61d374d06e9bc6fe64d414ce44d55e`  
		Last Modified: Wed, 27 Aug 2025 12:36:37 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:edbb5fe543cfa8a157b1555461e2ee9aac2cb4966298dac54a2365d322cb064d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282871609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6ef851b91e8e02217cc00952bc9a9875a9c46f2ac47452c42946d24488059a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
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
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11274b7b67f34b1c90618b5eb3b20b0a723f725f13144b8d420fa64deaab5389`  
		Last Modified: Tue, 02 Sep 2025 02:13:08 GMT  
		Size: 147.0 MB (147026986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57956d0dcc6ba572e32d91ffd36f3f8417cda5ebfa21518121ce5a096b3ccbac`  
		Last Modified: Tue, 02 Sep 2025 02:19:58 GMT  
		Size: 86.5 MB (86498418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fe109ebb6cf2b3e05cb20fde249f4c82e8ecb40f894c2ad8b5fffe7c698f98`  
		Last Modified: Tue, 02 Sep 2025 02:19:38 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afd9b9ba439749a198b557bf9e9359979e9c242c957acfb65d300e36f49d593`  
		Last Modified: Tue, 02 Sep 2025 02:19:38 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1166b582e2e895ca36547ca3f2ca2e0b0b6d90bab47d5dbd98e75a4d740c8f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7478378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c1380f661865f300f6bd39f248dce736f07ac55c536cee955c3c0d8795fb1d`

```dockerfile
```

-	Layers:
	-	`sha256:e90cae8d4011b6fab153abc2a01938675c2cf74fd271c7daaa4d5ea37f200fd2`  
		Last Modified: Tue, 02 Sep 2025 03:42:54 GMT  
		Size: 7.5 MB (7461913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fa32a7ff489acd7a48f62445a43fe7f5038e0d69e0ea923f9a2685a031cedc0`  
		Last Modified: Tue, 02 Sep 2025 03:42:55 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json
