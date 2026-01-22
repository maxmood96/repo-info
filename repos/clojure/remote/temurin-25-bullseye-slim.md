## `clojure:temurin-25-bullseye-slim`

```console
$ docker pull clojure@sha256:a7a6138971261183a62fd91b1d0830c650a81aa93360626c9ceedf9f05ecc78a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c4a8053240585dbd00be5ad5dfdb6f87ce731ce9cdc0c072d7e5e2c334cf20d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.5 MB (181454661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50fbf73256dbbd00e748b53c6ca95c41107ace01f77ac01d2b93f1137b46299a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 02:06:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:06:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:06:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:06:33 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 02:06:33 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:06:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:06:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:06:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:06:46 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:06:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb684e56c53b9c6d89d38b5645121f6c212ff496c750751402510bfdaa95c75`  
		Last Modified: Fri, 16 Jan 2026 02:07:06 GMT  
		Size: 92.0 MB (92045317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b607f1d198b2a5e8b51269cae1889a6cc523cfaa5d993e965721573ad0f9a0`  
		Last Modified: Fri, 16 Jan 2026 02:07:16 GMT  
		Size: 59.1 MB (59149807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f5013cdbb040d2e2a76aa2c20f0531dcea4ae91d7119732951db9b6f147514`  
		Last Modified: Fri, 16 Jan 2026 02:07:11 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a473c84f1494e3e1882d50a1773ad5442ae6a9b9fe5b2c50cf3d92970f2f78a9`  
		Last Modified: Fri, 16 Jan 2026 02:07:02 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5025a15c90b6b1bdaa6df40f7826d7d92ea7b539b58dba2c7208d2c31227fbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce0d2d1cbf49ab2ed8d1c28a603b481717f2025f1f8df706a7e2fc8dfae5f58`

```dockerfile
```

-	Layers:
	-	`sha256:49c07c1adc59ace043400b92cba567c5a7bc85eed65d028b0426765cb04e43ba`  
		Last Modified: Fri, 16 Jan 2026 04:49:46 GMT  
		Size: 5.3 MB (5259427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a43ba1346f3df33ed30d6234f1bdc0676ab64c09c9bc21be1cf83597d345f36a`  
		Last Modified: Fri, 16 Jan 2026 02:07:02 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c9f011044b0962e34661bd4a96bfebcb879881b319a49dc4beebb41e579800cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179085874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff4ca9faa4506bb3fc40c668145632ff7cfa0ba1a64e0faf84c9b03f6575eac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 02:11:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:11:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:11:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:11:51 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 02:11:51 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:12:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:12:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:12:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:12:05 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:12:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babdc50cd8aa366cbcba4c5edd207199df217c5d0db7b08db3f4dfe6b6c97d12`  
		Last Modified: Fri, 16 Jan 2026 02:12:41 GMT  
		Size: 91.1 MB (91052479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db9660a33b3c4114524e75dae21c9bd223eb17584f88eb4e36ba16c9fc3c95d`  
		Last Modified: Fri, 16 Jan 2026 02:12:42 GMT  
		Size: 59.3 MB (59283836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87a6ea8122b562e76548333c5a466f885cd423e1d0cd1cd722f8eddef1e690a`  
		Last Modified: Fri, 16 Jan 2026 02:12:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958bbda47b3bf55bc8a7799420587311fb0fa5959c4c1ee0103e066da9d912f7`  
		Last Modified: Fri, 16 Jan 2026 02:12:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e889cb897d9f773b2b9b2104eea7fb4cba6babad29c24a85c4df2de6ddb84c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6713cf05f3c8270aa089227462c82a0f6c454ba64ead7c07f18716ab4dc6eb1c`

```dockerfile
```

-	Layers:
	-	`sha256:c537f9e0dcc7dc091e029583aa2281e7e0c3058a38c764beed9389d8a681645d`  
		Last Modified: Fri, 16 Jan 2026 04:49:53 GMT  
		Size: 5.3 MB (5265180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eff46a18c2ad60b2cfc406be08438f07d4e7f3a41e02cd9b1b7d555f93329f42`  
		Last Modified: Fri, 16 Jan 2026 02:12:24 GMT  
		Size: 16.7 KB (16666 bytes)  
		MIME: application/vnd.in-toto+json
