## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:d3d103b4ada1c14911c0f8cd52675c141508b333b165e4511c0b930c4b8d1cc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

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

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

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

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:23ad60fd6b4bdb5c0d17b9596ffb463695f1e5bbbcd8717a898ed59206cf8780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (183018411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94af395af4ab1e6dab8be92b8799c1532370f16f0d5d381a990445a0b5ca0932`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd424dd9652860b9ac5f34e9706559ec6cee0a43c4d39d44ec434d36746a7cf3`  
		Last Modified: Wed, 11 Jun 2025 08:05:06 GMT  
		Size: 53.8 MB (53830505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea27430ef61f8f3799146ed8d105be8c445faf30b7cef929928759d9e259860`  
		Last Modified: Fri, 13 Jun 2025 17:54:51 GMT  
		Size: 80.8 MB (80848407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031a883b456769391869c00f56e8aeef93146d754661800fae9a50889a7ae840`  
		Last Modified: Wed, 11 Jun 2025 08:09:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:db7b8414d92880be700cc241767d2a8f96e74831dc57b4e415aaa6c7d69da696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2242abcc54b76a25b19b388c93dc1ffbf4932d73f808361c7359b86017cba4de`

```dockerfile
```

-	Layers:
	-	`sha256:5746c231290372c83bf3791b8dd99f494ad5fe91499a472366717872521d5830`  
		Last Modified: Wed, 11 Jun 2025 09:42:39 GMT  
		Size: 7.5 MB (7494983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c79a9c8c5e4dab3ae45384877a9e5ede12f98644e65e99f121a9929e4265169`  
		Last Modified: Wed, 11 Jun 2025 09:42:40 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; ppc64le

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

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

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
