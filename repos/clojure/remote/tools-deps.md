## `clojure:tools-deps`

```console
$ docker pull clojure@sha256:33c6e87d2d8e33191efb517b63efb3d1007b3d163744777f4d8af7474829bbfb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:bf15ee94d24a8fe837520a20386c379eac36b6b3cf4fb6b88631c87da4306836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 MB (287048505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5695e8a3d237d41dafbca7cc8ae6dde6a05dfac4a30ae2346e0f697579b2bb75`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:7cd785773db44407e20a679ce5439222e505475eed5b99f1910eb2cda51729ab`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.5 MB (48467838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3248bd232de03b5bda25a0b2e78c525e8cd21f373d956af2aabc00df226c2eb6`  
		Last Modified: Mon, 17 Mar 2025 23:18:15 GMT  
		Size: 157.6 MB (157585892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14af5fc4b33ba8a50397d3f0b828235def111b31cf05b85a002dae24024073a0`  
		Last Modified: Mon, 17 Mar 2025 23:18:14 GMT  
		Size: 81.0 MB (80993733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c38f7aa25cde6668fe312fd34c7f46b5094a5a30d3e896dba09c4105b1c885`  
		Last Modified: Mon, 17 Mar 2025 23:18:11 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abc4ceb2a56154d34d543be4dce2df750a320dafffc1aae15e31318aa872c78`  
		Last Modified: Mon, 17 Mar 2025 23:18:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:47580487496958860f065d1c0ed8c1e9498956f4c916ed4928c49c37d5167555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7194031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cacd27488256f5cd72621eafae862ff9f61159b962fd09c7cdad2d503919ce6`

```dockerfile
```

-	Layers:
	-	`sha256:2e20bde058fba76f437e50d6e3e1bcf26200f2bd7fb9ee1b24e2f1213d2411a6`  
		Last Modified: Mon, 17 Mar 2025 23:18:11 GMT  
		Size: 7.2 MB (7176210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40251ba096721399437fa8fce98732d0216c4757bd1a18d1fe4c5ce27bf2abad`  
		Last Modified: Mon, 17 Mar 2025 23:18:11 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b27070d5fba67237683abfd4e4883109683e1731364af192407f025d0eeb2b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (285007760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd0efdeed5d28346be9e4b121303e07c1a530ac24379ebff69d1fca8b90d8d8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeefa516d3f68b625053d7ffc6bf700f8016157a685ab86fe0d07456ee280936`  
		Last Modified: Mon, 17 Mar 2025 23:51:25 GMT  
		Size: 155.9 MB (155859256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249b3c3c22a5cadb196da1a98f3d956cd16310fdbf248ea5e6d7d1298512304e`  
		Last Modified: Mon, 17 Mar 2025 23:51:24 GMT  
		Size: 80.8 MB (80842609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc8e1c2fc5ec575b8284ad34beef2fee8f2c0bd127e993b9b1e975e4d489928`  
		Last Modified: Mon, 17 Mar 2025 23:51:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecddc602048c38589863089c44bed07922e3a18e312c745efdc1da973e2cafc5`  
		Last Modified: Mon, 17 Mar 2025 23:51:22 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:45ee215c8a9a9602a10b5a7d6e37a6980933d34b2884daa961036717f8cf467f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7200056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9660addf5796939e66d34da94a48c85223f45ab4a1b752a2111d95f5799a597a`

```dockerfile
```

-	Layers:
	-	`sha256:d9ea6cb43158598eb7889998111543f5fccf674ff6b6c9a0e70dcb83d773d6e4`  
		Last Modified: Mon, 17 Mar 2025 23:51:22 GMT  
		Size: 7.2 MB (7182045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a681e6a56e15e368ec4a4baa21413f75249b0f040ac7f94fd430e1199d20657`  
		Last Modified: Mon, 17 Mar 2025 23:51:22 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json
