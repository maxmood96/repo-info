## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:bec6b81f24cf41c289fafaaaa217881c8028c7e120635ee8b430e8c441b864f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:008d951140fd45f7cac405ffbc5cbb700ed2eb389197de5367345f192afc174b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234897990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca5f74a700622b472ecc016a8c5e5542fa661a0c5c38c08fa33ba4d692b2193`
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
	-	`sha256:3d79ccbe0210f4986821cddffc5c7fc6551d938e282044db7571e448bde1e24a`  
		Last Modified: Tue, 10 Jun 2025 23:27:03 GMT  
		Size: 30.3 MB (30256064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87c7bdb7e8b876875776c6cd5af421655cf64d94f67c2b384a437c61ae5fe2e`  
		Last Modified: Tue, 10 Jun 2025 23:51:19 GMT  
		Size: 145.6 MB (145635640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ec7744c34529ab99e7f0942cc13698f3f87f716387760d552f53916bacbb6a`  
		Last Modified: Tue, 10 Jun 2025 23:51:45 GMT  
		Size: 59.0 MB (59005640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7eeb140bbdfdec76010466779738243ce5df35db68333a0eaa152b2977854c`  
		Last Modified: Tue, 10 Jun 2025 23:51:41 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:455f062a7de6a1563cb9ed289efecafaad87fa60a6942bbcd7735dd27d2c3103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5342489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ca6c8e775170b15e478c6d7870f5a3926a93c99c9312b24f564ec5cea22a6a`

```dockerfile
```

-	Layers:
	-	`sha256:f367814007bba53ec85cc8f34612716d3e17464b11b2bef8ba89c1c249988adb`  
		Last Modified: Wed, 11 Jun 2025 03:35:16 GMT  
		Size: 5.3 MB (5328179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e6af7066675d4396674b0e19307b9570125681ae38a4a8ea67ceb28521c232d`  
		Last Modified: Wed, 11 Jun 2025 03:35:17 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c7fb3de216d9e0d695d0801af71adc1e58ea94ab3bb4ffb2926da7a41b0d4113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230305113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ad8b87ad14a735dbe1f0af14cb54381726962d911dafe28bbbcc82046eb55b`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192c7e75dcf364b2ceee07e82338697627a9716867e83933b2f790e9d0962da2`  
		Last Modified: Tue, 03 Jun 2025 13:34:30 GMT  
		Size: 142.4 MB (142420666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03568ce2f109909a948acb2f0c66270b88e149bfeb70e4d4399af6d4c2226352`  
		Last Modified: Mon, 09 Jun 2025 19:55:01 GMT  
		Size: 59.1 MB (59137546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c71fc32bfd29bc6be295994a0d8786b36f93ad0a31b943f9c68f4cc5fde8d49`  
		Last Modified: Mon, 09 Jun 2025 17:49:08 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bb241784e13f9fa854afa97f396489ffabd7e8aeac0e6fa62a521f7cb6c37395
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5350581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c4845e6bda11816fa44ebd48900667867e72817a968a9f5f394bf53ee8bd23`

```dockerfile
```

-	Layers:
	-	`sha256:ca8f2cf408568bbee1e34f7d3cea93b17c1a746a0b5e00ec193bd7c5c3b2cc57`  
		Last Modified: Mon, 09 Jun 2025 18:35:22 GMT  
		Size: 5.3 MB (5336153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fedf5281fb2191a2ec3d1d391d444d368a0f4ff38bf52ef46e95effb9fef3799`  
		Last Modified: Mon, 09 Jun 2025 18:35:23 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
