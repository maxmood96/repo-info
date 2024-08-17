## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:8908407f745c1d6a0d3a25f2a5b71a9ce88f6ca6ded851c45927bbc9f0be38d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:398f929585c2eb651fcaa487b8bbaf524a0fd98637a2744c08c030c8ff1237d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.6 MB (248580436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b4423faa61229bc7b8da32623f3efc2295900be9b76acc7a91e85a817aedf2e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a6e63b05df35057f0c2997f1952ac9f337d8f3746991ecdea5146397c18136`  
		Last Modified: Sat, 17 Aug 2024 02:02:24 GMT  
		Size: 158.6 MB (158579252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d3050e1418a82285b656591963f4fc9ae8dd2dc0d9b2697ad8bd4875c33401c`  
		Last Modified: Sat, 17 Aug 2024 02:02:23 GMT  
		Size: 58.6 MB (58571855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5536e2c91671d7545933cabdd0e9d4ac3f231617f198a6c0d11a3af1c1c4e1a0`  
		Last Modified: Sat, 17 Aug 2024 02:02:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b1986c2bdb6d15a46b297e7f16e0eb0c250d096141595df627466d0d867db7`  
		Last Modified: Sat, 17 Aug 2024 02:02:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1805322e43e41664fd7cfeb424c74c1cc11f3bfdcd7b8a3e02f9fd66b2c9ae2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4966741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be1978bb8d635c9d9f18e5e0740076195265dbc318cbf38d44ab4447f8ba811`

```dockerfile
```

-	Layers:
	-	`sha256:ad00f426f408ddf918b801846abc61946a5ed938f7ec61ff4585cf194f71c1c7`  
		Last Modified: Sat, 17 Aug 2024 02:02:23 GMT  
		Size: 5.0 MB (4950532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed915c62d11ca095a53e3e386852bf72497311a861b5e51e7679856450739aa6`  
		Last Modified: Sat, 17 Aug 2024 02:02:23 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:de4d75c0e63bc63569bdc6fd26c2750a2f5b370edf4362f7c4b5863cc244b445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245522907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633b927130dafdd92211b7450a4debb15f04f51e16a5875d393f8bc0aa7e8607`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48070084f696364fb223a70ebd2d666203d7d7caaa67f23a1c573084a896dd9f`  
		Last Modified: Tue, 13 Aug 2024 06:40:23 GMT  
		Size: 156.7 MB (156746205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5f9539206bd434a1bf752f79c25bfbe7c529b7b2b7099d9505b706b6808956`  
		Last Modified: Tue, 13 Aug 2024 06:43:31 GMT  
		Size: 58.7 MB (58699574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcb28f2fa963436796de0e60378b8675637fccc4291c21a17fddcee1aaab7a5`  
		Last Modified: Tue, 13 Aug 2024 06:43:30 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3529beafde10d339eedfe2819f564aebbd5a44a71a11dd2922314024a0d53194`  
		Last Modified: Tue, 13 Aug 2024 06:43:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1ed70474230f29061656228a08268cbac518d358580882bf738d6d2f0419243e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4973686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596658bd57675797ae0b083d4be3a21daeb0aa387e07b497e28c608c774baa98`

```dockerfile
```

-	Layers:
	-	`sha256:12751e6ea8824955679e21bca263680b82eefa99a77656d2b17537224cc5736e`  
		Last Modified: Tue, 13 Aug 2024 06:43:30 GMT  
		Size: 5.0 MB (4956912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a554f6d7130df2ee3c635a491f7048f5289a65332b68c07bdf17e7f47088c834`  
		Last Modified: Tue, 13 Aug 2024 06:43:30 GMT  
		Size: 16.8 KB (16774 bytes)  
		MIME: application/vnd.in-toto+json
