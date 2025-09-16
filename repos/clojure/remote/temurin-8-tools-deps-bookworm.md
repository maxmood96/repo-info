## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:bb7a4b5f6357d54352f6ea4d30296ceccbb4a82db78626c9139f35b0cc654408
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5d0e6e0416d46649425c0dfaad8e4afc7fbe169f620d15d23dec8c1a943489cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184350056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a772f0a2ac15ca4c728acaae52174469ba19a235068a811ea965494bc1ee0b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bedf44d1c376e2838c954836058cf3f229207ea12c44f37298b21fe5cb031a`  
		Last Modified: Mon, 15 Sep 2025 23:24:52 GMT  
		Size: 54.7 MB (54731291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bad957bc861833b1ca5f309195e8e4a9539de7d78d08afde865c3957414f41`  
		Last Modified: Mon, 15 Sep 2025 23:24:52 GMT  
		Size: 81.1 MB (81137508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b513088f56f5379c7ab3db0dfd38fb08ebd27472adddcb37b953ecc74e7c0815`  
		Last Modified: Mon, 15 Sep 2025 23:24:39 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:69836e4a32acc8736cc3447ff6da7c415201216bbada9497c253eac99adcdbd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7510737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394028abaaad5a186ed7af1ba1c230fbf491247dc269255d39fe4133c92c8b4a`

```dockerfile
```

-	Layers:
	-	`sha256:e357ab370dc3e722de75260e5a332a7b7ce097f4741214764aa899a7c4e55399`  
		Last Modified: Tue, 16 Sep 2025 00:47:31 GMT  
		Size: 7.5 MB (7496500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd137dd3bc86c525de1e4db7c09c4545d68b9e6bf4c072e3b8be0e22ebcb8217`  
		Last Modified: Tue, 16 Sep 2025 00:47:32 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:715ab31f9839bf5162b9106e0ab1c971e571c45921de5c1fdbf1f42a4057d5ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.2 MB (183220877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:317360d7117a4bc92bf2973621a3c24813d3f585333e79132b9e37cd9ae8ec2c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2817c8f36b15b3fb8ccca14fb674b40fc5f9b4a938c6c33d2e45129b4ba3be6`  
		Last Modified: Mon, 15 Sep 2025 23:25:09 GMT  
		Size: 53.8 MB (53835606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0acfb9a6d7eeb9961914a5d7d4134f44fdfec6f2599c56b0351317231a8792c`  
		Last Modified: Mon, 15 Sep 2025 23:25:11 GMT  
		Size: 81.0 MB (81025610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204d068b5f469e2ad38d54f75a5bd40e516272042276b65eb1931f27eb96609a`  
		Last Modified: Mon, 15 Sep 2025 23:25:02 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a3716c771a047de6269607943c12d673cc0c9a8b9485a8570b29635f0ede2ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a9bd30707c44fcf3e7cc7a57f17e1a5cc2209b6763ce7750fb1d3adfd67b82`

```dockerfile
```

-	Layers:
	-	`sha256:4452b19ce4e20e280bf7b076b466909269a81064e02e55155e3f88c5aa5bf130`  
		Last Modified: Tue, 16 Sep 2025 00:47:39 GMT  
		Size: 7.5 MB (7502961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b15dec33947a57caacef631f9b2997bef27f9d9fb0365b5d572d7ebd8e5900d8`  
		Last Modified: Tue, 16 Sep 2025 00:47:39 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:9c08410d294229336aa906cdec3d17f58d65ccb0b6fa18f393cfa4fa9389b42d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191471628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fabd5d4b44ced7125b83c351f95abd9e769239e24122bce275d4d0ddcf5920a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
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
	-	`sha256:64b8116dd43c29a2a4aa3131cb4895af0a7267cc5883e3761556e54c369be9af`  
		Last Modified: Mon, 08 Sep 2025 21:22:08 GMT  
		Size: 52.3 MB (52326822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7e1fda3375f21ef1250fe439fa1ccdb10e051bc01f9096828ac6125007aa7d`  
		Last Modified: Tue, 09 Sep 2025 08:49:08 GMT  
		Size: 52.2 MB (52165368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10192cbfeb442695bf772ccdc43c1f56ed799098909bfbd10a6c5a9de1478f74`  
		Last Modified: Tue, 09 Sep 2025 08:55:53 GMT  
		Size: 87.0 MB (86978791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754425367ec066cb5e4011a91505c0b942be6951501c357996b574ed8bb55ac2`  
		Last Modified: Tue, 09 Sep 2025 09:13:32 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c5a3fc752ee929311b186e62fb41441b616fef5361f49960b3fd24c06ac02330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7516592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b61d2a3cfa4e682f968df32818b094cac017ad40928bfa08d33b112ffc75394a`

```dockerfile
```

-	Layers:
	-	`sha256:cce17e1a8772b020d7d42b6721e20ee05607376eeeefc5a9df092d7f0ddd7773`  
		Last Modified: Tue, 09 Sep 2025 09:37:12 GMT  
		Size: 7.5 MB (7502307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce6a27b3a3c686a43392f89749e9a2e55ec7f664c31132201fe1e22e2932e4b7`  
		Last Modified: Tue, 09 Sep 2025 09:37:13 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json
