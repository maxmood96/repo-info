## `clojure:tools-deps-bullseye`

```console
$ docker pull clojure@sha256:ad75cac3000855911bfc67d31ef3f4da6b748ca05eb403db4a02fd3efcf60628
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:af359011dbcd960ee36b7b27c54b923313eaf90829dbb1594d1ddffd99ff8de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.4 MB (282413944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94972c3a7d276b6372c9c803eac1724843203ac30b41584f4d490664ae9d717`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
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
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be3345c005b31e46e702bbb41d8392b21f4fd92cfd1be18ec02e83935095ac4`  
		Last Modified: Wed, 05 Jun 2024 06:10:33 GMT  
		Size: 158.5 MB (158497970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4395dbfe4aa9eb14543eba1a325b6323f7f72361312c94be58cdd2d644e3ef6`  
		Last Modified: Wed, 05 Jun 2024 06:10:32 GMT  
		Size: 68.8 MB (68815527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5c301e29f08a2864c59fe59bcabeedce21e5764439f5753826613fdfc08498`  
		Last Modified: Wed, 05 Jun 2024 06:10:31 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b69b4c9becf3bf5a40359dc381e01533e42413f96a1bf12d2a65cb5a74ef01d`  
		Last Modified: Wed, 05 Jun 2024 06:10:31 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9b8f09b5e7ab0651cd59cb4fe00226164a1135a8dc92bde23ab4df75398adcab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7016503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb2d8a7e203e5e9c874cdf437d70a1b8694a87d1b507a30e2757c5e9790eec2a`

```dockerfile
```

-	Layers:
	-	`sha256:924c8a5a5138ea31bec1452c036a5110e68c1f412210a34e59ae55e24d24cd66`  
		Last Modified: Wed, 05 Jun 2024 06:10:31 GMT  
		Size: 7.0 MB (7000437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72549129c4e2d50956f209aab544952364b819e8675e61e2e52e86bd9b4c5f79`  
		Last Modified: Wed, 05 Jun 2024 06:10:30 GMT  
		Size: 16.1 KB (16066 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye` - linux; arm64 variant v8

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

### `clojure:tools-deps-bullseye` - unknown; unknown

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
