## `clojure:temurin-8-tools-deps-1.12.1.1550-bullseye`

```console
$ docker pull clojure@sha256:fffa5036c03fd0310f17360beba7b62f099950c04eed541de413ef53dd10f919
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
		Last Modified: Tue, 10 Jun 2025 23:49:45 GMT  
		Size: 69.4 MB (69409667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c3f896cea68ec6e0b35178a5276ec4e25a253d6c834dbdfb2e31e57e14aa85`  
		Last Modified: Tue, 10 Jun 2025 23:49:44 GMT  
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
$ docker pull clojure@sha256:4556378b3a5e4f45def9261fbed36ce2d23b63cc18e09cc7da9965bd473522c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175616363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde8eb3f0410be535f2fe81e98bec5ea1f3f422fc0adb46c86230ea694fd7daf`
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
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a5f701bfcb264810d9aa404e8040ce22b5b531c7f91508b60b5eea297f126c`  
		Last Modified: Tue, 03 Jun 2025 19:23:56 GMT  
		Size: 53.8 MB (53830516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090c55703a7acf2da976196d1d00d9f336c73c6c557c54596e96df6458c41ffa`  
		Last Modified: Mon, 09 Jun 2025 17:33:35 GMT  
		Size: 69.5 MB (69537447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ca4592240c3bfb0c86c06450829e97987d219df503221fe0af542023aa6f92`  
		Last Modified: Mon, 09 Jun 2025 17:33:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:01ac98b360d0c9b43d8ca854aa34e553a74459e1d11655ec89ba57de04b3f279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7539022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec740e690fd1c73fb6d27259d5db2656b0430e9630e8b37d298818d9a7944949`

```dockerfile
```

-	Layers:
	-	`sha256:5f65a78ad283564dd5dcf4b70cb0d3e5a14a17c1e1e3ff5996f9740608d6cb15`  
		Last Modified: Mon, 09 Jun 2025 18:42:51 GMT  
		Size: 7.5 MB (7524669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8818598b7df5a32f9cbb2b6fba687625e9aa0ddbd8fbf3a9787b41b862ee6f0d`  
		Last Modified: Mon, 09 Jun 2025 18:42:52 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json
