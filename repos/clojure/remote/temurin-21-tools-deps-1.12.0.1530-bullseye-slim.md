## `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye-slim`

```console
$ docker pull clojure@sha256:312a6cb6b3baff4522bb3406c5d3e50ecf58e6f9d6469f6ccef4fdbb497c7d18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:93da8d035d097a9e46830165c7d43d3d93db3b9951f3390c5276e8a1e626057b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246882943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef5a4a9835ba52ed3a45cf9fc360caf51aacb02e3c7479a7b5e62389a5349a5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51211fe73065b4e1772f8d452385e33ea70bb3d11aa6474d288d9083285fd89e`  
		Last Modified: Mon, 28 Apr 2025 22:08:17 GMT  
		Size: 157.6 MB (157634414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ddd9917a0dcd88459f329c4f34afe89c5c811218f4d04d949031ab54027b007`  
		Last Modified: Mon, 28 Apr 2025 22:08:15 GMT  
		Size: 59.0 MB (58992889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8354ba0011900ad8b4080715b249ca62bd925b7183c6ce89cd36699d4013493`  
		Last Modified: Mon, 28 Apr 2025 22:08:14 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e3a9942bfc36a47ab084516eeaca1fc198c7a3cce3e01aa4240026f9ae7699`  
		Last Modified: Mon, 28 Apr 2025 22:08:15 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4fd34247c77a12a61dbc20f4b5959cabb96747c46692a77ee6d7a4a7fbd0ecfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb23b2f461ef13d728cbe1d7c36ed08801b2a39128d8e200de6a0fb430cd96bd`

```dockerfile
```

-	Layers:
	-	`sha256:0fd5d46b6b0d30d30a763a2ca12acf760c0188ab2fc71fd8b5cb9cbdef1c6753`  
		Last Modified: Mon, 28 Apr 2025 22:08:15 GMT  
		Size: 5.1 MB (5122865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f811d3ce93dcb351b3a9091383a191434a2b7b4f79348c4acb20ebd62238c652`  
		Last Modified: Mon, 28 Apr 2025 22:08:14 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:15d2c194b75aea3f21dcc50563031a4c276aa1e343ac336d53c277eff1ea114f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243806652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df83d879a1ac0b09505011ffdbb828a570824f4ca4d1d61c7941f6e42384cb8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
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
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6ea0ce4481c6c59b9cdc12bd913c4b5bafca5da592cdedda4048ea90395fca`  
		Last Modified: Wed, 23 Apr 2025 18:09:18 GMT  
		Size: 155.9 MB (155928792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb6181e21004275c098d7ee7b36609911106b4eea148eb3dbf3b85d1a80d9ab`  
		Last Modified: Wed, 23 Apr 2025 20:00:39 GMT  
		Size: 59.1 MB (59127314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7290008066b80f0e9e3d3f707f7f9dd1f89b7ce850391453ff6c1a74f0e9bdc9`  
		Last Modified: Wed, 23 Apr 2025 20:00:37 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef59f216b41ee2e80b7708038c65f6c5d549e27a283e27e8be6e58d973ba50a`  
		Last Modified: Wed, 23 Apr 2025 20:00:37 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5fc716697a0807e68b6debed4fb80ce6671925930906664dbee7a30c653573f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5145284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5124ec248fc408c975b4f71e238a92d8588e9d1919f11906221ac9169d09c6`

```dockerfile
```

-	Layers:
	-	`sha256:0162214ca18eb0b02ba22c00d4491cc56fc90b6523a5fa6759af492d86d84aec`  
		Last Modified: Wed, 23 Apr 2025 20:00:37 GMT  
		Size: 5.1 MB (5128567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6fcd9001b0ceeb97d4b23c704a600bb4c055d17cf9dea693816410e12e39983`  
		Last Modified: Wed, 23 Apr 2025 20:00:37 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
