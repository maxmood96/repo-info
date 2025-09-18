## `clojure:temurin-8-tools-deps-1.12.2.1565-bullseye-slim`

```console
$ docker pull clojure@sha256:44f22889141ca104fecd44f271116d413ba6439d10e9b1096ebea8ad1a7fc382
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.2.1565-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8cf99be1022ef165ac0824ef4740206d191fb492df1dffd168d5cf162cf44fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144138718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc46d9a7c4d1dbd18e5145102db4090c039f1960ae59e216a59ad51372df26c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c21d0830b58af4f1b0d69cd6ecf6dd125c83ee8f98e57037e40224cf94021a`  
		Last Modified: Mon, 15 Sep 2025 23:25:03 GMT  
		Size: 54.7 MB (54731307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a9afcfdc27a780eb1a59b3b1a4fbd213921c647220b6964595079cb319078d`  
		Last Modified: Mon, 15 Sep 2025 23:25:00 GMT  
		Size: 59.2 MB (59150699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6184786cf5ce33110d41cfb5d429cc888defbbc5458450708d68533347e76421`  
		Last Modified: Mon, 15 Sep 2025 23:24:51 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1565-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8d5c9172bb0751dd0255c265f1ac7149d79065cc2b857e4756c60c7623a711e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fbe291959c97feb6b26ff8865d68e0d70ba545bbabe101e89ab2a574ca0adc8`

```dockerfile
```

-	Layers:
	-	`sha256:3760660a56b78c0458220e8bb13367ded8bc77c72b04b0480ca3b7b2eb682e05`  
		Last Modified: Tue, 16 Sep 2025 00:47:59 GMT  
		Size: 5.4 MB (5429677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8199642609624e24382322af88130717879df334460c3d3dfcd9f4f2b9ccf495`  
		Last Modified: Tue, 16 Sep 2025 00:48:00 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.2.1565-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7b94a7a010c76f903a6659cfe098074d3a8d83cc89933bc6aef38d5bcc5b088f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141869425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fda0afdc4bf12d1459214a934fca8c63e3e6b30575ad019aeb0707e718dac0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fb745d07b3773f637e4dab362713a4f2c21469689c788aa3db30bfda6212f5`  
		Last Modified: Mon, 15 Sep 2025 23:25:13 GMT  
		Size: 53.8 MB (53835607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cac44920650f6cffc2edbdbe1e6881f841864aedeaeeb76161f966d7fe50991`  
		Last Modified: Thu, 18 Sep 2025 15:20:33 GMT  
		Size: 59.3 MB (59282717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a756b996e7a41c8e1f4ac5fc658c3cda6138047d6dedf60d9cc7f180f3b129`  
		Last Modified: Mon, 15 Sep 2025 23:25:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1565-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c0ac265bf0f71b05fb88a0339552dce6c7783d40e9c39f5a7e6b02fca9779d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5450516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e715bc1a25e423c0fc6832a6cb745aad7de3c018f7dee468e3834f18ad3f45c`

```dockerfile
```

-	Layers:
	-	`sha256:e182975277496015bdd7a5222dc4f48d310617d75956d21624c209101e5e2e58`  
		Last Modified: Tue, 16 Sep 2025 00:48:05 GMT  
		Size: 5.4 MB (5436107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:578c7c548f3511319f30d75b68eea65256e1140d6266faf9e7bebf7c9fc9f264`  
		Last Modified: Tue, 16 Sep 2025 00:48:06 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
