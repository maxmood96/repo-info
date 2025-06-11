## `clojure:temurin-8-tools-deps-1.12.1.1550-bullseye`

```console
$ docker pull clojure@sha256:ab21710b078e18e331e648100aea492ad15e1db0bcab6d1f537adb8126904e83
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.1.1550-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:30b5f8c5e915092df816609ee3245387cebb560828c7bcc0b35fa62dd151175e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177881272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e198c834eda05d0dae51caee3f62729e2521a206962a2560f29404ef56143a`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe88922a6e5316132d246aad209d9c4862c0c30eec6ea69f4fdb29ea10e88c2`  
		Last Modified: Tue, 10 Jun 2025 23:50:19 GMT  
		Size: 54.7 MB (54716179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21155e01d7e23be133adb7c3b10125d0616b124d6061cd09a66db60e3bea3eed`  
		Last Modified: Wed, 11 Jun 2025 18:03:08 GMT  
		Size: 69.4 MB (69409667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c3f896cea68ec6e0b35178a5276ec4e25a253d6c834dbdfb2e31e57e14aa85`  
		Last Modified: Wed, 11 Jun 2025 18:03:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0bd2aa21bd32d4b03ebde08205fe24e3ac486efc449b82f1422ea91124c05093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7531485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b804e97caf2161571f99b935c7e026c85a2ff92a4d5569938c7025d261efdd4b`

```dockerfile
```

-	Layers:
	-	`sha256:198bfecdfe5255c2773ec32a65af7144cb8d40d499141e5ad764400a792e95fe`  
		Last Modified: Wed, 11 Jun 2025 03:41:30 GMT  
		Size: 7.5 MB (7517248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b95eb902940e30b3d27d5cea2216df2d62d1d5df27e0b9c673827837ee84aacc`  
		Last Modified: Wed, 11 Jun 2025 03:41:31 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.1.1550-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4d9aa5d509842a5853f1a9abcbe785fb2ca6b42b84c6e81de5ae166a7d770cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175621134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441d939cfd1ef09e127c25a770725d6cae121b6ec4ef5a34b3c75bb382574b2c`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
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
	-	`sha256:01b9f05048bbb73f25cf8fdb677f6390611ed20f4945645387ddce6122b5075e`  
		Last Modified: Tue, 10 Jun 2025 22:49:07 GMT  
		Size: 52.3 MB (52252301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9238fa77c1cf7d3726bdf1176f1785a2d438aba2d438256170e1fb235ca805`  
		Last Modified: Wed, 11 Jun 2025 08:06:35 GMT  
		Size: 53.8 MB (53830497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79fb1f0cc142254ddba390d7bd8aab22f1e7102c732bc28b725c26dc9f097a6d`  
		Last Modified: Wed, 11 Jun 2025 08:10:36 GMT  
		Size: 69.5 MB (69537691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3785b1b59048255677bd454ab40fb31e1d8a698fabaa5585b0af390591fa28`  
		Last Modified: Wed, 11 Jun 2025 08:10:34 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bc6c68fcdb3f23dc94c11e6aac712d033e684249de31c43f46d4a873abff0f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7537400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb843c83f4d23bd992ed36a9920d142fed5a9062cd74afc0d33f1b4ac1d77f2`

```dockerfile
```

-	Layers:
	-	`sha256:6d29631dbe948b17f89af07d0111f494bb0cd25d53c91b46ebdb0af995978cfc`  
		Last Modified: Wed, 11 Jun 2025 09:42:50 GMT  
		Size: 7.5 MB (7523045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aa0c5e2de2e2d12ab657e0eab09b2bed308ba9a95a324e563c281d5bea6a3aa`  
		Last Modified: Wed, 11 Jun 2025 09:42:51 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
