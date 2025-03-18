## `clojure:tools-deps-bullseye`

```console
$ docker pull clojure@sha256:c77e046c6f2056faa557d909387142faca448d1fdfc92b4f3ba55bcea0c144d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e8aae18dd305e49b0139c00322a7f77af2d338e54d43f470742e0ee494a324d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280512180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5555ed3d14a387fbe9ba2b7a080eb988cb0b51a48552798faea632c954d999ca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f90bb061116803b94a10922f61cc399187feca6c7cc5a113c6bb85a0a27001a`  
		Last Modified: Mon, 10 Mar 2025 17:41:49 GMT  
		Size: 157.6 MB (157585883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdee44983a3b8d58f4b938dae1f024d3240b9e5f2080f5f404f2de110ad2c3f`  
		Last Modified: Mon, 10 Mar 2025 17:41:45 GMT  
		Size: 69.2 MB (69183851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f407704e8e71bc5af6cadde5184c5f77a03771d8789a09d12a66659f3fac77`  
		Last Modified: Mon, 10 Mar 2025 17:41:43 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3374524fd1496d77a7ad7e824df1bfcd1f4ed717a0bee431b3cb53363896da`  
		Last Modified: Mon, 10 Mar 2025 17:41:43 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:284126dd352193b47a79c67f6807d054144ffc57cb16532274ac9a77579b2ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7224829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b8110a8ae8c5c41ef21072bc572c499148fe429bce7c86a6759b60cd81ebdf`

```dockerfile
```

-	Layers:
	-	`sha256:b3caebf8c8c84ee9130f29656ee3e847dfdde56f56222187a8890743ab4e5e81`  
		Last Modified: Mon, 10 Mar 2025 17:41:44 GMT  
		Size: 7.2 MB (7208333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44c7713b7deb2921f2624a179de349c8ff3278312858c70198d29c1b91963520`  
		Last Modified: Mon, 10 Mar 2025 17:41:43 GMT  
		Size: 16.5 KB (16496 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:651c718b48f5a69d14a1d4ee68b4e219d09110a8fceeda1ae10d61b9fafcf37b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.4 MB (277414556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302f44ea0cbfcb4bc7d8c2c0b2ad08d032e4575462efa46ca7007351c2454e90`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636169bbd96dd362eeb31f1fee1e9c6c676c31f3812c0ffaa52e7a7ea55fcd1f`  
		Last Modified: Mon, 17 Mar 2025 23:47:20 GMT  
		Size: 155.9 MB (155859250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492de70488e419281d48722a1b0f622d4104c51b82c0f4f3af68c2b7d56a2642`  
		Last Modified: Mon, 17 Mar 2025 23:47:18 GMT  
		Size: 69.3 MB (69305872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb1333bb443ed84b361718acecab86d11fe9eb70c08d28cbb1623ad39dec449`  
		Last Modified: Mon, 17 Mar 2025 23:47:16 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e539d1026dd3f96a944271788c82c7da5156bf71cada60587bcb9244ebf15012`  
		Last Modified: Mon, 17 Mar 2025 23:47:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6363870e8c31bc92554702080d764a0ecc412f206effa37025440b1592d31851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7230094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a644787e435faf27cf43ef06e8be8e41fd186c60950b072e0f3a6984bdba775`

```dockerfile
```

-	Layers:
	-	`sha256:71b1fe3803b45527d28d09e835b8ce8f2222162e0cc5a4c597158b8c6b23dafd`  
		Last Modified: Mon, 17 Mar 2025 23:47:16 GMT  
		Size: 7.2 MB (7213456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e33b981fb6ce0ef12fc184cf0b2485af7f01165086436f9211eb69ff7380b3a7`  
		Last Modified: Mon, 17 Mar 2025 23:47:16 GMT  
		Size: 16.6 KB (16638 bytes)  
		MIME: application/vnd.in-toto+json
