## `clojure:temurin-17-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:a682cb52e90142be172b7d8531c3068421e1359971f6ae5c97fad7044712f0ed
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

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6597f5a369925395a6c7a68283ae9a891c121333f145a31aeed1e0aa20b89c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246450480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfab93590b350c3926c869afad705277840705e8e17a5adb146f632d25bf6a52`
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
	-	`sha256:c61262b2f9dec48463fb7038ae959bb06c7fbfc3cb95a27709d122da050b6855`  
		Last Modified: Tue, 09 Sep 2025 13:36:47 GMT  
		Size: 144.7 MB (144693322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1116565b0dd4cb7e5c2cd9f385c2e66aedcb4d0164f41ceec52f678120757c`  
		Last Modified: Tue, 09 Sep 2025 13:36:46 GMT  
		Size: 72.0 MB (71982624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0181c1b978154b3dbd431e18f35869401bfe832f0d870089811ba5536006a343`  
		Last Modified: Mon, 08 Sep 2025 22:27:32 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948603fb53b0e629a0f9a475dbe5d66e04a09af4ffe48be2b75ce1607bc25c66`  
		Last Modified: Mon, 08 Sep 2025 22:27:34 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b476ac89a15eb7e3462ed803e57c39d573b4aeb06e9c8a709057bfa87476eef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:481d82837e94655369c3cd4841b5e6ee1e41254f099fce4d1383c5eb21054416`

```dockerfile
```

-	Layers:
	-	`sha256:7c7f879f59f9bba87df6c55c3562931aa8de98be25920067c32607397d65bf2c`  
		Last Modified: Tue, 09 Sep 2025 00:39:12 GMT  
		Size: 5.3 MB (5256113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a36a39294f49c45b150355515bd41888e6adfe925e2fe3a81824796ac0acb8e`  
		Last Modified: Tue, 09 Sep 2025 00:39:13 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b92d5ff7730458e87bef1d45c0cf743445a3ea81a66abc8daec9b60c21fe45e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245484043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b679293d9277702ce6715b97b5180c69f67e6ba63f518999c2e7b9f2b3531d9c`
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
	-	`sha256:ea8dd2429bd2cb979fa8e3836c00ab6940217269d8376b1d32b202a046926d5f`  
		Last Modified: Wed, 10 Sep 2025 15:07:55 GMT  
		Size: 143.5 MB (143542204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2488527a0e622305bd197979266f31e9ceeee82c0f7f1547a5bea3d4b88280c`  
		Last Modified: Wed, 10 Sep 2025 15:10:53 GMT  
		Size: 71.8 MB (71804166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902d019e5988536b8a5eb50cb546983836f1a263483af32ad69dca8b8e6d1d6a`  
		Last Modified: Tue, 09 Sep 2025 01:18:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0dc2c669529ce71c27206f9a821a277663483b7f6f8cc79bb5b5ddf8533319`  
		Last Modified: Tue, 09 Sep 2025 01:18:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f3598056e69e30a6dff1c14298da6cb26a29884331551c681a094939138c0dfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c5ca6d1687de0fb71d6cd1b52fb75630b6da80d9793a28d8ad04fdebb22345`

```dockerfile
```

-	Layers:
	-	`sha256:7f72a8d6c4832433be7f136dd12cccdf8a21f3bfa80dc2872009017269766eda`  
		Last Modified: Tue, 09 Sep 2025 03:38:58 GMT  
		Size: 5.3 MB (5261882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:258a1a46a19fcfa5a393f3496c6cf3aa8cb77c41319dc0759c3343fafbbe3941`  
		Last Modified: Tue, 09 Sep 2025 03:38:59 GMT  
		Size: 16.0 KB (15972 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:7a36c64adcea3f33dc01abc049f6bf4352df2eb16edc70e66592c86e5a998076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255366542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd851d9e9af416cde11fc31a97e48d0e19fdc042f32797a6d4cd0c747733a0c`
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
	-	`sha256:45f1300367a0a464ffeefe450d62f483090c51b26f3ac5e83d609f62c97592ac`  
		Last Modified: Tue, 09 Sep 2025 12:24:56 GMT  
		Size: 144.4 MB (144372674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691bc8be77f9e3eaa34e174834e6c100f948fa5eb5409c6ce06cf0a57336a953`  
		Last Modified: Tue, 09 Sep 2025 12:31:53 GMT  
		Size: 77.4 MB (77398473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8249c2034a210bc016060ceb18d5abff07f03317f800f07668998cc37184a1a1`  
		Last Modified: Tue, 09 Sep 2025 13:19:42 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b250eb14a455b18c22befda99a8a249b232b59af8b7a9eda33a009d5d886904`  
		Last Modified: Tue, 09 Sep 2025 13:19:42 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:94ceabef71df76fa9793c1828dacbe448b5a7e64831a89f4783429cc7a830f3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6754196e7c1599149d99f45ab84f366bffe37de93e601d982c172ba2290295`

```dockerfile
```

-	Layers:
	-	`sha256:bd242239a412a3dd3ac129ec81a70d92876ab399a43aea2bd8a9dec68edda5f4`  
		Last Modified: Tue, 09 Sep 2025 15:37:27 GMT  
		Size: 5.3 MB (5260484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cdff592522d759a0fd46304d03709f5f3abea4032882f79b17d3c032949cc6f`  
		Last Modified: Tue, 09 Sep 2025 15:37:28 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:e27c8cc431acdf268732ff3a42ec5cec36a409b5ca39099e125531e5224388a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 MB (237727884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27634b27721fc179bb2fae08aeba20b4cfb506c1e9f659fe35fdbfb95278e926`
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
	-	`sha256:d4e1d5e296080adcb97b55846e6f82f77ab692c109d2a4971bc1bbc3770f4f85`  
		Last Modified: Sun, 14 Sep 2025 00:09:17 GMT  
		Size: 138.6 MB (138575716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7be9c03992cf3a105f3599fa9d4a1d9a55ef1cc6e5d09437bdf32ccce9d3835`  
		Last Modified: Sun, 14 Sep 2025 00:04:32 GMT  
		Size: 70.9 MB (70879755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb77b836f64d58375d4e0c296e7557cd1a4c22e9d914d76de976f966aeb0dc0`  
		Last Modified: Sun, 14 Sep 2025 00:04:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca0ff13f9f7f2b97c443b50010995259a1677c9b0a0aa14235ee72375649e79`  
		Last Modified: Sun, 14 Sep 2025 00:04:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:200500d7b1652c425d1b367f72bf1f926976922a96158ba951edeaa4901e776a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a1917804615a975e326c5a59562b9841d448f88220430497c37909020da929`

```dockerfile
```

-	Layers:
	-	`sha256:a2f990921b23e9a51832f26a811646b5681c0c79ab05c4023f9f260656e2941b`  
		Last Modified: Sun, 14 Sep 2025 00:35:39 GMT  
		Size: 5.2 MB (5243658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6b3bb815e9d8be00fcfce5d605da6eca1663a779570553bf7e67330d9e53cf3`  
		Last Modified: Sun, 14 Sep 2025 00:35:40 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:0137236bece392db34a1d35dc9aa627928a7238ebbb3089c3af70eaf99176c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237509597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a23e63bc0b24e6323261a68062eea1efc045a42f9f7093b4fa41f39fa8f61e2`
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
	-	`sha256:46653f636035b640c3c0770e9665ba5f7b32427b0f72801b1dd838f05d9f0b28`  
		Last Modified: Tue, 09 Sep 2025 05:38:04 GMT  
		Size: 134.7 MB (134724288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77831e3a086d597ecc83654b643b54d99467548b3b89baddccc48ee699ffe0d`  
		Last Modified: Tue, 09 Sep 2025 05:42:26 GMT  
		Size: 73.0 MB (72951363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384b27db4a62c156e90a9bf33214ddb3ed8fbdcffbdb8d78d2381dee85218b80`  
		Last Modified: Tue, 09 Sep 2025 06:15:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38ddea3fa0f657636a83d5d7bcdc8799260a34c3e5340263580bf884b769780`  
		Last Modified: Tue, 09 Sep 2025 06:15:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:31ae19190cab92b32b4783ae265f726547e79fd051cfb94e951b9ae490f11a8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5267892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d71617b1e3b71ddea6c1af83754a8d9b813179b10b589bd02c3a3fc8f14234`

```dockerfile
```

-	Layers:
	-	`sha256:e156b194b5a0376d03ae97bfa12ca0f41bece6dab6c91c4bd028d593f67ca4ac`  
		Last Modified: Tue, 09 Sep 2025 06:37:54 GMT  
		Size: 5.3 MB (5252037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ae58f3299d5cc4ddbe291d669db0a2708cab247bfdb2841e251d761b8b99d46`  
		Last Modified: Tue, 09 Sep 2025 06:37:55 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json
