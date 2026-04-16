## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:88331c651bde96efe3619e318c6db6770003252d31182818988b1cc40a7cec83
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
$ docker pull clojure@sha256:e30018fbdba3c26c676e25d30bf8afe3c8ad8d0597f2e07bf697a06a3f0424d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160259273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d9fb84a8e6d7d6b6b47639e501cf0e78e751f6622a681c95b0c92aee0643f4`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 02:31:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:31:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:31:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:31:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 02:31:40 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:35:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 02:35:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 02:35:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca09ab2f7ae5f0a2c569e6862baef7188079f93d19533ec83941e939b63131e`  
		Last Modified: Thu, 16 Apr 2026 02:32:47 GMT  
		Size: 52.7 MB (52650382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920c130019a3cce2cf5187302cd0102edb21e6071d3c123eb8915f188bdee2ed`  
		Last Modified: Thu, 16 Apr 2026 02:36:27 GMT  
		Size: 75.5 MB (75529781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b3378a4fd945a07400d62324ad5385d9df936b11841ae0e8fe4c4d9160fa3f`  
		Last Modified: Thu, 16 Apr 2026 02:36:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d5e3bcaf3034ddde9ab1793165081e5af87a893418f208bc43c5973ee54ff2f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5257203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c763f924b74cb4184ff96b5c90ffe722bca3c228e054639cef94cc18fb8a98b`

```dockerfile
```

-	Layers:
	-	`sha256:384532cb4d0be5afedad9797b33cb068db7c9cd14ad694a41322b24e82dab057`  
		Last Modified: Thu, 16 Apr 2026 02:36:25 GMT  
		Size: 5.2 MB (5242907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45ceac58de47a2e3a0bb1a7d46607bc03ba0b2273b2488dbef4f07a64db98986`  
		Last Modified: Thu, 16 Apr 2026 02:36:24 GMT  
		Size: 14.3 KB (14296 bytes)  
		MIME: application/vnd.in-toto+json
