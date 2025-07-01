## `clojure:temurin-11-trixie`

```console
$ docker pull clojure@sha256:ae349b4c5b7069ead1bd70d972263092a2b98850520d9efc1242d67e29757c04
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
$ docker pull clojure@sha256:6dee209b54ea27fe5b221b3cca3aed3db384abd42df3cb263d6dc1fcbcacdac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.3 MB (280255520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcdc0a58284ce5d292f5e14d2958af35b8bd85da8960022ede2762e15cbe2445`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b72fed6e2775feec9291a4bd4b416f996dfc503eda11eaa00def55711302b4ce`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 49.3 MB (49263877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae0382d47e92076eaf2f80f142f5e38db25d5965da921b9362f9dd94291ad5c`  
		Last Modified: Tue, 01 Jul 2025 02:39:13 GMT  
		Size: 145.6 MB (145635655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e012934285451f1e3a12d07e5a44db9081b3636626b6148be7ff4e90eb03935e`  
		Last Modified: Tue, 01 Jul 2025 02:39:27 GMT  
		Size: 85.4 MB (85355344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e45053ae1b4b73ed563fb5381f632f2d96aff4ad4299f9fb71876f41ebb48f3`  
		Last Modified: Tue, 01 Jul 2025 02:39:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5c0e8ec15290decb1056d93514e00412343bd3c658086956a6cb77e035371559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b9d8353e7794e39b59d06834a4f44e3a323363d1ce53f733cd846de091faa4`

```dockerfile
```

-	Layers:
	-	`sha256:a05815a427b0b744f5ad84db0c1da20b30add994e1c9f95d3edaf50e8103b163`  
		Last Modified: Tue, 01 Jul 2025 06:36:30 GMT  
		Size: 7.5 MB (7479294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be34645fecd5344dbb8009c6fc385e3a0509fd4d6ffac65367e8050fdfca6525`  
		Last Modified: Tue, 01 Jul 2025 06:36:30 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:980df3795b0606605841b14b8c99e1868af409140c313078af8825fbf3b21142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.2 MB (277239175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2bed20d16f4e53f95ff36b3bff08f31f2bc5e1aabda8264005ee4f53803647`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:546a427a0109bbde3a869c6a4ff1ed90ec74768e7fd82dd00441608d83416632`  
		Last Modified: Tue, 10 Jun 2025 22:52:49 GMT  
		Size: 49.6 MB (49621528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d780a3a01a9b1dea561cdbd6b3757dc17dc751380a900c5d002fde515f87636a`  
		Last Modified: Sat, 14 Jun 2025 09:10:31 GMT  
		Size: 142.4 MB (142420640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ea44cec7b0de0184833dae722c0cfd35fc21fdde0b1256cb45e59984a4485c`  
		Last Modified: Sat, 14 Jun 2025 09:10:28 GMT  
		Size: 85.2 MB (85196362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df23f82ce32a4db6347b9eb25a3d22d1965bbdbec4e07f7cb9a20889d27e092`  
		Last Modified: Fri, 13 Jun 2025 00:53:44 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ad5484085b1aafaf2f6d6d427e893107181c94301f41c92adc0bf0c16c316335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7501284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac72a510ce2109ca1be9d1d67b8c322d42affd177af6827c4525e68f1b6daea0`

```dockerfile
```

-	Layers:
	-	`sha256:f7df23b2268603593c65f68aaa7162b67ec18b86fadeb219064ea807a2ef0e2d`  
		Last Modified: Wed, 11 Jun 2025 09:36:51 GMT  
		Size: 7.5 MB (7486938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:628da8d79d826bd00ddf3df144a29d32fe5162d05115a1b9d29f81a511d2b1ce`  
		Last Modified: Wed, 11 Jun 2025 09:36:52 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:232f7dd77618ac5c732f188419caa731c3d296be07f80ba88a6c32baf0752b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276677689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c7e947e242fe54dc4ebc6ff7fad06abda417e9f64b070374f64da89812a0db`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5c6a246a80c20351fe842a314b6b3f8561a5ceaea736decf36fe380b29e53224`  
		Last Modified: Tue, 01 Jul 2025 01:18:57 GMT  
		Size: 53.1 MB (53097236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85a969def2863a9e85601ef2d4f2e86efa8ff38674c223fec6a8890f4ca131a`  
		Last Modified: Tue, 01 Jul 2025 08:32:36 GMT  
		Size: 132.8 MB (132810557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845abc443984b91ec28ba019dd19c9f8abec41b136ce13c23464c3a610aed834`  
		Last Modified: Tue, 01 Jul 2025 08:39:01 GMT  
		Size: 90.8 MB (90769251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e606c630e86e2c648c6171c1d9054ecb63b619e3c167d1ce8dedd2123fd4f3`  
		Last Modified: Tue, 01 Jul 2025 08:38:54 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f7e0b2cba4b2239f5de93649d8f912214a807f8561fcd6a348bd5e6ec019974f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7497372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac794b57eeb18fb861ca8862fdb0edc348dcaf6af777546dcea1972c539f847`

```dockerfile
```

-	Layers:
	-	`sha256:69ba6164b99717a2992bcb82af4afda8fdb945904e1c206c9a260bb490e46f94`  
		Last Modified: Tue, 01 Jul 2025 09:36:45 GMT  
		Size: 7.5 MB (7483096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2988fbe22981cf6d006827246d039f4146ffe6d58658fc549947a75a498c5623`  
		Last Modified: Tue, 01 Jul 2025 09:36:46 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:700d0c84855c04d767e1621213c8769b0467cb5c3b4214caed3ac1f606401630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261264439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29207b0c3d33cda50ea0f45aa0b6ffb29c5dfb98d3dd2ae4a9723fa117e1abbe`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:48de1d8f52c0a2a00375babc11bf69628b8225862d3b6ebbb2205e4ae2f3e96a`  
		Last Modified: Tue, 01 Jul 2025 01:19:00 GMT  
		Size: 49.3 MB (49343660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51563ad6f8cf46e75e2593bfc2fa766379abde52fc9f681453ba8ac4cdcd264`  
		Last Modified: Tue, 01 Jul 2025 08:04:07 GMT  
		Size: 125.6 MB (125585349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31201692663d65b7986960faef5b758a85601b5ab6f89720a25e7b0ed0b6f42`  
		Last Modified: Tue, 01 Jul 2025 08:08:01 GMT  
		Size: 86.3 MB (86334787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de67d94ccccb180fbd8e7151cb742d20ab7092b8c5dbda3111d2f9e2fbfc78fe`  
		Last Modified: Tue, 01 Jul 2025 08:07:54 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:cd8df4d5b2ba0c473562b528619a1ca1d902d0083d0e4fe85aad478a4cbd2e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ce33a56bc401ca5bd7029fc06ca79c8d1d0fb0894fd009a1d81128a5bf45f1`

```dockerfile
```

-	Layers:
	-	`sha256:b2974525a1886550b4b117f50d8995de1ed76e5586972a44e03109b9ca4535f6`  
		Last Modified: Tue, 01 Jul 2025 09:36:51 GMT  
		Size: 7.5 MB (7475220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c433d3e7cf8ed9f68ea1d403e65971a2a6b49b418adedf425b2d7ced3c3b57f`  
		Last Modified: Tue, 01 Jul 2025 09:36:52 GMT  
		Size: 14.2 KB (14227 bytes)  
		MIME: application/vnd.in-toto+json
