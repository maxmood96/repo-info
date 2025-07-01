## `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm`

```console
$ docker pull clojure@sha256:1023dc7abb066c97f9113bbace8214d601912380684d7ed171980202068049f2
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
$ docker pull clojure@sha256:ef0ee2aca689050b4132e161659fbb9ca76d37a4be5507da49ba60579ee44f61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184204219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afda7e5cf6ecf96b9adf9831acedefa14ba1c94d3631ad8023e3b8defdb9c0a`
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
	-	`sha256:0562cd9be3a9c7e8adabb849f4121515e2b212a5c8b7bb57f0e9e2357357f8ae`  
		Last Modified: Tue, 01 Jul 2025 02:37:34 GMT  
		Size: 54.7 MB (54716160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d253fa79654441154a797152af3f9b1faaf6738c960847db360052b1661bfe`  
		Last Modified: Tue, 01 Jul 2025 02:37:28 GMT  
		Size: 81.0 MB (80993130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bab05d7ee0f768c996318eb19ffda14baba85808f15d1a8c94b64573f022ab`  
		Last Modified: Tue, 01 Jul 2025 02:37:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:03879457d637274999b24740a3b68a183bfa50b6cff3994bcd199cff3af89775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7504115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:161eea731ac64240e92d211425658c15e3c4802347c94a5eeaabd8f9ba9c6b19`

```dockerfile
```

-	Layers:
	-	`sha256:a137e92cb3eedfdcc06d141916a885247511ce9028f28e71eb374d1740d00ecf`  
		Last Modified: Tue, 01 Jul 2025 06:42:10 GMT  
		Size: 7.5 MB (7489878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d12aa082e8d3021c1611a17422fe6546d4e7c27d03406ef2cb3a87aba9c7ede5`  
		Last Modified: Tue, 01 Jul 2025 06:42:10 GMT  
		Size: 14.2 KB (14237 bytes)  
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
