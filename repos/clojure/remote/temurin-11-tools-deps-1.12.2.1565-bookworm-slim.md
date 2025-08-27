## `clojure:temurin-11-tools-deps-1.12.2.1565-bookworm-slim`

```console
$ docker pull clojure@sha256:742b11c3bb026c309545818225d679dd0cbfce9b8703a48192f7534836478c46
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

### `clojure:temurin-11-tools-deps-1.12.2.1565-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cfe424c349dd4a346bc466c50142d1a78866acb8cc491e0ce3c470279bbce6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243565181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93deae1ca8b786b7ccf231a5d20eee892f498606351fd7586190a5b7cc377cd9`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897b92815931530ca35c9bf91cb0c1367bec17fc8ec9c0acc55660838ef295d6`  
		Last Modified: Tue, 26 Aug 2025 22:59:55 GMT  
		Size: 145.7 MB (145658140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30adfd049455032efd093f314cd50ff6b5f3744c894b6eaa1154ffe7416a35f2`  
		Last Modified: Tue, 26 Aug 2025 17:28:02 GMT  
		Size: 69.7 MB (69676140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97aa0d322d775042861f3167caae70bc8f241696311009e140c7c74e9552154`  
		Last Modified: Tue, 26 Aug 2025 17:27:53 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bf97dee813d6da568685e7d51a098e85b4ecfd3cb06337330fae548e94dda8c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5145723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5337572fbdc6e6b83b82da97c420d2e0e1c0f7f75e50958610b3114315517074`

```dockerfile
```

-	Layers:
	-	`sha256:156c0563f11b8e98f1633f2f5358641f055171bf8f33851eb8113083f68a0ae9`  
		Last Modified: Tue, 26 Aug 2025 18:35:11 GMT  
		Size: 5.1 MB (5131414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba84c1e7669a541705ced58409c6fbf8b2b9bf35a2067ffd8387c7b6eeecbed8`  
		Last Modified: Tue, 26 Aug 2025 18:35:12 GMT  
		Size: 14.3 KB (14309 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1565-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4e93f7e6388971e7c3aeb51dc1a6cca5e07a56a8ea734106092cb975cb18915e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240092605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:027f9af29d6bc4aa189bc725e2a179c92e29cf8f409ba875a49aab06067fd683`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f170599e0d0d7ce8452567f601dd39705883bb1c67f4c2b875ddcbef1651e1c`  
		Last Modified: Tue, 19 Aug 2025 04:12:46 GMT  
		Size: 142.5 MB (142460571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875928e609ba7ea865f1ac22346508571fc68d3ecc6bd0894187e0019b880a65`  
		Last Modified: Tue, 26 Aug 2025 17:36:04 GMT  
		Size: 69.5 MB (69549387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b01cd6da0da37e45dab5ffb36d7d87cf793b09d0aa947218efbc27110ba4bc`  
		Last Modified: Tue, 26 Aug 2025 17:35:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cc9da806c8df6da92a4019a5363c63e7970da6676951e9fe8e7504f658d4f0b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:582ed83bfd9a1d28bffe348e9a04bf528d4ffb2ff0b9798fc898875d9c8cc0b8`

```dockerfile
```

-	Layers:
	-	`sha256:ef84be1a5947880015b93902205d8d40313f3a185839591576ec675e17265922`  
		Last Modified: Tue, 26 Aug 2025 18:35:20 GMT  
		Size: 5.1 MB (5137793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cc709fc3496f5d6c2dc5fc116a48590c7e5f34422a4db998b83b09dfaa59afa`  
		Last Modified: Tue, 26 Aug 2025 18:35:21 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1565-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:dd40fd6126f9d39720b57589a36160d3d902715b0142ea5bf62d7298a62f1caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.4 MB (240431243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ddf8eaab629bdf496c9ad563fe3e20df69b8ee0a015e9c4ec2a63f5f8d130f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46561d416a7c35ce0f5f369f09b10c84d52b854df0532c3ee5a10948491d390b`  
		Last Modified: Sun, 24 Aug 2025 07:12:04 GMT  
		Size: 132.9 MB (132853303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd7f7f274926ad57780e6c458611cc3530c51d1bb349efe6e1123b0561850d1`  
		Last Modified: Wed, 27 Aug 2025 00:21:07 GMT  
		Size: 75.5 MB (75503872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057d01bed82329b99fe9c9c623bc92c0e24fd516fb4d00c7d9e8370e802e3a55`  
		Last Modified: Tue, 26 Aug 2025 18:30:23 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:457f0a0484883c9be76fbb04ee1ee9b7beecb0fd6eaf8b2faed7c09e122301a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c87564dd333ebf296e473665be56dd610b93aaa527c805a7b1f77b1ec626b6`

```dockerfile
```

-	Layers:
	-	`sha256:17b70f7cf498ff20ca656ece3c5ae40f6d0b0ea9a0df2d641fa17571f2d8e647`  
		Last Modified: Tue, 26 Aug 2025 18:35:26 GMT  
		Size: 5.1 MB (5135957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66b36a02321cbfe89fcc0399ae5c13175f438098a06e46855c7ebac5c5feb499`  
		Last Modified: Tue, 26 Aug 2025 18:35:27 GMT  
		Size: 14.4 KB (14358 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1565-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:588dae454d8bd171bc57ec62582df65eef26802f82796812db6847ab113d1de0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (220994945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a18aded2990e2d8b3ce71845c246bc1d630da72d00be6f0bd8ac0f241db981`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae251331425e0189671e4f2efc07cc0c01261608ee3bdd189f86daaf400b4734`  
		Last Modified: Sun, 24 Aug 2025 07:12:26 GMT  
		Size: 125.6 MB (125622148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4201ab1ceab4d1e40fff044f80e02aff1f6701e399012173babfacdd260e954a`  
		Last Modified: Tue, 26 Aug 2025 17:47:23 GMT  
		Size: 68.5 MB (68484316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aecb0987c44f11240baa9ee07492adef0c6162b2b16aa8cecf9447a5da4633bc`  
		Last Modified: Tue, 26 Aug 2025 17:47:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ee823e8ba9ac39d2233a92397dba443f14445640a0b84abf55dd326b2c50f7ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12edc50082821444c9c383d8de0701c782fc8a22e8fb47010f52e8bdf9368e74`

```dockerfile
```

-	Layers:
	-	`sha256:990e9620d24082d407efd34e1c29057fef3d9a5379d2199da77aa52eb7e16534`  
		Last Modified: Tue, 26 Aug 2025 18:35:31 GMT  
		Size: 5.1 MB (5122739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5f38224873c3117f6a88ca281584047385a9a9922f2eab2f9fdd564954f8042`  
		Last Modified: Tue, 26 Aug 2025 18:35:32 GMT  
		Size: 14.3 KB (14309 bytes)  
		MIME: application/vnd.in-toto+json
