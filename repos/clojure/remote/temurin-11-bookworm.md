## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:dd2aca37e6fe186201d38f6fb97cb00a26687b0f5b03430872dc7451274749e5
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

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5bb6e138f9fdcee283d0cf7d0c195b91c485c015902bb3f865750c68d04a00f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272513783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5411e9798f32f4c30e21c43d938fa32d3b268b8838555c73328db242a03a0e5`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:17:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:17:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:17:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:17:50 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:17:50 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:18:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:18:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:18:04 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b396a3a8bb80c31d302a982d60da99f3845628af4ce5f8ba76237b45094e9dd`  
		Last Modified: Thu, 11 Jun 2026 01:18:28 GMT  
		Size: 145.9 MB (145886263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a965a08f2041ba5d398c38b5b96954448426a9641bf62d3edba32c89e88f150`  
		Last Modified: Thu, 11 Jun 2026 01:18:27 GMT  
		Size: 78.1 MB (78124835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9151e42636efb33e63e1aa411c71859ca08715ee03ba7badd9f654250f2a0ab1`  
		Last Modified: Thu, 11 Jun 2026 01:18:23 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c4a184b3633865ca5ef28ca407388b08ebc6c6321c1e9c5b6d135c7a47f6d949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7410013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28150ddbc215b874180aa00107e39e0016584c6b5e771cde2e9c50ca9dd9460f`

```dockerfile
```

-	Layers:
	-	`sha256:46ecde778ef678a00ee76ff7869769076f967ab37e0c65cb4458dcba7f1e41a2`  
		Last Modified: Thu, 11 Jun 2026 01:18:24 GMT  
		Size: 7.4 MB (7395650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8500dcada1ffe2e9fed6526c75162ae01f738e7ef99e03aa0580fe16e3743a4`  
		Last Modified: Thu, 11 Jun 2026 01:18:23 GMT  
		Size: 14.4 KB (14363 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:38e3a1fb6e00d6cbeb46db6bf04055ecfb6b10b6739eccc5491015391018b458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269101060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97af82132ad98398e297e5dc3acf4845cd68a07ff7e038568e8b0981913b612`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:21:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:21:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:21:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:21:31 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:21:31 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:21:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:21:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:21:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b4bb1a1d7a17c510854f2bea7756f49dc7c4325e5ebbfebb2175867ed49356`  
		Last Modified: Thu, 11 Jun 2026 01:22:10 GMT  
		Size: 142.6 MB (142582228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c15214ea34f7469f5175d27b72c6c0cb1e7f00bc81f225e47815eb77abf5bf8`  
		Last Modified: Thu, 11 Jun 2026 01:22:08 GMT  
		Size: 78.1 MB (78129172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfcbc028f11605c32ce3ea8162cddbf668a59c5d18c04df1a5cc527af052b480`  
		Last Modified: Thu, 11 Jun 2026 01:22:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6219178e79f42450848c6ea032060804869ed7f446fcd44b247b187b2665214b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97bdc463188173595be921ab2f72ed8698ba5dc1f4f14929cb62cb87f2b0d507`

```dockerfile
```

-	Layers:
	-	`sha256:60c5cad069c7d92c7ccead7948936696479855ce58f422a82987c9a618841e01`  
		Last Modified: Thu, 11 Jun 2026 01:22:05 GMT  
		Size: 7.4 MB (7402031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dc17659735d883a41ced32a134373882581e7ad069538e94cf85228dba4a788`  
		Last Modified: Thu, 11 Jun 2026 01:22:05 GMT  
		Size: 14.5 KB (14481 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:3f2230e1937b96659c9e191700002bb37f0164dc483954d99a6f9438eede6aef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269410312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f4af26956b93eedf2aa3de46fe8dc40b92ba903d87eb5a33cdb574d157dfdc`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:47:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:47:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:47:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:47:10 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:47:11 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:47:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:47:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:47:44 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd9dc5a9f698e91b12b1467b7637f73943248991b66286c4adb373e93e4a55a`  
		Last Modified: Thu, 04 Jun 2026 17:48:31 GMT  
		Size: 133.1 MB (133110195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67baff48f2fb740cb9b58c99889751fc6fb36f7716775b3afd54893c0d419994`  
		Last Modified: Thu, 04 Jun 2026 17:48:30 GMT  
		Size: 84.0 MB (83959274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97170153d151b39c93a714ee8ac9104e995669928f855f9e4da4e7d710d8a35d`  
		Last Modified: Thu, 04 Jun 2026 17:48:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:515ccd69540234c6832d73ad86ddb2ce1f0acc50e8901a9a1228d55ca3a2660c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7414642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebbee4fa0b4468c7831e614c8ff450813bf840299f4a3de105430235df311aa8`

```dockerfile
```

-	Layers:
	-	`sha256:0ab7327b989a39c4761bf3351f22731d4f54ff08f820cc8f345f3bd83ef7d5f1`  
		Last Modified: Thu, 04 Jun 2026 17:48:27 GMT  
		Size: 7.4 MB (7400233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:246aa680ba4407b809257fabff7c68ba2735378b29a887cff164b1dfd637fab7`  
		Last Modified: Thu, 04 Jun 2026 17:48:26 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:390b74eaa7479671e7d4fdbb44ea6e25fdf8f20694c320859d0f896e518be990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.7 MB (250743148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a5aef015b2d45ea436383a162b0a1926a6a1090e1c76907a93d1144b20594c`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 03:06:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:06:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:06:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:06:24 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 03:06:24 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:07:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 03:07:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 03:07:50 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04e0036eb3da965180e0f61eff76ae583a3a15ee0f71473a89a49560bbc21f0`  
		Last Modified: Thu, 11 Jun 2026 03:07:07 GMT  
		Size: 126.7 MB (126651735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1bd9439e108bf057c69052169a130a1d31cbb2dbe6a9507546d1c97a2c1629`  
		Last Modified: Thu, 11 Jun 2026 03:08:19 GMT  
		Size: 76.9 MB (76929268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd70c5e2cad0e77c2db1f00ac09360e764bc7c2de5cc5162ad984f40025f108`  
		Last Modified: Thu, 11 Jun 2026 03:08:16 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:07789710ee108f34edc8b3fbe9ba29e55f8f5465dc56e44e8efe89f0d209e30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:908f18731ce5674b64d3b6210f2600d5fcd16e789b9f74f27abc08120f54cac0`

```dockerfile
```

-	Layers:
	-	`sha256:378ba0b832674e960262eed396711f75f7a4d4607c66865028c091ed867c6e4d`  
		Last Modified: Thu, 11 Jun 2026 03:08:17 GMT  
		Size: 7.4 MB (7386973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66e4d0efd20c33f51ad912a803a23f194df1424bab665c60e0aea58b7d3d887d`  
		Last Modified: Thu, 11 Jun 2026 03:08:16 GMT  
		Size: 14.4 KB (14363 bytes)  
		MIME: application/vnd.in-toto+json
