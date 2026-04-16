## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:d8b12fcc533ef0db5e352035f1b5939d9a5821f5a342b7c7b7f1a9b2bcc56998
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9a020df494bb3c53304a22289307a6a00c03b8958ebc9c3d427e98c8ea3187f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153106086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ebb71c7df3ad031cadb5c7fdc5d1f8420420ea5c1f6321a16d3407fe863ff5d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:01:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:01:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:01:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:01:45 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:01:45 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:01:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:01:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:01:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6ccfec3404b33ad5171717a6e6b65d9319928376efa1fce96036c7e2b11d7b`  
		Last Modified: Wed, 15 Apr 2026 22:02:18 GMT  
		Size: 55.2 MB (55170060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381af5240d6e4a66fc35c17c9678bb8940e9f06dea5e1b0b84e685e793a88011`  
		Last Modified: Wed, 15 Apr 2026 22:02:17 GMT  
		Size: 69.7 MB (69699048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967dad97476f85da308b7d9a7b9c58548a8253c2d821db36f4625ee30a65c81a`  
		Last Modified: Wed, 15 Apr 2026 22:02:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d71f84aff0d1636cbec7391210ddca20fdf0793bd0e873fa005f8370869631d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5251402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21056df182cb2c3f84e37df6101034e561e8ee3f3ed37efc5a77d39c038bb21e`

```dockerfile
```

-	Layers:
	-	`sha256:fe21080fb3d4ff691735320d2ded12610728ef4400eadf3cdbfc56dbedc5a985`  
		Last Modified: Wed, 15 Apr 2026 22:02:15 GMT  
		Size: 5.2 MB (5237154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:082a6574e6ca2d12afc1d75fdf8691d4f3d5d95c3f293fc0a05f62eb84907251`  
		Last Modified: Wed, 15 Apr 2026 22:02:14 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ef052700333dda9375035c6ca07f6aea45f1ffc749c2a5c235dbf5bb36ca1ad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152060191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db83b13a323d5cda888607af6b7aa8691c15a72fbad1a88575f6865ad04d58c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:12:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:12:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:12:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:12:49 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:12:49 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:13:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:13:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:13:04 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ed681e68ddbe8c2afd429e099f5fd3705a6888a2522566f48465ee655e150e`  
		Last Modified: Wed, 15 Apr 2026 22:13:21 GMT  
		Size: 54.3 MB (54251620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d9a0abbec20ae736dcbaceb1f5c08a64f6c6e86bf97ac1c6b04e30972e5267`  
		Last Modified: Wed, 15 Apr 2026 22:13:21 GMT  
		Size: 69.7 MB (69691761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3e17a272f4ad3d4a7828be3e5a7f99191d2ea2c527fb865e1608c02d6e62d3`  
		Last Modified: Wed, 15 Apr 2026 22:13:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fc362f530c68c5587f37d0042e9addad06ac40698dffe6ae29094a4b10600ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5257981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3589732c694f6f3441b4d38a37fd4a77131a532adb8ac0769ef3a6bafe2a4e4`

```dockerfile
```

-	Layers:
	-	`sha256:2121d6b228f9aaccdedb958b73b545c29efa024d7323fd82778321c32432624e`  
		Last Modified: Wed, 15 Apr 2026 22:13:19 GMT  
		Size: 5.2 MB (5243615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e7723732bfe4d3379f85d73fdda237ab199348ffae94473e85d3355677202eb`  
		Last Modified: Wed, 15 Apr 2026 22:13:18 GMT  
		Size: 14.4 KB (14366 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:8baad9fc04f6f6c0ea70599431c10ee4382b184a74576071142598510c1ca7ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160262927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0566b978f9cf5da6205b4cffee9a4d6b751fb4f01a67c7604aa5ab185ad7342c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 14:21:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:21:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:21:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:21:25 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 14:21:26 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:25:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 14:25:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 14:25:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef0ca85ab92bd3ffb3fe25036c18fe06d6d124a5859fb5b8e910ab095f07e02`  
		Last Modified: Tue, 07 Apr 2026 14:22:42 GMT  
		Size: 52.7 MB (52650390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a1d234cd617eddd68caad1d3f67215d92766a1937ed15be490730caf73e78e`  
		Last Modified: Tue, 07 Apr 2026 14:26:14 GMT  
		Size: 75.5 MB (75533427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831db49059fd4990e2f5e916699268a78c129c5a90a3835fda01f85d311b99fc`  
		Last Modified: Tue, 07 Apr 2026 14:26:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:565f787eba19850e0e2a4f7a62111c62849f70f5737801c2145a141c1188a076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5257202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0179c67f0235bd33491ceb1f7e3e69f475b1ed3e36746538e23441fbcf60aae2`

```dockerfile
```

-	Layers:
	-	`sha256:9609b75217bdc4411ef2b30912f671e8e8e700f3d7498161975760af8e78ed4e`  
		Last Modified: Tue, 07 Apr 2026 14:26:11 GMT  
		Size: 5.2 MB (5242907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:535dacd8d887ff64eea38bc3e6877a6a9aec51386f693c3ecb3e2342e94daba9`  
		Last Modified: Tue, 07 Apr 2026 14:26:11 GMT  
		Size: 14.3 KB (14295 bytes)  
		MIME: application/vnd.in-toto+json
