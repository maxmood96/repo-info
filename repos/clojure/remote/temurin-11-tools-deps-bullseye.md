## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:9280aa055760c0466a1b8527d7f83441cdb9e7b524add75940d151d6cf3c770d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:39647f7bb5527100ce2de96b45bfafe6d27298ad10d68e3f505711483c43fb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269246992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff38b4114d13b52419f54cef3338eac4bdf8af4c93c86c847a7f01e5430e51d2`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 29 Apr 2026 23:15:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:15:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:15:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:15:09 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 29 Apr 2026 23:15:09 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:15:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Apr 2026 23:15:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Apr 2026 23:15:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210c4bf2e9a62dfc38b14f319b9481589acc7387f2063b2757e34a6d64b47b5b`  
		Last Modified: Wed, 29 Apr 2026 23:15:43 GMT  
		Size: 145.9 MB (145886247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8411ed383ca235dad1ff8a100daf932d7515bb7f6cbdb41af9d8bbbd6bc700`  
		Last Modified: Wed, 29 Apr 2026 23:15:41 GMT  
		Size: 69.6 MB (69596948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7528f7a070d07c70e0010b348c72afeb5bc5f54228801ff9e9dd13ebb2f93a81`  
		Last Modified: Wed, 29 Apr 2026 23:15:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bea3d08df8d06e567cf5eb8feaf28b39b7f2888de3370f5322256b220cc189a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7442005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9cde08713b25c9c44a1d75450d6492399092e78747332d9063d3699a081308`

```dockerfile
```

-	Layers:
	-	`sha256:daa94d81377083e90195d8e62999cad20962eb60547361d82e267e5c392d0969`  
		Last Modified: Wed, 29 Apr 2026 23:15:39 GMT  
		Size: 7.4 MB (7427796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2036c974a06c7a7885998a39be1cb66c366cae1993256233b4db703401cfd4a1`  
		Last Modified: Wed, 29 Apr 2026 23:15:38 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c53552dce78583afc6769c63a08b60947491799a99b3c14393341d7783a2442c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.6 MB (264576501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4a9917110750d7b8c9b38af4748bf11ca5398567d3bad7d6e73514a36fb09d`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 29 Apr 2026 23:14:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:14:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:14:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:14:33 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 29 Apr 2026 23:14:33 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:14:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Apr 2026 23:14:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Apr 2026 23:14:47 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72167b31c0a74b7443a6c9d053a8833ea14724fb758471bd381ffbe5e5df5fe`  
		Last Modified: Wed, 29 Apr 2026 23:15:11 GMT  
		Size: 142.6 MB (142583978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df02b79c3ba3a0e7ad7dfb73c1d79aa2f85358789ca113e32f257619b2ef6010`  
		Last Modified: Wed, 29 Apr 2026 23:15:09 GMT  
		Size: 69.7 MB (69738881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705b22233b2f84695d6e0d3a47fbb76ab562a71eb4ae9ac0c8e0feaa87907b9e`  
		Last Modified: Wed, 29 Apr 2026 23:15:06 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d45d784f18ad69b259e31b8046897162d34bd2bf79272efcdb4c8dce55077f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7447839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1443e795911a5ea17124f8fe48e585f53a00ece3841f17f8a6ccd9efe1a005e8`

```dockerfile
```

-	Layers:
	-	`sha256:e9b9d5cd9e31c0f4c95f0be824bd9b8a369202cfaec33d7a525a27c8a3af120f`  
		Last Modified: Wed, 29 Apr 2026 23:15:06 GMT  
		Size: 7.4 MB (7433513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c53549dab8e766bfff905e9320347a8100a9c511b38dbc26d50dbad5bd51a058`  
		Last Modified: Wed, 29 Apr 2026 23:15:06 GMT  
		Size: 14.3 KB (14326 bytes)  
		MIME: application/vnd.in-toto+json
