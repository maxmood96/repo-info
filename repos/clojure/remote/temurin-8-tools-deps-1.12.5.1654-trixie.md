## `clojure:temurin-8-tools-deps-1.12.5.1654-trixie`

```console
$ docker pull clojure@sha256:4d1a21b57e2613d06833e44e5a286a960076d256f2c8077e7d51806fcae833f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.5.1654-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:62da915ec137b06d5cb4e2152469f1c9c94ffe1a274244789555afade721515d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.0 MB (187035403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4abdf99894a87e350e1d1ef42732f4566cae4c511e1e947e2c575b5e546d806b`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:14:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:14:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:14:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:14:44 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:14:45 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:15:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:15:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:15:01 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:aa3e9ef32f73c30e8b065800ee66429992d3bfea6a1fb8224afdd878ab5b994f`  
		Last Modified: Wed, 24 Jun 2026 00:28:33 GMT  
		Size: 49.3 MB (49317255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625ba20eda01da6cdfd88d31ff8f002d79e3fbea3809dd50bf8881292c7d9209`  
		Last Modified: Wed, 24 Jun 2026 02:15:22 GMT  
		Size: 55.2 MB (55198726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e78758f70db572e2ad98845c43f24395837733040e56691dda6e64531be383`  
		Last Modified: Wed, 24 Jun 2026 02:15:22 GMT  
		Size: 82.5 MB (82518776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef4a47cb504899a87a98c70b204eb30b9dd95c4c06e5d1075f517206b47f226`  
		Last Modified: Wed, 24 Jun 2026 02:15:19 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1654-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bf86c3c442dc864edb889fb91683a96e0a3f276c6cb1a20e8f84229cfc32367f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7603455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38fa9e51a5ca86818e2100dd84394d60fc9d97363093853e4c9bd1612b30c34`

```dockerfile
```

-	Layers:
	-	`sha256:f9864df8aaae31e8a7a0a7feada0368d9a9cbeae17c10e508e29e4210851c8ee`  
		Last Modified: Wed, 24 Jun 2026 02:15:20 GMT  
		Size: 7.6 MB (7589131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a92d027197bccb9d46a7c8debfa9e3ed6343234c7ef17da3193634cd67a429a`  
		Last Modified: Wed, 24 Jun 2026 02:15:19 GMT  
		Size: 14.3 KB (14324 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.5.1654-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:69d1cbdd3d80681a3a37e0c30b8b61c0ecfb99abd4ff3e03f957a3ddabfcd00a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.3 MB (186290125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c9992c471b76f4b66d420e9a5c1c603f2be6b6fb7e4352de3a72457b451702`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:15:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:15:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:15:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:15:13 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:15:13 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:15:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:15:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:15:31 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981a2458f0dceacffb75afcf6a218b9c21b8829d14bbac65155cb251bf4d0644`  
		Last Modified: Fri, 19 Jun 2026 02:15:50 GMT  
		Size: 54.3 MB (54272923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f791b2dbe0c8933751a6e6025204cb229a45882ec0314ee74f22e26023a39a`  
		Last Modified: Fri, 19 Jun 2026 02:15:51 GMT  
		Size: 82.3 MB (82338387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0acdea49442625a3779f467828f0dc7ecb0036c76485d8cc44d410dc32fe273`  
		Last Modified: Fri, 19 Jun 2026 02:15:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1654-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1f2faf39c9b98c62dc6294a34de88375948ed1251ec20eea08eace847ad9a93f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6224d0de8e8c3d7e21eead451a913fcf1ee69d4b94ae3b98f2cc8b5ac6ab6bd8`

```dockerfile
```

-	Layers:
	-	`sha256:3d9c56fd000a42462195fe735dbe13be2f0e18f960555ce521f8b88fd15ab41d`  
		Last Modified: Fri, 19 Jun 2026 02:15:48 GMT  
		Size: 7.6 MB (7596224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b1dee2a7b14b367a5c0543d4722a23ee6d0894ea87e2a9fdfe1fcea640cc18a`  
		Last Modified: Fri, 19 Jun 2026 02:15:48 GMT  
		Size: 14.4 KB (14442 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.5.1654-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:60da5bbc6a57cbca44fc2608924598e23d3f0170a1c52d4f125a26f91535f1f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.7 MB (193746550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a41c108b78cf7fd36f95f5566ac9785a67a4c3dbea938d748c5cdf5b6e62cf18`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:22:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:22:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:22:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:22:23 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:22:23 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:23:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:23:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:23:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e48d9e8a7aaea509ea047e9140822d0ae3d2b693a7bf9daea2c924ecd909bd5`  
		Last Modified: Fri, 19 Jun 2026 02:24:09 GMT  
		Size: 52.7 MB (52669121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fdefd08e6ed395d989bff315a62a4c98c3cb4a8ae3e22ef0dabf693c252451`  
		Last Modified: Fri, 19 Jun 2026 02:24:10 GMT  
		Size: 87.9 MB (87938843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eaddcfc034c4a033ca67d9ce46b533415604596bfb9414884cd03f4f85f694b`  
		Last Modified: Fri, 19 Jun 2026 02:24:07 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1654-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:07f1d96f4844bec30c6d4bd18a2759542333e0bf6597e3ef35b19005c988cbb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7608519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ccf104197404039050942aad357531a45aa9a526277292c27d29841e2cee60`

```dockerfile
```

-	Layers:
	-	`sha256:efcd0eca6b5ce977811616b3c7697f4b44820fb58ef3f114d60ae53c60845528`  
		Last Modified: Fri, 19 Jun 2026 02:24:07 GMT  
		Size: 7.6 MB (7594147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:135d3f864b19b4b924ad5919c676e62cfaced700f422c73872007eca96546157`  
		Last Modified: Fri, 19 Jun 2026 02:24:07 GMT  
		Size: 14.4 KB (14372 bytes)  
		MIME: application/vnd.in-toto+json
