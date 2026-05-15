## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:260f4f86d6f2972f35782b7275f29d9d88f81e8630270aabedf9acca6744f483
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:13d06ac84991485107f7d754c161181adfd5cbaa1795756b67e0a751abdb751d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.6 MB (178586864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d468c7679906a75068bdd0ed2f1095ddb009ccd588bc1a2cc4d033c3f902f1f`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Thu, 14 May 2026 23:33:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:33:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:33:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:33:47 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:33:47 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:34:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:34:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:34:00 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6afc8b9d3bbe5994928f69d852ff69236cdc6737f20708a601e43ecb91c2c3`  
		Last Modified: Thu, 14 May 2026 23:34:17 GMT  
		Size: 55.2 MB (55198685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968dbfe8de40dd7c0d999abfbd677b4e82d407916a3d321944f88d8a7a461293`  
		Last Modified: Thu, 14 May 2026 23:34:18 GMT  
		Size: 69.6 MB (69624191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f413e1380e67341e722fc912862e322dd4789b0045400f5cedb22428ed646f5`  
		Last Modified: Thu, 14 May 2026 23:34:15 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7cb41632615a4e98f7db3d4d328d1c62d931b8d553b552a86306995e96dcac06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7542986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e6385f9b1f3057f193ee2f064ed319e28fb74e3fb1cacab51bf8020c2c4bf8`

```dockerfile
```

-	Layers:
	-	`sha256:3f241a614af53817f319f060cde7230c01be8545796e8cfa14e610b4b379eb11`  
		Last Modified: Thu, 14 May 2026 23:34:15 GMT  
		Size: 7.5 MB (7528638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05ac50dd7b4321373db996eabe5a84bfcca06fa7f6f69771a1ba61ec623bf6d7`  
		Last Modified: Thu, 14 May 2026 23:34:14 GMT  
		Size: 14.3 KB (14348 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0882a7e458f4bd367b298c3a3925d76551cedc108e55b84ae52e9a711aaaf910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176291509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b439e016cfcec53bba9e5d4220c3e8333d87ad5671c9254a7a04b37d9e0c8c47`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Thu, 14 May 2026 23:33:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:33:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:33:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:33:35 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:33:35 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:33:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:33:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:33:49 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a831d99cec7e7a42d93411d04540d01e3fc2fb05949a91789a0601cc421daff6`  
		Last Modified: Thu, 14 May 2026 23:34:08 GMT  
		Size: 54.3 MB (54272903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2956163e7e819df12187ca85b24dec09246c353c0cac93dee5d89bb6dd232e43`  
		Last Modified: Thu, 14 May 2026 23:34:08 GMT  
		Size: 69.8 MB (69764748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e802da213e29889c391b85cd224a29aec075ec06d5e583fd1d1f218ff0b60d9`  
		Last Modified: Thu, 14 May 2026 23:34:04 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:738ca93c48fccae856d1ce65e9d9ab2d6793153eb05ba7f191db33f25cd9a0ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7548903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed32d0b0bd738dfd6b49bd9203b92ccefb2a4b4357caf7eb05b6dda04e7c696`

```dockerfile
```

-	Layers:
	-	`sha256:515b2167101cf3ab35de88476cd79fc914df4d33a485d6d71271b2bef4145db7`  
		Last Modified: Thu, 14 May 2026 23:34:05 GMT  
		Size: 7.5 MB (7534437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b45d8d9ff139da70b47cda5da9cf806a500897e86a3a8e48cd2bac1610a9825`  
		Last Modified: Thu, 14 May 2026 23:34:04 GMT  
		Size: 14.5 KB (14466 bytes)  
		MIME: application/vnd.in-toto+json
