## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:6cdaa2fde8446a6a1a6cbdd46b3102ceb77af9b928ccf8ab49c3c6f3ceb1adef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:79ee478d6f663fa5563e1aba4361a80ef2a1464aab9661c5b9f3e674e7fbac28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266172630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443dbfcae8c9eaf7a4f3ce61403fba4452982bf3ca1b6dc1abda010ef06aed96`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:16:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:16:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:16:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:16:42 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:16:42 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:16:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:16:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:16:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c67cddb4b9fcdeefaf829aa012f0ccaefcfa862a558064326104b95b8849cd81`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 53.8 MB (53773009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6596c7ebec6c0cef9e119a16ec321f1f4c88b8be534a9096d9102e730c48c92`  
		Last Modified: Wed, 24 Jun 2026 02:17:17 GMT  
		Size: 145.9 MB (145886179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b96eed767008e6f1e32277ccd025e1511f3d4a76a73a3752ed9f3924882f34`  
		Last Modified: Wed, 24 Jun 2026 02:17:16 GMT  
		Size: 66.5 MB (66512798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c0b6347fd4923aed18145a4f2f79e0503ddc98f8caed759c555480a805c0af`  
		Last Modified: Wed, 24 Jun 2026 02:17:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e984685f920cce75f2ff971319df6f967da89e32b53ae1da6c5bb5afb34f2caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7439328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b714af4cc30ab4deabea71829f9b8ff9fb758ad7c9b121307bea0113731dfa92`

```dockerfile
```

-	Layers:
	-	`sha256:e906a6ca997cfd6bbcb694518eb9a37428fd88074f4902c5139dbe6c21f0a003`  
		Last Modified: Wed, 24 Jun 2026 02:17:13 GMT  
		Size: 7.4 MB (7424965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9889896ea26c097614926bb6f9e75ff9d75c83857afbfcbaf4d19a6c272b58a`  
		Last Modified: Wed, 24 Jun 2026 02:17:13 GMT  
		Size: 14.4 KB (14363 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:87fe6ba7a89f7ef9851483d0d5c9793e031f49b15305109dc1806eef779695c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261517698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd766efae6619e9d3d8ee266fae83401efe9b47c14dd6bb2e5c23d3a8e20536`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:23:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:23:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:23:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:23:13 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:23:13 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:23:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:23:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:23:27 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:35157acdff35db21da73141f382d0dca0f6bc6d183c3a816d283fe39f471e539`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 52.3 MB (52257219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae12af3d923fce2e88756054a36886b70b1ab1f5ad23ea7a906b70862440a44d`  
		Last Modified: Wed, 24 Jun 2026 02:23:50 GMT  
		Size: 142.6 MB (142582159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9eb266ae763da3b264f0fd42660da3ae52435c66e886c6d7f1359b915ba2f74`  
		Last Modified: Wed, 24 Jun 2026 02:23:53 GMT  
		Size: 66.7 MB (66677675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ec51edc4d2568161c764462be5e5da24200caa1d0225938b7f7112e667350f`  
		Last Modified: Wed, 24 Jun 2026 02:23:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c2921f7acc6d1d032eea57eaf7eaa70aa3ec9a77fc8e2b20b73da0f19268b520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7445162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62c72aeeecf34919f3753e68a75b356a8465e39cdb7478f2091f298b13413c23`

```dockerfile
```

-	Layers:
	-	`sha256:0521d252c683391a2f99a9cfae0046862b97c219c5b875c1f8abde27c38438d2`  
		Last Modified: Wed, 24 Jun 2026 02:23:49 GMT  
		Size: 7.4 MB (7430682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45bce495302c6506e70cd6106fb66c0337ab998e2339b40db3bb25ab27e646b1`  
		Last Modified: Wed, 24 Jun 2026 02:23:49 GMT  
		Size: 14.5 KB (14480 bytes)  
		MIME: application/vnd.in-toto+json
