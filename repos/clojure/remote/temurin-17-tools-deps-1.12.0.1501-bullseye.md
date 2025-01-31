## `clojure:temurin-17-tools-deps-1.12.0.1501-bullseye`

```console
$ docker pull clojure@sha256:543193c0edbe8dafd39ea04fce663a0d0b3aa64104eb9b59e03178e768c66221
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1501-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8e824067d4f9f927b578ea59d7d04e593ec7fce1a02a49c18f65c88fca27d3d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.5 MB (267468012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8893d9e7dcedf84597251ffb27c79248a49f16077993fe8a4acec582d23a5e23`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3491c374b8855ec5debf98a07bb4889ca169d746c85dae1b541f6e1bdcac23`  
		Last Modified: Wed, 29 Jan 2025 20:27:38 GMT  
		Size: 144.5 MB (144536692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c334d544226e58827f2ef06ed921c52bed21ca892998b5e7cd37f89293d467a0`  
		Last Modified: Wed, 29 Jan 2025 20:27:37 GMT  
		Size: 69.2 MB (69191113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31067e9697b37a64aac06c12e30f7cee00622e805bea9740263b3eebfbe4a91b`  
		Last Modified: Wed, 29 Jan 2025 20:27:36 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4653df7ca1cf5e0aa2cf07fba082b131114be5c2ebcb38ea62dd7574c86cb0`  
		Last Modified: Wed, 29 Jan 2025 20:27:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1501-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:76d7f3ac70da49363bc1e61bfb6abc0b430bb1545af393fead096afbba4ca452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7220378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a329f19b2c614a5eb92f5a280f94ea2089f0f314e1dac6ceac9ad8608420d16`

```dockerfile
```

-	Layers:
	-	`sha256:3199571c9542d8602854e2584751046642f76f713f0a9435c7c414828b26733a`  
		Last Modified: Wed, 29 Jan 2025 20:27:36 GMT  
		Size: 7.2 MB (7204557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecc6b19cebfcc1f6085dd40f79c927fa88f1db6194882338939e549653e27b6b`  
		Last Modified: Wed, 29 Jan 2025 20:27:36 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1501-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:17a248372c6ac8b4cb4a8a473c9e9ae7eddf3880ad2c0bcd9ac54b9ecbc72e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.9 MB (264918950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e31705393861168daa8e0d8d9de3bcd130ed4a57432ac7e04e3b693f6561beaa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a83cadea50845dd03abea7a3d6efb27e951eb9e87f1d5e10c0e89572e38b27`  
		Last Modified: Thu, 23 Jan 2025 02:46:21 GMT  
		Size: 143.4 MB (143360991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c269e18cbcc7c6f5a22d051b05f8155ff89382f6ac7efe1dc7cfcd23f90a59`  
		Last Modified: Wed, 29 Jan 2025 20:49:41 GMT  
		Size: 69.3 MB (69310859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12b876c5b234b955ab34a2e7c6c1ddc8920cb235b94910d302ea013c25df299`  
		Last Modified: Wed, 29 Jan 2025 20:49:38 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6c88368c6b30bb6a150e930e3097a10c9ad5d2f190aa79a6e120084c9fb9b8`  
		Last Modified: Wed, 29 Jan 2025 20:49:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1501-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2ce8b20ef16c328be4211fd85949b933cc6db3e7179c9d0fd98a0f7bd677cb2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7225595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea0ebddd6cfebe99b1f395529f9a5e6bd3fba8d8de43ada6eac8609f68bee50`

```dockerfile
```

-	Layers:
	-	`sha256:22bb2d7e26a442e58aea62cd7049a3b7610da8298d876fd8d5a2b2d648c0fed2`  
		Last Modified: Wed, 29 Jan 2025 20:49:39 GMT  
		Size: 7.2 MB (7209656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99a1e498034457f666e3175a2a7163a360a78d68898ee281e272d9cccf7e42b6`  
		Last Modified: Wed, 29 Jan 2025 20:49:38 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
