## `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye`

```console
$ docker pull clojure@sha256:1dad3b34e5b0bac5c6a14ff0323ca93cc7d16bcf67555b3a1aa74cb2028d3a5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8402af9b3b9b89d8f42af2fee76bb39c87407160c122ec7184e3b678feab3863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280511910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6593d17e216706c28f9fcab8d4b3899612b2e3d65afd714e8caa5615aae5eb6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:8d1bfb80edb9306e3de72f4095daeae4c281712482255562f2e236ae85233e7d`  
		Last Modified: Mon, 17 Mar 2025 22:17:19 GMT  
		Size: 53.7 MB (53741275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52b7fea528eb7e68130795fd6442c00fb0877015813384cd37c5727e6e5ab60`  
		Last Modified: Mon, 17 Mar 2025 23:21:20 GMT  
		Size: 157.6 MB (157585894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814497f579b5531582a2b0e2e8e732a44175594fa1665211072437f8fe8df833`  
		Last Modified: Mon, 17 Mar 2025 23:21:19 GMT  
		Size: 69.2 MB (69183702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8ab16a3f8c19b67165e13278e4ed2373f788c324ff279a70f696b52c61d0cc`  
		Last Modified: Mon, 17 Mar 2025 23:21:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96963b35057e791235bea5b591533d82d37fb2c1e737a8cca6d1b84143257ad7`  
		Last Modified: Mon, 17 Mar 2025 23:21:18 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:26c19972a36b9449f0cd0ede478fbacda4f9498e7702c4ff6f2d7412ca123df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7224830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d5f47298fcda40e06f3d955af29af4b5bc1db77753f9f99e7529ea30062992`

```dockerfile
```

-	Layers:
	-	`sha256:d424a95a913f0d76da1ee9bfed25a68554521c347822081b6e42074c1b1d2172`  
		Last Modified: Mon, 17 Mar 2025 23:21:18 GMT  
		Size: 7.2 MB (7208333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14bdeaa9b0511714082f34af6cca20afd74c93bee7b5fcada56e50917f3bd6b6`  
		Last Modified: Mon, 17 Mar 2025 23:21:18 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye` - linux; arm64 variant v8

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

### `clojure:temurin-21-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

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
