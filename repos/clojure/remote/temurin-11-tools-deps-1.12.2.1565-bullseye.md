## `clojure:temurin-11-tools-deps-1.12.2.1565-bullseye`

```console
$ docker pull clojure@sha256:841cb527242e5f61eed39ba3c13de60ba2b27c94b874539fc03af6dd66ce1b24
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.2.1565-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:252348cb388361a06498642b1e1d705bf6a6351ffa1bb74cfe3670479ba64aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268970865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85ca431b6729f621842bd84543b7bd619c0810dd12b4ec24e374dd67e99872b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1b375f938c9f1ad67eff1d80717f8c34ca50b82830ae94665bf4e76217ae1d`  
		Last Modified: Tue, 02 Sep 2025 00:17:13 GMT  
		Size: 145.7 MB (145658232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c7b735378a7b2fb6425f035ce9998162676fb71bc3e16f522ef0ed2a14b11e`  
		Last Modified: Tue, 02 Sep 2025 00:17:51 GMT  
		Size: 69.6 MB (69556643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee654f7929fa46b4ed8b2445398675a6170f7ef34ba55cfbf0f4570330cd46d`  
		Last Modified: Tue, 02 Sep 2025 00:17:40 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1a1a17551ae6ec12c8a450fd314e47f6b2a5db532d1e471e2f46f3a736ca2927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aebe2516630d64774163ee0070c89776cb2802559acdcbba41110e2c4a41ec9`

```dockerfile
```

-	Layers:
	-	`sha256:a32c8ce23ef77a90f69875e7bd32974f903cb492d9de9c068a2bb3d9b08cccf1`  
		Last Modified: Tue, 02 Sep 2025 03:35:33 GMT  
		Size: 7.4 MB (7415808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b3ecb9f2d16c834f00fd2d3bf06321cc59b022a66c0573413c5f91635694b45`  
		Last Modified: Tue, 02 Sep 2025 03:35:34 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1565-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:71860bef0fc3a5af968bbf6ce2cec2b1c5c3a45f9dc3bbf57129936df54f9f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.4 MB (264393451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9481f2e9b28ef8355a0c01a058414ea72f011209763ce3976f76b7fafd5662f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61737f5a5e55be362f75457232f49e7bc4d9d42eb74342ca632255e8150a311`  
		Last Modified: Tue, 19 Aug 2025 04:11:00 GMT  
		Size: 142.5 MB (142460513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58ff496dab8b280e4974c9d162e9c6511f1ddbe58a6086ed7785eb7725110a5`  
		Last Modified: Tue, 26 Aug 2025 23:46:23 GMT  
		Size: 69.7 MB (69683884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a174d324a5755660cfc6b601f8e0106f9f05552939107b61548e3c57fc184ec`  
		Last Modified: Tue, 26 Aug 2025 18:27:07 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ce01305e91494516fad0ca129f407876c06ae9b2380d236087e11ff140942727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c787b34a1f88b67f1ac36e767fba69754c9bc13937b62e0a56ec0748bc95dc7b`

```dockerfile
```

-	Layers:
	-	`sha256:d984f75590cc156744fb6fff648a7b38db54d32825a51e256a9e3ba7e15b4f63`  
		Last Modified: Tue, 26 Aug 2025 18:35:26 GMT  
		Size: 7.4 MB (7421525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1cd630ff0d93357232293705ac83d0a04ff0b80b50043dc6f5ca42125fe9289`  
		Last Modified: Tue, 26 Aug 2025 18:35:30 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
