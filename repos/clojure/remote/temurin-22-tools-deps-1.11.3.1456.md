## `clojure:temurin-22-tools-deps-1.11.3.1456`

```console
$ docker pull clojure@sha256:166cfc10ee32cfa609e20eaa38c5eaac5869977fe7e00d305f849c9dfd64d20b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-1.11.3.1456` - linux; amd64

```console
$ docker pull clojure@sha256:5099aa52770ac8bb8181e4a4ae2cfeee513170e30cb5d96a74bdb9cffb7252f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.6 MB (286592743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5902cdf715b4e9e383e9717ef483261fda9fe82b20219377fd62b6cdcd79b48`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1be7480ff186bf4401710829ce4127dec1b7668bff4ba09be1c74544c46961`  
		Last Modified: Wed, 05 Jun 2024 06:12:43 GMT  
		Size: 156.7 MB (156715500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebda725f227678a9f452c738618d42700abec6ae13d4f9c2a7fde3e6b020a42`  
		Last Modified: Wed, 05 Jun 2024 06:12:41 GMT  
		Size: 80.3 MB (80299808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54666769fac3162d9486fcc2cccbfa0ab85f1a2cc27a7575caa5f4e9442fab6c`  
		Last Modified: Wed, 05 Jun 2024 06:12:39 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a60b530aeb5f252b8bfc0b1ef127149100ad63d483f5f4357570c773c8fc035`  
		Last Modified: Wed, 05 Jun 2024 06:12:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.3.1456` - unknown; unknown

```console
$ docker pull clojure@sha256:78af58fd60bbb76261c641147fc48cbade8b026ab2874aebaba0f91f7fff383c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6977418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b825970191bd8abc7655d81a54ad441189d9ea91502c810b03e14606a5e807b5`

```dockerfile
```

-	Layers:
	-	`sha256:3c1c7b51c8c630fd511939512b9ba5d17cbc60cad1d415922ffd431d2c7656bb`  
		Last Modified: Wed, 05 Jun 2024 06:12:39 GMT  
		Size: 7.0 MB (6961344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:521010bba5a66b6edfbb63d7ce14b083a1f37cbb6c6ceae409cf96307c2735aa`  
		Last Modified: Wed, 05 Jun 2024 06:12:39 GMT  
		Size: 16.1 KB (16074 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-1.11.3.1456` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7d09b526f2dad0be20a27aff976816da1c4ba077ca4490f2d31ada3e52161907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.4 MB (284397055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fdd5bd88f49b42e67a6461e88d565c28ac4a056116826c285276a3691f508e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a7de9ee68abedc6c5a307899774444d3faa4324c90df9c8bb81d7c84f33414`  
		Last Modified: Thu, 13 Jun 2024 11:59:37 GMT  
		Size: 154.7 MB (154738035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700d1b3ef1da44e6e96f3ba993d36f968ea1a8ce71de573c05b2b4ba87f4b030`  
		Last Modified: Thu, 13 Jun 2024 12:03:16 GMT  
		Size: 80.0 MB (80044571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f2425113bbd696cb4e059bc20b86840300e4fa5503e4fc2b84e6b75e1734cd`  
		Last Modified: Thu, 13 Jun 2024 12:03:13 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f1e3a0b8f135dca52f9913b27d27f3f813b7e29e421eb606e1ef99cdb8c451`  
		Last Modified: Thu, 13 Jun 2024 12:03:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.3.1456` - unknown; unknown

```console
$ docker pull clojure@sha256:6bbea5642e92098ca260374db7b2529d3f18f093007d3bb65839d9448449cfbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6984437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb57a8a5db454a905eeba35f507abbf68b33d2ee898012aa25327fae98237d9f`

```dockerfile
```

-	Layers:
	-	`sha256:fb2a0720afc0f2141a75d2273474d53178626e2351bb34d1e17a70f06c3bb4e5`  
		Last Modified: Thu, 13 Jun 2024 12:03:14 GMT  
		Size: 7.0 MB (6967755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c836e2dc742b683315db1fc9b5442de6d214487bbfc00c5e4587deebf997400f`  
		Last Modified: Thu, 13 Jun 2024 12:03:13 GMT  
		Size: 16.7 KB (16682 bytes)  
		MIME: application/vnd.in-toto+json
