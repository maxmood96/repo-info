## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:3ad53c00f95f77804da94718e06abe23f53d23e7f6c027862714a66bed02bb1c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:520581583c803a9fc161c918e51f18d17c746216ebf1bb4a3447013a560d35fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234897602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d64b11acf26a4838b3a3af18eabdfa19b4f30a0214ddf721ec60cf9d609e99`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
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
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7547776343a3f86c5dd644cfa47d292c3f64406d4a7188b72c03ae511c828dfb`  
		Last Modified: Tue, 01 Jul 2025 14:25:15 GMT  
		Size: 145.6 MB (145635675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac9591f6f703fe839483501887bc13179fb3685f4089ed3c05c67c7d7e5f9bd4`  
		Last Modified: Tue, 01 Jul 2025 02:39:12 GMT  
		Size: 59.0 MB (59005235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbe64b1d0fd0dc05156d7bc631349227da82058ef0b29c459f43b0b560cf8a4`  
		Last Modified: Tue, 01 Jul 2025 02:39:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:610d7a38e797dd036a2dba641d54efc9d4cdebfe60d21b675cb5d9c0b9653697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5342489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9f20df88d32773c63f0e2685547db31b44e691963b2a81029e11c0484e9fd7`

```dockerfile
```

-	Layers:
	-	`sha256:79638aabf2bbcbbaf7bbb1b94655c70ab95a6e464275c95335d9538ac47e598c`  
		Last Modified: Tue, 01 Jul 2025 06:35:29 GMT  
		Size: 5.3 MB (5328179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eec3bd7a1f847a02075846328e78eace9209bb22e0fdf161ecb895dfae112c0f`  
		Last Modified: Tue, 01 Jul 2025 06:35:30 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:23af5d94fc4cefde09379f64efe07e52b8a6e9fa3442cc6c33a99970d84694a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230303151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53787f829a1cb81d3ee3db64a0e58bf833c12a7eede4c79fbbac36d65d300217`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
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
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bbe1bfe4d9f860b1ddb0515cbcb71e77bbe9fa70ff23d4f32f7012ab7e3791`  
		Last Modified: Tue, 01 Jul 2025 08:49:59 GMT  
		Size: 142.4 MB (142420681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73844f314c3ac4ca186a056ea3a8c2e28eb4b530be17ecc69fcd8c8014fa39e2`  
		Last Modified: Tue, 01 Jul 2025 12:15:28 GMT  
		Size: 59.1 MB (59137687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9172d920eaa5d8e779c97071b3d33d1ee07b3f935024ec6e2c4b71122aa463dc`  
		Last Modified: Tue, 01 Jul 2025 12:15:23 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3bfea80201f3b7378a87f3a40c18818d30e18608abe91df617d7a9e9364a0997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5348957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d65d67378c7204f69ac4adc407fb630a2e78ac383fdd79ca9fad24f2b953cb5`

```dockerfile
```

-	Layers:
	-	`sha256:b6e9b49cda8da0758e6a55d9b325e0099a2e697ade150380f146d34d28650983`  
		Last Modified: Tue, 01 Jul 2025 15:35:19 GMT  
		Size: 5.3 MB (5334529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af70f4a116cb337da0901c13bdf8e09305c8e8be3e8f3dd8db5ed3dc4543f420`  
		Last Modified: Tue, 01 Jul 2025 15:35:20 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
