## `clojure:temurin-11-tools-deps-1.12.4.1612-trixie`

```console
$ docker pull clojure@sha256:7736ff9dcba9f3db2b65784027dd7b6ab4d6d9524e9737a6b2f3b449ad582f9c
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

### `clojure:temurin-11-tools-deps-1.12.4.1612-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:23650da62962151c40e050d07d3e70de805c1b91438474f4d82271faad537973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280667273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a671d8d87882253e64ad88c1136ec79e59d66ec02580802dbe6949b941dbe6d4`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:49:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:49:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:49:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:49:39 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:49:39 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:49:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:49:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:49:57 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4cd9d879903cfdcceff807266baf7a41fff8b85a15c1f11dba4ff612f3940c`  
		Last Modified: Wed, 04 Mar 2026 17:50:20 GMT  
		Size: 145.8 MB (145806756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418ca658d76f67ee032e69cee2d9f2ea397ca4fdf55fb13c743e026acb00d180`  
		Last Modified: Wed, 04 Mar 2026 17:50:18 GMT  
		Size: 85.6 MB (85566747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4ba6cedd7a7ce291b5c24c480bf58e2fa8cf7be56324cee52b3356d46ced24`  
		Last Modified: Wed, 04 Mar 2026 17:50:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1612-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3e62abd4de8b8862e4261e53b6a77db31a5bbc7de0566f7c4e7702c8cf1dd104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7504919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6719c08c728ba7e570d6b1d6ef868d050bb784b8aee4146122fccce7b07d0ef`

```dockerfile
```

-	Layers:
	-	`sha256:7d64a9360af9ac7b93a4c02f29e440eb3e9c94c54d44c404604827851520cc74`  
		Last Modified: Wed, 04 Mar 2026 17:50:16 GMT  
		Size: 7.5 MB (7490734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfdf8af9f2cc0ef8c5c05d7b01382696fa60c536a58306e83ec77207ce650066`  
		Last Modified: Wed, 04 Mar 2026 17:50:15 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1612-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:486be1578db293f41470ea7fe11f76113afd07ae0e1d281cb078e0786b495164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277536895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c877456491555b4a1e099bf1472aebeb3f6c9bdbb3b96bdf7bc25da604412c02`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:49:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:49:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:49:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:49:02 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:49:02 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:49:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:49:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:49:21 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5833a70c7db3d1ccf063f8e1c018ccecba27f8eb929337464df3b38302184534`  
		Last Modified: Wed, 04 Mar 2026 17:49:44 GMT  
		Size: 142.5 MB (142501445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb6e288c3d579b2c340968f8ef2782f0ba87ae84fabe99a8f8d0303c696cd82`  
		Last Modified: Wed, 04 Mar 2026 17:49:42 GMT  
		Size: 85.4 MB (85382637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3acdbaccca40c9be5565d9e93c8f0c8b9b2ac5f69e71a34787126f78e14b84`  
		Last Modified: Wed, 04 Mar 2026 17:49:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1612-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ccde8063e434cc77f3a2e53c9c05747db42a5c9feabe245ff2a7826ca40b5031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7512685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f343788d5266ce2e6de92b2be175a11159732c45a906ec6929cde73c211b8750`

```dockerfile
```

-	Layers:
	-	`sha256:18c4b0597cd035dce978a8e7d82364329cbb82ee0c6471cb3e6d1c73c3be18bf`  
		Last Modified: Wed, 04 Mar 2026 17:49:40 GMT  
		Size: 7.5 MB (7498382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5da163403e458c93f4fc0dbcd58bdae8f2fc8d342a2737f5571f59b11f7f4f95`  
		Last Modified: Wed, 04 Mar 2026 17:49:39 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1612-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:331946ef788fbd81b7f6cc6440bb24a5c37e90b772ac444c20f76417901fd597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.1 MB (277087199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c86c3938f0864e5514dc12d6b4759931680325c3dd3ec4262a4f8e8a55e43682`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:55:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:55:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:55:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:55:05 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:55:05 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:56:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:56:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:56:02 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77aed0506e2670e465a8b7ec8eb1a96aca867c6fcdb4b9d9cbc737c3a774b24e`  
		Last Modified: Wed, 04 Mar 2026 17:56:49 GMT  
		Size: 133.0 MB (132997811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066f521fc0acb0fe03ddbf2e0599d0159f4b222deded703c4254da7c194695b8`  
		Last Modified: Wed, 04 Mar 2026 17:56:48 GMT  
		Size: 91.0 MB (90976480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea6c56194fdda9ec7aced3864b9752d5c69b2fb8b7f4a6a344d121214683355`  
		Last Modified: Wed, 04 Mar 2026 17:56:44 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1612-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ddba06864cdd34613d8478ab63190eee838183e8810d408ebba04bfd5bef7f6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7508773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9044a78604efa3f8257a219d1239f8c4bf7c84c62c480ff1c32a623cfc573f1`

```dockerfile
```

-	Layers:
	-	`sha256:0f8a6f44c7c0a25eb382fe9b772deedb6b2f386b387cc7b8eda9680145d31aae`  
		Last Modified: Wed, 04 Mar 2026 17:56:44 GMT  
		Size: 7.5 MB (7494540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:122a5397ce348f401f2ae489a27a1225a71ca0dec9e09af65529850ca141f572`  
		Last Modified: Wed, 04 Mar 2026 17:56:44 GMT  
		Size: 14.2 KB (14233 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1612-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:428c55d6f9b8028899e151f98b178a71c84143733b2c88b81fbb69cd2d7b43be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262446996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:003c372a3b74677af11f173fc2e018bf0d1f0b1ff323028cd30c053c17534206`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 17:48:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:48:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:48:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:48:02 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:48:02 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:48:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:48:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:48:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ab4f589fb47308397f08eb8455b01d1c1f047ace5cc45b8d36a65c3bcd404d`  
		Last Modified: Wed, 04 Mar 2026 17:48:53 GMT  
		Size: 126.6 MB (126561997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987de3156fa1eaab712dd2c33fd4cb353a4b8b7af745fa32a8eb2bdad91ae77d`  
		Last Modified: Wed, 04 Mar 2026 17:48:53 GMT  
		Size: 86.5 MB (86529823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8690e3c756f168879719b77d8f2f544038a6cb62f08b2a525a0d3a3d9faea3`  
		Last Modified: Wed, 04 Mar 2026 17:48:50 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1612-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ad7c580db1f469788268ab632a0512c8b2cd2a578814188cfa5bd28acc26fa26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7500845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885aa0dc5814f6d42abb70377f211f20a30f2ca8c2fdadf50c6a52c82f0007ca`

```dockerfile
```

-	Layers:
	-	`sha256:eba1374fc8e71c65e664ab101417d01319e3f5666cd63b1ee587bf3e951349ef`  
		Last Modified: Wed, 04 Mar 2026 17:48:51 GMT  
		Size: 7.5 MB (7486660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a9345f91bad2d7634d7473428d86487818b0db2bd948d9d3455e1a5590a6e57`  
		Last Modified: Wed, 04 Mar 2026 17:48:50 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json
