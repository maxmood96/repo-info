## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:5956d9f909096f3daa1360e5a6596ef734b59901890afc96f0f6260e81dabd16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1a5f6c385f894e26ccb8cd7e2a84dc2c2327d0eb8fd67a4856781ea7dbeb61b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (268010278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23500eecfef23dd3e1bbf1ad1bfe76cbc6ff74135619d6ec2ebdb9abfdff01f7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:10ffc47270cd106d2d04bc7ef4749d579620e45a84804ba3b18f0898fe5ecc64`  
		Last Modified: Mon, 29 Sep 2025 23:35:07 GMT  
		Size: 53.8 MB (53756064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d00addaec6425362b96bcc060021ce25f90b663f13f76c30299fdf4573f5183`  
		Last Modified: Fri, 03 Oct 2025 08:24:18 GMT  
		Size: 144.7 MB (144693625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f9501d30acabf00351c2772b85b91d27316e36d18980fc9b41c7b83c728eb1`  
		Last Modified: Thu, 02 Oct 2025 08:59:14 GMT  
		Size: 69.6 MB (69559553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b50f52fbb8b715ad9eea4fa053df7f4394355103a9b10bf1109d278cd8bda8`  
		Last Modified: Thu, 02 Oct 2025 08:59:02 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabe4f93b56f6fd15e75c40b5c40d80db9eb955aeef734dd5b22411b4ef902c2`  
		Last Modified: Thu, 02 Oct 2025 08:59:02 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:eb178bbe877b9f7c4320c8ae07410a2d75b235d6ed9589d7b07c8fe7f8a30b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7411488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b71f70046babcecf4d6b5edde093d650186a8c52abb843d7d7bf0e09272b731`

```dockerfile
```

-	Layers:
	-	`sha256:d2cb33d0d1d1d40284384669eaf2159fef48f705bbb6b11cfeb7c3eb78ffc10a`  
		Last Modified: Thu, 02 Oct 2025 12:38:10 GMT  
		Size: 7.4 MB (7395667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f01182f5470a60ed8090f4248029c732c52eaa42c1f4a4bdcf6cb0e6c0e1837`  
		Last Modified: Thu, 02 Oct 2025 12:38:11 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cd7f7a82d82304c8b5cd8e942d29a12b89b1c327b0034134b28bd228b7765d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265488395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9918dfd42a34609f4b0367f90a8312bbadce7c05a1aaccffd2a5fd8a4ad06bbd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9b16ae1bbd1ada84c12528379a10e280bd89e0d0332670c8487145eb77fe2fe1`  
		Last Modified: Mon, 29 Sep 2025 23:34:42 GMT  
		Size: 52.3 MB (52257414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902d5b8238c9c2eaaccf7f5fd1f022112689dea9268b37d68e55bf18b0e118c7`  
		Last Modified: Thu, 02 Oct 2025 07:55:32 GMT  
		Size: 143.5 MB (143542162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe521a29a30883a5ec99d8bb5471b5caba6dae8c8ebf880b86aab6ea53bf30d`  
		Last Modified: Thu, 02 Oct 2025 02:44:23 GMT  
		Size: 69.7 MB (69687779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bb03cf5266a0c30913bd8a3db30bdcb3eebfbd76e6651570ab720cdd0b5107`  
		Last Modified: Thu, 02 Oct 2025 02:44:17 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f0b9f6b0780feddccec17d229fd0ddfaba29d075ea23b44a312ab9c4f9f06e`  
		Last Modified: Thu, 02 Oct 2025 02:44:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d34ecb2de0f9c540332bc5adb820b82cde3aabc9e9c20cc05156190e270af7a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af4d39fb6c25f94910a4061fd8cfe1ff520a2a8de550d0f8debeec98419f319`

```dockerfile
```

-	Layers:
	-	`sha256:b6417ec38779cb0202bc6da873b5b42ebc680a693867a2b7d3ffebd1c89c3d1d`  
		Last Modified: Thu, 02 Oct 2025 06:39:08 GMT  
		Size: 7.4 MB (7400766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5dad6056bde7fdebdfba5cb5c0e5ddce9a04397458d3a6fef87f526158d99f4`  
		Last Modified: Thu, 02 Oct 2025 06:39:09 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
