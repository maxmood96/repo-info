## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:396b09b0dc0740b564d31d703736330e11f9abde1a94c30932adb94b306fa152
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b91f7cd13727595f2109427042d5fe4dfd340034d9e0a5a377318c0f116fafd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233609777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa2ffe746c46aa1f3a7ccb2960bd8b07b1a6b01860f550fbf25bfb85e0193cb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70d8f0d47dff0ce19b8d433830013cbb65165ac9cf7731cd27c9d558068358a`  
		Last Modified: Tue, 25 Feb 2025 02:33:16 GMT  
		Size: 144.6 MB (144566545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7df0a8272e272daf4dbc52a9f76ae6eb8a5796949c357975cefcaa9285f4e2`  
		Last Modified: Tue, 25 Feb 2025 02:33:15 GMT  
		Size: 58.8 MB (58788258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9760ef131b03e1eedce2f10d00214b46c90ed0f5caf91b25a3d97665c2062847`  
		Last Modified: Tue, 25 Feb 2025 02:33:12 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8c2ef81e8b71ae677a463bd828000f811e50ff9ec71e0813f2494face6a5b4`  
		Last Modified: Tue, 25 Feb 2025 02:33:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:427020e08e08b4306bf584e9bf08f6739b5cd46d3089f88d5e5a6c643f6da375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c601edbd3091dc8bf496c162359d6b2500c06fa1f1af3b83864475840c7c7b`

```dockerfile
```

-	Layers:
	-	`sha256:b912d51dd8fe300e613aa51fa2097353209839b3df2753d2da7d8ad0424dfcdd`  
		Last Modified: Tue, 25 Feb 2025 02:33:13 GMT  
		Size: 5.1 MB (5117067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f09a1048f70f0f2f3464e3d6c5416e069cb474c9d80d8cda6a020a7ecf10a1b3`  
		Last Modified: Tue, 25 Feb 2025 02:33:12 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:588d3e693161766c43c1cb417b9d94955ec2c81ee8b49e46cf9b97b6decafcb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231112280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f6735622c42f97706c454bb0fa7696e85e4c08c9f054097b774844ac1ef32aa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c69ddb8171ab442b4c78f6ba1c213d7f0faf66d684d8219bf06734d2357cc73`  
		Last Modified: Tue, 25 Feb 2025 06:07:16 GMT  
		Size: 143.5 MB (143454713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7097f01e196da8ec8be94a9f28cf3ebded7884995a0830c34e3bf372357e9a`  
		Last Modified: Tue, 25 Feb 2025 11:08:10 GMT  
		Size: 58.9 MB (58910537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b778056790985d15df5256719b78625ab5bab506804aa80a0555ea8e1e9a619a`  
		Last Modified: Tue, 25 Feb 2025 11:08:08 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d8d937b52497ddb577bcd7ba001e6609d1a501df872ff9e53638456a7f1c15`  
		Last Modified: Tue, 25 Feb 2025 11:08:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e4f84a87b725f4a0f3e73539b07b678ab74d010a3c740eb4821f765ecd435aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057007ce580374a9c1e0b8043fd61a77dc0805fc5771a7f50a010820bdab7c40`

```dockerfile
```

-	Layers:
	-	`sha256:bbb7fd612938a4394250790de9fe6f599bd565fd9e2f6119150da680f3d52fe5`  
		Last Modified: Tue, 25 Feb 2025 11:08:09 GMT  
		Size: 5.1 MB (5122799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ae65d28cff1b185bb9ca350653de7ae50def9dbdcc711fed434cb1a1aeb762a`  
		Last Modified: Tue, 25 Feb 2025 11:08:08 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
