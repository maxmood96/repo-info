## `clojure:temurin-11-trixie-slim`

```console
$ docker pull clojure@sha256:5a63321a29aa4f7f481a2e2ed4dda7e342912c2f0a5e624a6844c7fbb65fe539
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

### `clojure:temurin-11-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a43a97402513799701812e533faf965dba824140cbc95f15fbb875e4faf6ad18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247414794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1779269778204d45174f94141021bfacf69d42bed0d8b9f446b0d33b41fb9653`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42043324336a4cd74b981eb601b25044ba266a9641951f2496c19516721ee86`  
		Last Modified: Tue, 02 Sep 2025 00:17:37 GMT  
		Size: 145.7 MB (145658226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa96266bf3921366ddfd59cd9f8be844acf059295be2c3148f0a61e5cede938`  
		Last Modified: Tue, 02 Sep 2025 01:54:10 GMT  
		Size: 72.0 MB (71982636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b6b4c1d9a64f3d22ba9e02d6d9452c2b015152717877d93fe8c21c9fe35948`  
		Last Modified: Tue, 02 Sep 2025 01:54:02 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e59ceb363e4c74f9f9545e6853c373dc74d2cbcc49e57c334042582897184d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fca4db188be459a53ed867920c34ed943cdac98b313c8c675b3abaa472de2b`

```dockerfile
```

-	Layers:
	-	`sha256:aeddd19b66d32329663ad03d24f1d1f9b79dc72b8f940ee125066a826a90a9dd`  
		Last Modified: Tue, 02 Sep 2025 03:37:35 GMT  
		Size: 5.3 MB (5275378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d183769baf4edb996fe0b00bb4bcdefeb9cb51edfb4a6b66987b0df0758b0ac9`  
		Last Modified: Tue, 02 Sep 2025 03:37:36 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ba662089d24a8da9407f67320329ef69f824a265c9ab53d2399f49e2692cb77d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.4 MB (244401015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2368f5377fe433510b0eac759a9846a71aad459838b5cb712f651819f966531`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d575fc3fc33f3212c68f0b4bce5426cd5a68295ab95b0f84cdc65794583043dc`  
		Last Modified: Tue, 19 Aug 2025 04:00:33 GMT  
		Size: 142.5 MB (142460557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f5eb6fb037fcf5bf1da5787e8a845cea470eff8bf42db6b5cf16797fe04243`  
		Last Modified: Tue, 26 Aug 2025 17:40:22 GMT  
		Size: 71.8 MB (71803769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7be3f990d9174a9e9c67973296344f3f6c40d08c9b7f4b7a4d8e88cf1549a02`  
		Last Modified: Tue, 26 Aug 2025 17:40:07 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:af6e5ff9e6c6a6980247bef9c95bbfc34dbc0f93ed128d001d3421fb79740675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5296168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee694cf8df6f6711f83bf8752dfd82e49c766c56470b73a9d67c09fcfe990e25`

```dockerfile
```

-	Layers:
	-	`sha256:a26d855c95f81fe02388f84ec6282419f63476fe18c2711666c32030a37a00af`  
		Last Modified: Tue, 26 Aug 2025 18:36:50 GMT  
		Size: 5.3 MB (5281765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3937a43a1776a270a43370884ab632a853412d8c5903a31ec20caf4d6f9a8485`  
		Last Modified: Tue, 26 Aug 2025 18:36:51 GMT  
		Size: 14.4 KB (14403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:7d3b9f1d4b8b214976553ab1dea8eec0d738a93905206058c6826c9e7da85479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243836953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cadbb3a360615d3b278ab30bbc1d2c636b9fb17bf929a16ab0a3efa06458b24`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d40da39c1e05974afe8d7dc7c9ee044827e979d78538852469cea98a61ef8ff`  
		Last Modified: Sun, 24 Aug 2025 06:19:53 GMT  
		Size: 132.9 MB (132853302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b925286cb7e081b4b8b05e18cca4e8112e43cdcf86ed21f836f6b0fd0b44e07`  
		Last Modified: Tue, 26 Aug 2025 17:51:49 GMT  
		Size: 77.4 MB (77388791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb168031d7dff9f8f2988384a67f2b30e186dcd0f56c1d30bd34efebfd06810`  
		Last Modified: Tue, 26 Aug 2025 17:51:29 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f30db2465180fb040e0696a59ddec9c80add349d7fade8b1d27de83e9c4d85de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b966c772220b4779b3d5c7d3697b267de0d2243675d0f1f4fea5b357b16a57d0`

```dockerfile
```

-	Layers:
	-	`sha256:7b1519ee0a3761eade276c3ab8b6ded6514c6c31d8e48ac399b191b8510a1dbb`  
		Last Modified: Tue, 26 Aug 2025 18:36:56 GMT  
		Size: 5.3 MB (5279134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81435949029dec1a446e185e1338c54b29ab6ef7258bcf29e65e474d90f467fb`  
		Last Modified: Tue, 26 Aug 2025 18:36:57 GMT  
		Size: 14.3 KB (14334 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:7ed72d1f69e38dec8fc98678e664b269bc7e0512fb7eb527126e17d7887581f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228405584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c58858a392bea69e13c5169a351633a4b5d7597abbe7b79eb86828cbf17bc2a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d60f4f708fd5a97ca5b2bec02379236d1ba8e24d3cf4658ab3e32d0e0c22bd2`  
		Last Modified: Tue, 02 Sep 2025 01:49:59 GMT  
		Size: 125.6 MB (125622179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10650f1b6c260b6e0f2da8ef46d0895d7e03379a8c3ac2de4862c89a2133a5a0`  
		Last Modified: Tue, 02 Sep 2025 01:55:52 GMT  
		Size: 72.9 MB (72949702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03aab98a27cfb3333ced61564c49746165ac305da55eda28b263afdd0fe506a3`  
		Last Modified: Tue, 02 Sep 2025 01:55:45 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:af37ee9c8e8f79e4dfa747419111690d56548bce0b768b57f9821ab2c7f1ea23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5285592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06b81d5b04141ea9c5b9146a0ce18a57f815dd07f23a49746e6f5f9f60ae1da`

```dockerfile
```

-	Layers:
	-	`sha256:38121554690ab305d4a1d16e2c48d13402355886a93377091903483ce753a7af`  
		Last Modified: Tue, 02 Sep 2025 03:37:49 GMT  
		Size: 5.3 MB (5271306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72353a18618cd7914b175ac28242d423ea7f89fc6fcaa06368ec1663977f5167`  
		Last Modified: Tue, 02 Sep 2025 03:37:50 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json
