## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:079fdb5a19b4eb5adce03401b3eb281bada3e13422526579e98e8dbfe62071c1
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

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:282d962518088b61191cf0250333d8cc3cdd64e3b5947ce0771d24e4934c256f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243392349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205276201ee84b1a0c1f61fcbb52a2f411fe5c0c6633fa6e2a6e571a5168ff86`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c24f86009b1c00fc9f9fa3fd2b920c0c4124a0dbb43f02e91fbfb26acc203d`  
		Last Modified: Tue, 03 Jun 2025 13:57:51 GMT  
		Size: 145.6 MB (145635638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697596115d59e583175ebb99846fd85671dea1b71a4b7fa8acc176a01b509f6a`  
		Last Modified: Tue, 03 Jun 2025 13:57:43 GMT  
		Size: 69.5 MB (69530738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdb72589ec9de7ec995b5c8733237fbaa515c2e7fe7e052b46a931f15308440`  
		Last Modified: Tue, 03 Jun 2025 13:57:39 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b1f42be41dd9270d5d25471ccd879087c11a60e9bbe1a6e7b192b2038e5baec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4995948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c09682d92cd489af575a1f52f91a369411f84f518122dc9a225211466ce98ba`

```dockerfile
```

-	Layers:
	-	`sha256:234473c43c8c88c31880d562a72a9bbc033236a9e8a1da6d0840ce9a7c42f5da`  
		Last Modified: Tue, 03 Jun 2025 05:16:02 GMT  
		Size: 5.0 MB (4981639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0e3d4274a14f3ddc360395b83686d85a9bc9b7c0c32ceba642c1b47a960bdc1`  
		Last Modified: Tue, 03 Jun 2025 05:16:02 GMT  
		Size: 14.3 KB (14309 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7a6679f75eb67acd696de500ba995161decb37d64994fda6c6d8325af048fac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239872929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5389d47318b781264113391d75a5ae63fd4ec31b4d25a27d0272009f6204ea6`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fefc44eaff424442f81822836abca91702f398096a9228568e0ead8c9faa1d`  
		Last Modified: Tue, 03 Jun 2025 13:57:49 GMT  
		Size: 142.4 MB (142420640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0914fdb4e479eba5e37f1142d0779efa018dad6c23158ec6cd625218fde44c`  
		Last Modified: Tue, 03 Jun 2025 13:57:45 GMT  
		Size: 69.4 MB (69386366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a9a691ebc7ebf5549e309b69c13fb0557d7186bf12940cdae6b82db6e85e2`  
		Last Modified: Tue, 03 Jun 2025 13:57:41 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3831e8e2bf26685d10bf2e8f86e23a51d8e270cd6ab108f5ac980e0b26dd70a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5002446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6da34104ec8d29f38005804e97512432a1639a57256c0a8a781685cd30a6d66`

```dockerfile
```

-	Layers:
	-	`sha256:f022bafadba95a456af8b25f40778437f04218f911186995bad9d4d6bf06a5a5`  
		Last Modified: Tue, 03 Jun 2025 10:47:18 GMT  
		Size: 5.0 MB (4988018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ab71e747420c70ad807bef28ae943005d627d4b3048fbe49b6255ce87c7d619`  
		Last Modified: Tue, 03 Jun 2025 10:47:18 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d76e531855ae7c14b2e9142036d7e2af659cbeaac758a00e4e0e440f2e3e5974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240225089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc729554e0562b498528c67fbc156862899d043565e8e2ac05c912f9326a16d`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb70de7f1ea6e9e8fa70cca464f19bf365abae7dceabc396212b1df21d889e84`  
		Last Modified: Tue, 03 Jun 2025 08:26:43 GMT  
		Size: 132.8 MB (132810522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66bd504b98f3565ae669ab8846ee7563197d37f65b5cdbf13740cfc6fa7d5b9`  
		Last Modified: Tue, 03 Jun 2025 08:36:48 GMT  
		Size: 75.3 MB (75347011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d666cd7346c4c5d75ea664bccce2b72e06ced315ba11668e8e5d38dab88e3eba`  
		Last Modified: Tue, 03 Jun 2025 08:36:45 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:be80a114ae8e43ef6ea3c8c0016b1b178a9ce82b1dbc495f98d3c40e31b62165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5000540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000f34904dd1bfcfff3bc7c0160721505a1df8632548b5915a19f3ef72b815d6`

```dockerfile
```

-	Layers:
	-	`sha256:9c82b908924c8e24547f0064c8ae021e0874439c2fe5782c943d2121faa9b7d0`  
		Last Modified: Tue, 03 Jun 2025 08:36:45 GMT  
		Size: 5.0 MB (4986182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:594e644fa4fcf3955cc27dc59647c63ea4a8cf370649987e9bafd1023e0be8e8`  
		Last Modified: Tue, 03 Jun 2025 08:36:45 GMT  
		Size: 14.4 KB (14358 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:3fc39073d324666ff1a1500028a25172429d3373aa8c97eaad71e1676b5bebe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220796040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400212baedff5cac98c7853e2bfeda3d90f2079724350946ffac9f170007fbb8`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Tue, 03 Jun 2025 13:31:54 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed11ad230f06796b3ae1c13456129099ee497fa349ff5586d1c755ec5be7b03`  
		Last Modified: Tue, 03 Jun 2025 06:01:19 GMT  
		Size: 125.6 MB (125585354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c3386ab2ff9e61ec2f7500ee78d580935d2b22e775ddae68c0de1ef3d4e009`  
		Last Modified: Tue, 03 Jun 2025 06:07:10 GMT  
		Size: 68.3 MB (68327234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35d929b14f37a205ccd25e2fe735b9d783ec4192fddd58fd8da774db5cacf51`  
		Last Modified: Tue, 03 Jun 2025 06:07:09 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b79d644e244f85ef25ff972fc440a0eb897add95e0a8e21bdb3122d1593684d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4990166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8320447d4e0800eb7aae8b72fa4e51615f6d8b9d90c60ca9646c006f924186d4`

```dockerfile
```

-	Layers:
	-	`sha256:4db509322db2609099ad60347bc23f261804a87582303513020dbfacec4f3b84`  
		Last Modified: Tue, 03 Jun 2025 06:07:09 GMT  
		Size: 5.0 MB (4975856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80d0de48b60a512822aaeeccd7b51e807f7fd743aec2cb9d5f1076bd9714244b`  
		Last Modified: Tue, 03 Jun 2025 06:07:09 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json
