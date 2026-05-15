## `clojure:temurin-11-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:7e2370a73d04f2cb5957a417c5159b2c32d3354fa17853ab911db67814d5234a
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

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:51fef3c089941ad62c2a14fa41dfe314355e3ffaf15a0703d75e8e9c36128f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247713361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:086c49faddb696c40b5218ea287e04d2bdca53bfe16b8ef288b16535c0302cd2`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:14:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:14:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:14:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:14:16 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:14:16 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:14:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:14:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:14:32 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91acd95a14fd0f377b33075bf2c9f2f114b6b881507eb8a1d731c567208a729e`  
		Last Modified: Fri, 15 May 2026 20:14:54 GMT  
		Size: 145.9 MB (145886195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0713807f19c02d6bb8c3274326a49e70ae390fa6808f54ff6ef0e8dd60929fc`  
		Last Modified: Fri, 15 May 2026 20:14:53 GMT  
		Size: 72.0 MB (72046294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7832286e00207b2263a0724b75540190920764f6584eaccd0acca48837b1f3d4`  
		Last Modified: Fri, 15 May 2026 20:14:50 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2ccc48e6c3c0d0a5c8034a448fba2ce7b64c4d6db41236347fe57deeb8bc95de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d51aa9d77d2252b6bd5cbe7b065dcbff7d8d88b500973ff3d0e1e11c283e82`

```dockerfile
```

-	Layers:
	-	`sha256:83066d7c385991202eadbefba9bae49aab74287cd4eef6d70d3924a0a7801503`  
		Last Modified: Fri, 15 May 2026 20:14:50 GMT  
		Size: 5.3 MB (5279369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67283ca46fcceddd9c6c1ba860bb65866a04502346e5bb96b32fb8f2da55a2ce`  
		Last Modified: Fri, 15 May 2026 20:14:50 GMT  
		Size: 14.4 KB (14397 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:93c1a24c08c1f4ed09bede923077c387d9c3395d3c040e0f8a0162df6c6154d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244581412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c366fc4ab54c1091b9dc243f29cfc94e9917134d778b957d87f9b71d66b9646`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:14:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:14:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:14:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:14:15 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:14:15 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:14:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:14:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:14:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c049ebe13875a14d1e4cb2db2bbc21c19d799c192f6ba58d7351fc042d216986`  
		Last Modified: Fri, 15 May 2026 20:14:56 GMT  
		Size: 142.6 MB (142582235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c87a166977cbaeec1c1870aba6b3fe26b76d8e2d7c047125f97ec9d752121f`  
		Last Modified: Fri, 15 May 2026 20:14:54 GMT  
		Size: 71.9 MB (71854887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cfec96b13baa206b9f3e82c3f0e715625888888e9706b4af2293cd8f58d51c7`  
		Last Modified: Fri, 15 May 2026 20:14:51 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4ed1fe7ab4e665546728b21e8fcce98461e2a7cc33c3d1e60a5aec0ed77623f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5300271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3f76982e8900543f608e1a1ac340e6d4d59dc231fc23cb6829354880e6738f`

```dockerfile
```

-	Layers:
	-	`sha256:bde1e633f7eec41e53d91e5912e61dfd2e27f53f1ca41534cd6dd5d87d130eec`  
		Last Modified: Fri, 15 May 2026 20:14:51 GMT  
		Size: 5.3 MB (5285756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c130ca09221c5a78f31b95485f5e45331f3ba3b213e51848be0d829315f28796`  
		Last Modified: Fri, 15 May 2026 20:14:51 GMT  
		Size: 14.5 KB (14515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:a06112d7a790986852fab7534339c7842a2bd7b5b9ad70c14b5ef8c67ac77803
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244164515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757c845ff7eb38f0080fbcc135029bb65c8620fd0322ae74b05679dfb7158678`
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
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:26:45 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:22:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:22:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:22:10 GMT
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
	-	`sha256:6481e726fcbce8985d9ef871fa019cec438ce11ba352b263db3829d5f3de8261`  
		Last Modified: Fri, 15 May 2026 20:22:47 GMT  
		Size: 77.5 MB (77455602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012a4cc5edf76685fdc04bb99ec4ce8701d14f4cb3d53ae9f6b2936ced69257f`  
		Last Modified: Fri, 15 May 2026 20:22:45 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:65a6544a976c7397ba78c8b9d82c674c0696a9f6e0f440648112b219251d17ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5296614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d4418f70ea001a995469459574e7c1bbe4f3c1fceabc3dd19e73de15159329`

```dockerfile
```

-	Layers:
	-	`sha256:77422c8861229e713a1be1b1f4233399e97af309e5d91fc21cecc4ae0476f29f`  
		Last Modified: Fri, 15 May 2026 20:22:45 GMT  
		Size: 5.3 MB (5283125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:699a79bb8faac7f4ebfd8bd589ce41734a8bd1c386b57f317f56b5619428c237`  
		Last Modified: Fri, 15 May 2026 20:22:44 GMT  
		Size: 13.5 KB (13489 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:1a626f44467825c61025401d161f08da865295ceddfd7a8e40287f7cf7e5e599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229507690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48909835d53beb1d45be96d390cc84055d230367455e58201ac35a5ab59c2f59`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:14:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:14:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:14:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:14:47 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:14:47 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:17:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:17:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:17:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301d03359195b2db4e16ef3d853eef1d64ffe78f0949990c433cade4fd354430`  
		Last Modified: Fri, 15 May 2026 20:18:36 GMT  
		Size: 126.7 MB (126651735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbd4bf7e1200a07e20bb9e7daeb32b5aca93c4012904c44850a3ec1c51c5dd4`  
		Last Modified: Fri, 15 May 2026 20:18:34 GMT  
		Size: 73.0 MB (73014962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5efb4a8ebcfc0e455fb88dc2743b8842b269050c2aee3468a4d22d2ebdb9383`  
		Last Modified: Fri, 15 May 2026 20:18:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0cf9e3ee0d17e2172febe5d69867cbfc2a404167cd1d01a403622e8f1bad4874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689d53c210853473ca46fee538b93365d2c925db011566cc5359f73eceb89fff`

```dockerfile
```

-	Layers:
	-	`sha256:92864466c07ffac746f99d647062b7fd53be0bbfeea89780f050238ac96e784a`  
		Last Modified: Fri, 15 May 2026 20:18:30 GMT  
		Size: 5.3 MB (5275297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f741d9ac94049679565bb556c84c7ede90f8624f030658ea9aed19196e1883e`  
		Last Modified: Fri, 15 May 2026 20:18:28 GMT  
		Size: 14.4 KB (14397 bytes)  
		MIME: application/vnd.in-toto+json
