## `clojure:tools-deps-1.11.3.1456-bullseye`

```console
$ docker pull clojure@sha256:f94530a4fa9c365a0566df9caf3c1489c3e374bcb0184a806a6043f5da29d7a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.11.3.1456-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:fcd4bf5b6eef5702b5cb5ccd28fc5fe42349b4ea2c9f0d7f21e614adb5866918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.4 MB (282414712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ee36b89dbf8550da41de8e606860b00350b83decd03084df0049e1ce23e6ac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
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
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1ff4108980db63822e8435bfb13dd2371e05879c1cc94687bc40c32916a2c3`  
		Last Modified: Thu, 13 Jun 2024 18:14:04 GMT  
		Size: 158.5 MB (158497944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a2d59a94de5eaf4a568d2066b5efea390e176f5b71b865f2bb503b60576106`  
		Last Modified: Thu, 13 Jun 2024 18:14:07 GMT  
		Size: 68.8 MB (68816531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a15f7ff4918ca45051e606fb104df390d477c5fd57c8ffa89acdb83c8030df`  
		Last Modified: Thu, 13 Jun 2024 18:14:06 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9916537138f0eec61f9153520603e0af629767a12ecbc25cda59e514d3303dc5`  
		Last Modified: Thu, 13 Jun 2024 18:14:06 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.11.3.1456-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a1ebd20805a4be371d7f6d1b04d9f9c6cd583fe47600a2561fb6f0504cdf4dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7016552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5fa13dd668da72619c73c48c9a2f7075d00f3c0ebf611034e09d72392235b4c`

```dockerfile
```

-	Layers:
	-	`sha256:6fa62b0f104a94a9c9aa1256696f2d38cca283f4bfc4e843bb1cdb8058610a7c`  
		Last Modified: Thu, 13 Jun 2024 18:14:06 GMT  
		Size: 7.0 MB (7000437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55120278ed97c002710fb12b83e88bc03234ca84e49336c4c010ce60708938eb`  
		Last Modified: Thu, 13 Jun 2024 18:14:06 GMT  
		Size: 16.1 KB (16115 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.11.3.1456-bullseye` - linux; arm64 variant v8

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

### `clojure:tools-deps-1.11.3.1456-bullseye` - unknown; unknown

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
