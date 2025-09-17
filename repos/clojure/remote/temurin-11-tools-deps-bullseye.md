## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:af2cecf70d9116179c489358074ef74f328e854391e3aed969a3e6e37b09581f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:288321f07b12a1414031c20f6ccef8c3dcb3fc48f65fa0caa6a5dddc2c7ed87e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268971052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf27036089ceba3cc29f0b0fda70210e87409f6f668c4ed8351d1089913b8f86`
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
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe8637fc732129e530575821f96832b956183412ba628be6423421d2ba9f1fe`  
		Last Modified: Wed, 17 Sep 2025 13:10:18 GMT  
		Size: 145.7 MB (145658256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43268f568ba91754673817c9123d4da2a888754709072dac3beba0bcf28f187`  
		Last Modified: Mon, 15 Sep 2025 23:26:01 GMT  
		Size: 69.6 MB (69556754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376d6818a46c6b5606c0f0b9892104537dde013ba5ab2d77c588ff13cb357fa2`  
		Last Modified: Mon, 15 Sep 2025 23:25:44 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:13161eae956c8df0a271135d2bc8969add92d577be12674efbd45ab0212c0081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6cc4b384d23232830c1dd2d7c2ce2223ced28d8dabee3b5494b53555e53d32`

```dockerfile
```

-	Layers:
	-	`sha256:d4ae20b13786d9576e6b5b6f4319c574dc2634504fd3fa9ddead55d439d1c437`  
		Last Modified: Tue, 16 Sep 2025 00:35:41 GMT  
		Size: 7.4 MB (7415808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7dc9a07a04bc7ed68f7506bd922dc4519cfc467047638c118ab0788ce8f0606`  
		Last Modified: Tue, 16 Sep 2025 00:35:42 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:842a97e9f5f21132fcdd287849bc85fc6788c09c94aa58b96af39392b3e46bfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.4 MB (264391652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8c8753951089e6480f0cdad1089d457491902b710eb1deed7e63a4858f027f`
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
	-	`sha256:7df02cb4a974a4e8a9eb65ffcff7274f9dca341d29aaa763294c42e49805ca19`  
		Last Modified: Mon, 08 Sep 2025 21:15:41 GMT  
		Size: 52.2 MB (52248370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969e936015dec832f16bf00131cd85957bd67a6674d96869ce8894c17fa9d841`  
		Last Modified: Mon, 15 Sep 2025 23:25:47 GMT  
		Size: 142.5 MB (142458730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d7851b7db99a177cb169b1cbe8f8798a9fc175f5b80be93fae8098f274f603`  
		Last Modified: Mon, 15 Sep 2025 23:26:09 GMT  
		Size: 69.7 MB (69683908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416061c94a2d85f9f03a9e085cdfcd349f94c49499c945f56de7f5fee10c8c7b`  
		Last Modified: Mon, 15 Sep 2025 23:26:03 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f26b3b9ec47a908ccef863cf3351bfdcfbbcee1ae889c2cb59f6657cc59e5a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e75593358f308c2babccad4294ea7b7ed295fb5cfd14b097b34f3a5276f83ac`

```dockerfile
```

-	Layers:
	-	`sha256:d254e63404eb3b83103f28ba78d3fab3a9139b75f45340974a791929be7368ef`  
		Last Modified: Tue, 16 Sep 2025 00:35:48 GMT  
		Size: 7.4 MB (7421525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8055379d283a11c5865062a23fffd69a354cd02526408026c9e739ab882a14d`  
		Last Modified: Tue, 16 Sep 2025 00:35:49 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
