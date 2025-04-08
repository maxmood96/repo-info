## `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye-slim`

```console
$ docker pull clojure@sha256:b0128b4ed641dd766cfa1bcd4bc5ac6a546f4efb0c5c0968c029c350ca75d7eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2f120034f80528fdb22628d38ad7865e56c8fb6ac7f427aa1d085936a4d78134
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.8 MB (246837269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b51fe51c0517220b5306512aaa0c1dd93933d87c45a4eb5052d6619a10b5798`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5ff8c684ee42eed5a7b257173a662abfd03a86367a55744d04172a94afd0ef`  
		Last Modified: Tue, 08 Apr 2025 01:36:43 GMT  
		Size: 157.6 MB (157585931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652457747b2ac9aff5462c27000ee0a75b24dd00bb4c7e04a94f02dc1a0202b4`  
		Last Modified: Tue, 08 Apr 2025 01:36:41 GMT  
		Size: 59.0 MB (58992876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d600ad9350a508a49efebc11d2f9e0b8c4f76a6c859bda1364f0970ded467e8a`  
		Last Modified: Tue, 08 Apr 2025 01:36:39 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae83516e0e0de224b28bd856a88134d945cb2bf5a3f1c79d37387118f73bd42`  
		Last Modified: Tue, 08 Apr 2025 01:36:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6f6405ab4b1cb389e6d1fca993bd323b67c6d8daa04dd9b3610dfdeb7b48d1e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b8d52eda978993e60e561fc8f7c81f87650b50c593ce3d32d19fce68741735`

```dockerfile
```

-	Layers:
	-	`sha256:5c17fdb9690b05530bf8e33b52aff36713b06859bba3f73e9ef4d7a1cb748945`  
		Last Modified: Tue, 08 Apr 2025 01:36:39 GMT  
		Size: 5.1 MB (5122811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1c00c40297925f3531d798d79f4f58278a79044fbef5fa26138089da28429b1`  
		Last Modified: Tue, 08 Apr 2025 01:36:39 GMT  
		Size: 16.6 KB (16574 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:148f85d23a404d61f2a1c0d0c871b8ce744fb543243c1aad80d6abbbbcd4fbb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243514673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d864f9aef376527772ad90ce938d48ecaac58590222262c36298eba474917181`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b944b2358a5a7ab6f38260a8331507c0b05ceb8f17b4c303253b790f49755487`  
		Last Modified: Mon, 17 Mar 2025 23:45:31 GMT  
		Size: 155.9 MB (155859248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f96fc14e729de4bb894746ac78825b983e37eaf1cd3d103f83e39ecec2e432`  
		Last Modified: Mon, 17 Mar 2025 23:45:29 GMT  
		Size: 58.9 MB (58908461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b6376d55fdffcf69d15c1910c72d6758c2d36f029835c03922e557df39031e`  
		Last Modified: Mon, 17 Mar 2025 23:45:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b62b006df4fba6a53871a545f143ff2bf46d416179af136f1e2cb08e3bcadaa`  
		Last Modified: Mon, 17 Mar 2025 23:45:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0481633737015d0e52c6cb965772ab47996bbe7819ee1e5835482217234a1b72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5143338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffd66f335173086a2a5c773d060eebe5a41b3e8d62658c0a915f254197ea943`

```dockerfile
```

-	Layers:
	-	`sha256:72c9d30fa37d7285c1a7239def94bc92f5ee42610327f122eed4c1b9a2799fdf`  
		Last Modified: Mon, 17 Mar 2025 23:45:28 GMT  
		Size: 5.1 MB (5126621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82e95552355e0d168b9acacde11dd664cfd4402e266eb280d498a4a100db3637`  
		Last Modified: Mon, 17 Mar 2025 23:45:27 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
