## `clojure:temurin-11-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:5dcac67837defe428b6e9e2c993b3e31650b47498508b7b80ebc7719348d7d86
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
$ docker pull clojure@sha256:a43a97402513799701812e533faf965dba824140cbc95f15fbb875e4faf6ad18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247414794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1779269778204d45174f94141021bfacf69d42bed0d8b9f446b0d33b41fb9653`
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
	-	`sha256:f42043324336a4cd74b981eb601b25044ba266a9641951f2496c19516721ee86`  
		Last Modified: Tue, 02 Sep 2025 00:17:37 GMT  
		Size: 145.7 MB (145658226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa96266bf3921366ddfd59cd9f8be844acf059295be2c3148f0a61e5cede938`  
		Last Modified: Tue, 02 Sep 2025 01:54:10 GMT  
		Size: 72.0 MB (71982636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b6b4c1d9a64f3d22ba9e02d6d9452c2b015152717877d93fe8c21c9fe35948`  
		Last Modified: Tue, 02 Sep 2025 01:54:02 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e59ceb363e4c74f9f9545e6853c373dc74d2cbcc49e57c334042582897184d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fca4db188be459a53ed867920c34ed943cdac98b313c8c675b3abaa472de2b`

```dockerfile
```

-	Layers:
	-	`sha256:aeddd19b66d32329663ad03d24f1d1f9b79dc72b8f940ee125066a826a90a9dd`  
		Last Modified: Tue, 02 Sep 2025 03:37:35 GMT  
		Size: 5.3 MB (5275378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d183769baf4edb996fe0b00bb4bcdefeb9cb51edfb4a6b66987b0df0758b0ac9`  
		Last Modified: Tue, 02 Sep 2025 03:37:36 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a6ecc5a239fdfd4f977bc8fa7820042e07a225490a0cac03fc745bc0f54ad7cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.4 MB (244399536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5be3b6e8ccaaa4e90547399fa4fc385a66051b030e6473a0649c925ef4c453b3`
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
	-	`sha256:7d1062bf6ae195b1716538f53ad0adec231767cfbc3f6533c7972f614be66d60`  
		Last Modified: Tue, 02 Sep 2025 07:50:40 GMT  
		Size: 142.5 MB (142459067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d6e23fb9d5fc35a8878d9b31275ebb5065583c83d7b0cc706c28b00f15093b`  
		Last Modified: Tue, 02 Sep 2025 07:56:33 GMT  
		Size: 71.8 MB (71803779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686d7b2c3be63a1dd0d4d7ddfe672898182373ed479e4d1204f1cd5156756db8`  
		Last Modified: Tue, 02 Sep 2025 07:56:21 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c7baf960fa3e09a40f4f502bfe9e46f0f1f46ed20ba0994d81f85df90db52e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5296168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:499b222027c0ebefee369e266a7c3d63c31e71d9fa1a98b7d2b5278a0c14ae74`

```dockerfile
```

-	Layers:
	-	`sha256:cc38bfcc18db6c8828b9379d6a258a937c712cb95927b0f3c55d9f7f6fdba7d4`  
		Last Modified: Tue, 02 Sep 2025 09:37:30 GMT  
		Size: 5.3 MB (5281765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:181ae3f08adf7f63bc22988168a8d0c962f7d999837f067a01dd5ddbafa3b067`  
		Last Modified: Tue, 02 Sep 2025 09:37:31 GMT  
		Size: 14.4 KB (14403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:96f4faae709e3c1107bd949a2756f37a24aec9a84aa65385d6a2ecca752a5f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243837320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa034d93ee668256941e361409694bccc6b7adef4b81f1355f0d8b3090b0fd44`
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
	-	`sha256:2adee34b5367d1099f54497f4aa263aef11888acef04df6d42006db6cf1a4bc4`  
		Last Modified: Tue, 02 Sep 2025 08:19:02 GMT  
		Size: 132.9 MB (132853137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c6cae3057979106144cc348a8bdf1f3616c6cbaa0e38e5edcdf0d33e6ff58d`  
		Last Modified: Tue, 02 Sep 2025 08:29:21 GMT  
		Size: 77.4 MB (77389324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a835b7cc286b17ba64a90cf67f814651ec5438435b46a5ea976224ef7e2e1007`  
		Last Modified: Tue, 02 Sep 2025 08:29:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1c4d0b180cd6deff2a343ce6220a8dec1c75b194ef90c68a2e0ebab0f9b1b3bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ab43cfc3449ea7e004849468d2e29ecaa4613266ff1a35ef1790eb6f5d93b6`

```dockerfile
```

-	Layers:
	-	`sha256:bfee6e90a8410278424f52cbcc92bcbe36be22935cedeed6c1630bf89a595279`  
		Last Modified: Tue, 02 Sep 2025 09:37:36 GMT  
		Size: 5.3 MB (5279134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a985cbe048ba80e41f5b883ddc2004d31b4de7fe9b5d57330e0b978167f039`  
		Last Modified: Tue, 02 Sep 2025 09:37:37 GMT  
		Size: 14.3 KB (14334 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:7ed72d1f69e38dec8fc98678e664b269bc7e0512fb7eb527126e17d7887581f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228405584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c58858a392bea69e13c5169a351633a4b5d7597abbe7b79eb86828cbf17bc2a`
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
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d60f4f708fd5a97ca5b2bec02379236d1ba8e24d3cf4658ab3e32d0e0c22bd2`  
		Last Modified: Tue, 02 Sep 2025 01:49:59 GMT  
		Size: 125.6 MB (125622179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10650f1b6c260b6e0f2da8ef46d0895d7e03379a8c3ac2de4862c89a2133a5a0`  
		Last Modified: Tue, 02 Sep 2025 01:55:52 GMT  
		Size: 72.9 MB (72949702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03aab98a27cfb3333ced61564c49746165ac305da55eda28b263afdd0fe506a3`  
		Last Modified: Tue, 02 Sep 2025 01:55:45 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:af37ee9c8e8f79e4dfa747419111690d56548bce0b768b57f9821ab2c7f1ea23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5285592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06b81d5b04141ea9c5b9146a0ce18a57f815dd07f23a49746e6f5f9f60ae1da`

```dockerfile
```

-	Layers:
	-	`sha256:38121554690ab305d4a1d16e2c48d13402355886a93377091903483ce753a7af`  
		Last Modified: Tue, 02 Sep 2025 03:37:49 GMT  
		Size: 5.3 MB (5271306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72353a18618cd7914b175ac28242d423ea7f89fc6fcaa06368ec1663977f5167`  
		Last Modified: Tue, 02 Sep 2025 03:37:50 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json
