## `clojure:temurin-21-tools-deps-1.11.3.1456-bullseye`

```console
$ docker pull clojure@sha256:0641cfd42267d023dc74343f36d0b43b09f009229239617824643e032446eb8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.11.3.1456-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9cff7f5aa50d7b3be4df00ef057ba367effbea8743ff6d225fa0c6c3058565e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282601635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4809d50f7aefe0af7771618b1ec19255167eaee237ec599c0c565535477a2d4f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
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
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af26d14095a48a592e7f9f4b188cb9b14a7825fc15b8b593c75315290715e6f3`  
		Last Modified: Tue, 02 Jul 2024 03:03:05 GMT  
		Size: 158.5 MB (158497960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5096b1fc389fe6caf612a15ebabf0d0a6f2475696537768e88d0356b8a639d1b`  
		Last Modified: Tue, 02 Jul 2024 03:03:05 GMT  
		Size: 69.0 MB (69021272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d64a613fb2cb1c4e42ae8518ac2fcf6b39f19380c361ba423ffe2edab08b86e`  
		Last Modified: Tue, 02 Jul 2024 03:03:03 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d937571f20073a21c671915dedca37ea2e30d6930cf764427ec2183115df3815`  
		Last Modified: Tue, 02 Jul 2024 03:03:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.11.3.1456-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7e5bfd29de69922a57034861b9463fc6e42222736d5cc5d524984173ea344ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7016591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51145a0210c9178a173c2bb6d4282786c90365557eb550f3bd14f72f149304b`

```dockerfile
```

-	Layers:
	-	`sha256:43f51d09370bb7b125df55ec07a12e54e9077a6c83dfbf1041a78fceddd22da1`  
		Last Modified: Tue, 02 Jul 2024 03:03:03 GMT  
		Size: 7.0 MB (7000476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79119051a35544e800da8dba7305dd624f69940405663150cd431b6d2d8a756e`  
		Last Modified: Tue, 02 Jul 2024 03:03:03 GMT  
		Size: 16.1 KB (16115 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.11.3.1456-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:590dbe32d1d96f2d26596911770f2d4be6d8c8b155756aebc8a1033c41022a55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279335617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c2abf4e6975aa069eff49509efe7279ad0e3374bb46bfd023cc83d26c29e412`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
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
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc225c447f91c4be02defb90577b27de277549c671dc8c3aac51f798be945795`  
		Last Modified: Thu, 13 Jun 2024 11:54:31 GMT  
		Size: 156.7 MB (156665603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5270225b880ca42bfcfa84dc5e218b8557bbc19a46ca505c1476646aa120000b`  
		Last Modified: Thu, 13 Jun 2024 11:57:55 GMT  
		Size: 68.9 MB (68929385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2da30965decf511868fb64ae1714d43125558e62897247377f98d073c2f0e80`  
		Last Modified: Thu, 13 Jun 2024 11:57:53 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789243ce01a144d8146a73ee0b9aaa7650f6193250c7cdbbea8c049c35d869d3`  
		Last Modified: Thu, 13 Jun 2024 11:57:53 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.11.3.1456-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ef5afe926931d78812b361835734d33c1a6842cccff7205f6010cc0750a66576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7022858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18edf628c0257711d130c1a1c250f0c13f512301cd015841b89e9373790d826`

```dockerfile
```

-	Layers:
	-	`sha256:1406217f4ea78f6a672284dc0d1c6fe93eedb8565ef8589ba6e51aa606425a36`  
		Last Modified: Thu, 13 Jun 2024 11:57:54 GMT  
		Size: 7.0 MB (7006183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69cf5f520536cecbb3093a135f5abd0454847d60e7a75158cf12ce7788158fbb`  
		Last Modified: Thu, 13 Jun 2024 11:57:53 GMT  
		Size: 16.7 KB (16675 bytes)  
		MIME: application/vnd.in-toto+json
