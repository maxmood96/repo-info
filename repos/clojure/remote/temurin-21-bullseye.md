## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:3d466f50287fed1500e4577645ea64dbae9e4ba9e7dab00f12b838820721fdc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:de9dca5a2258848df661542dce7608228ec4e81758c97e24fe96cd67b936cd08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280730230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9560da96692013f491c487e9b993875500efd7bd14baaaf9f9929add49ae03`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
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
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b732fade28be14de0c0bae987afd4df0b1561744cfd195cc0a7414be18ac3f`  
		Last Modified: Tue, 08 Apr 2025 01:36:40 GMT  
		Size: 157.6 MB (157585893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013b4cf70a7ceb08895a85985ce7e1015a738c2eacbc4d2f4b9b46830a79de3c`  
		Last Modified: Tue, 08 Apr 2025 01:36:43 GMT  
		Size: 69.4 MB (69394767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf9d1462907c1b441c988543dcca3a398b6e8b99d7131c40d8da60da3ecdf1c`  
		Last Modified: Tue, 08 Apr 2025 01:36:37 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563402afaf1a48b004cd660a31056535c69455609686fcc2d89aedaddb6710c7`  
		Last Modified: Tue, 08 Apr 2025 01:36:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:187113a6f1b89602445744d2c27d2a96fed5c1d5557e213f2a804b38cabd3567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7226776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077a426586ac05fe0d3c774db16cc986bc63ee7750020f46c18eba2f4b77d69c`

```dockerfile
```

-	Layers:
	-	`sha256:de87881d02564a01e0273822fc1a825317449f27be3c995b3ffe5a19a7d83d65`  
		Last Modified: Tue, 08 Apr 2025 01:36:37 GMT  
		Size: 7.2 MB (7210279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdfe19f2c6917beceea4407c06a798478b0b6e9ba848404b3ff7ab273b4f0ad2`  
		Last Modified: Tue, 08 Apr 2025 01:36:37 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

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

### `clojure:temurin-21-bullseye` - unknown; unknown

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
