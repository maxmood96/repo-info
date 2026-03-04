## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:e09d7cf690afef1171d8a0331e6e099630e3903fe301570c6fbfc5c21679986f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:2401a1bfe0366c8d66af23dbd1db8f432b6580384d04f8043e2d4616c0613da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269150956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c3a3a4228f0c9984f1719c75ee595d4f29becfd52a10c4eb774071ab9566b1`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Wed, 04 Mar 2026 17:49:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:49:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:49:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:49:30 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:49:30 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:49:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:49:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:49:45 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1ac153b958b527dcacd516376216a8bb7fff34875d03d8808c3be1b75c8be6`  
		Last Modified: Wed, 04 Mar 2026 17:50:10 GMT  
		Size: 145.8 MB (145806748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0516ebace6b46047074f496b6d8f4ed4ac1a693e2dd8b29da34468a09f11a2be`  
		Last Modified: Wed, 04 Mar 2026 17:50:08 GMT  
		Size: 69.6 MB (69587131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a188005a80e3c71bde04b19a286ef9599f55d1158119d277b45fb935ae9af217`  
		Last Modified: Wed, 04 Mar 2026 17:50:04 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f96e0cca9a07ee925900f589926f1211c69a2e2654e9f9c73d44f6daaef175c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7443626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c6e366463b188e543e1fe175226bbb184b99fc292c29f7259d9ac7161bf9b1`

```dockerfile
```

-	Layers:
	-	`sha256:c58c0f2cf8b6cde11ee09c03e0d506b41506b1eecf9f2277a3e81e263ae982d5`  
		Last Modified: Wed, 04 Mar 2026 17:50:04 GMT  
		Size: 7.4 MB (7429418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ff5befc452e5545e5adda200968dd80a505a73083ba334734a273aa5e803c68`  
		Last Modified: Wed, 04 Mar 2026 17:50:04 GMT  
		Size: 14.2 KB (14208 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:17fac03cf95f24ece96138419c750aae3b65d845fc91462c811338eaada2afba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264488877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:977790e003e0c1e0e693d8405ba5d33d3f84fcc8bf71ffca7bacf4230b405c21`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Wed, 04 Mar 2026 17:48:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 17:48:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 17:48:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 17:48:58 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 17:48:58 GMT
WORKDIR /tmp
# Wed, 04 Mar 2026 17:49:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 04 Mar 2026 17:49:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 04 Mar 2026 17:49:15 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0509053f2cf8072309184287dd2fd397e589dc5db17a1ddc469001be80ea07a3`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 52.3 MB (52258392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15808364fec276ea2221e9aff6b766c1faf537f97992c562c67036637fa1d0ae`  
		Last Modified: Wed, 04 Mar 2026 17:49:35 GMT  
		Size: 142.5 MB (142501433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb93e680134fa1c0f9172def08e97e90cc6ea83dc2db12bde9a7dd70e7d8e023`  
		Last Modified: Wed, 04 Mar 2026 17:49:36 GMT  
		Size: 69.7 MB (69728410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae911a2bff6ab1c7600a169f05781de216b3767031c5c0bf2d61c27c5351e06`  
		Last Modified: Wed, 04 Mar 2026 17:49:33 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:23385352300e26893d13726036f2e8a02e294c54b15583d7d0f11511bccb66f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7449462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9918d16a3b9589bac6387fa6a8fc20bf3f9ea1e686a6b38a55737a5303b23d4c`

```dockerfile
```

-	Layers:
	-	`sha256:be604fd3f88c0ead5b27755b94715cdb377e0c53dfe382582759cb2eb886e67c`  
		Last Modified: Wed, 04 Mar 2026 17:49:34 GMT  
		Size: 7.4 MB (7435135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01179e8ab4845f6acb734f2e55d1960acf33f234825915cff3bec832cd363575`  
		Last Modified: Wed, 04 Mar 2026 17:49:33 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json
