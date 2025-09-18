## `clojure:temurin-24-tools-deps-trixie`

```console
$ docker pull clojure@sha256:6e350e1792baaeefac674ca8471d7292010d5d8814ed2039bc2b522b2277cc34
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

### `clojure:temurin-24-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:720017204cd5d0fc1507876940ae0f2c8f189380e078eab162bc069e4eb0c9b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224789458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9cc63ef6884e13619c857ac7c4e51f9e58afcf52420e07a8f0678b964e1dc34`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41a7ea64d408c9ef2bbb3c2cf6aba2beb61fd67d6fd382fc3abd7c836cc4463`  
		Last Modified: Mon, 15 Sep 2025 23:29:02 GMT  
		Size: 90.0 MB (89975169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75203288c8dec1313eebb78b84992eb80633fe97f73a7a80a6cf0521eb9930ab`  
		Last Modified: Mon, 15 Sep 2025 23:29:17 GMT  
		Size: 85.5 MB (85533715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28112828a3effbc5b43b620c49b0c6d3cdbbf0aaec07d68652370ba3ed7250bc`  
		Last Modified: Mon, 15 Sep 2025 23:28:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c62fec89a25a781194060c7f6dc690abccfb01fc08bad00059b3d9586afa28`  
		Last Modified: Mon, 15 Sep 2025 23:28:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:308e4e42793f3dafa0734f733b78083f527efbb1c6a955f6a934e7db15800636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9227a9dda16334b26f060034db9b63039ac888eae038a160ce0056686a33153d`

```dockerfile
```

-	Layers:
	-	`sha256:415b36dd4d315e26ebc191007472109da91dc8f060efcd895d9e53c12e7efa99`  
		Last Modified: Tue, 16 Sep 2025 00:46:52 GMT  
		Size: 7.4 MB (7417493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6b1fb6284f9153d321231d967f2530eec18b6e494fe0756214c7954cf971467`  
		Last Modified: Tue, 16 Sep 2025 00:46:53 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f54b40599536d6131d344497e1ed163c14302ead2486d462f6203bc2efeec764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224095171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c64eb481139a62b673f86c73c78898bec71c363034f2caf9fbaed99225019c3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f941f8753c92c9adffc3ba0e32dca99be8567110d4b66dbb6946c9dadaaa143b`  
		Last Modified: Mon, 15 Sep 2025 23:29:37 GMT  
		Size: 89.1 MB (89092540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047de31dbd1be5b82d18fb242951e15cdf726a5b784dc88d46b5f5f187b8fdec`  
		Last Modified: Tue, 16 Sep 2025 01:03:53 GMT  
		Size: 85.4 MB (85357846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa00dd3c416e35545732a1aa46b5b273ae01c9c90fe189d55e08ebaa84d65e9d`  
		Last Modified: Mon, 15 Sep 2025 23:29:33 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198352cc39ed559b930fa98f9eecc18cd2728179d74616fa09869216270eac96`  
		Last Modified: Mon, 15 Sep 2025 23:29:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:00b73e0badfc69dd9ca35442d6a54ec3f8bc2d39f38b8af046dedbaab099bc9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6feeb1b8505bcd566e00b6f6bd09bc2bafc6199cc2dbbf6f8cebefff7e3e5d6`

```dockerfile
```

-	Layers:
	-	`sha256:36cf02c7fecb4e48ae3f5a014cdf7db02f31cee5d1f8f0adc6178bd90f5ec27f`  
		Last Modified: Tue, 16 Sep 2025 00:47:01 GMT  
		Size: 7.4 MB (7424520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1e5333b5e28747a0b9c055eb48ce2d1b45a47c34565da0a7535fbc4318bf3f2`  
		Last Modified: Tue, 16 Sep 2025 00:47:02 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:a68d71af10dfa8808340ebfb9b48251d9a6ab834d0552e25964f5087b45d14a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (233974386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d5edf08c2d5339f05af35bb20577d1fbca63d42de936fd05e134711dbd9c9f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5b739094a78d48c0bbc7fb63510f63ad98a27b361a087db2310996e81c516f`  
		Last Modified: Sat, 13 Sep 2025 03:54:37 GMT  
		Size: 89.9 MB (89918174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc81508cdbac8194ab26c6dd0825bbc7fa05da625a28238b1eaea7871125eafe`  
		Last Modified: Tue, 16 Sep 2025 01:35:59 GMT  
		Size: 91.0 MB (90950734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6328c5eb9f622700866cdbff04abbfcc164c52d0e2e9ffd4c442b0c94745d030`  
		Last Modified: Tue, 16 Sep 2025 01:35:55 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95cf85728041cc8abaa147e70f8180f1fba3e42030ddfb3395c3275e15e38fc`  
		Last Modified: Tue, 16 Sep 2025 01:35:56 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bb8e6426f8a44a38a922cf194da323c34c32f4da548623892c5cbfff28c9bb7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7439048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:566bc4deb241df40ddf372fe26f1552f12a88c3bd15a57c06335e867a8217406`

```dockerfile
```

-	Layers:
	-	`sha256:24d486f26a8156f1e524b50c2e5aa5849c9663c9f2a82fe62fad482d6672c2d3`  
		Last Modified: Tue, 16 Sep 2025 03:43:59 GMT  
		Size: 7.4 MB (7423210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:209d2ed4cb7810e7c8caf7401babb7986d99da5159b4f067e2d71cedb30c165d`  
		Last Modified: Tue, 16 Sep 2025 03:44:00 GMT  
		Size: 15.8 KB (15838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:878f38f87a33ece92268463cebee152c833243ea6ac35fc5909abea5d7fd118f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219863987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c047a07d4763c9a6229e4a9d74baf98f010fabe543cbfd6abb7f18fd0940ddfb`
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
	-	`sha256:8f913be5ecadf79e3ee9792194aaab366421c7e066487d572f285b293ff78a7a`  
		Last Modified: Tue, 09 Sep 2025 00:25:27 GMT  
		Size: 47.8 MB (47765447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7d189ceacdc7f5da0211b697db9d729111f59e6d463a6da7206d9f465b3934`  
		Last Modified: Sun, 14 Sep 2025 00:31:09 GMT  
		Size: 87.7 MB (87670426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671fab5ea11a48213198fd20ff524839b329c2e5f7b39a7d84f5075cf5ce4cc9`  
		Last Modified: Sun, 14 Sep 2025 00:31:10 GMT  
		Size: 84.4 MB (84427071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebed05a67432538b9c78ca65d73f2743cdb98f1bce4c832b4dc0485a19c9b5dc`  
		Last Modified: Sun, 14 Sep 2025 00:31:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f8efaa073e814eaee7cfccb40492c1af76cfe09bca81b866f802a50c6e3c90`  
		Last Modified: Sun, 14 Sep 2025 00:31:00 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b16d86565f99797b14fcccaae60623e084ae4f79731b2f9e47d5a053eb3b56f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7421241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fcdb4c5c76285d0b66af98d2b327ba21c1b3a27124f3156aad767ba021818a3`

```dockerfile
```

-	Layers:
	-	`sha256:0d17498f9221fe222b0ea66fa95703f300be847892d1bf14f6c6c5a2a416b161`  
		Last Modified: Wed, 17 Sep 2025 21:39:06 GMT  
		Size: 7.4 MB (7405403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d13e8ecf46ec625e835b1d0e0c370dab364d46d7795d744c21c36f5de4c83bcd`  
		Last Modified: Wed, 17 Sep 2025 21:39:07 GMT  
		Size: 15.8 KB (15838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:945833f003641f3c8dfe3a3833f7fb29ba8cf52f6d4671c8fceaec3ed39a1946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221079601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f277fabb7ab5fa3b74dd5cab2b56d3b5ec3811297e9571fb92ba1c39a6620082`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
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
	-	`sha256:28eee642962fd09c10ecf87da2d4b65d208f3d5c1bf3fcca21c105c0213f558a`  
		Last Modified: Mon, 08 Sep 2025 21:32:18 GMT  
		Size: 49.3 MB (49346327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09349677796a376b1cf6d7ed472d5ab8acf54c67c758a17004a2a4e5cc7fb8e`  
		Last Modified: Sat, 13 Sep 2025 03:20:43 GMT  
		Size: 85.2 MB (85226397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffff4166fbbcb0fb045db129fb69579865b79e59aff12a85dde7fad92e07b6d6`  
		Last Modified: Tue, 16 Sep 2025 01:05:58 GMT  
		Size: 86.5 MB (86505832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283c04815a9a592ed15a49607e28d30db3a8a99bd987d8ee60087b552ae05da9`  
		Last Modified: Tue, 16 Sep 2025 01:05:54 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c0e568367c50a287462f2c6cbd1fc5f49844c1da9c0415d549b143e7d70c0e`  
		Last Modified: Tue, 16 Sep 2025 01:05:54 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fcd621c9ce5fb50d85a63971e4cf5339523f8f7007596873060627696761b612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7431753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b7bf64480a00315d402f5450a6e0d157a3f5fd630410dfa5cec6cded487d0a`

```dockerfile
```

-	Layers:
	-	`sha256:ec9650668113249dec352325e7dab53f300c9eb3850aa9a78417a908c595f2e9`  
		Last Modified: Tue, 16 Sep 2025 03:44:10 GMT  
		Size: 7.4 MB (7415963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0986da4a81cd93be550ae6cae1b495806e37deaa419d4ac611a82df78668fc5e`  
		Last Modified: Tue, 16 Sep 2025 03:44:11 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json
