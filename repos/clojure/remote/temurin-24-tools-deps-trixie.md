## `clojure:temurin-24-tools-deps-trixie`

```console
$ docker pull clojure@sha256:e6008164b7ae49d9357eb586096d553b11afd37d5115dcb9a710b8079f74cee2
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
$ docker pull clojure@sha256:19b53009b1a12f1c88f0d584d6bc0d1dc7ed05684b28421838b81f66804906c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (233974250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b5790089244f4cc8dd5ddaab6b925b812ee08124b0c7349e4db8312a016ba8`
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
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22288e692ffca781fb8068806004c9b9674c1fdc964f366b16d682c6662ee0f7`  
		Last Modified: Tue, 09 Sep 2025 12:58:49 GMT  
		Size: 89.9 MB (89918194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9959619a40cddadafb9d65434c016ec238f4713dd9893323888ce3f6b00a37f`  
		Last Modified: Wed, 10 Sep 2025 09:03:38 GMT  
		Size: 91.0 MB (90950577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fe6cf77742100b5456ba151f4b18add92823f357c9fa5cae1d060894eba2fa`  
		Last Modified: Tue, 09 Sep 2025 13:06:32 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a508b8540f18de7cc5a9b9152aea74ee62de35012476b037aca5eb458072b71f`  
		Last Modified: Tue, 09 Sep 2025 13:06:33 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:700e1fa99cf70c4e6d0a1e45ae5f8dabede94e2c244c761b80281d8c34428a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7439048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1462c6b2f06ad0d70f7da9b41780913e52cd0c261cc81409fffeb34ca545bf`

```dockerfile
```

-	Layers:
	-	`sha256:9fbbbdb4215ee27356f5171deb07f886e29294b98983baa208519d3419d80ba9`  
		Last Modified: Tue, 09 Sep 2025 15:40:40 GMT  
		Size: 7.4 MB (7423210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b8634f2bde207422790244187f2d33c9fdb1f9719b5f99cfbe1ade6bc93fe42`  
		Last Modified: Tue, 09 Sep 2025 15:40:41 GMT  
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
$ docker pull clojure@sha256:6a8f065cf175a8ef7d327f765d9dc34ec9789d625be58260286af1ff9b64e034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7421240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e16081243f66034530a0e7993afc56108484fd21d9435396f082d566ab6f36`

```dockerfile
```

-	Layers:
	-	`sha256:b5a34aae958656d35ab2266d8746a8329c254eb37fa531364a0bc2fe445370d3`  
		Last Modified: Sun, 14 Sep 2025 03:36:56 GMT  
		Size: 7.4 MB (7405403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03b576aad7b1cf940308b9fce8eec4bb99b104d7e68634b708c67fbda688630b`  
		Last Modified: Sun, 14 Sep 2025 03:36:57 GMT  
		Size: 15.8 KB (15837 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:b8b5c0306db7de0913a70b4c16c43e0f64c8392136d647a37a1f030560479eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221080091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cbe7288ba9dc1f4be05f486b38d108cbefa747f05e8288ad0838b2600ffa680`
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
	-	`sha256:28eee642962fd09c10ecf87da2d4b65d208f3d5c1bf3fcca21c105c0213f558a`  
		Last Modified: Mon, 08 Sep 2025 21:32:18 GMT  
		Size: 49.3 MB (49346327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113126536af3f2c7de1d551db8a59d80161c593dd41126b7de2dabd16d17dad3`  
		Last Modified: Tue, 09 Sep 2025 06:41:28 GMT  
		Size: 85.2 MB (85226409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5086c7bba49d56bcfeaa9f9ff2ee2ef38b8398b01cdf893c3879e7ea801aa6cf`  
		Last Modified: Tue, 09 Sep 2025 06:41:39 GMT  
		Size: 86.5 MB (86506316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3112234ed69956236fb4f790e02d0765212dbd951a2676c485f45c467e4c36f4`  
		Last Modified: Tue, 09 Sep 2025 06:41:30 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe924675305de81ae27409a852e7d1974ebf352c618b3c5ec6467f899b116a08`  
		Last Modified: Tue, 09 Sep 2025 06:41:30 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3d6eeb3e6c4abafe879be48f2493055aa896aec8281930ef6ec9baa5db7f9c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5489d490d53b88ff9db4aa8ed97cd772549c56db269c596fe8385c0c05017db6`

```dockerfile
```

-	Layers:
	-	`sha256:b222b9408ea027742ae50871ee44c15142ddbf9d7ba236fc6dfe774e23840c5c`  
		Last Modified: Tue, 09 Sep 2025 06:41:07 GMT  
		Size: 7.4 MB (7415963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59590fe88ef64ecac3864d7ba29ee00ba9427b1f6a83892af02b904ca7da6d66`  
		Last Modified: Tue, 09 Sep 2025 06:41:08 GMT  
		Size: 15.0 KB (14991 bytes)  
		MIME: application/vnd.in-toto+json
