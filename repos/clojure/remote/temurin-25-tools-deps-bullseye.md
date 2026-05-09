## `clojure:temurin-25-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:d7a66448dbfd753cbec57fe18acff45aefeac422e0dd3e3dbca9f2a8c5f19a2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:6b567aea970072a04887b1c9cb9b0f7fb12ce00a3d8e1f9b82b06d3a3d2d8457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.9 MB (215936709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf1992d2eb87aa26007153e1886afff9ecf918d179c4b08e35bf1995bd05ea9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:19:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:19:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:19:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:19:27 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:19:28 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:19:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:19:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:19:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:19:40 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:19:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7a17dbf03df5e3fe86db16676d90afc30f4fdcaf0f69d5a2da5cffdab2742d`  
		Last Modified: Fri, 08 May 2026 20:20:02 GMT  
		Size: 92.6 MB (92574587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5525ba40966973926b5f61c4217bb22f8f8f8010142405b4859f7b1bcabafa76`  
		Last Modified: Fri, 08 May 2026 20:20:02 GMT  
		Size: 69.6 MB (69597738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fc006cffbd2eef7d5fc70d051682ac5f57013b80fbdc544ea513b7e26fa58b`  
		Last Modified: Fri, 08 May 2026 20:19:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e081ff74d86d3dc912ff64ab305606d69830fa4d9e53e9a90798de87c87dc3a`  
		Last Modified: Fri, 08 May 2026 20:19:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:fede53a99255c2f34c8666a22e0fb0e2ce0cae3241bd4c020c26f87e180be365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a072ca930ecc2ee79da4f5c7ed68e843c3633f9cf75cb0b6f14ba97da1743abc`

```dockerfile
```

-	Layers:
	-	`sha256:6196d1c74f05c6d3901a89abfb570affd4120514044153da6e07da3f151a3d76`  
		Last Modified: Fri, 08 May 2026 20:19:59 GMT  
		Size: 7.4 MB (7376350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07ad3e531ac75b63154650ed9a1e702b50437e2f0a9655760f66b2851f0a440f`  
		Last Modified: Fri, 08 May 2026 20:19:58 GMT  
		Size: 16.6 KB (16601 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6ae4f209d4bdfe1d06fc4d4c4723395d734c1f891e5d914c74521c281fb31832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.5 MB (213535272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72319e50b260c1c2b5a2475d4ff1171d435ddfb34962abbb882731d37ca07779`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:23:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:23:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:23:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:23:56 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:23:56 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:24:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:24:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:24:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:24:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:24:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7b89f28a4d9f12808e7c2f9e4323a184234f6259e3e1caf17d7d0e9ad6600d`  
		Last Modified: Fri, 08 May 2026 20:24:37 GMT  
		Size: 91.5 MB (91542268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a43eed3e783fca67a9e7d85c4d92c7598e3d4954c5c70a7da9b2783fc7d3bf`  
		Last Modified: Fri, 08 May 2026 20:24:37 GMT  
		Size: 69.7 MB (69738753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8546b9e4c4cef9e8d7fae0f155d09745edc95c59f3792f32f94536aa876b04`  
		Last Modified: Fri, 08 May 2026 20:24:33 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3ab70a102565d2bb91643ac373bcf313e84c103bba632516a87c85b97a8102`  
		Last Modified: Fri, 08 May 2026 20:24:33 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:5bb9ebbc2a62527eaf1b58cedda1bc747cd5ea120dfe8bbcdc567cd136e163d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7398213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed511427d3fa785bc44ec9dc77473d2b0f638d84cff9ef2876caab3dc7637e4d`

```dockerfile
```

-	Layers:
	-	`sha256:f9421c13a4f64322d28cd7af9af3e8d63be93ea59c271641ec2b9cd5312a54e1`  
		Last Modified: Fri, 08 May 2026 20:24:34 GMT  
		Size: 7.4 MB (7381470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:904dfe60aa7473268d025db93a122369355196c5c11a9e8f32946736ab3ffe81`  
		Last Modified: Fri, 08 May 2026 20:24:33 GMT  
		Size: 16.7 KB (16743 bytes)  
		MIME: application/vnd.in-toto+json
