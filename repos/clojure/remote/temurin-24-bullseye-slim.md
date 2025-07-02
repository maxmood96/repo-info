## `clojure:temurin-24-bullseye-slim`

```console
$ docker pull clojure@sha256:a13cf6f3e063d27a53b9ab57e0fe3a21592ecc1c5d1e78aa5b980e06b51ccdcd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5e23f75d11596e21d155ec772597655f8a99ddbaac199d8f82b300183e4d6ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179214785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a010f47ca043e080d6551a48eac82c024a8c001abef946a6498b8d088a46e8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1448dfa7929f6375abf1bf167311d1ee62765a83f3c101ac2157fa5538223e81`  
		Last Modified: Wed, 02 Jul 2025 04:17:50 GMT  
		Size: 90.0 MB (89952001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03287e6f5b32d0eba51614894bb15762aec5b2479477b6933ad3e2645cfbfff`  
		Last Modified: Wed, 02 Jul 2025 04:17:41 GMT  
		Size: 59.0 MB (59005696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ceffade24538ce7fea3821e584626f5de95da8c72be3d75be1369106c92bbb2`  
		Last Modified: Wed, 02 Jul 2025 04:17:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b34c54fd31f5beab876cba538c769a538fdf33e21255f56c09a4a02d47fc7a`  
		Last Modified: Wed, 02 Jul 2025 04:17:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f1571c9b9b1a4cbdd9b99eb3acb1be9af588914d23d11a1bcf5184bbba17acde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5274555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d1861eae91eb6c4124485e0a5a43698a57e1a1608101f0e824197273ab2479`

```dockerfile
```

-	Layers:
	-	`sha256:50a8094838f542e94ebc8b3d39ab7ca06902880d3eb8b218b291879c88061cb5`  
		Last Modified: Wed, 02 Jul 2025 06:41:13 GMT  
		Size: 5.3 MB (5258684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c592eca75781f610e0b94a345cc771171714bb6a0eda322a5fc61ae163902b6d`  
		Last Modified: Wed, 02 Jul 2025 06:41:14 GMT  
		Size: 15.9 KB (15871 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:65c190b710179aa99fe01ec0c6dbfa9388e1ef6113bdd13d985cb8c176573481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176974126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e161d45f266403ca435441fd9e2ebdcfe50996a1775e25074deace86886c82`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70f5a28c76e18532e41dffe087e67fc70d78bc8a4a7d0b30373b001b9fc6a5c`  
		Last Modified: Wed, 02 Jul 2025 12:57:49 GMT  
		Size: 89.1 MB (89091234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499cf710428bd97a408677d6548a5ce4c43256d1948c721ea2657b30c2d0c1fa`  
		Last Modified: Wed, 02 Jul 2025 13:03:05 GMT  
		Size: 59.1 MB (59137712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86841a500f26178a382f28e92e4c428c1ebf3bad0bfcb55f4afe76aeee707319`  
		Last Modified: Wed, 02 Jul 2025 13:03:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08dc50b6a62cd09a974f1ff9c56339aaff00748960e3ecfae6bdfca3e7ad4bfc`  
		Last Modified: Wed, 02 Jul 2025 13:03:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fde7b3b7c2aa6f97b7002e7dad6964df293b29c59142a3729ff1124aa0ed1462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed541fc5048e0df43df14d06049ac5e7d5217fe7065423364b9e7a40e287516`

```dockerfile
```

-	Layers:
	-	`sha256:6c7e6a32ad5d2fa86af3a027dd79d9f712c1a2cd1eb4ae3c4fa6222de0d97804`  
		Last Modified: Wed, 02 Jul 2025 15:42:02 GMT  
		Size: 5.3 MB (5264413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3485b3b49cb0abd4572a9a3c49b46ddc05dffe34aad10d19278a835d587a35b`  
		Last Modified: Wed, 02 Jul 2025 15:42:02 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json
