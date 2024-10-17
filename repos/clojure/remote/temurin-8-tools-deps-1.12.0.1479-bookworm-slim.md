## `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:e40a21a4aaec1232dc3be271552da512e5dfade692d5a3d9d0458fd8ca1252b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b8b2fb3cfac9d0b486340a768d677b94dd9210fb87f317f049a4001274f4fea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.2 MB (202221507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c19d84bf251ee2433631e4517ef126f4ebabe4f29a31cd0ba6fcb9114566a8`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a380c3c662d99deac90f73af70785c9242b3172868afc11414740d486160566`  
		Last Modified: Thu, 17 Oct 2024 01:13:50 GMT  
		Size: 103.6 MB (103611909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e3d74097a497a64a283c2dc43c0d1463bbdf2b411ecf96afc82799aa07200b`  
		Last Modified: Thu, 17 Oct 2024 01:13:50 GMT  
		Size: 69.5 MB (69482663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e166eabfd05adb141f8835118c7bc77f81e00b5890741d4315121c77d139e51`  
		Last Modified: Thu, 17 Oct 2024 01:13:49 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:89c460fea9c6b5c6c208778b77ec78171d55acdcab47a055b2ff7776a9866c82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5030975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e080329518784f9479204e25060aa5ab87173cfa24b0938ce65f1538445f8cad`

```dockerfile
```

-	Layers:
	-	`sha256:1ef0604805de0feeadae54ca52d275be085704880dabdaa575afc4e9c5333b8c`  
		Last Modified: Thu, 17 Oct 2024 01:13:49 GMT  
		Size: 5.0 MB (5017017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a64bda1f745ebcb601dc85a3fef9f939239f287c0d9a33955b0a48c2a6533632`  
		Last Modified: Thu, 17 Oct 2024 01:13:49 GMT  
		Size: 14.0 KB (13958 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ea6ac39d21aed385cf06895d149d827f06836a32c2491781fe5025efe507bae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201231454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf858d1771a32e7f33499b30f283bf8e63ab74c8433e1ef491295aea6bdeb623`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4d3ab9f9f5e11b08623fe806247e07bf17740018797c1594cc65ba4f34f7b2`  
		Last Modified: Thu, 17 Oct 2024 07:56:41 GMT  
		Size: 102.7 MB (102729259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5ec7254addbc4961aa50bc992a3a5817b8aaaa3125022646062ae6e21ee06b`  
		Last Modified: Thu, 17 Oct 2024 08:00:35 GMT  
		Size: 69.3 MB (69345210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a3ca03a6c0b0e8d1bcedbc0b77ea6466883bfb5e737eef86ab1713524bd984`  
		Last Modified: Thu, 17 Oct 2024 08:00:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:20c8cd3faa635f4f3918e3b3ee3e0c1cc395522332200427155ca4a949edd0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5037547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfc9b470c7adbfbfbb1746b0a95deb2f42cbf90cf65dabc92dba2bfa53f1e05`

```dockerfile
```

-	Layers:
	-	`sha256:e824c0772f2c0e998d216c3c34bc5ebeae8877e949491f9b6ec1e7091fb54208`  
		Last Modified: Thu, 17 Oct 2024 08:00:33 GMT  
		Size: 5.0 MB (5023482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb4c0c12f2d2c139870caa657b86560705a44af542ac7387a0eafec6d8a9533e`  
		Last Modified: Thu, 17 Oct 2024 08:00:33 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json
