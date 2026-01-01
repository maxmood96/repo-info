## `clojure:temurin-21-trixie-slim`

```console
$ docker pull clojure@sha256:f5e144659f9751580ec95d7cfce26c3c0161ab8fd048a10e55b2acfcd584eaa3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:669f96c28fbbd651e6833f0a8ddc862211f07f410172bf06000761e7ec7611f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259596212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a86ccd1dbd59c18ebee01872ba24ae53a68ccabcc65ff1ceee5b8bb8cb7960`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:05:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:05:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:05:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:05:42 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:05:43 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:06:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:06:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:06:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:06:00 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:06:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e802ce0544a0f52ee7001cb6f793e919fb73b11cb152aa40c2e4e4f7070c6f`  
		Last Modified: Tue, 30 Dec 2025 01:06:48 GMT  
		Size: 157.8 MB (157825957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa14d33c6670a4178faa6c0d19844b616dcca829ad362deb2538cb640660e95`  
		Last Modified: Tue, 30 Dec 2025 01:06:37 GMT  
		Size: 72.0 MB (71992684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c73809e5f52043a76fbacd766abd76d53a16064ea811f748bef92d6a2c8d962`  
		Last Modified: Tue, 30 Dec 2025 01:06:30 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecec9b9492ae5ca2aeecd350fc371ed87efe257fecdd7a122389b0810ce44ee7`  
		Last Modified: Tue, 30 Dec 2025 01:06:30 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e0daf6fd34fa7a049412b618045d73e5d7b9cffe3cf2221dbb146c71b4c339af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723a76ad80062c92bb345d168bc08e8c58bbb0c683191d3ecb451ca850358d21`

```dockerfile
```

-	Layers:
	-	`sha256:7b8520169882309b003670ec3b7c9538d7927878ccd41d136ac15fe1cdb65222`  
		Last Modified: Tue, 30 Dec 2025 04:45:21 GMT  
		Size: 5.3 MB (5259301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2521b6b7cee84911e682ddc603c148cd21aa0cea85fa7737ec727b038996bae3`  
		Last Modified: Tue, 30 Dec 2025 04:45:22 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3dbeba32bc87e6bca69c4913aee5b2c674a30a01853f4e91f3dba1a4e37126f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258054356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8473e19ad797ab0036991462d9d37ea225843e8749f952d7782fd3d389980c0f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:06:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:06:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:06:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:06:33 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:06:33 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:06:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:06:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:06:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:06:51 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:06:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eca58aa5c6ea7678b5733c493eea507d316c9c02594558457e30283edf2b9ab`  
		Last Modified: Tue, 30 Dec 2025 01:07:30 GMT  
		Size: 156.1 MB (156107650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7698731fbea3bb735f7c8ce2754db6ae903dd19cb553d61ead28b60252deef`  
		Last Modified: Tue, 30 Dec 2025 01:07:28 GMT  
		Size: 71.8 MB (71807029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a6f139d8d82c6ce6b53f74e75046c182afbfc602e44b218a18b6ad3e5f404e`  
		Last Modified: Tue, 30 Dec 2025 01:07:21 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d41be9af74d04670281e234077c5df92ff204b02e8bd293ce9ed758ce47346`  
		Last Modified: Tue, 30 Dec 2025 01:07:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c647283559fdb6cd4ed099c198bab9a09bb2e9148f8713c5c427e747cb7e785f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94652db3fff227bf52499e822d1ca7cabb42a22dce17e8972e82c52e697d2546`

```dockerfile
```

-	Layers:
	-	`sha256:8dd9ecd129093e3cc47875f13dac5dcf1971bfa53b303d704c40b254f5db7038`  
		Last Modified: Tue, 30 Dec 2025 04:45:27 GMT  
		Size: 5.3 MB (5265070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24621536011f8240767c9ff094ac8e69d8f473e10a69b964d8838c173bffc078`  
		Last Modified: Tue, 30 Dec 2025 04:45:27 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:51877662f745fd5bda19558adacc0228bdc1101ee61f690ac96d9fa6e9e7bdc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268927827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c3603a65b0a3330d9c26d214b778954015c7df96ebe9aa97b1e39190ee452e3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 19:12:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 19:12:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 19:12:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 19:12:27 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 19:12:28 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 19:13:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 19:13:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 19:13:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 19:13:23 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 19:13:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:34b56ab3c5579c93222f3403d640c7a7f19044e9e46a2d1c6b1da60bde918efc`  
		Last Modified: Tue, 30 Dec 2025 15:11:02 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014e34982fef363cb98e1c1e9b321958d9efab2621f8862b9eed44798f4ebcc8`  
		Last Modified: Tue, 30 Dec 2025 19:14:27 GMT  
		Size: 157.9 MB (157942938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f11d408c432491b6a9eac491381654e40b3b9b38cf631b6b8acfbc53170e0240`  
		Last Modified: Tue, 30 Dec 2025 19:14:39 GMT  
		Size: 77.4 MB (77386955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962743c453917fca800113fdc6482f3097c0fde748b7878112f0a903e42f43d6`  
		Last Modified: Tue, 30 Dec 2025 19:14:17 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283af9fd7eebc407529b4417f404ceba38aadfff331856ae7b57ea7ca8c98d35`  
		Last Modified: Tue, 30 Dec 2025 19:14:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:85754d3e3ebe9737be0f391d824c52a1cb7fdfe1eac95cd5be00b63688199ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb00112ba1c09292213228b170b4bb8a5e8d671b62b83c7f973d080199fd71b8`

```dockerfile
```

-	Layers:
	-	`sha256:e1b99ea11b4d8d96b47df1c5a8aebeb4b3f55d53f86467b82b6ac11067995389`  
		Last Modified: Tue, 30 Dec 2025 22:36:58 GMT  
		Size: 5.3 MB (5263672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f56ab03cd69b791ade89efb5349d936b2c7dd8f7ddbd72894594b7f8afe2b81`  
		Last Modified: Tue, 30 Dec 2025 22:36:59 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:67cd579232b51203a3dc13b303cbe8615108f9c08fd30fcce37235fe31f04664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.3 MB (256346826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6e76c45c6ffb4623aa308d2eb2f7e058c36158f1eed21588323d911d91a44e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Thu, 01 Jan 2026 07:02:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jan 2026 07:02:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 01 Jan 2026 07:02:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jan 2026 07:02:49 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 01 Jan 2026 07:02:50 GMT
WORKDIR /tmp
# Thu, 01 Jan 2026 07:19:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 01 Jan 2026 07:19:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 01 Jan 2026 07:19:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 01 Jan 2026 07:19:57 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Jan 2026 07:19:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091162d898a2d4e7b50f7bb9588aeb36e7979c2a93097ad0bdcd2473aa01fb84`  
		Last Modified: Thu, 01 Jan 2026 07:09:19 GMT  
		Size: 157.2 MB (157194291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b596bea77b5945f1b112128096634da44c9318253db5c4a5d2e7e3264007b7`  
		Last Modified: Thu, 01 Jan 2026 07:24:11 GMT  
		Size: 70.9 MB (70878363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6257729749f6b2bdc6b07d335123d519a150a21ec4fdb22e5857cec4645bac16`  
		Last Modified: Thu, 01 Jan 2026 07:24:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fd48c429a24d9fcabd2d239fc71b9f43db7daf050603101ce83ad55dbf3acf`  
		Last Modified: Thu, 01 Jan 2026 07:24:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bb4bb828e91d6f09b34605193fdb1084fba497b4221692e904e76af7b9509fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80f7527c92c3b15b147ca02fb0d7ad7ab326bbe6fd2d318503e5585ad07a4bf`

```dockerfile
```

-	Layers:
	-	`sha256:88233960f8e761e594c8af3dbcbea20f0052acb9d6f2b64a3627a9d7ae7bb413`  
		Last Modified: Thu, 01 Jan 2026 10:37:13 GMT  
		Size: 5.2 MB (5248765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4090cd20b637de4d3b7f8f028f36df46f003c9b0bb4c0826e1836a0dff99b919`  
		Last Modified: Thu, 01 Jan 2026 10:37:14 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:6e298551e9cd57d2082f54bca3d97bcbe0b8ec65eb968b11a81de95b1df482db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.9 MB (249858588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77bb7f6346e939d1e0397ff9601cfdae6a2967d27fecd463d1838fb24bfdb59`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 02:05:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 02:05:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 02:05:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:05:22 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 02:05:22 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 02:05:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 02:05:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 02:05:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 02:05:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 02:05:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be255ab5ccf8106b6424684700a41d5baa9ffc3f05ddc252ead95e6e46ebca94`  
		Last Modified: Tue, 30 Dec 2025 02:06:35 GMT  
		Size: 147.1 MB (147069816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af02edb872696285d0059648f5fda78473a16e7f45085331e954276b0b291bba`  
		Last Modified: Tue, 30 Dec 2025 02:06:19 GMT  
		Size: 73.0 MB (72953314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba514d7b4df23748f9fc44353b5612abdd8ddc7c1ff7697f4e53dd34cb78739b`  
		Last Modified: Tue, 30 Dec 2025 02:06:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69727ab2da9ac14dfcada379cf95ee8b0df3ef8a6a1574b7eedde25f5c70bf99`  
		Last Modified: Tue, 30 Dec 2025 02:06:14 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e68d55f270cb6807736dbbb202605e278393475b67aa8a737d4a7ef9d1a4904a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0bfa882c84ab3cf8a119585ab41e93547942e8d1d52643bd7a3b0d6ff83d73a`

```dockerfile
```

-	Layers:
	-	`sha256:e9b450569355b1115edfe3159a1679fa74b99cf98736562b068e2fa68e8fb5d0`  
		Last Modified: Tue, 30 Dec 2025 04:45:41 GMT  
		Size: 5.3 MB (5255225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c75782e05cdc1ee963d94967f9997be37c165ed5d79a2d0ced55c76c90886bbb`  
		Last Modified: Tue, 30 Dec 2025 04:45:42 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
