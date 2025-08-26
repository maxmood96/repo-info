## `clojure:temurin-8-trixie-slim`

```console
$ docker pull clojure@sha256:711fd2319e668de5e6000848bf2095784492d9d4810ca893792e4fdd8a848490
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1ffce34f2f7a18faaf66e2d30933c22afa708ac6e2e5f15c81822913850ea4ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156487032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03b17d8dc02a48d89c6f6d535b701f3395c1b73decca8dc182a57745f257325`
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
	-	`sha256:c16a28dc03ae97576a29ced1841d537d098ad1be02f31c6826de510d07fbcd1f`  
		Last Modified: Tue, 26 Aug 2025 17:28:10 GMT  
		Size: 54.7 MB (54731324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7245a7439965e115c4f4dcb7f1b42c69d57dda326232c6eca32ce034ed1553cd`  
		Last Modified: Tue, 26 Aug 2025 17:28:17 GMT  
		Size: 72.0 MB (71981777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a3ed18f1b1212b3412902c838c14d74e8a7aadefe0945ae31776651da44366`  
		Last Modified: Tue, 26 Aug 2025 17:28:00 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:296cf62650d4bbb1c8c0979cda84c5296fe745bf51de20d81ee0a2a612b5a38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:671d73cf8906193da7cc85887669a2ce70de083125fecbdadd49b85e7200987e`

```dockerfile
```

-	Layers:
	-	`sha256:1fb2e7221010d431d88d4cbd930264cbf47b26aa9cb6405c3f9cf80b5e0417b9`  
		Last Modified: Tue, 26 Aug 2025 18:45:07 GMT  
		Size: 5.4 MB (5376847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de786c33b4813a038b648751398fcf8a8fa98e7c5a5fd53ac7a1fbece585e283`  
		Last Modified: Tue, 26 Aug 2025 18:45:09 GMT  
		Size: 14.3 KB (14270 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie-slim` - linux; arm64 variant v8

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

### `clojure:temurin-8-trixie-slim` - unknown; unknown

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

### `clojure:temurin-8-trixie-slim` - linux; ppc64le

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

### `clojure:temurin-8-trixie-slim` - unknown; unknown

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
