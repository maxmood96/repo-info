## `clojure:temurin-8-tools-deps-1.12.2.1565-trixie-slim`

```console
$ docker pull clojure@sha256:2d95c8f1ca0f041e63cab29fdb1ca1fc2c2e2d59e4e6d4bde17f59ce192c9290
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.2.1565-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:be7dbafdc6a07447384158032b8cd2b4c4ba952da123ff9cfc1caaf7717b1473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156487985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b67e96a4ce5326dcf29225591e8c3c8b0237bcba23771eeeba423149aca61c`
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
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a4e0713c1c0b870472979bde305efa29d921decfab2c962b1c3f46d1562023`  
		Last Modified: Tue, 02 Sep 2025 00:16:57 GMT  
		Size: 54.7 MB (54731323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7869ab945edd40d0dcd3d3fbae535592077b5b9fe1879c317a2a5402f12a4ed`  
		Last Modified: Tue, 02 Sep 2025 00:16:59 GMT  
		Size: 72.0 MB (71982730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d66b4dcdd47fd024afddbab028db780116171c23e69bf24870e12f2976340e`  
		Last Modified: Tue, 02 Sep 2025 01:00:28 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d079af20fa629a79ba94d4346879529821b4c968ec33cecb5cc80e5b70307196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97cea394aae6069311f046f11e5aa2d791e091c99c059c1dbb7fd2f7e51669e`

```dockerfile
```

-	Layers:
	-	`sha256:c6d82d7d4faf96e88f26bc362e19c3bc02b2dcf1edaa373a75a98c3701f2bd49`  
		Last Modified: Tue, 02 Sep 2025 03:46:47 GMT  
		Size: 5.4 MB (5376847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dbf5ca6b7933188285fc3aa47cbe57e75030f951534a8886e6afb4eae602649`  
		Last Modified: Tue, 02 Sep 2025 03:46:48 GMT  
		Size: 14.3 KB (14271 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.2.1565-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3ea0603af9d8a7e34ebb4d4a7dbd3396c18e05f37fe759978bf1371d07c5b344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.8 MB (155776045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c4209d9274881c0849ded5e1586e69781198e995eae34a4034bc65c5e68b20`
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
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e947fda8da40bbdedae94665dc12b0f76d05c15bdcfed7d7c7a25a08a34d4e`  
		Last Modified: Mon, 18 Aug 2025 16:59:02 GMT  
		Size: 53.8 MB (53835656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad1b01d57d77cde395f1bdf1b60b7acc199bc086d73df480c62a0705032b069`  
		Last Modified: Tue, 26 Aug 2025 17:34:25 GMT  
		Size: 71.8 MB (71803700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55aeae1836835d284b93ab84b37a064ef011432f5d2a898d3cc6cad0cd0c630`  
		Last Modified: Tue, 26 Aug 2025 17:34:15 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e98aa856b1ddafc07954de88e96ce079e4578972d837f26ead72d30a1d2b0e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f796cd1fc9fb6db877cb9f00b4cb7c538de0ffdf18b26baa116ad76460f7681`

```dockerfile
```

-	Layers:
	-	`sha256:5a70be552235093f2abb55067f2eaa4188ad949d94021423f249adfbcb2ce515`  
		Last Modified: Tue, 26 Aug 2025 18:45:15 GMT  
		Size: 5.4 MB (5383314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6c4a167ead406d74deddecbdcd3d8c8039de4b670fe0eb92a15a43d401acb39`  
		Last Modified: Tue, 26 Aug 2025 18:45:16 GMT  
		Size: 14.4 KB (14389 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.2.1565-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:08256f5ab5e994dbd9c5e674931bc6fab659c4b36710e2b9849828f24e263672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163148946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b38e8ff705c9ec0aac295f9405f411bf8375284ccdc67a867013b30cb22a7ff`
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
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800d9364a2f77d9c82408af7eefafc8a1f6c3cba74df0771e743034519bdd812`  
		Last Modified: Tue, 19 Aug 2025 18:05:57 GMT  
		Size: 52.2 MB (52165401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba67350a0f5a1203a21b9e42a998ba13186b6e9fe5f675937e6707f7ed49ca40`  
		Last Modified: Tue, 26 Aug 2025 17:39:55 GMT  
		Size: 77.4 MB (77388687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de2b5e7254d9834b155e634938f32c4a7e58851ef92af4b59b7f64b3bc28ee2`  
		Last Modified: Tue, 26 Aug 2025 17:39:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e645e607e972e83897fcd07cd8855c8cf243a0bccdad3474838b5b4bdc698418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ee3ddcf06d97ebef3c3e398bc1bd07821d01f83da1d4682510f70204ba0f7c`

```dockerfile
```

-	Layers:
	-	`sha256:2db5fe0f7b327a2b47d474df2782702bd973073c3d2e8d43db7c59c8733aa140`  
		Last Modified: Tue, 26 Aug 2025 18:45:23 GMT  
		Size: 5.4 MB (5381811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2359dcb5384d7471e18b1a390e64f5d2d45e182950fec189b397f2624c919e5`  
		Last Modified: Tue, 26 Aug 2025 18:45:24 GMT  
		Size: 14.3 KB (14319 bytes)  
		MIME: application/vnd.in-toto+json
