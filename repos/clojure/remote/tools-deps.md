## `clojure:tools-deps`

```console
$ docker pull clojure@sha256:94dbe76df9d5196da0bf35028fa5666ae5efe52fdae8ed682d254e3bc43571bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:70e5c40a7230090ff04a0526980fbd6682427d8e00952ef14fa08f18c6dcbc39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221665299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d304f1ecf86e2a250d128d6edd74e9bc126bfc1026c39362c7b85c541c839365`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:cd01849e3cbdfc6993640303768edbb56372cf9f1ae101d516334c8d462341af`  
		Last Modified: Tue, 21 Oct 2025 00:19:25 GMT  
		Size: 48.5 MB (48480563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5805c41b7595c97916ed1f1d3d2115d964f61298914d882d943bf34b91fd5941`  
		Last Modified: Tue, 21 Oct 2025 02:18:28 GMT  
		Size: 92.0 MB (92036044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1b09ba1d358b1f73eced3fd3903ec671c72b16490f17c4c77d1df231d9fdb1`  
		Last Modified: Tue, 21 Oct 2025 02:24:19 GMT  
		Size: 81.1 MB (81147653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89534c6736e552b5d1011497741503cc5d2a0ec1c80c3ce44dcb3236011ecf6c`  
		Last Modified: Tue, 21 Oct 2025 02:24:14 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3474d79177df934640d74ad65c72cd1b7f8aac6941134f05d64ac3d7fae2f60`  
		Last Modified: Tue, 21 Oct 2025 02:24:14 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:3d7257198064dd6d5299ab76437ab94aa33f33a891992bb0a4dbb476e1318c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7344554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf218e6fa80d04572facfcdaacfab36efdd0257fd0031dd881caa6a24fba048`

```dockerfile
```

-	Layers:
	-	`sha256:04ca72fdb4fe442f365c619e9956055f033a8f984c4afcc8d929224fe92ee6c6`  
		Last Modified: Tue, 21 Oct 2025 09:43:58 GMT  
		Size: 7.3 MB (7327540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b08bd7488e0efa3fa4d8627271a74921fc283901e43fe61fc419113894481f`  
		Last Modified: Tue, 21 Oct 2025 09:43:59 GMT  
		Size: 17.0 KB (17014 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4b8f14df3125cde0cbaeaa92540580f0b7750917b9aac4076bb2f31ac7f22d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.4 MB (220433616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a31f32a707b3e1ad02bb6c3f312dd70c2895772f3198cc1f1cd50e2ceb2e43`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9b33ca3d6cf60049b4113fbb54195dfbe288100dcbbea36bea9717a7361325e`  
		Last Modified: Tue, 21 Oct 2025 02:24:47 GMT  
		Size: 91.0 MB (91045213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a0537702d269c954dc5b9a79f8358533f8f07e029352b94d7e3a960d8cc4a0`  
		Last Modified: Tue, 21 Oct 2025 02:29:49 GMT  
		Size: 81.0 MB (81028365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530375599816dd5c0c6ed8a123a5c30bb96d655ed56cea9a6d17ade6e6e4abd6`  
		Last Modified: Tue, 21 Oct 2025 02:29:44 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb98a63a84e0feefcdfda2de699d619972230e58aefbb71c7ec0a22eaae8de5`  
		Last Modified: Tue, 21 Oct 2025 02:29:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:cdf217cdc35504fa19908096be6a166ca6b6af281c3593a78ea795bb54ef6f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7350577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b4d32470241874aa17cb3528083b68077a2f0d8281ed298074bbb8f894e209`

```dockerfile
```

-	Layers:
	-	`sha256:36d6cc6e3a9693cfc7a9eac5ff4493fdc625b8d087e26c7248d5575d03285fe7`  
		Last Modified: Tue, 21 Oct 2025 09:44:05 GMT  
		Size: 7.3 MB (7333372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8678a59a8b622e02cbcd0598b24e505142f94d0a66dbe2709fe1f90ff9a20375`  
		Last Modified: Tue, 21 Oct 2025 09:44:06 GMT  
		Size: 17.2 KB (17205 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps` - linux; ppc64le

```console
$ docker pull clojure@sha256:4dfca76a2596b231b20357f54545aae9be7b28177082bcebbdb3c35c7b10c609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230915083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee45776c74c6901d5ba036a34ebab5832adc99e7c6e236d5445093809163543`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
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
	-	`sha256:297b234228c60cb6a9bc0156bdf582119f3c4f22112d7d2e8128e4d1403158cb`  
		Last Modified: Tue, 21 Oct 2025 00:19:36 GMT  
		Size: 52.3 MB (52326787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd54176529d4ace0644eba88da8cca76ee8b5b9bf2f5f806af82dd66a460a0c`  
		Last Modified: Tue, 21 Oct 2025 15:18:53 GMT  
		Size: 91.6 MB (91601715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc9d7502a36c8561e60863df38d787cba6da4dad70ded88cb4e7ace043a7d53`  
		Last Modified: Tue, 21 Oct 2025 16:23:48 GMT  
		Size: 87.0 MB (86985541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407557df2682ccebddb304970af0035c3ca8cdb75bda08693996f89a93acb778`  
		Last Modified: Tue, 21 Oct 2025 16:23:36 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151ca82c8c05de050fe6d826168a2eed3a89f3a677277db66661fd42418a676c`  
		Last Modified: Tue, 21 Oct 2025 16:23:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:9663ffb9074993371d2b56518994958da77d412b240240014476c04ff382a74c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7351986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6fb79c61e21b33a437e4820697c734a411c95a48e7829321d384a9d205e2f8`

```dockerfile
```

-	Layers:
	-	`sha256:0ab04724bf68d0be70a86f6b24a67db0c7ac4c323500f03ea01ae816dde2bac4`  
		Last Modified: Tue, 21 Oct 2025 18:40:25 GMT  
		Size: 7.3 MB (7334088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51100f86c1b82282347bd620676e85b4954cddf4cb973add16b7b056b1143a69`  
		Last Modified: Tue, 21 Oct 2025 18:40:26 GMT  
		Size: 17.9 KB (17898 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps` - linux; s390x

```console
$ docker pull clojure@sha256:a218d120d722cbc6b45e9e3920b191edbb2c969eda5755b7f9cd0fd972674546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215301718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dff2160d7d496a3fe7dd8fb831eb2fc7bc8cb8ab25b7ba8b7f7a884dfa5ff9e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
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
	-	`sha256:769a86a44e9ad2fad1b0132047fcc9c080f859777f09d3856b818bc85f1c5895`  
		Last Modified: Tue, 21 Oct 2025 01:19:50 GMT  
		Size: 47.1 MB (47137521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099c8a1ecb54dd92b837ffc9a8f452313bdf052751601de2883d9af4001e429b`  
		Last Modified: Tue, 21 Oct 2025 21:41:46 GMT  
		Size: 88.2 MB (88206434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657cb15f0f3f99a9c18531cca78ead67fd00cdbf4f9a0b2f7138c53b4217e740`  
		Last Modified: Tue, 21 Oct 2025 22:45:57 GMT  
		Size: 80.0 MB (79956722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fedf081e26928211b8c4282558c368d495ac0445c65a0e5d516b87077f5379`  
		Last Modified: Tue, 21 Oct 2025 22:45:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e51b8571a6882bd26f1310025151cf58ed3020c413ae727e0e388b7ee46dd6`  
		Last Modified: Tue, 21 Oct 2025 22:45:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:03da815655888f1f4a23169c82a453939cbdb99c267fe4f30684e36d03d6a5ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7339221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae71b9eb06c375629e0334ed5256aa8445e001eb3b294b865a9b7d8a8931e2c`

```dockerfile
```

-	Layers:
	-	`sha256:71a84613bfefb35ae2e877b8ab5f486582d155767a76cbdcdb87dfbe75accefd`  
		Last Modified: Wed, 22 Oct 2025 00:40:20 GMT  
		Size: 7.3 MB (7321407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19d3805b8d1b8196bef51a714ffba4d642c0122198240148da9617cff5f635fc`  
		Last Modified: Wed, 22 Oct 2025 00:40:21 GMT  
		Size: 17.8 KB (17814 bytes)  
		MIME: application/vnd.in-toto+json
