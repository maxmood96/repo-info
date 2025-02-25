## `clojure:temurin-23-bullseye`

```console
$ docker pull clojure@sha256:91e8451f270b435737833cc07e7794302fad92b02917475aca52d78d40d4eff2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:076397e60174b1b0be916125af8f816e3aa9b09cbd78ee8ff7da4ad850b6662a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288246053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca51d4a2ebe23afc970f08726b6a36d398cfd9b2ece235ba4d003d7f45347d99`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e172a9cf2f0b060db83cbb3ee5424c16e0a6139d678c49f8e3fe5a9eed526b`  
		Last Modified: Tue, 25 Feb 2025 02:35:39 GMT  
		Size: 165.3 MB (165316229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706401864d511ad61534e2e88833c8b243f80a6a70500b9561bd2295deb702d2`  
		Last Modified: Tue, 25 Feb 2025 02:35:38 GMT  
		Size: 69.2 MB (69187382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82010919f1e9749e5a92747cef8561af959b67a372fcef925bb8a8e069d572d4`  
		Last Modified: Tue, 25 Feb 2025 02:35:37 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f56ee8049feee0dbb90319bf647fc1b8df86e2968376288551be7d7ff8d161b`  
		Last Modified: Tue, 25 Feb 2025 02:35:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7c37ddbd631e8b65f133ae4abcac063764008b8c585aa1abfdda590db1747b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7225379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4852174b368876288728d212fb3e4385ada9361cea6f0de15bc1ba56e52e0a40`

```dockerfile
```

-	Layers:
	-	`sha256:564f2bbdc651bff9f17268414bc3a56f79566265679ebaa488ed2dc29e9e1406`  
		Last Modified: Tue, 25 Feb 2025 02:35:37 GMT  
		Size: 7.2 MB (7209560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c9c455e8d149d5606283e1d6300cfea64f3d3f12cc9c2614584849bd5ad4171`  
		Last Modified: Tue, 25 Feb 2025 02:35:37 GMT  
		Size: 15.8 KB (15819 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:28e3a3b98733de96053e67513c2d0e0d404d2bea4ea4e4619245ea953da5d037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.9 MB (284897399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c81ab6856c495d3b4213f084bd037e1b91d2570520f06a8298f97084e281724`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0038ef039a89ede34c57806e684dc9d9be7dcd22d3c08b90deb36bb22a2c7122`  
		Last Modified: Tue, 04 Feb 2025 01:38:11 GMT  
		Size: 52.2 MB (52245695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd20da7c7dc2925173ad8f68cde57ff31d8100b23263e02413cfacd43e2050b`  
		Last Modified: Wed, 05 Feb 2025 00:01:57 GMT  
		Size: 163.3 MB (163341455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ed37c95b9df030ae58c047d9f5745cc1255f5547bc996dcb8a13aad8811d0c`  
		Last Modified: Thu, 20 Feb 2025 04:02:23 GMT  
		Size: 69.3 MB (69309210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc551394301cb49fe96e95b36fcb4a04c6751234d0a0545a7ba6ab436122394f`  
		Last Modified: Thu, 20 Feb 2025 04:02:20 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57b896d3f19ede9a7df1050f2c181e5340bd653b88de280494b32058ff244ea`  
		Last Modified: Thu, 20 Feb 2025 04:02:21 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c68607ff1a79e2c5da11ebfde89bb9404feb2df929010e75afe0caf127360e9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7229976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b80c92d5a854a13a480da162e32b999a09541067be6ba8301c150ef732f1d26`

```dockerfile
```

-	Layers:
	-	`sha256:ddb0da2e7a9b2c0e7ff23fd259370b871061d18a51028dfced9016ce01703b8e`  
		Last Modified: Thu, 20 Feb 2025 04:02:21 GMT  
		Size: 7.2 MB (7214038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4fa8f5b05dd7d2e046ed6725ee49857cebfac4d5be9bcbffd26104f8c4ecdaa`  
		Last Modified: Thu, 20 Feb 2025 04:02:20 GMT  
		Size: 15.9 KB (15938 bytes)  
		MIME: application/vnd.in-toto+json
