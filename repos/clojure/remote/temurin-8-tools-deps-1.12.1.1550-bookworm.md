## `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm`

```console
$ docker pull clojure@sha256:205d19d8eea18ba57dc0cd9f7225b83a04589185028715aa64f92221006f7e47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:93038409acbc2fca2bbc4a4adec3e6ca0c1d0d378e595c008e3ab03f4888dc51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184204090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965ba19a71dc64d4e3d7462729cdeefe49f78b44166827ec3a9edccd93b4cee8`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c32239774341a019c02247fc1d1b12148b23ab0de67d3646f332b880fb9cf1`  
		Last Modified: Wed, 02 Jul 2025 04:15:56 GMT  
		Size: 54.7 MB (54716198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67a3f1ab8d00c4f4982129ddd608e5bad6f641538af2e44d28973f311021ca0`  
		Last Modified: Wed, 02 Jul 2025 04:15:57 GMT  
		Size: 81.0 MB (80992964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d3661b4ece01d9d674b26693eba5a795d37e372a322efb058dd5502605eee9`  
		Last Modified: Wed, 02 Jul 2025 06:12:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7663f4bbffc6b729d36f85103497ec7ad64b7cf5de6d7cc1a371b189a57aaaef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7504113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5da904ba5346a7b39e9c0074fdfe3d4d9fe9f732fd3d2519176b3a31b9ff011`

```dockerfile
```

-	Layers:
	-	`sha256:a8266c27c0ecf802ec941bc0707cff532a69cd89407e68f8d342edc9deac788a`  
		Last Modified: Wed, 02 Jul 2025 06:42:52 GMT  
		Size: 7.5 MB (7489878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2336a9b0d43ba170fbcac1cf3b852d6e6a86a5496e8d037bd9645d44d37b3ea6`  
		Last Modified: Wed, 02 Jul 2025 06:42:53 GMT  
		Size: 14.2 KB (14235 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e1be96d824f267f42c41dc081251b8ee69011ab921941898f79f2d3345b49cd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (183021787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621484e683fa2bacdbbae13cf4015bc0beaa7f57040e72a3199009db1a8651c1`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cbe0c83e5331d1922a8e4dc226e292346021b1558e9d501823f8a7466a9420`  
		Last Modified: Tue, 01 Jul 2025 11:56:04 GMT  
		Size: 53.8 MB (53830517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4827f7cc7adfb9a7f1473bebbf8e79b46669543ba23f746d9d1bb1f77e2482b3`  
		Last Modified: Tue, 01 Jul 2025 12:01:05 GMT  
		Size: 80.9 MB (80851842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9dacd084f76ec1728e55f99598c447f96d1a102788aac2baf3676d44b15e42`  
		Last Modified: Tue, 01 Jul 2025 12:00:59 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:603aa1867a2b6254c4ba37ec7fda7c30ae3835bb1d213a6219c14a4d80145c41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7510693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2869c4e880ddfa572aba8feeed7e1f6a153ef9251164e278ab40c3db6e0a5c14`

```dockerfile
```

-	Layers:
	-	`sha256:6ab85a356c76b6c2f75a617381cfedfbff39a1d908f2e198b84465be8019b829`  
		Last Modified: Tue, 01 Jul 2025 12:38:42 GMT  
		Size: 7.5 MB (7496339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4ee2878e0de7312e86bdf219fe83971efaf70cccbc78f0aa3dd4b7d10d7e9cf`  
		Last Modified: Tue, 01 Jul 2025 12:38:43 GMT  
		Size: 14.4 KB (14354 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:a549dc2a8173c01ec8cb9af87ff636d9385d014929589f1bb37cde4ad57100e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191325352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a79baa528bc457eb2562a31fd2f46a275020fee83ed0cb1c455bd69ec4a988`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2819217d87219cbf8b5ec7dfbc47c9a16195c7992a9fbe92da8723c42180b19b`  
		Last Modified: Tue, 01 Jul 2025 01:15:05 GMT  
		Size: 52.3 MB (52337243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74216f9848d7f720b6d1a7879adf3f154610cf3f35739e365719835880e26321`  
		Last Modified: Tue, 01 Jul 2025 08:14:56 GMT  
		Size: 52.2 MB (52167968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24cb329ff04af5e276afb299e398cebd9e5d1d80d0e9aeb07fe430429255976`  
		Last Modified: Tue, 01 Jul 2025 08:22:05 GMT  
		Size: 86.8 MB (86819498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d77d50daaa5401460cefe43d4b7b77b0aa63b7b4b4943ba2707763050b7dba4`  
		Last Modified: Tue, 01 Jul 2025 08:21:59 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ddac287d3844c4170b30d90a441783531b4e1ab007400854d64df1917241bd95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870c4bec24d1f28d9a649c9772a7d4b45f101d33978ea0f2812004d6fda5c556`

```dockerfile
```

-	Layers:
	-	`sha256:a1274b3e4999983e7a85707467a8e9835c4d8ddee23f96ee584e26351482404f`  
		Last Modified: Tue, 01 Jul 2025 09:42:01 GMT  
		Size: 7.5 MB (7495675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11480450234479369ba250306b36ea62cf9db47680a223ed734fcd9730f1870c`  
		Last Modified: Tue, 01 Jul 2025 09:42:01 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json
