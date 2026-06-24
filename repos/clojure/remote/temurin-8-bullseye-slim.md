## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:319008ea8f6175792831fe97c0e29a5b81889ae16c899052c261963c2972cc73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c44e9e2a539a5fbdfde328bbd4e90b7380021e2f5a2d00e72eff529b7d746be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141559254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65c0a579e2ea69f53a6a2ab8acced81f1f8ffdadc8d21406ce6f6c96a89de56`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:14:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:14:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:14:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:14:22 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:14:23 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:14:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:14:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:14:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0251c4232e4025b51352f0bb7119fd866d4a6a62861f09baea6fe5af4c6eee59`  
		Last Modified: Wed, 24 Jun 2026 00:28:14 GMT  
		Size: 30.3 MB (30259447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ad780ed165b0b0b2e440cdf13a61617a97626cc344e9277eb1528417be9c6b`  
		Last Modified: Wed, 24 Jun 2026 02:14:53 GMT  
		Size: 55.2 MB (55198723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:facb478b12822d4192342ef0f360057e909710ba80b8f4a6549e4a67e61b27f4`  
		Last Modified: Wed, 24 Jun 2026 02:14:53 GMT  
		Size: 56.1 MB (56100438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0a2623bca8876d9a21be46913311f338022e0704167d8f563f0f11b4d025fe`  
		Last Modified: Wed, 24 Jun 2026 02:14:50 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:584d08d0cf57ebb6571dc76775fe738460baaf68e0cd98dc07a98a0586aedef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5452611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ee79dfc45ab46d3d0174c4da44e70cfb11cf1abbc0d2b599894a56bb1af539`

```dockerfile
```

-	Layers:
	-	`sha256:bf7246e024309700465230adf2c33d9dc5bab562223b518a539c7a723bc87cf0`  
		Last Modified: Wed, 24 Jun 2026 02:14:51 GMT  
		Size: 5.4 MB (5438209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e92ff5e04b23090eec378d15b549efd713c92501a70e7207f50deb328178ef42`  
		Last Modified: Wed, 24 Jun 2026 02:14:50 GMT  
		Size: 14.4 KB (14402 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:eac2af48bc0df487259c339cafa4a2171c9354ea1be3769bc3d5945841ea2847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139288001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a248f0778beac0720ed5f99680401d25400f0b91979506af4b70037fb1772a8f`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1782172800'
# Wed, 24 Jun 2026 02:21:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:21:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:21:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:21:21 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:21:21 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:21:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:21:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:21:35 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:58009b48fe731a10341c4f5f98dfa280afd10fa34cc71961411d37e306120dd0`  
		Last Modified: Wed, 24 Jun 2026 00:27:56 GMT  
		Size: 28.7 MB (28746926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd229bbf1257f5b8e5cdfc793a40e58d6b9691825ccda6474fec571ddce2b6bc`  
		Last Modified: Wed, 24 Jun 2026 02:21:51 GMT  
		Size: 54.3 MB (54272901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e3fe57106e34e8e61af9630c804263b9d2abc51db7d48a137e609a15eb9b5f`  
		Last Modified: Wed, 24 Jun 2026 02:21:51 GMT  
		Size: 56.3 MB (56267531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e92b57834015edc687c6ad4488da6a052d98011da101f85164b3f2410475376`  
		Last Modified: Wed, 24 Jun 2026 02:21:48 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5c6fc0ee88624f22e8f313522eafb086c26e077d6c07ee2e1e17979a9e5918e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5459161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb982b7ba5a8fa0f79b26e36d0beb65a67330782ef32aef21cfcc8f7f26ababf`

```dockerfile
```

-	Layers:
	-	`sha256:5d147c3d6e9fb7724657690ec731d34896f3213694b90d16f6b5c48112e1c724`  
		Last Modified: Wed, 24 Jun 2026 02:21:49 GMT  
		Size: 5.4 MB (5444641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed5dc2850124f9da7e3f5e4959158f50fc347b8d48bc05b92fcd98ba4ccfa0f0`  
		Last Modified: Wed, 24 Jun 2026 02:21:48 GMT  
		Size: 14.5 KB (14520 bytes)  
		MIME: application/vnd.in-toto+json
