## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:58e5844537867ca0c62bf5e98375fa3db158cecf8c0c24640f54b407fb5d05db
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

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:0b10f255493b28a033eebcd87f3befc1e35a7fb879f5fdafe03ae4abbc5582c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275285179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51be4d9939d7aa4ca3f63dfbeae2e0c247310ececa5ca9ec6a62b9c8b30dc25f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:04:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:04:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:04:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:04:02 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:04:02 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:04:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:04:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:04:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:04:17 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:04:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743be0e1a74c449b8e6dd7c5721bd5585aaee7bc4aa161f78729828ce86c2217`  
		Last Modified: Wed, 15 Apr 2026 22:04:39 GMT  
		Size: 145.6 MB (145628750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592a139358ff8881c217684c9b4b4476e9735e686be4b534652720d79aa4197e`  
		Last Modified: Wed, 15 Apr 2026 22:04:41 GMT  
		Size: 81.2 MB (81166564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6fa0ea72920f4ac89cc5a8aac3a9b115fb28d4048ce8b06f74046335416dfe`  
		Last Modified: Wed, 15 Apr 2026 22:04:37 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd6026ec4063da3dae96f4428310945d52b18a686af0928041edb1cf468c9f4`  
		Last Modified: Wed, 15 Apr 2026 22:04:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:317c8e3273ebd88404faca6148975e0ec7dc2d4b7669cf07c815f451c8a460e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7394080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4110e9691cd337912627f05fd33fd6ad3f7a392c383439eb4c9630d8565ee2e`

```dockerfile
```

-	Layers:
	-	`sha256:4145863a91f2fc69834d6f718032d4a41e8b3ec9785fa23fa175f27eaa926af0`  
		Last Modified: Wed, 15 Apr 2026 22:04:37 GMT  
		Size: 7.4 MB (7378302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2319b2436c6ee8612541fd4f1d1ac466d02762b907a0e41491a698f0263eeea`  
		Last Modified: Wed, 15 Apr 2026 22:04:36 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b9229a013d78f3b34b5684c882439ada194d8637d1ccff5f552d8ed0ad72df03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (273969003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a56abbcfba60562ba4039857eb03b235a459b2cc474059a1ed6abd4abd9e163e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:25:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:25:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:25:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:25:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:25:44 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:25:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:25:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:25:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:25:59 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:25:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a5640f6d669bd0b44f1458a8caac2a42f65ba877ec921985b35ea3014b6f49`  
		Last Modified: Tue, 07 Apr 2026 03:26:21 GMT  
		Size: 144.4 MB (144436224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772bccb823acc039efb828b9ed24d2474323c72b1d7bfc7b0f4b7e612c67212b`  
		Last Modified: Tue, 07 Apr 2026 03:26:22 GMT  
		Size: 81.2 MB (81158474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714a31aa0f893068c76366e8048e57212ebf4ac4c3199d71956ca1472043a3aa`  
		Last Modified: Tue, 07 Apr 2026 03:26:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f655425a74c45ce6e042136be130a23fa4bb0e17fbd248bc0e8986ea35441c1c`  
		Last Modified: Tue, 07 Apr 2026 03:26:19 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:737f54f834f31ccaf63d9137da5dd37ac913412f6e168e53ac03fe3522ef8a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7399961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d25cf4c302a61714ef220bf1a8cc7f022c136f4ff9bdff69eaf243b80cf2219b`

```dockerfile
```

-	Layers:
	-	`sha256:93ee0cf18dea5efc3e1fa63e8ce3d3dbafbc348d818f0d1234c33bfbd7a05330`  
		Last Modified: Tue, 07 Apr 2026 03:26:19 GMT  
		Size: 7.4 MB (7384065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e355f44d0f3f160d5d76caee76be1c9d1081e342bbcbed5e038674188b222b73`  
		Last Modified: Tue, 07 Apr 2026 03:26:19 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:a003ad1479b3ba06052c11d7b1b4fc1dd0b296ed990f0831e8418b12b341c3d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284776421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aaf931bdca0a09d0d01dc957d6696d4308c6c2c5edb58f28fef97d0a50bd409`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 14:37:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:37:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:37:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:37:01 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 14:37:03 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:41:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 14:42:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 14:42:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 14:42:00 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 14:42:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358c872239542a9bb50f47b623d9a261564b534e153d9618343a4775810c5781`  
		Last Modified: Tue, 07 Apr 2026 14:38:26 GMT  
		Size: 145.4 MB (145438242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b947218617262b743e622947a9c6ab4d3d112d1d66300451c3aed6e0a13050eb`  
		Last Modified: Tue, 07 Apr 2026 14:42:42 GMT  
		Size: 87.0 MB (87000201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b97ddfd983e8ca63b5ed5184e00c626cd9446d4c223ea33d6599b428e9a28bc`  
		Last Modified: Tue, 07 Apr 2026 14:42:39 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72481cc7226444c83f411f00f60be5917e2b4cdf315a1c1fe2c15d4c9e4cd696`  
		Last Modified: Tue, 07 Apr 2026 14:42:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0d1e20d605ba32364b49c66460b0abcd11344d8472585d1f9990eb4b5007b499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7399344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a6d4260f093a587d415e234a79ada95348d36f1c4d78303c91a98ade59f200`

```dockerfile
```

-	Layers:
	-	`sha256:565ec1ea619f983171c4386ff7dc47f7086c15d8b87fec9f322a7581b8404adb`  
		Last Modified: Tue, 07 Apr 2026 14:42:40 GMT  
		Size: 7.4 MB (7383518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9efe4489f05e21df8426e6aea8ecef38a66d2f705ec3f95538b20e19bed4db72`  
		Last Modified: Tue, 07 Apr 2026 14:42:39 GMT  
		Size: 15.8 KB (15826 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:e2a710701f1b6955f34cb6ff4536fa55c22c922dd6826008133c33d47e469032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262764440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96191873ea5d50f1e1e07439e913dfda1b87c236fc22da56c816ec8a0b868b89`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 05:42:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:42:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:42:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:42:49 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:42:49 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:43:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 05:43:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:43:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:43:03 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:43:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30386c1a9a679281d9dbcfe1187ba3ef51a1f5825055d1c84b6336c179be5344`  
		Last Modified: Tue, 07 Apr 2026 05:43:34 GMT  
		Size: 135.6 MB (135626801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7281f00443a9c179f688356ffd078e1d9a310e3e67ff5ff3388ddab19f423266`  
		Last Modified: Tue, 07 Apr 2026 05:43:33 GMT  
		Size: 80.0 MB (79988515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dca601ff6c924639bbf4cff951b047327fef4fcc498cf38cdc6a668cb4145dd`  
		Last Modified: Tue, 07 Apr 2026 05:43:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cca82ee843d5953f936b9bc446200b275a6ac33d433fd1313d9dd1aca0a47b`  
		Last Modified: Tue, 07 Apr 2026 05:43:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:09f3eaa0ecf3dd257c1d5eb5f158204be8a8ca4a279e3db210d8b22fd5be7421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7385398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3050d8763d81288715bb7ccbe0f87c8bd1a84bd1700f965dff20281e1e5c732`

```dockerfile
```

-	Layers:
	-	`sha256:2faf2eca202154050a3103a693bf97ae86c7f1a9ac922ed75c21f663e4e272ed`  
		Last Modified: Tue, 07 Apr 2026 05:43:31 GMT  
		Size: 7.4 MB (7369621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac0dd3456d381910f3e6a2cdcdc715dd9f79337fbd1724d20dd1d7b5928b8440`  
		Last Modified: Tue, 07 Apr 2026 05:43:31 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json
