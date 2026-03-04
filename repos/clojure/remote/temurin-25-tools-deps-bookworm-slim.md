## `clojure:temurin-25-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:259684760b11682f12febb354b848ce9458c9795f015a462686ffa27c3c9b209
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

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:049b915d89278c7e62dfb88e387fddb6f622d43063329bc90a879184362b8fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190195125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13169884352097bb5885aaa62fc2c02d073c52861f761de30479cf31bdabf60`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:51:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:51:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:51:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:51:31 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:51:31 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:51:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:51:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:51:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:51:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:51:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2cdc7ec6cbae5bde6dbdf899ec643a7eab42a1599e3bfc8d462207e0566279`  
		Last Modified: Wed, 04 Mar 2026 17:52:07 GMT  
		Size: 92.3 MB (92256315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f6036b41672e8ac4a78410d4ca0a2e9bdc6c23be9c1516935eaa5c0eaf1e36`  
		Last Modified: Wed, 04 Mar 2026 17:52:06 GMT  
		Size: 69.7 MB (69701489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604df859344e0fab7f27a26ce7ee741cce624a16752adb24656c856b1419bea1`  
		Last Modified: Wed, 04 Mar 2026 17:52:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b81b900181a5cb81955dcb5f719e6f6f38c84933538cb0876e7b3ed39f1038`  
		Last Modified: Wed, 04 Mar 2026 17:52:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:467781e40d72f7737f909086beec202badba2e93d58d7d92ff904daeaf3a3fa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b74cb3a9f3d446ecdc66accd3120465d90ace321b6d875407f834dfa48da69e`

```dockerfile
```

-	Layers:
	-	`sha256:d928ee0f2675b9269641d245b8419775f77b941552df44f70a72d54a92d5f200`  
		Last Modified: Wed, 04 Mar 2026 17:52:04 GMT  
		Size: 5.1 MB (5084261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b31fbc59518ecc02f5db8a577dbe443c4a76ff844f9332ceb3a5cf83aacfb7a`  
		Last Modified: Wed, 04 Mar 2026 17:52:04 GMT  
		Size: 16.5 KB (16524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:689f55e455fce47c45c5df6d7da0d0df144ccab41a04fe70ff9b0294216b6c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189093886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a92e5db305d04112d0540dbc3f8652b941f3eba15f5a19edc4bee195676e48`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:51:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:51:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:51:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:51:06 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:51:06 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:51:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:51:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:51:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:51:21 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:51:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b66315d987329206186560af3c01facf726a72ac978a0792b640ff19583d651`  
		Last Modified: Wed, 04 Mar 2026 17:51:42 GMT  
		Size: 91.3 MB (91288289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce956a72c6584cf26a3d8acc8c1c8a8b279e6ad46f355ebe7748fa2d60c49a42`  
		Last Modified: Wed, 04 Mar 2026 17:51:42 GMT  
		Size: 69.7 MB (69688476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cb342144adedeabdd490b4147c37663b5bd119b1e54117e6ce54f23a6e97a2`  
		Last Modified: Wed, 04 Mar 2026 17:51:39 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951e739ad73321f2d63ed6ecc74bff7622d4e7f18ff611031e6d3ad5e00833fe`  
		Last Modified: Wed, 04 Mar 2026 17:51:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9dcb3cee3016c0ecf3de27228c9686cdb711d93a26a7e9311d27234ae65ddfad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5106709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:112c6a51fc1843dd60cf227e1b8857adc78023032916a83efb8eb843d71cdf06`

```dockerfile
```

-	Layers:
	-	`sha256:6f58bc724df283ba002db9a1ac39f2ecf12307b5652e2830b377c66756a05220`  
		Last Modified: Wed, 04 Mar 2026 17:51:39 GMT  
		Size: 5.1 MB (5090043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d6e405e7cb4c3f0d1192bf9320092f7f8c63c86835611473466d3fb1cbcb3a5`  
		Last Modified: Wed, 04 Mar 2026 17:51:39 GMT  
		Size: 16.7 KB (16666 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:09adb8c111f044c2e48c2188fe8da14b6790e8123e641d59bd322ff3b9c0b473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199245375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6deff96b727651c5a6157cd6e838e4911159e6a66d9af3f223a72cfa388243be`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 18:08:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 18:08:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 18:08:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 18:08:47 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 18:08:48 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 18:09:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 18:09:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 18:09:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 18:09:42 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 18:09:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829ad7a07e1ddbf691451995b704ca3268eba628fdedf2f605d70a36a8a03929`  
		Last Modified: Wed, 04 Mar 2026 18:10:20 GMT  
		Size: 91.6 MB (91632879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10c782529e2977fcd02f922208c4c2456bf0bcd8d90d666d48f79de6af56c09`  
		Last Modified: Wed, 04 Mar 2026 18:10:20 GMT  
		Size: 75.5 MB (75533117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c3163d179f4c1a95bb829902cdc1a63b82369cdde22e02f93dc170b646cb43`  
		Last Modified: Wed, 04 Mar 2026 18:10:17 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40060af29dc2d454e9fb0493c3590600e3c2f4d0a810648ac41627ea539d56ef`  
		Last Modified: Wed, 04 Mar 2026 18:10:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0a4ff93e0bed6fa1f556c5258e73eb48f13ba1f8f97afb771c2689a196246cb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5089328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ab8d97f2bde82c2b915283642b05eeb680d637a332c028d48f51f4f20ff30f`

```dockerfile
```

-	Layers:
	-	`sha256:0bb4d10c45fc872a6f47a739e68a502af4606feb6faddc2185b9a47d96f6699b`  
		Last Modified: Wed, 04 Mar 2026 18:10:17 GMT  
		Size: 5.1 MB (5072743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f54a98a99fba67bcb9e4e950dd239c51d109b31ae2900406561877fe176384b`  
		Last Modified: Wed, 04 Mar 2026 18:10:17 GMT  
		Size: 16.6 KB (16585 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:a83227455fe6d4f0b870d9a080e2e91c0b80c4a43b6a5a7d3567d51a93af9890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183639725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2853dfc14917393f9601ae245443f6896d41ecc50c5f4de0f715e49a3bfe18bf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Wed, 04 Mar 2026 17:52:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:52:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:52:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:52:23 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:52:23 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:52:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:52:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:52:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 04 Mar 2026 17:52:37 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 04 Mar 2026 17:52:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65f405a760b9e020d136b3a3a540a5ecb3b3b7867aa1cbe2b6452335effdfa4`  
		Last Modified: Wed, 04 Mar 2026 17:53:05 GMT  
		Size: 88.2 MB (88233824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea12a795be387c0bb64a1cb4eda9d38644321dbcddce2682dc693ac2b82220a1`  
		Last Modified: Wed, 04 Mar 2026 17:53:05 GMT  
		Size: 68.5 MB (68513335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41faf1a20236bd0b7415178aac4225b2fccb3f7864c244561f6bed4f56d5d458`  
		Last Modified: Wed, 04 Mar 2026 17:53:03 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2225d9caa8c8681aab4f2ece20bc46868843f7e5f71d37f1aeffe70cfb614c`  
		Last Modified: Wed, 04 Mar 2026 17:53:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6c771bfbcc49ea3fce66379e25e8e286965db151dec87374d95f012e75ca6536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4287754259acf57bdd42c1a4ae4ecc2fb4fb08f355f9106548fb345f06e0905`

```dockerfile
```

-	Layers:
	-	`sha256:dbe874bacd06ddc2ad0d2f39dac1ac5428f9e90fe20adc0b33afaa64af47e07b`  
		Last Modified: Wed, 04 Mar 2026 17:53:03 GMT  
		Size: 5.1 MB (5060144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4622fc43f6ce3d18d142d05e9cb6b47922192eab3fd6c796b5797a060c67e705`  
		Last Modified: Wed, 04 Mar 2026 17:53:03 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json
