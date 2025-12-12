## `clojure:temurin-11-trixie`

```console
$ docker pull clojure@sha256:df26063d007993f23b9717b98cd357a4ad03d6636f98061af4781059446abbcc
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

### `clojure:temurin-11-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:401aa45e2c0e86a6dc570b876c2a4c8a3862a66e17be97b11bab03f7496ec6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279800289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf8452c7ca2ed48886fefc97a24aa0e535a7e221abc5d9029332f99701eeef1`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 22:38:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:38:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:38:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:38:52 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:38:52 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:39:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:39:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:39:09 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1fc0cea3e40f8496d16067876af26cc46ab35f332070ac8106248a44e28a6f`  
		Last Modified: Fri, 12 Dec 2025 09:31:01 GMT  
		Size: 145.0 MB (144966626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39489f470195925d57dfd2057f7ad7c079f8964a69afa9154e4826e8c4c4172a`  
		Last Modified: Thu, 11 Dec 2025 22:39:48 GMT  
		Size: 85.5 MB (85543496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff7bc0c79dda178b0112e03a36433696c7cc1c064bf3f8f046a861c85a4eec7`  
		Last Modified: Thu, 11 Dec 2025 22:39:37 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a2f1653d9456f8e50bc67dde0593f79da508d085cb88ccc8b0728ef01ebd071f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7501254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23f876c4c0dd92005b90d8ea84f4c0e880ed210950f3109561cdbef9da474127`

```dockerfile
```

-	Layers:
	-	`sha256:60a7af0339640831e131e8a357f2b0badedc3cc38c939154fd49186fc80c40e2`  
		Last Modified: Fri, 12 Dec 2025 01:36:44 GMT  
		Size: 7.5 MB (7487070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1a36021790547f4eb29af5bb0091248da8d5f40fb6096627228668b66c6b2c2`  
		Last Modified: Fri, 12 Dec 2025 01:36:45 GMT  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a5686fd863648a14f15771ac0203fd3bbf7261257f3db0ff14600aa34d9d761b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276743868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece9ea067c0e621b8e663008d690bca257a0ca13c2b4b7d72a0fb120de0d1cdf`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 22:39:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:39:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:39:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:39:09 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:39:09 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:39:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:39:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:39:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dd0e08b54b0f19a14f098c3f5ecf223842810aeeb56bab70f028f087355299`  
		Last Modified: Thu, 11 Dec 2025 22:40:04 GMT  
		Size: 141.7 MB (141731561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b74934c08203defbf7752d22b642d65f2fe810843eef71a1f3a0f6f224b7cfe`  
		Last Modified: Thu, 11 Dec 2025 22:40:07 GMT  
		Size: 85.4 MB (85361440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5b3fa878357b7e2b2be6fa75fd46c96e1185df02b23b5d4ca95efd350b2165`  
		Last Modified: Thu, 11 Dec 2025 22:39:55 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b6ab56f9eb2c38823748772f6e93bc49726eb9a28b1e8301b72e998a2d3e2ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104b5a1edc56d843b83c6703409601d495f0ca143ee5947966b3373ee73d1f2e`

```dockerfile
```

-	Layers:
	-	`sha256:451112621aff4d466f4dcc6a7e9a3b4cb575a219598d0c8bd00e05773053e91a`  
		Last Modified: Fri, 12 Dec 2025 01:36:51 GMT  
		Size: 7.5 MB (7494718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96edc97cb3f87b18ff1b646bfb66d647f99ea35791bb732893fa1840a063680b`  
		Last Modified: Fri, 12 Dec 2025 01:36:52 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:257542df661f4fc1ec595e84f5b8751bed0b1a890255a4684cdacd00286ef3cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.1 MB (276136263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c78b9418026399adfdd6987863772c09ccc097a366d50747ac61678047db267`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:25:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:25:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:25:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:25:25 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Mon, 08 Dec 2025 23:25:26 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:52:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:52:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:52:04 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37d1cc451357decc266df875d9334bbd4504581a335e8cd24c32ce8844bcd57`  
		Last Modified: Mon, 08 Dec 2025 23:26:56 GMT  
		Size: 132.1 MB (132081948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168d6c6f2f67c7ddfb21fbe127a2dd89d1f629c89eeedd8082a23cb46a0581a0`  
		Last Modified: Thu, 11 Dec 2025 22:53:09 GMT  
		Size: 90.9 MB (90945190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d034c0e4809f4bfd8e0d336e77a5b7c24168dd8f871b7a95e7331eb3a0607a33`  
		Last Modified: Thu, 11 Dec 2025 22:53:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6173ffee61976a3f29fda3b6106572da88a203200cc8578d5f154e57d7b03894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7505107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125cacbef7c0db4aac224f1d241c4f0aff42963e740cfbbd00cd05ee16b6135d`

```dockerfile
```

-	Layers:
	-	`sha256:6989470e7d13294ffa44c96010059106a1215edcffd0dde7edde256457cdc7c3`  
		Last Modified: Fri, 12 Dec 2025 01:36:58 GMT  
		Size: 7.5 MB (7490874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a29c7ef641a786f18546ffe042ab0e8ece99ec3d06d4719c957d64bdb541bdf2`  
		Last Modified: Fri, 12 Dec 2025 01:36:59 GMT  
		Size: 14.2 KB (14233 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:020c26f9bbc9905a194c450425d24f267c289c53d208aff08fd39a03d8b04166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261549605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd818a6583ee1467ec4dba5369ab80877bacecec71cdd6803edb1a6cf6d3eb04`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 22:33:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:33:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:33:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:33:03 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:33:03 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:33:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:33:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:33:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3f8967bef2f6a8ec916f7d3a0d528a6724093176621c5758addeeece50e41dec`  
		Last Modified: Mon, 08 Dec 2025 22:16:15 GMT  
		Size: 49.3 MB (49345908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179e7c978a5c9b16756c11984d3e35b7b98189223b21d5ca750af0a4063fa46b`  
		Last Modified: Thu, 11 Dec 2025 22:34:16 GMT  
		Size: 125.7 MB (125694399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c511c3a8a3105cc77312310c5d00e326d87f42a339720990f033cb30e9f5528`  
		Last Modified: Thu, 11 Dec 2025 22:34:09 GMT  
		Size: 86.5 MB (86508652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f527c6070918282c8c00bf54624a552988fdc73fc7c894fb7de39f08a0807c`  
		Last Modified: Thu, 11 Dec 2025 22:33:56 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:15ed2ea22fc3c883a49345e1017f61c912f9c95e57ee9d68b44850ea7ee6d767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7497181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3927f57385a931a4bb58304534d12f30482f1ea8fdfcf0943e0607f06480c3`

```dockerfile
```

-	Layers:
	-	`sha256:de99bdd42a59c43ebaf608499b4aabaa50d4d0fd34c9d25658003d5705c116a6`  
		Last Modified: Fri, 12 Dec 2025 01:37:06 GMT  
		Size: 7.5 MB (7482996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c33eeaca0ee4f2136e1179ab3c7ddd96e089631614a9b63a2f5eeaea3a93563`  
		Last Modified: Fri, 12 Dec 2025 01:37:07 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json
