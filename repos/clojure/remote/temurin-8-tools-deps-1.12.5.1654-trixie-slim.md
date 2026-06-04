## `clojure:temurin-8-tools-deps-1.12.5.1654-trixie-slim`

```console
$ docker pull clojure@sha256:984790fe73daac4b9abc7990dd0c861257c0c54b7997c10c841ae3238042432b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.5.1654-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bcf4acdcbd72e663011ee870e7ac2cb4705ee4879072755646aa31bb037ae161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.9 MB (153931387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a96be8f8917400b6ffed0297c2b968ac691a485351f79a2ff4fbd266c52c83a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:42:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:42:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:42:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:42:42 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:42:42 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:43:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:43:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:43:01 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d908f9b8750b71e440514e9a187edd6063f939f28453b0517640f9d6a348ae50`  
		Last Modified: Thu, 04 Jun 2026 17:43:19 GMT  
		Size: 55.2 MB (55198698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d952ea7f84def48592eccb50dc263dd99c060856eac1674ccf62c15ad27a3566`  
		Last Modified: Thu, 04 Jun 2026 17:43:20 GMT  
		Size: 69.0 MB (68952120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1919a312dc4e5e7cfb7902668a649f50904f38ac8e4520d87e53d7f0a749af`  
		Last Modified: Thu, 04 Jun 2026 17:43:17 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:726a35ef2e7c4cc339a6247b1530660f0dcbd2869676baae06cb1bcb7c599685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:566d284fdb3db547bc0bc7d82c8f89726b3add33c52d7a07bf63c6cab717895b`

```dockerfile
```

-	Layers:
	-	`sha256:ad5c925dba77409b2c61148d7b6301a4e126367de355454e057103942eba99f8`  
		Last Modified: Thu, 04 Jun 2026 17:43:17 GMT  
		Size: 5.4 MB (5377602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:380f6ff592506462425984a2c7da62366aa36370cacddcacbd261d700b82a310`  
		Last Modified: Thu, 04 Jun 2026 17:43:17 GMT  
		Size: 14.4 KB (14382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.5.1654-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:739bfb00d7e2fe9788ca8c1411ef6e3fb264e207ebdf18bf52c21b78d91f4cf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.2 MB (153192832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f747ac6aec413def88f81d697a4e406eef5b00fd813986f5654b1ad0aee52e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:42:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:42:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:42:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:42:38 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:42:38 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:42:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:42:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:42:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f7bb5ccaae3c473d47646aa3e01234f0eb668dd388de53a020dcb6e1455f1a`  
		Last Modified: Thu, 04 Jun 2026 17:43:12 GMT  
		Size: 54.3 MB (54272936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e027437dd7e1d375ae689165a872626d447fe6b6adba84b12da5db89927dc10`  
		Last Modified: Thu, 04 Jun 2026 17:43:12 GMT  
		Size: 68.8 MB (68777333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373dc21e3930e2c2d3ccc380200fdc102210a20ca94ae438585097c940f15e32`  
		Last Modified: Thu, 04 Jun 2026 17:43:10 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ca3a828fcf08022dcb202c5790b1a7279542015ef7480e5fdd6e0ac9edc627ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b23d94a3aeb71716f0bfa885056e603fd8b56f7e3e96412d43db9d2d4fa97e6`

```dockerfile
```

-	Layers:
	-	`sha256:11119bc5adbd8f9b7847c45e3394393eb6914d74cf1c08ab21ae254afce7224e`  
		Last Modified: Thu, 04 Jun 2026 17:43:10 GMT  
		Size: 5.4 MB (5384063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb1c8a8c6be925477e3fc9bcd67a98e83e2eb9c125afa3b290d11c9374c72162`  
		Last Modified: Thu, 04 Jun 2026 17:43:09 GMT  
		Size: 14.5 KB (14500 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.5.1654-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:3ed3c23397ec1909bde667891acd31f75b89766ce3747189bf6fc0337a13a7d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160639350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609a0f7feb19dc5ef7e9c0e441152cd2e6b255673e394f186471657b97c1160c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:45:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:45:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:45:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:45:56 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:45:56 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:46:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:46:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:46:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7961f98cc972c19f52c3da7f9574fdbd686cce1a2ba4e6c10d8ccc0f8c2c5c`  
		Last Modified: Thu, 04 Jun 2026 17:47:34 GMT  
		Size: 52.7 MB (52669122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fb51d82d4f82f7c9b0cb2393b13b569b19effd49b6f8cfaf7cafebd6330c22`  
		Last Modified: Thu, 04 Jun 2026 17:47:34 GMT  
		Size: 74.4 MB (74369128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d615f2c88d65683aef13b230568eec639f487e8f0e3647d8a02db789d7703d19`  
		Last Modified: Thu, 04 Jun 2026 17:47:31 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1654-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:24ff5af648ad466f0663fb4cd90290b3cc63f9dd08900e5284e0631c99e67361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3760cbff6c8e9f378f5a8b94ced1b246ddf750d26f21c45511170440fd667a3`

```dockerfile
```

-	Layers:
	-	`sha256:1838536e4d318280af607eda166a3d14956e7a460ee5f3d50a409f053ad3656e`  
		Last Modified: Thu, 04 Jun 2026 17:47:32 GMT  
		Size: 5.4 MB (5382568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e3902f501ad845d13568cbceb6458daa325a82b4c949bcf1d3f5c39def83191`  
		Last Modified: Thu, 04 Jun 2026 17:47:31 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json
