## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:b82667a0ca3f09fa8b120e5bd6fe97ca162698fe40daaa43431e6ef8bfc48794
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1fd8bd16616e8bbe2b7864662db4aa5ab0b873a41fca58b1f76d2cf7bf884083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 MB (247302575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f924f4078afc237fe7c966e98af37ba49b4c947b11c5856e576e404566c5d2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:19:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:19:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:19:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:19:59 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:19:59 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:20:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:20:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:20:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:20:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:20:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a508e71ec02e7a220660db00e74bc645ae2355d0ffcb1fdf41c1501c082fd0`  
		Last Modified: Wed, 22 Apr 2026 02:20:36 GMT  
		Size: 157.9 MB (157857104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b005290d5eeb19ef32d42f7ae5d50fd86f864aa4320a3ce5fe9e51123dfe4a`  
		Last Modified: Wed, 22 Apr 2026 02:20:34 GMT  
		Size: 59.2 MB (59186497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8add59255586f714b72c82e19c0ca6e6da60ce017bd5e705121f62d65a93dc57`  
		Last Modified: Wed, 22 Apr 2026 02:20:31 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5182ff007a5e444bb20f5af9cbbb133a9eebdf5b1148118b5fe794c138a67c40`  
		Last Modified: Wed, 22 Apr 2026 02:20:31 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a72b9fb6a9dca192626fbca8258d9c4e41149e9152cc72d114c3c32a79b2b5b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5337741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1070746e80a0dbf38dc2c174a069fedc0ec624ceeff28e7598f0d8955f8097`

```dockerfile
```

-	Layers:
	-	`sha256:acb64e1fd34db826f9e42acb67732956b8f92c0ec4e56afad0fcfd0ebf25d2d9`  
		Last Modified: Wed, 22 Apr 2026 02:20:31 GMT  
		Size: 5.3 MB (5321905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec5920d7abd0d58e146e81def3797d9827ccecceb98c9105a16fbf484008abb8`  
		Last Modified: Wed, 22 Apr 2026 02:20:31 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4c5a48c5627010ac472bc8c27fdb2ee78ef3dc4597c77aa37947ee3869a39fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244535915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92733cd28410225c2c73c0b579f4e2d9b85c1f9edfe6d8a41ad013a42f2e626`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:26:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:26:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:26:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:26:39 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:26:39 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:26:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:26:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:26:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:26:53 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:26:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf2f299b35f3aa2555348553f122da909630c304c4c6f7eee6c731cb2b93bca`  
		Last Modified: Fri, 08 May 2026 00:27:19 GMT  
		Size: 156.5 MB (156461247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8151fa76a2dc6cc61e37ddead7e0e81cfa7228519350a077dae01c7ccb177794`  
		Last Modified: Fri, 08 May 2026 00:27:18 GMT  
		Size: 59.3 MB (59331115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65be3f74f84b4423b61d05371dd77b51bbb11a5a5efda0e4081d191ebdac5ac`  
		Last Modified: Fri, 08 May 2026 00:27:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a06c36066fe15fb911b0cfc08adf2a3febdf0c77d3b9d342b29dd7c2046bc0c`  
		Last Modified: Fri, 08 May 2026 00:27:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d894d1a5b7ecc6d305db41b4386652e30160ce2ce58d99c3dd411870d7234193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5344372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12eba352581c89975cf3e4297ad624f8eff0ce779677d041d623518d0e4c55bd`

```dockerfile
```

-	Layers:
	-	`sha256:37fc55a401df54821b3c4b33fe60f535ea402130b7be8401c245a4cdfd40feac`  
		Last Modified: Fri, 08 May 2026 00:27:15 GMT  
		Size: 5.3 MB (5328264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1b7361363723c7efc5a23f69fb5299d038c896d48f656ef31c9896ffba6d52f`  
		Last Modified: Fri, 08 May 2026 00:27:14 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json
