## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:c22d824c582f1032226640a53f83a3d620d5ab162680f1ef6fb3da47ac1acc8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:b4cdd8441d32c3adef018e4b75e8c83696d825ec433dccf2b7182e890dc22245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272513984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c29907a144f39f1ba5d3c7c9e1ae24de7a93ab7562f818186bc61daffc192d`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:16:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:16:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:16:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:16:13 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:16:13 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:16:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:16:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:16:27 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:425befdf76e52426879d2abe42093a00dca59a893e7b4fa2a7679b0180b71d4b`  
		Last Modified: Wed, 24 Jun 2026 00:27:40 GMT  
		Size: 48.5 MB (48502210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6e04094059a6e9a7424d56f4bf26e07a2b3de3a9e1397684c36bd3a0071756`  
		Last Modified: Wed, 24 Jun 2026 02:16:50 GMT  
		Size: 145.9 MB (145886179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3d19878bc0da425e6bc645a5971f2a89939c7584540d92e6ac80ec3802b57f`  
		Last Modified: Wed, 24 Jun 2026 02:16:49 GMT  
		Size: 78.1 MB (78124949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe9bd90ce83d899d5ee51f74b9350559c30a0cd97e65f9ce2b34e854221185f`  
		Last Modified: Wed, 24 Jun 2026 02:16:46 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:57cb9044da04654d817a720ef3c86e2e48d207edb1f444f125b4d815e6c17304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7410013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f01d9ba538bf997963384d4c44ea8d9a9f03e6c44867d74a41aba3e38b8f6f`

```dockerfile
```

-	Layers:
	-	`sha256:05f667dcf596a25b702528877e1f48829a2bc17d87cbda6c96469e1326563754`  
		Last Modified: Wed, 24 Jun 2026 02:16:46 GMT  
		Size: 7.4 MB (7395650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c999bf49487757006b3c43b313edead1eabe6809eb595a22b88bc557fa9198e`  
		Last Modified: Wed, 24 Jun 2026 02:16:45 GMT  
		Size: 14.4 KB (14363 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e290451720d90638f0e734b68f07132c3bc2e88656280c54f3c70004fbe9439a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269101548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7666fff61664842b2fd8f0e6e7947acc37a408dc1cbd6ad0bab15d1d8783375`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:22:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:22:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:22:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:22:51 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:22:51 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:23:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:23:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:23:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0fb1189398e2e4b474d43aac6502510d0da0318e70137a377c21087f198814db`  
		Last Modified: Wed, 24 Jun 2026 00:27:19 GMT  
		Size: 48.4 MB (48389201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d48cf59b42435d555435bd35ed2a5ccea5ecd106b0adb7c2604fb04721f70b`  
		Last Modified: Wed, 24 Jun 2026 02:23:29 GMT  
		Size: 142.6 MB (142582131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e8103d4b3fe770e52824ed096b6c35ee0bf3431aee272e76d1f6d264fd5b59`  
		Last Modified: Wed, 24 Jun 2026 02:23:28 GMT  
		Size: 78.1 MB (78129570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4815f6738b0ce5a0cde06d825e49cf845bd44186b0ef743f7fed5ad2fc128f`  
		Last Modified: Wed, 24 Jun 2026 02:23:25 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:975858433711fc7070017de45bc86feba530ef1b34dad3ce1cb9841edb948b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c374dbe6b7447ea683aaafadb6b7e45642f2abb05ea146012e1d70501dcdb8`

```dockerfile
```

-	Layers:
	-	`sha256:4b526c27c7a1f6dafc2c81debbf4056742b2125cf2acd0ff913689be43d8f859`  
		Last Modified: Wed, 24 Jun 2026 02:23:25 GMT  
		Size: 7.4 MB (7402031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b635c5de0f4307ea363c0fba76a0c26844642632c0f472aaed199209b9bb1be0`  
		Last Modified: Wed, 24 Jun 2026 02:23:25 GMT  
		Size: 14.5 KB (14481 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:7da3810917e8b3b3d7a66c3b22bf6d2fdb4929bc3c32cb81ce104dc5abb346e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269416838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d44d464b0ec20fb3e6e1d68f92c3e1775dd70b5abf34e2af66d81211e153b7`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 07:51:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 07:51:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 07:51:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:51:40 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 07:51:40 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 07:58:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 07:58:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 07:58:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:55b0e891f4e8dc14bf4bc7e853254fcf1f3ba5a8e8e3c07c21e7dd5bd6d87882`  
		Last Modified: Wed, 24 Jun 2026 00:27:34 GMT  
		Size: 52.3 MB (52346847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6f7e0af16b59b2185aa4fe22c4b220132f777573b7d58787df69c823a158ec`  
		Last Modified: Wed, 24 Jun 2026 07:54:27 GMT  
		Size: 133.1 MB (133110623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41327a8f94461aa74b0d85ffd065e748a1a0b82864cd0ff165e12b47c0acd6e0`  
		Last Modified: Wed, 24 Jun 2026 07:59:25 GMT  
		Size: 84.0 MB (83958725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf5b89a52c3d470a123c4fad83a9c8c0964816870e2caf50236262ec90ef9aa`  
		Last Modified: Wed, 24 Jun 2026 07:59:22 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4f3d433a9f98151bcc61f1fccb4bf5d75c7afc8a362550d5d187f5bacab27387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7414662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782c83030afca9f104ee73114b91866d6f1852a18b3879d851613e143f0a361d`

```dockerfile
```

-	Layers:
	-	`sha256:537788cb2b234c748d7df97fbb59b34facb9aae57661eb13e0bb90ab16b01721`  
		Last Modified: Wed, 24 Jun 2026 07:59:23 GMT  
		Size: 7.4 MB (7400251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30a6e2cd83b2132a54d976fb3754a9fb790db8fbca4d2478328bda3a65683de2`  
		Last Modified: Wed, 24 Jun 2026 07:59:22 GMT  
		Size: 14.4 KB (14411 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:f1a99f0544fcd8490a99e1fe6824824eda3aea5c34ad3cb648a25caaaf32b877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.7 MB (250744273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99c32be7f02b067e82df34d4b91b4637eaf375ab9700315c3c0806ba04c9fa92`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:07:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:07:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:07:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:07:54 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 04:07:54 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:10:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 04:10:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 04:10:04 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:bdd2e9d83d68023204331dd445067114dbd3500d2d496368624fa7ef81743d4a`  
		Last Modified: Wed, 24 Jun 2026 00:27:09 GMT  
		Size: 47.2 MB (47161675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894f0ce15fa11bb3c6ca37e7d0ec532b71cf5687d8bdbe22e95582d18a8c14f2`  
		Last Modified: Wed, 24 Jun 2026 04:09:28 GMT  
		Size: 126.7 MB (126652580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff96b5ca2da5328a94f232b3161280a9517346737a6a208018e682c31bfe4402`  
		Last Modified: Wed, 24 Jun 2026 04:10:31 GMT  
		Size: 76.9 MB (76929374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55e87f0c98f9392007bda5522a86e613ad5bd65884e4b83cec2ce7420508712`  
		Last Modified: Wed, 24 Jun 2026 04:10:29 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:365937c30578238bf05fedc908ec96b1d1e3e04ed4f4d897ae5a8105eae91c89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3ebb34a9c181f5629b9eb5185175456296e7e41758ecb25d5abc03724c672a`

```dockerfile
```

-	Layers:
	-	`sha256:dcf45b3b48a01682a5b376879e1b535626530004e38d03b7c5ec1028f4ae8d9f`  
		Last Modified: Wed, 24 Jun 2026 04:10:29 GMT  
		Size: 7.4 MB (7386973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:924333b6f0fd3a0a428c2bbba2a10fd59907859c0ef6676d1b2ad4409114f1ca`  
		Last Modified: Wed, 24 Jun 2026 04:10:29 GMT  
		Size: 13.4 KB (13408 bytes)  
		MIME: application/vnd.in-toto+json
