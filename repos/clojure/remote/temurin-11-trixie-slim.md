## `clojure:temurin-11-trixie-slim`

```console
$ docker pull clojure@sha256:312e2584e3c7b6328cc3e213bf9e31c7501e705669cbed692da0acf1c00ebe57
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

### `clojure:temurin-11-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:71c6749692b55800c9e0f56dadefb3081bb93a968eb9a70c7258664499479745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 MB (247595383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a6fa399d09154414cc17eb39ce2474ab0f3c1441b7b3089606fad6279551673`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:14:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:14:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:14:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:14:02 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:14:02 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:14:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:14:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:14:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a142a4bbb6b4687cd315539a65c06ffc64c59873996e68636b36d28afe89349`  
		Last Modified: Tue, 07 Apr 2026 03:14:39 GMT  
		Size: 145.8 MB (145806914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580c4fef6742fd902f33a08b27c24a968ef22184a0e888e5e357560be600df9a`  
		Last Modified: Tue, 07 Apr 2026 03:14:38 GMT  
		Size: 72.0 MB (72012183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a9d8eb680c94540d2666726892a9d2ffbb7f86af9784dcfad14db9ced91d61`  
		Last Modified: Tue, 07 Apr 2026 03:14:35 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:693c1f673a005926bb7dd331e93ecce16db0e0229d0e46b62f1851086a58ad81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa984e9ddde46578ba05d55f5a37a0e33c107b1604551f2f918415ed2e3eabd`

```dockerfile
```

-	Layers:
	-	`sha256:edf1211a1ebc26ec1a89584fca176f7a86fbc1889911a870730ab1ad22fa5479`  
		Last Modified: Tue, 07 Apr 2026 03:14:35 GMT  
		Size: 5.3 MB (5279279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99312fa6883e236c28488b634f6251dd83f9edc1c7bc293fd301b0e9aa285a14`  
		Last Modified: Tue, 07 Apr 2026 03:14:34 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:77418b964f2c3a9807cd25803a2c39f48d808ddba994ddf85e2af4ccac5a2a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244470986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a63de7852638c2b0a8d81bae8e0e679a93be4d87fa092fb21928c711539d39`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:24:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:24:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:24:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:24:12 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:24:12 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:25:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:25:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:25:14 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329bec000b8c51d641ad70625e6709b178a1f342640b122744f30dc2de641fda`  
		Last Modified: Tue, 07 Apr 2026 03:24:49 GMT  
		Size: 142.5 MB (142500070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0916d1eaa5d7f03412a723c0122d78dad7c3bb6aa8064fd66fb6f385fda2d3c4`  
		Last Modified: Tue, 07 Apr 2026 03:25:31 GMT  
		Size: 71.8 MB (71831719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9868b4226bd186817e2533231479fecd2d00f2d09ed92b106533d262fe0b5760`  
		Last Modified: Tue, 07 Apr 2026 03:25:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2b43dbe9362ba7818984a5b0ac482c5881bf2b17cb7cab3dee2a2057c4638273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5300027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa21f6e8ded323640541a1e0afa31c7ca49569be4178bad211d231b6d3a303fd`

```dockerfile
```

-	Layers:
	-	`sha256:cd8473fe7ef88b11260c3d5827c99665073f07346d52a2c0f251dbad96dec78c`  
		Last Modified: Tue, 07 Apr 2026 03:25:29 GMT  
		Size: 5.3 MB (5285666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d284e454a5096d8d1b79317f19d4c221af4a339175acf580abac698880ab0dab`  
		Last Modified: Tue, 07 Apr 2026 03:25:29 GMT  
		Size: 14.4 KB (14361 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:32281b7c02956fa335e30a40026ca1afea9449d62538aa08d990a4c7b6e639db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (244019330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb8e966432f4acac977a142dcad4f4ef0efaebfe003b6a212eeacecfd7cb154`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 18:18:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:18:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:18:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:18:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:18:17 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:23:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:23:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:23:49 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6d8bc187d9d77c2b576c45cef2edbe313dca76b0d35a49ca751f0587487fda`  
		Last Modified: Tue, 17 Mar 2026 18:19:41 GMT  
		Size: 133.0 MB (132996714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53b836d66d91e22b570ee107eea8357b31cd2c26e0469e1f67f84350aa4f2da`  
		Last Modified: Tue, 17 Mar 2026 18:24:25 GMT  
		Size: 77.4 MB (77429143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ff01b39ee4c05cd706d2f9bf0d4a1dbbae99b7defee725941e89d3f87c0a84`  
		Last Modified: Tue, 17 Mar 2026 18:24:23 GMT  
		Size: 607.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0db2a626d04fa56858774dcecc2047251dbb0bf3a319cc49c3e47a6be847254a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9334f39c04b16986ab17dfbc57da78bd0d62da139b5c702c20f1cfd7db5eb65d`

```dockerfile
```

-	Layers:
	-	`sha256:39d905225768cc265235581bea62f63e27a380ecfcdc3ade7eba98f930ec7291`  
		Last Modified: Tue, 17 Mar 2026 18:24:23 GMT  
		Size: 5.3 MB (5283035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c77308363b15cb7466b2a19bdb01aeb028f7174152743c643edbce642fb80329`  
		Last Modified: Tue, 17 Mar 2026 18:24:23 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:934ad825c9862e5bfc9bf2c9ae7b397de871ddd429bb362547841b2834cbfd2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229385369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a8901136fa55f5b7dc4fca7111128daf48f1a4132f3d56a4139c00ce871417`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:41:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:41:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:41:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:41:14 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:41:14 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:41:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 05:41:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:41:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3bd3257f5995d825c3c93d6c134675d2a96ca8e8bc241408714637624b064b`  
		Last Modified: Tue, 07 Apr 2026 05:42:00 GMT  
		Size: 126.6 MB (126562194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7784992323bc39557d6fdc023185e05f8bf46d81784d747e6c573971ed86ad`  
		Last Modified: Tue, 07 Apr 2026 05:41:59 GMT  
		Size: 73.0 MB (72987113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6df84d8535f86c910d5dcbb4568390a4dfb11295f495e197d1c2d941557a579`  
		Last Modified: Tue, 07 Apr 2026 05:41:57 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e61da64dbe8c5e8dbd93a0a5451dedbfb19e26137c68094e882e60ac8d09bbfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ed5d6e3fac87e0e9a1f9849ea1be93a6bcca0574ad0c60355058c8fff3b10ca`

```dockerfile
```

-	Layers:
	-	`sha256:a0619a7855b5053c5ed9355864981de5486da3245652799c7492a4ed69e41c17`  
		Last Modified: Tue, 07 Apr 2026 05:41:57 GMT  
		Size: 5.3 MB (5275207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:136df1a679d87b6de25cc3dcad46493e123e77c5a185ad67ff28a24bdcf8662b`  
		Last Modified: Tue, 07 Apr 2026 05:41:57 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json
