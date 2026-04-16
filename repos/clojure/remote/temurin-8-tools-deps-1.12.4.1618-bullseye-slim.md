## `clojure:temurin-8-tools-deps-1.12.4.1618-bullseye-slim`

```console
$ docker pull clojure@sha256:e6157876df6c9f99d28a4ab0e36d4da86c2aea1c8a00993ac8e4bb93a59cac92
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1618-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2f8210513289f6ee3b50a946fad658a64da9c9c7c2e20c607ef8449b00beb78e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144620325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b645bda120bb976fc48ce9149a4e93e3caf90d64150a3e31cb7983f3b9b79c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:01:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:01:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:01:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:01:25 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:01:26 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:01:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:01:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:01:39 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d355d4bf1dcd13465390a658a6a99710161fa7cfa3884a28bdbfef1ea5f43b`  
		Last Modified: Wed, 15 Apr 2026 22:01:56 GMT  
		Size: 55.2 MB (55170061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8358e1a09adcf6361b18b2b6c8872f835c024439b0130f8b4e2c0465f0bad2ba`  
		Last Modified: Wed, 15 Apr 2026 22:01:56 GMT  
		Size: 59.2 MB (59191599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7b61e6164b0ae611d4095f97b951301a0c57ffebfcda15f77970cdcffb62ec`  
		Last Modified: Wed, 15 Apr 2026 22:01:53 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:626bff9b2b805291851bb5a65bafc3e504660f95e99948e66b4dff243103051c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5455288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbc2234c41495eba474bb3eed5cefe02c7c924195df5688001f096be9440fafb`

```dockerfile
```

-	Layers:
	-	`sha256:7c43a8a09ba4a7dfe5f857df2062b4ec8d54d516cbfc564a89d3d35fdf079417`  
		Last Modified: Wed, 15 Apr 2026 22:01:54 GMT  
		Size: 5.4 MB (5441040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:828a32b5538c91b593b9bdcda7fd5a05f3d4a53e0ca2ffacf127762d1dcef712`  
		Last Modified: Wed, 15 Apr 2026 22:01:53 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1618-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a12dcc47113bbe7c6bd861373fb7e349429f1a10c5860765940832baa922fab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142327455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9062808e7b1152e02efed33111946b22e2d22942cfdb8490c5b8cfd1517cb79`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:12:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:12:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:12:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:12:55 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:12:55 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:13:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:13:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:13:10 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d13108b9d1843675a258819fe9b3d97e241c9da5740f3dcf94e11b5f6c6512e`  
		Last Modified: Wed, 15 Apr 2026 22:13:28 GMT  
		Size: 54.3 MB (54251613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e50d7878812ee75a5b134ea40cd6ebd197674af2742083485396aad3ddda0d5`  
		Last Modified: Wed, 15 Apr 2026 22:13:28 GMT  
		Size: 59.3 MB (59330507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e092918f0f278f8fbe4482ee2602f727dff276c0b1a939682e74239243d6252a`  
		Last Modified: Wed, 15 Apr 2026 22:13:24 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:83a03d7c4f861d15dac7b50106b44c89401f30a43b42904f91d2f0d3cebd76cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5461837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca0a7634c3afecc8d7f72168c6d95fb54c0ec959f6112086c20d8acc21c92c6`

```dockerfile
```

-	Layers:
	-	`sha256:1c2fca0e3f33e376bc7aa8330debe42ecba66189be9e73a7e434243d3efb4db2`  
		Last Modified: Wed, 15 Apr 2026 22:13:25 GMT  
		Size: 5.4 MB (5447472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d29f75dbc838e1fa48f5194c1ec8789716f726b49cfa620849a9467e76e79c21`  
		Last Modified: Wed, 15 Apr 2026 22:13:24 GMT  
		Size: 14.4 KB (14365 bytes)  
		MIME: application/vnd.in-toto+json
