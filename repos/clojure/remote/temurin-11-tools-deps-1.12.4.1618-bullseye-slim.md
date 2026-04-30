## `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye-slim`

```console
$ docker pull clojure@sha256:8911b92aa4c5bc6563631e1ea07038a62a377a4311e5286b303d3ba6b7e90701
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b7983d20658f9ad88f6f1e58d9ebef6ebb09e6da782de0073ebe52da5982aa6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 MB (235330691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62fed5d66a292f4022dd205ac28f55b126a9e33a0da374d647af957a85e924ac`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 29 Apr 2026 23:15:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:15:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:15:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:15:08 GMT
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
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210c4bf2e9a62dfc38b14f319b9481589acc7387f2063b2757e34a6d64b47b5b`  
		Last Modified: Wed, 29 Apr 2026 23:15:43 GMT  
		Size: 145.9 MB (145886247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab8eec05b80c571205637a8b36e6ab0c0cb78cb2101bbbcfd02da2dbb36c701`  
		Last Modified: Wed, 29 Apr 2026 23:15:43 GMT  
		Size: 59.2 MB (59185865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7528f7a070d07c70e0010b348c72afeb5bc5f54228801ff9e9dd13ebb2f93a81`  
		Last Modified: Wed, 29 Apr 2026 23:15:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9b4f6b64b8bb372ec44c8938eb9d61a398529ef101e3f88a7728756e26de4a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5354462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73541a205669be6bcb15f538f08e13f54953e6ba436adcb68c858ff45709924f`

```dockerfile
```

-	Layers:
	-	`sha256:cd95d03c8d99cc980244cbcdba0323a2b79c8ec5348913185ce0e9c7f6b4cd5d`  
		Last Modified: Wed, 29 Apr 2026 23:15:40 GMT  
		Size: 5.3 MB (5340196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f32c4ab7c309bc6c33b3d164b6a55a159d7497a86f7aeffc5d688de7d5fa616a`  
		Last Modified: Wed, 29 Apr 2026 23:15:39 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9eb67dfe649449fce7ced556951dd7fa5511675c4580b7e650bbbce379bdd4cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230658209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5953ddd1e23c151dfc4d3701aaa43fc66dc4ba966c89c79f93ae1100f5e760ed`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 29 Apr 2026 23:14:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:14:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:14:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:14:46 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 29 Apr 2026 23:14:46 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:14:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Apr 2026 23:14:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Apr 2026 23:14:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d272ea91b2bd9ba4af1d8841a41368812fdf515e7ebb377e16477fd20a424924`  
		Last Modified: Wed, 29 Apr 2026 23:15:23 GMT  
		Size: 142.6 MB (142583969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fb6d4a4fc5600c668150d8bdc083aa76ea84d661e3d43a14632591b869f1e6`  
		Last Modified: Wed, 29 Apr 2026 23:15:21 GMT  
		Size: 59.3 MB (59331083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a4d28c9273630518fce47edc0aac9b96425e14f4b288df899dce70b13f8c9e`  
		Last Modified: Wed, 29 Apr 2026 23:15:17 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:86c853df322fe5d2b179a279548cae2cf652d32dfa26f4ae05e7d6c9f0b9026a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5360931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a61d8acb223798961973f43af4e9439f3ebf8e314954e57e3d6e9aba911f281`

```dockerfile
```

-	Layers:
	-	`sha256:d4a1af1b4b5b944d5b4cc64684213f2e307494c9abacd7a17c57620045ce8606`  
		Last Modified: Wed, 29 Apr 2026 23:15:17 GMT  
		Size: 5.3 MB (5346546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80e3f8644f490bb8dd757c6bb79d26d7ffc3e918e0b85aaa7fbc53ac56449540`  
		Last Modified: Wed, 29 Apr 2026 23:15:17 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json
