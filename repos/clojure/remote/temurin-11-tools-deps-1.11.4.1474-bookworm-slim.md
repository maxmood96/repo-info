## `clojure:temurin-11-tools-deps-1.11.4.1474-bookworm-slim`

```console
$ docker pull clojure@sha256:89fc15248dfebd82749790f8a9369c3d9f85b2c3adc01ae7359551708daa4bcd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.11.4.1474-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7c5ed1aeb8ca8286fb0fc7a484d9bb93382515e5b9962372e6ce0e621288ca11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243701405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ef1ac255a45fd0661ec090433aabb92a29e41653ccebbb9d1c3f71882ce697`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6969288d82173de26f76e2070519761e525362685f1a3ed505974753ede76a67`  
		Last Modified: Tue, 13 Aug 2024 01:11:30 GMT  
		Size: 145.6 MB (145550363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a389f83c8a2c8da2c9b44dd48150452331670b3e8aba68acb464f0359de2b30`  
		Last Modified: Tue, 13 Aug 2024 01:11:28 GMT  
		Size: 69.0 MB (69024165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5668413ffdbd3f7e9b73c205ffb1ebe8fe1afe5c2e72fc53f500414029d59d8`  
		Last Modified: Tue, 13 Aug 2024 01:11:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.11.4.1474-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:975412c00dd50d03f8a6d8c90c345dc0eb299df31b07056f5f24fb1aba63723b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4759102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7acf38f70e10094ad75efe87cd1647438616ed25d35cf075b2a029e49517c18`

```dockerfile
```

-	Layers:
	-	`sha256:82167a3204e5c1c887cebfaf248a9b456b7d9dfb1389205611a322550c9eacdf`  
		Last Modified: Tue, 13 Aug 2024 01:11:26 GMT  
		Size: 4.7 MB (4745164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dcac5424f71a732e40c24051d3746316cf27a513d81a874ebf06deedbe3f157`  
		Last Modified: Tue, 13 Aug 2024 01:11:26 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.11.4.1474-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:df77516712f5f801cbb25741e4d046dfb763a105705053c8e7340dcf58bc4a2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240286741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1e673452ceae9f0fd955474b7987424d5eed843e7c20f708276242c1d271c1`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:51 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Tue, 23 Jul 2024 04:17:52 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0044c6bef07efe98365d4134f1e7365a1e3909e34e33fb33d8bfe3e8273ce26f`  
		Last Modified: Wed, 24 Jul 2024 11:25:48 GMT  
		Size: 142.4 MB (142356420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be38dab9d807d191673024a5daf265be4fb48d5a6699dbd04f66ebb4bb012e3`  
		Last Modified: Wed, 07 Aug 2024 20:03:06 GMT  
		Size: 68.8 MB (68773103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fab342d133c7b415a9aa7569aa891d012d7d037f7b6fbf3735a26b4961bf03`  
		Last Modified: Wed, 07 Aug 2024 20:03:04 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.11.4.1474-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:631e88fae45c70b971be461229e737385de7654c8631d00e4a424fe0960bb920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4766028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630250e8a647548932f727b43739bc0a6964493d13b92c08e739abc3878b0f9a`

```dockerfile
```

-	Layers:
	-	`sha256:93484a032cebc553f7986d2d3d6a61c27142bee854a2c4821003ec8958966b3b`  
		Last Modified: Wed, 07 Aug 2024 20:03:05 GMT  
		Size: 4.8 MB (4751549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87020d7b709ad72141349ce71d12a9eb0cf450249418ce216dbd5efdc78dff05`  
		Last Modified: Wed, 07 Aug 2024 20:03:04 GMT  
		Size: 14.5 KB (14479 bytes)  
		MIME: application/vnd.in-toto+json
