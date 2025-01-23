## `clojure:temurin-23-tools-deps-1.12.0.1495-bullseye`

```console
$ docker pull clojure@sha256:4c31400786cb32b1cabb299f74f0ec8fdbdb24d5107803d33cf78410e08b4b29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1495-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:acc3fda51246d463c4a34e5e041b92ec0500ae0713a15df4ec859cd9f23011d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288213811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bb64632e1d77e11bfce9fbf3510e753a144d1a80c5129a976ce650f7bdd9e5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fa3d69ccb77ff6de2f635c97308a8572aed742c141aca82562820a87d64bcb`  
		Last Modified: Wed, 22 Jan 2025 19:42:37 GMT  
		Size: 165.3 MB (165295135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbd4113f2eca4c739b381186e78924aa42a7f9007dbd729c53d80ed3c6d53b8`  
		Last Modified: Wed, 22 Jan 2025 19:42:36 GMT  
		Size: 69.2 MB (69178471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84be987bbb30377aedc29d3ac6fd5bd835ad1b3c0f1415993dd96894cb131c9`  
		Last Modified: Wed, 22 Jan 2025 19:42:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54f661ab0a5fdc01cadab02ffc40660b91196f35fbf3b04b2c3cf944eb6c602`  
		Last Modified: Wed, 22 Jan 2025 19:42:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1495-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7eed94775198dc7ad20c903dbda6de21579e62ea114082ae1fbd5db2440b5cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7225382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989943abc6bc3677af3233a6cca37029ede17876b5befc8e1a7cc753e0d2b932`

```dockerfile
```

-	Layers:
	-	`sha256:1bfc9813dd6b2af143a871228fdbf4f9fef905a5d53aee6df3710d74ac395e4f`  
		Last Modified: Wed, 22 Jan 2025 19:42:35 GMT  
		Size: 7.2 MB (7209562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a600bc465a562703ba8efec181ada78b3cb1d288797a31448b64134f254dc1f`  
		Last Modified: Wed, 22 Jan 2025 19:42:35 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1495-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:65a7309357814a3ecaf22f5797b03e8816f7d36c8d3871e2cfd48a48640adea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284833261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862d829747edf94793b8b89888f5507a3cb38b55e45936cf0b2074f585cdacb2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ca543c77f30c2f45d64e12050b7d093e1c0ddaf3c74b92fda20bba862b0f7d`  
		Last Modified: Thu, 23 Jan 2025 03:55:52 GMT  
		Size: 163.3 MB (163281769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ee9f76c83e31ea463a05dd3f568af62c4bc22be75f2de7dffffbf093fdde21`  
		Last Modified: Thu, 23 Jan 2025 04:00:00 GMT  
		Size: 69.3 MB (69304389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c01cd8e4758c5b87adbde8c7d61e2709d45c4d653766d47bed0187a2f426547`  
		Last Modified: Thu, 23 Jan 2025 03:59:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8da532aef7f5d6e85ef8811295351e8d6e1cd07a70d0594513a710f16d5deb3`  
		Last Modified: Thu, 23 Jan 2025 03:59:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1495-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:571df948a3f6e762427942db9434c05f018da180600f7bc890487f879f0dd7b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7229978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7deb76a1c76a666ddb77b7b4fbf89d1a23cb5f2a235ec1b3991a8053c23c3c20`

```dockerfile
```

-	Layers:
	-	`sha256:83e990138481f252f0e8a077c453f9235582d173ef690dc53b681ac4ac457fbd`  
		Last Modified: Thu, 23 Jan 2025 03:59:58 GMT  
		Size: 7.2 MB (7214040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b65ce44bb0c432a8ea4919fcd49f16bb6a1ca72c761f70b7533994604089ab45`  
		Last Modified: Thu, 23 Jan 2025 03:59:58 GMT  
		Size: 15.9 KB (15938 bytes)  
		MIME: application/vnd.in-toto+json
