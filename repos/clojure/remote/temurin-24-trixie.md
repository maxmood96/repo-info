## `clojure:temurin-24-trixie`

```console
$ docker pull clojure@sha256:a44ea6fb2668ee7fb7b74ee6299647d89770436989ab31e8338a314effd8a1c1
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

### `clojure:temurin-24-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:fd85b11605ba6e6b52169ea783ec9e578143ac22f58205eea4c4921304ec45d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224789281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3173feec6d4d41c217854f3a0eafdf13c2e2b61c57c7896a06200e0c91f4be29`
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
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0336cf383e1122827daf2705abf4681ad4cb6e3b78e770d661729be608ba5443`  
		Last Modified: Tue, 09 Sep 2025 06:41:44 GMT  
		Size: 90.0 MB (89975189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f403d97e70549add85009e44b5d9222e3d8d45504e86cbe2f240f01a2d9935d8`  
		Last Modified: Tue, 09 Sep 2025 06:41:41 GMT  
		Size: 85.5 MB (85533517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a7b714ee428eba7619f61ad01178a47c35e03072b2602bfe253ea63c009cf4`  
		Last Modified: Mon, 08 Sep 2025 22:36:33 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae6d500d2889fc53d14ce3d4b661e15b9fdfb4624fa1c808df97833630ffa1d`  
		Last Modified: Mon, 08 Sep 2025 22:36:32 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bbcb65ad29319be5dc7eed16450bd91a4926a30b041d902373e846cee821564f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57fb6bc8cc0db31ae249aa08a5ce64cfac85440ba8d214ae124b89819223a0a2`

```dockerfile
```

-	Layers:
	-	`sha256:5a194e710bb4f6e3bd59920ecbeb9525cb062a0d65e858a69c0a2d131e15978e`  
		Last Modified: Tue, 09 Sep 2025 00:44:56 GMT  
		Size: 7.4 MB (7417493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:601a694ab142fb0d24dd010438cc1869fd6767539e73cd67632311707fb97799`  
		Last Modified: Tue, 09 Sep 2025 00:44:57 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5c3fafb6b995ba6143e7dcec81768e4f9986a346954192e787e00e9da8366462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224095146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa6aafd18623bcd8504c97bb5c51d897f5b515b07a3a63d5f5426e853861fdd`
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
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db082e585a30dec2ec23e85f8cf920ce07b3ec9a3d0149cd102c4b63f6f1514`  
		Last Modified: Tue, 09 Sep 2025 06:41:42 GMT  
		Size: 89.1 MB (89092502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60847bc0aebf34c600b3c9fa75890cb9ee919f25ed9ec1d7fba24d3b7330e7d6`  
		Last Modified: Tue, 09 Sep 2025 06:41:41 GMT  
		Size: 85.4 MB (85357856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613ca07509cf640c0ab7ae04f562bb473a16c1babc6a85a8dcc596f72016e5dc`  
		Last Modified: Tue, 09 Sep 2025 01:00:18 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466bb31fadc8819c66a9f64f517dde0f28a9258a8c93c8bba2e56d07b0b6f81f`  
		Last Modified: Tue, 09 Sep 2025 01:00:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f1cb571d3c39a1a7566fb87944f3982a18030c74a4b86ae31f28d39bf4414d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3923faf3c8359b90e3d4742e69192003d5e3fc4a11fb714c8162bb405dfc6b0`

```dockerfile
```

-	Layers:
	-	`sha256:2a070521e76209226e4502cb73481e4b62d7f6ff7cb0f00ad3ab4d862478b01c`  
		Last Modified: Tue, 09 Sep 2025 03:42:58 GMT  
		Size: 7.4 MB (7424520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fa92a520b4d345acfcba9f659eaeb7ad60c704976519d2bb7601ad9315fe9e8`  
		Last Modified: Tue, 09 Sep 2025 03:42:59 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie` - linux; ppc64le

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

### `clojure:temurin-24-trixie` - unknown; unknown

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

### `clojure:temurin-24-trixie` - linux; riscv64

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

### `clojure:temurin-24-trixie` - unknown; unknown

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

### `clojure:temurin-24-trixie` - linux; s390x

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

### `clojure:temurin-24-trixie` - unknown; unknown

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
