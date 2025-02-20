## `clojure:temurin-8-tools-deps-1.12.0.1517-bullseye`

```console
$ docker pull clojure@sha256:bc59a3cd85e0cdd1932960ecd2f7386e17909607f3301dad2ca250ac077371df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1517-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:770e431c96457d131685fc6d77034332bc3b4971af99aca3a6551d0f16c1d3ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177648289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69379fc3deef9f5dc8c5ab59b619ec295562d8fb8eefdf649b9682c7c1f22c04`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 04:23:03 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec14d64a081d47b831cc813d0e2855810172ae9bedb6c8c7de18548f5ef78a9`  
		Last Modified: Thu, 20 Feb 2025 02:29:35 GMT  
		Size: 54.7 MB (54721234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b64c20482ad9b7dc4503cd2c797a76a8fc8d75d99e31aa1f496d5bbe5eb029`  
		Last Modified: Thu, 20 Feb 2025 02:29:35 GMT  
		Size: 69.2 MB (69187538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78ced363a4d809a8ead32e4dcdfac31ae250f4e37ee6edc2e61b5f54c73b96f`  
		Last Modified: Thu, 20 Feb 2025 02:29:32 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1517-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:dbb281b85e45f24682767b62f46829b0a3adfbb05ad2b0cea33f3b2c55cbec0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7340402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e64ab22b5bc851ae06dd763473e71584ce21b5f5096d8c55ac4dbf67659d9d`

```dockerfile
```

-	Layers:
	-	`sha256:ec2fcb1fae1dfbbf0debff1cd3cee97c711f2860cd67551f2a2408f81ef83591`  
		Last Modified: Thu, 20 Feb 2025 04:38:52 GMT  
		Size: 7.3 MB (7326165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b29e584c842196b17d42e4a34280f84d5b86610ddd8bf9139d1d6ba5e656674c`  
		Last Modified: Thu, 20 Feb 2025 04:38:52 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1517-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:12c76e35254f21ca73d039ed29afaf148a28a69f8ac4f1f3e7c2ef02d1527c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175378438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72972b16588cc9f7a3b212550641dbe2340bbcdcf03dfbd0df76d8ec79515006`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:0038ef039a89ede34c57806e684dc9d9be7dcd22d3c08b90deb36bb22a2c7122`  
		Last Modified: Tue, 04 Feb 2025 04:34:59 GMT  
		Size: 52.2 MB (52245695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7e26da71c068cb6c68e55199cec0b81f2ef30055e49e4a653cd41241402103`  
		Last Modified: Fri, 07 Feb 2025 06:31:31 GMT  
		Size: 53.8 MB (53822761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2870157ad64dc96fcfd49b9ff7f7f36bb3866d2f185f25dc37fa06d4a0cb1365`  
		Last Modified: Thu, 20 Feb 2025 04:06:27 GMT  
		Size: 69.3 MB (69309337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ff6a7b89f695b5b65c786c6fd0c7c0daa7e1ae82ff42d1e8a9390369e8c30c`  
		Last Modified: Thu, 20 Feb 2025 04:06:16 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1517-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f3dc3a0f532ca2bd16cba20a521810041640116d43ffc27f6c7c33778f6bcc2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7346315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c910c0ada1fc9ef0739cace436d32e40eb2724c945c2a1d8d4868908ca6ad2`

```dockerfile
```

-	Layers:
	-	`sha256:84c507c76e0c7574ab2b89df98a56578e571cc546089a6f9a04c3ccb05c6f5ce`  
		Last Modified: Thu, 20 Feb 2025 04:38:55 GMT  
		Size: 7.3 MB (7331962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b41472c366e1a168237299772dd33dcc236f38ab934af4d56dbd16513fde1cb`  
		Last Modified: Thu, 20 Feb 2025 04:38:56 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json
