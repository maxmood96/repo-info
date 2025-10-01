## `clojure:temurin-21-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:cc63f75577ded95182e4801e4aa2f1a29643d13b75d3ec8939630d60e085b9b0
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
$ docker pull clojure@sha256:93df7bca4496dd6a58cf6aa1b8fb9f08e39984a891da9995d75d513679caea86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259578782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628aae683d35bf36b75c87c22c8a3d4340e3cce2a792a6bd922e45d73162b5da`
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
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499630323d50d1bac3ac3747459b6af3cd93ee93ca1c87b31e66bc05bca1b16d`  
		Last Modified: Wed, 01 Oct 2025 20:36:08 GMT  
		Size: 157.8 MB (157804740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155b368562870b7f6f738d96366c7d5201e4584c468ffc191bb7ca129bbfb96f`  
		Last Modified: Wed, 01 Oct 2025 20:36:27 GMT  
		Size: 72.0 MB (71995238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adfbf193bd484960a30a9561ed46ecee86a16c3d2e9ab6fada8a7af4228e5b9e`  
		Last Modified: Tue, 30 Sep 2025 01:39:27 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdf152c91795f5d24065b632e1a197478a27e424be4fca0edc4705753b247de`  
		Last Modified: Tue, 30 Sep 2025 01:39:27 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9be9e61080025f13e27ac78a55511a70790ad0e77bc3356be1bf7c9be2f9cea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c38dc7740f04156b809250a434c17b287fef853747c0da879513179c348301`

```dockerfile
```

-	Layers:
	-	`sha256:e3c56ed042b1adfb94c32ef9038b95a7375354ef4b3c317eb2f81d9d1b68f34a`  
		Last Modified: Wed, 01 Oct 2025 15:41:26 GMT  
		Size: 5.3 MB (5259215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fca2bc9e114710a8665f491d80dd2e8100699509c1829758d6cf5d5ec6c2bb98`  
		Last Modified: Wed, 01 Oct 2025 15:41:26 GMT  
		Size: 15.9 KB (15854 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:928a22ae7e828a83eb066ea9e4bac8f85c9cff6f5608e3d9f903bf0508253d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (258027371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4b0fc60b22ddca830f4cd28761d63cced7c3c7dd965550f03f204879d5fb0fe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48885ef8df8d31bc8d2cd58eca60171687f26de7b020a6b9351edc676f80aedf`  
		Last Modified: Fri, 26 Sep 2025 20:02:29 GMT  
		Size: 156.1 MB (156081176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c166cb09f87a111adeda7ebe3a6652c6050a9a12ed3d6aecb3b09f0ac4ee136`  
		Last Modified: Fri, 26 Sep 2025 17:56:20 GMT  
		Size: 71.8 MB (71808521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53db4625540af8edb149e0c3ce73ed3a71c0043939b59d0857029b08e0e86d3`  
		Last Modified: Fri, 26 Sep 2025 17:56:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e498dcad9bf211461f6d8a22b6d0a071dcc6356ef83396f0dcbc31abcaa404be`  
		Last Modified: Fri, 26 Sep 2025 17:56:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3da92b82bad2a82a92ce03e29d08e51a1d4570f80c14a98f8db7c653cce74d26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53975e4de1fb13fbbec8a9abbeaf916c48f54270f8815cdfccfa39f65237152e`

```dockerfile
```

-	Layers:
	-	`sha256:b15789167c2e46d35e8033d054c31043b34bffad2024f8fc612d7dcba7846dd6`  
		Last Modified: Fri, 26 Sep 2025 18:42:56 GMT  
		Size: 5.3 MB (5264984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fb363f21810c25f701cdd4a08d00f5ed26463517e265e0185e585c5f97af7d1`  
		Last Modified: Fri, 26 Sep 2025 18:42:57 GMT  
		Size: 16.0 KB (15973 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e995b62525e2f6fab7da276a7125e164090ecb3cf86208806aa7cc40a893a388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268952468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc811d5739a079e3de2b3d696a3a5961f01016bdf5d907943ddcbc15563d10eb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03f10a1d117429fd4264e1411eccfac8f7dfaeedc79124dbb9e3449936146e7`  
		Last Modified: Sat, 27 Sep 2025 20:14:28 GMT  
		Size: 158.0 MB (157963520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5906daf5411363eff4bb04e142d8922197f6e2ab3aad8024300af318a8dd2df`  
		Last Modified: Fri, 26 Sep 2025 18:31:04 GMT  
		Size: 77.4 MB (77393556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13fd05611ff1a4bb680631edab9093a4677607d446244a8501f859be62c4a6b`  
		Last Modified: Fri, 26 Sep 2025 18:30:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125b92261895e84d20a91da768ffa420527e9ee283e962e10c07642c19b53989`  
		Last Modified: Fri, 26 Sep 2025 18:30:58 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7bc52e982bad219338aa1fe5cf1ec75b72ec0b840b587052b5b21a0c40af9cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02757eb655c00689f0c3a886c3affe9ad36d833bb80bfe39388711254bca7908`

```dockerfile
```

-	Layers:
	-	`sha256:46454f54d5a75a3652da9145fe1e34d062ce6091a0be7596ffac72d13eb3a015`  
		Last Modified: Fri, 26 Sep 2025 21:40:18 GMT  
		Size: 5.3 MB (5263586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e577cc25718cff0c3b21d023041ce5f780b45683b1369a46d7be06b9a651c6f`  
		Last Modified: Fri, 26 Sep 2025 21:40:18 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:8f0638980a34346987ccc3e6c0e9bc28457cde0666f8511b95427fd935455a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252746926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7010361391da66739ba133336048d7531923a371f18396f81045a8a610a1a8d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
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
	-	`sha256:aad65798ac3af68bb3d796da257a0138854ff669ee25377b5c0c648e9bbef733`  
		Last Modified: Sat, 27 Sep 2025 00:47:33 GMT  
		Size: 70.9 MB (70881018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dadd4cea2a07fe4570727784cb847ea0f0a240bf0462cd20c2d11eae1490fb2a`  
		Last Modified: Sat, 27 Sep 2025 00:47:26 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7d9cf1957104da57f9801eefa7be4852302482f90cd81afbdfb2432c4de08e`  
		Last Modified: Sat, 27 Sep 2025 00:47:26 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:803bbce4b2ad2abcf02e3dbf846df2d44ce596183694890ff5f8153dbec97b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aae94893d2a1785c3cf25f358558d14df2123aa906839d01168fec7da164042`

```dockerfile
```

-	Layers:
	-	`sha256:9c0244d422b3ecbb16c67ab330781b0db89388dbf320e2c40fe5a73007a80e60`  
		Last Modified: Sat, 27 Sep 2025 03:36:50 GMT  
		Size: 5.2 MB (5248679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b6f2325cf600513400ff9d10485f9e3bb7fb94e5a95ecfc1267b97f3cfe466a`  
		Last Modified: Sat, 27 Sep 2025 03:36:51 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:2e9eca6ff064f60151bfab836de1361c120526bb70c2a1b97babc9daaf835513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249814604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1ac15a2e2ef6e7470349583623525c2e5a0c258d7a248164efb08343ce8469`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
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
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed27b54b5da895d580e2677d4f4c020abf7f5c32353c331fbbc3b3b265e0c68f`  
		Last Modified: Sat, 27 Sep 2025 20:14:30 GMT  
		Size: 147.0 MB (147026970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b767af00f984cc2a85446548155620f2a6dc2b3e52ea38c36eaa092c1878867f`  
		Last Modified: Fri, 26 Sep 2025 19:30:03 GMT  
		Size: 73.0 MB (72953688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c686228badb7265e04ecbc3930a6e033620e45fb0bfeb00bedd7c30d5fde77a`  
		Last Modified: Fri, 26 Sep 2025 19:29:57 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e024fa1adbba1dd6957d164b16857beb07f4ea2c1d11d4d3551e122462e79b`  
		Last Modified: Fri, 26 Sep 2025 19:29:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0245c0569dc8759ba76580cd552a08b4c87d5bbc68d22954d9fbbc82940ad446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133122e2ce26e44f52e77cc0454149e6519e6f7ef1a44a781fae05e9a82f4eb2`

```dockerfile
```

-	Layers:
	-	`sha256:6f33a12db91b8a18caacb4fbb86f9d725620fd90998e0ffe235f3e371258c4e8`  
		Last Modified: Fri, 26 Sep 2025 21:40:24 GMT  
		Size: 5.3 MB (5255139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce9592f214fb7a024e394a00a895862bb08414acd3e6fa58fdb41a5d0ccd9ac7`  
		Last Modified: Fri, 26 Sep 2025 21:40:25 GMT  
		Size: 15.9 KB (15854 bytes)  
		MIME: application/vnd.in-toto+json
