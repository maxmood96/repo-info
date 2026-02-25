## `clojure:temurin-11-tools-deps-1.12.4.1602-trixie`

```console
$ docker pull clojure@sha256:2e90487131e8e2b4807ba2a0a69fa235a3030eb0023b3dce2eebda1322082dba
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

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:87a7204b521893dfceaecad3244d8401ad4ee8265909733adef781a060da7ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280640534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761891f32cc70cace142e29980a141dded818d0f831dccee3e2fc1d059c98f41`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:54:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:54:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:54:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:54:27 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:54:27 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:54:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:54:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:54:45 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf008242c67674e4b5f31f9239f06401c7bf0e3a604f4adb3bc3b61cf6e93f6`  
		Last Modified: Tue, 24 Feb 2026 19:55:09 GMT  
		Size: 145.8 MB (145806755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a30c463f6db66e92dcb7b342c7b3c8e871a7141313940f9738b087270f89cc`  
		Last Modified: Tue, 24 Feb 2026 19:55:07 GMT  
		Size: 85.5 MB (85540012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc5fc932c6e6f59bd6a9985d3e5c7fbb4a369ccdb0b13a1abd0d8f211d4d5fc`  
		Last Modified: Tue, 24 Feb 2026 19:55:04 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0ed8eda7b4c809ea17a9ef4630fd0b1f2923b5f57a268ccebbbc390c99350308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7503406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfbe997f5ec2a993f26e4999ce7a359ecb711d73c591af554e3445c8b04b10b6`

```dockerfile
```

-	Layers:
	-	`sha256:bcbd34ec3039ebf324ec8cbc2e5273fdd6e0a2b82c247354e34c2f9e6523e41f`  
		Last Modified: Tue, 24 Feb 2026 19:55:05 GMT  
		Size: 7.5 MB (7489221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7545d70d5965d3930d4519d45f107d2d65023c1178c5ed5f126848b1902c203`  
		Last Modified: Tue, 24 Feb 2026 19:55:04 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d3afb0574dbeba0c6156202556a22a8fbcf4e3ee710dab87a8f1a8a22866414e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277519100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ee704cb4f4252cd9b4ab069a945a578e0faed11bc74faeeb6b78c4e719742f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:05:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:05:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:05:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:05:01 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:05:01 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:05:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:05:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:05:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51837a702ca51bacf6a9c26ccd8663fe8ab5764d31f01529649aad1104baed6d`  
		Last Modified: Tue, 24 Feb 2026 20:05:44 GMT  
		Size: 142.5 MB (142501443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab6d49d50a3eff93bfa6c033b7f0bdcd2c00d37e31d3e648f62bad3e6377452`  
		Last Modified: Tue, 24 Feb 2026 20:05:43 GMT  
		Size: 85.4 MB (85364847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b985bf43a004938f27b09ffc01c8eec6fe06f592f4e620dd31568f2b7fc76b`  
		Last Modified: Tue, 24 Feb 2026 20:05:39 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:79983c861546e074ff552af699de92dd7b2e06bb0f2244b4f7e7294ab38145ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7511172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37cfc07443f44b1e8034cdb182e088214dc3dda6f6552aef44ae8c7a70e991f3`

```dockerfile
```

-	Layers:
	-	`sha256:e5e596634d735c2666b642365edb048e8fbd91ae1a5f2a57c4ff4ae5c61f79f4`  
		Last Modified: Tue, 24 Feb 2026 20:05:39 GMT  
		Size: 7.5 MB (7496869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:556776dd7e8da2d8f23b74896fa70e659d52cba0165cf29d25565472ad856de2`  
		Last Modified: Tue, 24 Feb 2026 20:05:39 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:48364fc64ebc0da1d467ed59ca3391580df4c0116011543e34a20f3a567d66ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.1 MB (277067713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec1478350dc0fdccfbd6e82004d8bc3aabcf9327d292f01354b11e6ec9da3e8`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 01:50:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:50:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:50:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:50:51 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 25 Feb 2026 01:50:52 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 01:56:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 25 Feb 2026 01:56:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 25 Feb 2026 01:56:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd587e6f98d18981b1fa39b879e07792b8b34045978a1c4c5b8a1982d2ae24e7`  
		Last Modified: Wed, 25 Feb 2026 01:52:39 GMT  
		Size: 133.0 MB (132997811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115487e94d9bbe32fb3c1cfd1ba882d9353298863c015d157393a696587ddcf0`  
		Last Modified: Wed, 25 Feb 2026 01:57:14 GMT  
		Size: 91.0 MB (90956995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589e183488fb3fe9de0c05ebe2d1f965298a02aee8921d950da74d88c15af61f`  
		Last Modified: Wed, 25 Feb 2026 01:57:12 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1d120f8fd14f9805dec6c1a3e7837490b3a400e8b2aa424b07fe3a5e15444f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7507260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e489411b594969af11328be27f0b36453237d0ffa4e3b4f21d1c9d3a620b5a`

```dockerfile
```

-	Layers:
	-	`sha256:b28a8d0fb74973e40af7f50fdeff55c7c1bb85fa59bba77d45b937f5c39d2e24`  
		Last Modified: Wed, 25 Feb 2026 01:57:12 GMT  
		Size: 7.5 MB (7493027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1faea0b11e82751a47c1c01044afcbcd69e90b7836fbad594d93150ca6cb376a`  
		Last Modified: Wed, 25 Feb 2026 01:57:12 GMT  
		Size: 14.2 KB (14233 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:49d443ec26facb0a9d99d75b6d35d42760dac169615bdea92090135d2084360b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262431702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff75fc1a64ed388d320ed8aa6ec2538a9be05939c1d39cb0be2552c2ee3270a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 23:12:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:12:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:12:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:12:58 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 23:12:58 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:15:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 23:15:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 23:15:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf3ca8078f9a8ff06106e2ddc819bac030792db65741aa1c31b6c84c638804f`  
		Last Modified: Tue, 24 Feb 2026 23:14:35 GMT  
		Size: 126.6 MB (126562017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe536551e240c35eaf6a9e969d8e2bca1157a538e657324bb33d60fb7a509d7e`  
		Last Modified: Tue, 24 Feb 2026 23:16:28 GMT  
		Size: 86.5 MB (86514506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6255a8a4bab27f42c382ff1d69b17b23aa32c525edd671a17a70f1e94478c7`  
		Last Modified: Tue, 24 Feb 2026 23:16:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b91799184ddf71592d3cd6945e8288907c7ef946bb10915694589c24b3fcc1e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7499331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7024010da6fb453f8038477f871a190f8d82203278f3c9937eebc4c6f32ce5f2`

```dockerfile
```

-	Layers:
	-	`sha256:38f0ef4c331c6ce100c3dee4db59ffa0f637f1c51b0f9a435539e92cdfc69223`  
		Last Modified: Tue, 24 Feb 2026 23:16:27 GMT  
		Size: 7.5 MB (7485147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:016a1d64ca6b4f1d96237fe71e6d07dbdb37268f708b93e938e173ca33c86ff0`  
		Last Modified: Tue, 24 Feb 2026 23:16:27 GMT  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json
