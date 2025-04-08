## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:de346a1366628f630f79963136f242fc9576bde053b966c0e71ce2380fd22ed7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5853f86364d3ecd45c3c98c1fd42b8389e910b59a160e2a2ac6847d78129c266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268742917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4027275489792fe7d29cd77cd5420cfb045fd87fd12b72149f7988932651b417`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0d1311d9205ea9032e232c5aa42c6e274a4921fa956aa1f8f71109b6f5ba64`  
		Last Modified: Tue, 08 Apr 2025 01:35:56 GMT  
		Size: 145.6 MB (145598936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776a4771680ba35fd5c9a5553508bc95a59a2ea10de20a26f6a61a542c00ac6b`  
		Last Modified: Tue, 08 Apr 2025 01:35:54 GMT  
		Size: 69.4 MB (69394806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2342dd7339cf22026f10e4225d9b624ca8ee118d7162486741c07d1efff5ae`  
		Last Modified: Tue, 08 Apr 2025 01:35:53 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:13e894609a01174b6e0c4cb1bbb912245b42c6d9642ff4b913e723a5f5850d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7240894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2cd3214b12d589a5fb4e9ac3107c2ecc363da2377827891345329d3fe268777`

```dockerfile
```

-	Layers:
	-	`sha256:462194882a0d7e8b8f76230d4e603f3019e11ac1494093c715cbb336ba3524fd`  
		Last Modified: Tue, 08 Apr 2025 01:35:53 GMT  
		Size: 7.2 MB (7226642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0e07db3c1fb2d2501b27c76833e9856fa6f240b20ff3c204fbf04d44aaac016`  
		Last Modified: Tue, 08 Apr 2025 01:35:53 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1f30be1123ea4494d0c3bde4e9d225da44c33d9467e2a54accdc4ce04c271d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263940177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a403ae04284faed245b7be1b33cdbe055abce62523cdc207f55e344374cafabb`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8057d11a0e36606efc6417a4f1d278ae299d550314ba1d8dd9b79c1df0c19479`  
		Last Modified: Tue, 18 Mar 2025 00:09:12 GMT  
		Size: 142.4 MB (142385423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042e699ed6ea8c59bcd528f8a4853280bca17fb04196362328b6f5ba33cbac81`  
		Last Modified: Tue, 18 Mar 2025 00:09:11 GMT  
		Size: 69.3 MB (69305714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1faf066b9cb64d6e007ba469031c21959835368fdd59757de4fb83a58bc1a390`  
		Last Modified: Tue, 18 Mar 2025 00:09:09 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c33c7c3f0cf542c6adfe92e028bdd21034945fdb5be2f33861cb8ac9243475e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7244783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51334487e4b7f059066ded8d79c933b9c8a111ff0ac7b847b3821d40dff955e0`

```dockerfile
```

-	Layers:
	-	`sha256:a56682995d7267755b160008c3f78b73fd0543727ae8d11acabb019bbd389507`  
		Last Modified: Tue, 18 Mar 2025 00:09:09 GMT  
		Size: 7.2 MB (7230413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ead768d1d03db9346603469229726b88551c49c37ca7f90f09c6d9d034208df`  
		Last Modified: Tue, 18 Mar 2025 00:09:08 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
