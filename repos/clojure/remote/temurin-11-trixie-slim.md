## `clojure:temurin-11-trixie-slim`

```console
$ docker pull clojure@sha256:766187690c0f79a11bf179fa49d64393ce594de307e3015ba3d2763d7e3d8095
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
$ docker pull clojure@sha256:28ced3a4cbb0dc6fd7f004156780c2769374bbe351f4542e7c5b86a0edd99bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247713674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17abf40ea5f140f0e306d7a4036c0eb6a546a54dd0ce259c2c563ffeb6528000`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:34:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:34:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:34:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:34:39 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:34:39 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:34:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:34:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:34:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed2b80ea9067fbacab73a448857782b22ea513a328d858b90b854b0f5f4866c`  
		Last Modified: Thu, 14 May 2026 23:35:18 GMT  
		Size: 145.9 MB (145886201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3cdb4c9219d2770f27a8ff98e4e8276d12202597cd094c7fc0d79d110c5b0ca`  
		Last Modified: Thu, 14 May 2026 23:35:16 GMT  
		Size: 72.0 MB (72046602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee029bdb223b56d3bbe3d377c09efde46861f5e7bd64546636c12f97c81c7102`  
		Last Modified: Thu, 14 May 2026 23:35:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:736de32fb12715542df8b6602e8e0e0c920143317f75d916eb21f91c1d15ca65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8431858885733417ebd9a3ef3c07405723a06bffa352b75e65d6daee133c2e5`

```dockerfile
```

-	Layers:
	-	`sha256:768eb727372703cdb9f468115593c8b3ea78d0582a96d50ecc61d57057e3e01d`  
		Last Modified: Thu, 14 May 2026 23:35:13 GMT  
		Size: 5.3 MB (5279369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2af5b3a802f72af2560ef85339d474e86aef27f8f19696d63a3907a4862e6af`  
		Last Modified: Thu, 14 May 2026 23:35:13 GMT  
		Size: 14.4 KB (14396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4dd1ca84a9bb78092efa300283ceb2265cf2537d0a611ece5d4755b9ed8e1425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244581143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b8541f10b68c39439037c7ca756d4342252911626e8a8b15c0c11c863d4735`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:34:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:34:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:34:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:34:23 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:34:23 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:34:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:34:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:34:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100a67fc750014eddbe61ccc32fd9b672434b569d0af63d4385a52b056fbb792`  
		Last Modified: Thu, 14 May 2026 23:35:02 GMT  
		Size: 142.6 MB (142582235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23768031b3873a68218ce7e80b72c830e41f557b5dd65a4921ff6497057e74ac`  
		Last Modified: Thu, 14 May 2026 23:35:00 GMT  
		Size: 71.9 MB (71854618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e49a6a71b9a880d0ab5a15370a586853e0adb9a398d36970c55fed534782f1`  
		Last Modified: Thu, 14 May 2026 23:34:58 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b51fb21a22aff363ad808382c0bd2cced3066370452ba9726fa69f8cc4fe2f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5300271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1650e14673e530f2cde1477d9a53c4a914b129f5ce7434e40507678aa024f978`

```dockerfile
```

-	Layers:
	-	`sha256:1d2ff2dea6d933a21eb48fb01fe33649b8ce02ff628be4ff6ea3a1ab0d4bbc1a`  
		Last Modified: Thu, 14 May 2026 23:34:58 GMT  
		Size: 5.3 MB (5285756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74e0c2a5d5e1f8929c706a97f37b7e1bdf0b4bfe639252a22b22103b401d5a75`  
		Last Modified: Thu, 14 May 2026 23:34:58 GMT  
		Size: 14.5 KB (14515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f61834a4f2874d5320728ca57711d1a7568fc61c3d59d45d299d0abbfe13a7ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244165957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f18ecd4714fdd4e8ddae60e32609f389f68eb7a3a7c0ad8ff53f05627c7e6795`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:26:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:26:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:26:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:26:45 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Sat, 09 May 2026 02:26:45 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:41:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:41:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:41:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96ee5b4d347c9b3ee6f86dcde18c044f7ee128c0ca544845fafbcc3bad0c1c3`  
		Last Modified: Sat, 09 May 2026 02:27:49 GMT  
		Size: 133.1 MB (133110179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150d56f05235b350ea61b8b9bd8ba304aaaada068ec74d6f884c0dbc9ce5b884`  
		Last Modified: Thu, 14 May 2026 23:42:30 GMT  
		Size: 77.5 MB (77457044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba42fdb7f7f7974b0816aea2a5c476842e02964a54dd637bf43a4b37abf89f09`  
		Last Modified: Thu, 14 May 2026 23:42:27 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d2b0cb49e65eb83e9e13adefd9893fb7491c8ef47ea2cae25582063ee16c8c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5296615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ce032e4bb83d20e4a60780c3cb95677cbecf31fcd360043838d6e057f07bd6`

```dockerfile
```

-	Layers:
	-	`sha256:a0077e2056287f5fc6e4eab418684b8d7945b02e39b8f30870cfabc895f48996`  
		Last Modified: Thu, 14 May 2026 23:42:28 GMT  
		Size: 5.3 MB (5283125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15f0e23b6b733f66a00dd3cf97f2910f9166d254e7951c5c0cd3b3092dbf294a`  
		Last Modified: Thu, 14 May 2026 23:42:27 GMT  
		Size: 13.5 KB (13490 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:004b263187fa6e94371f1a4f1d2ce51cb10adc8749fd0b3463d21f1d5bb4d229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229507249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8012883a0cfb5ec7d281cbf247467f12e7332fb17feef27caf49e81881e9c8`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:33:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:33:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:33:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:33:36 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:33:36 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:33:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:33:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:33:56 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb586f00a76cf072ca95451b1e1aaf6006bd5b8a79963eb003d4a8449ec900d2`  
		Last Modified: Thu, 14 May 2026 23:34:24 GMT  
		Size: 126.7 MB (126651716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:329c1a8d8325966637ba7689cea82beca90783387413f00dfc9319d396499ccb`  
		Last Modified: Thu, 14 May 2026 23:34:23 GMT  
		Size: 73.0 MB (73014542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d25c33738f0b82d0702924460b571d056dcabbbc1a593e145b1488486076df4`  
		Last Modified: Thu, 14 May 2026 23:34:20 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aa1bff5ae82dc095a5b610737e6c281c1811f2c56f486ca21421528996aab2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5be0fcc345d65e05ffdfc855eff7e45e6e9dae9a5361073b7112e1b306596f`

```dockerfile
```

-	Layers:
	-	`sha256:87b3658f33df32c4ad1d61d43658a1e08cde7fbbee9851057157b3008e5caae6`  
		Last Modified: Thu, 14 May 2026 23:34:21 GMT  
		Size: 5.3 MB (5275297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:748eb7264c1cb57dfd2a2de003727647836fb650b6f4c8630712eab7e28fcec6`  
		Last Modified: Thu, 14 May 2026 23:34:21 GMT  
		Size: 14.4 KB (14397 bytes)  
		MIME: application/vnd.in-toto+json
