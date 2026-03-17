## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:2b0a5cd7f6a6b33b93553d209acd2e92dde1a7f66999568d710682c1754dcfc3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:791d612453d1f62043e1f85af7e0286419387315e5aa79819c6d7014f5bb1092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235248990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26c3f052731360099bfc12339aae1e686be1a4d88fae176f71f9251df1321189`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 02:57:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:57:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:57:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:57:22 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:57:22 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:57:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 02:57:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 02:57:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2def39ba61d018877eab029bb49f5312188fcf3f564be382981f921d932f625f`  
		Last Modified: Mon, 16 Mar 2026 21:58:52 GMT  
		Size: 30.3 MB (30257826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9d7fec8de3068f08fd4c94742281a15c5586241bc6df70c38def795c405961`  
		Last Modified: Tue, 17 Mar 2026 02:58:01 GMT  
		Size: 145.8 MB (145806912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd8463be2070e86bd089fefe2d21b70176b015d666ba91bc522da35e5ff250f`  
		Last Modified: Tue, 17 Mar 2026 02:57:59 GMT  
		Size: 59.2 MB (59183608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e15f42c95275eae46d38222bceeca342e8a37212126fb7935d918b4c8692d2`  
		Last Modified: Tue, 17 Mar 2026 02:57:56 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:113186701cfa045579bc81a7a581adf3e9584de37dceab96857be8fa583075b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5354459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9499b0a23ad26ccbe49dfceefebb2836761bf21ce0fc6ed36418601aa88010b0`

```dockerfile
```

-	Layers:
	-	`sha256:0c2a8958d6dd173b2b1ee599ea9742e481b2423b61bfb85904054d7ded6103c5`  
		Last Modified: Tue, 17 Mar 2026 02:57:56 GMT  
		Size: 5.3 MB (5340194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85a87c47e5126d18b6749439b178ced49b5ba1470213b41d7e91c430131109b8`  
		Last Modified: Tue, 17 Mar 2026 02:57:56 GMT  
		Size: 14.3 KB (14265 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f3d6106ebc2ee695916fbaa001492c3acce98ab8b16291c2908aa71d18737a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230568876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f301c03eca19dbe8f65c564d58c02c45c54a815fe5d799944c0eee1e6d02088a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 02:45:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:45:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:45:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:45:42 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:01:54 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:02:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:02:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:02:09 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:345f33ba283982a717a4e5e736aae0d965b9ea4497df11e15c24675df605ff01`  
		Last Modified: Mon, 16 Mar 2026 21:53:13 GMT  
		Size: 28.7 MB (28744526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2dd853de985ad9f186b9d4a4f7e0c74736f29dd53f5b7ad0e5dba8b1eb967ce`  
		Last Modified: Tue, 17 Mar 2026 02:46:31 GMT  
		Size: 142.5 MB (142500035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a69295e9e0c8109e437bbe26382d5b2960661b3093d656e533594ebd2cbac1`  
		Last Modified: Tue, 17 Mar 2026 03:02:26 GMT  
		Size: 59.3 MB (59323672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92307eac3708f3dfd195ee6617a9f485d71c585a7ba5fe2d4728cf6dd6dad7d2`  
		Last Modified: Tue, 17 Mar 2026 03:02:24 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a2dbddbac81df332cd287b0b9933ac3a05f68ae144126e41b218eaaba7e976ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98afdb37889a0dc48364eea3a97d58636afbb257bde86b63012ee3a00e1d3bd3`

```dockerfile
```

-	Layers:
	-	`sha256:d43858c33c7849834e5f5566d97d8db211f480aa1da887ea2e136418ddb34730`  
		Last Modified: Tue, 17 Mar 2026 03:02:24 GMT  
		Size: 5.3 MB (5346544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cad224d537af0003eb288bfce77310933d639e79135169f6df05135ed0cf66ca`  
		Last Modified: Tue, 17 Mar 2026 03:02:24 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json
