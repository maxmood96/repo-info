## `clojure:temurin-11-trixie`

```console
$ docker pull clojure@sha256:d345f5336b7792fec320fa3a75408f52af9323584c4fe44aec9962a80ca21f3d
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
$ docker pull clojure@sha256:7f8c2fec73a69f2cafcc2c6bfe41bc6b7540d29a413a98df4263ac4a7bb75d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280470007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d58958be912d7767896f85bb7479b1719bffdf354fbd5aefe47be6316d926c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7317ca72d8b623cdca20b6b0ee6bac7abdbd3cc2b7b0f6b69af48e9a911c1f0`  
		Last Modified: Tue, 26 Aug 2025 22:54:07 GMT  
		Size: 145.7 MB (145658140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6d44ba8cded44eaaa1b21b04bd7694b6bc821b92c203db85b6bfc5fe2a9841`  
		Last Modified: Tue, 26 Aug 2025 22:55:35 GMT  
		Size: 85.5 MB (85532940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a73ee64f7ca66bebf9e12c31527deb1be5c7326653df692dae7a0bda7c2c71`  
		Last Modified: Tue, 26 Aug 2025 22:55:29 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8d397404f6bce1e33e19f8bdc22a2de9893d89de1e81f1ddbfd54310acc970d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7496590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b992f00a095500ff0cf58e77a34feaa31b34a33e23d7f3ea0f8c49fb869d4ee4`

```dockerfile
```

-	Layers:
	-	`sha256:6b2e907ae43839a8a18641bab40de076fe23f0ec1c35c633862f10563fee11ff`  
		Last Modified: Tue, 26 Aug 2025 18:36:32 GMT  
		Size: 7.5 MB (7482362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d3185d5e1badebe8c8c001d31160dca82ca76a1bc8bbdce9e84bafb6d993fc6`  
		Last Modified: Tue, 26 Aug 2025 18:36:33 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dd942728c438a512c4bb989151ea3257acbdc65a033f5d68480d476bed60518f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277459391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c699493732cc2a8ef9bc539d7c7d2f2cef41e5dc95dd86db7f2abbeb1f58c45d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1cc20894541cbd711745752d2223fc23d38752d9fb22d82b12f78632b069aa`  
		Last Modified: Tue, 19 Aug 2025 04:02:21 GMT  
		Size: 142.5 MB (142460532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4630ba644b29313632b773d36ea30d91a0070f635392464eca3abb2fd92dc32e`  
		Last Modified: Tue, 26 Aug 2025 17:39:32 GMT  
		Size: 85.4 MB (85356612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7de4ef35ff3b1725bcc68922bf0bda777b571e3c28ce6491ef0bc1271da3bd3`  
		Last Modified: Tue, 26 Aug 2025 17:39:21 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:975c14989cd81fc86463752f18941ce70b4104c15bba6bd20e9f54323c3255fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7504356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba11663d4a2d97c892fcb5f6e7b6e0ec4ee289e94394bf92bca6553067d66b50`

```dockerfile
```

-	Layers:
	-	`sha256:9a9727a237f1ba3df2e6124953c7bfe1e9157398c1baa2183ba7849771da081e`  
		Last Modified: Tue, 26 Aug 2025 18:36:40 GMT  
		Size: 7.5 MB (7490010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d55605d5d273b96b9c659450b68d63952503e842fa6b9b772708ba74f7f5cf3`  
		Last Modified: Tue, 26 Aug 2025 18:36:41 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:98a3bb6e468c11c503c85ff553c5cab0c056f91a75b63ada3a5589cd89a6b821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.9 MB (276899752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5352fe46e2435452c935662a42f8fe89e76048f5b41fba9a2dd7d95254a31ab8`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
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
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967a97862e5fba4f3e376cb8ef40e6f26a430a3f4696b51f2bc128f1d58140fd`  
		Last Modified: Sun, 24 Aug 2025 07:06:26 GMT  
		Size: 132.9 MB (132853303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417d8069dab23936c2d1d039dff524ded06650dd99322e79ea4fe9ee415fed52`  
		Last Modified: Tue, 26 Aug 2025 17:49:32 GMT  
		Size: 90.9 MB (90942420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36233893fec70f54e69beeed9cd6a3e47c278e5775563d7f0178369576728429`  
		Last Modified: Tue, 26 Aug 2025 17:49:16 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d4bd64b20d9418a770fdc6a3bb70fe437b7efbec7ca86929f15d3a0941511bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7500441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ac2a211973c9e0078a8ee8bad7d685236038e5f0bc2c4ee57cded9c545acf1`

```dockerfile
```

-	Layers:
	-	`sha256:0a052cd7ed7039f1e56953f02180ed5163d890c8b7bebcde2efe39d15127ceda`  
		Last Modified: Tue, 26 Aug 2025 18:36:48 GMT  
		Size: 7.5 MB (7486166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02de2099d0f1c20a3a9cf74c1a28d0da637836f8b210c304cd27c468910fc55b`  
		Last Modified: Tue, 26 Aug 2025 18:36:49 GMT  
		Size: 14.3 KB (14275 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:ae740d8a23d95a2d0e88ba3a173ed4f195e0434d818412e0ea3913a834a37025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261466615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2162108d3b70c5fa5de944ed88b2c258f27bf1b3717946a38d3db28c57790167`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
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
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6ab5525c66f1bbcad56e2757390ec72fcf1952e5dc1a6fb67ffb9b8e6bbbd8`  
		Last Modified: Mon, 18 Aug 2025 17:31:25 GMT  
		Size: 125.6 MB (125622148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8001be109fb287ec9f194048280a4fc0117000f0a5a476321253f64773d5c507`  
		Last Modified: Tue, 26 Aug 2025 17:59:24 GMT  
		Size: 86.5 MB (86498659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df8565e06ea135e14551c082401b48bf4c1bee59abfd4059ab4e4a62468cdb4`  
		Last Modified: Tue, 26 Aug 2025 17:59:15 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f31cfc9a6e8c89018284833f60ed59bdbc7b83457ecedd5a1fa2d5d017776a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12506cdd71091e02ad79bf561c2bc6540c57d3b0fb056539b252ba6652689c0b`

```dockerfile
```

-	Layers:
	-	`sha256:490256f548e208071c2b2b32dc498a892979ac59798a8f6a4ee0ee651dea722b`  
		Last Modified: Tue, 26 Aug 2025 18:36:56 GMT  
		Size: 7.5 MB (7478288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3882a24f8ec575ffe831d06199d89ec1b5f8199d32260c656535ad655ddb6d73`  
		Last Modified: Tue, 26 Aug 2025 18:36:57 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json
