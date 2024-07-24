## `clojure:temurin-22-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:df994ab7e73d37589047f6af1d59ff7bc5f2df7e402b1a756074e9229c28da3f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:70254c58573071b70b4ecfcf0bf330fd5488be3e83a06c0c95a54a9f98c651db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246534966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d401186bc61fc31d3094bd1ada6cfcd56849d994f07d71f5e30aba2a3e15b9a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac8c73f1cedc60c4faef387182b05c1c58630284d759a2639d6c464f80b9176`  
		Last Modified: Wed, 24 Jul 2024 03:04:43 GMT  
		Size: 156.5 MB (156481594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f7e9df9c1b2b43b8c4a62f0fb325eb2eb76c914179853e6e69911a502858a5`  
		Last Modified: Wed, 24 Jul 2024 03:04:41 GMT  
		Size: 58.6 MB (58623999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a333f0431e4b574d498dfdecdb6b7b80aa72b669cb87f6ab8496a73682cecca`  
		Last Modified: Wed, 24 Jul 2024 03:04:38 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089eba102420634f8e81b6bcda27ed79c932b5f8d82e4dc9adb95d7e785d4af3`  
		Last Modified: Wed, 24 Jul 2024 03:04:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8818d2fe5ce40874315a50ccaab78010969a0eeef8fd8edd4a222ed50433b79d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4965333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e8d95e4ac7cbf194eec4720db08cb8ca78e4f206d06cb8b52ed55275f4e0d4`

```dockerfile
```

-	Layers:
	-	`sha256:6699b01afc5cc89291b3192be646e5f21e952e6ea449a064a4834edc40e31de0`  
		Last Modified: Wed, 24 Jul 2024 03:04:39 GMT  
		Size: 4.9 MB (4949820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bda7ca1121d060e335be6e1476bd9ff8dba6787337b22af8a2a03f5dadaba4f`  
		Last Modified: Wed, 24 Jul 2024 03:04:38 GMT  
		Size: 15.5 KB (15513 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bdf89f734d94afe1f9f4e2db0d80c07478dcb54da470e3e989e4ae854a1aa8d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243559342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69fade71df5ec8c4bef43dca0978ff02b18bcb4bdf07058ddeae528d4af36239`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 20 Jul 2024 21:06:39 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdac81b04b7bdd0d4dc8848806fa0d56434ed7b178d060b43af981609f449ec`  
		Last Modified: Tue, 23 Jul 2024 12:56:54 GMT  
		Size: 154.7 MB (154738009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7967e90168c13e7d1bd07076963fdd0990d9919600cc81ad764d2a9a79495482`  
		Last Modified: Tue, 23 Jul 2024 13:05:44 GMT  
		Size: 58.7 MB (58744206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4539f676c939b8f572c167c7fc1d48826d2e328821ba8bc6f45b5f383714d31`  
		Last Modified: Tue, 23 Jul 2024 13:05:42 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158f1e14ac948a1d9380209b2523ba20209f9d9414084fc70688c4543fdfdb73`  
		Last Modified: Tue, 23 Jul 2024 13:05:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a5ae1ba17aecd8d288e4c12c20d9ff266bbe782ecfae3c8ae91710aec99cbbbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4972229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b70c0196630c26f9cb33e360e3b9c1006bcc651eb7c1fc70d4040008aabefba2`

```dockerfile
```

-	Layers:
	-	`sha256:8efd72d0a267f46cdbc0c999949340e276eeaae8b51df2aaf534430f859c204a`  
		Last Modified: Tue, 23 Jul 2024 13:05:42 GMT  
		Size: 5.0 MB (4956176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62074e82fe8b78a5ed6b3a6983d2f9ef81f3b35de8831930f5513de21995ac7b`  
		Last Modified: Tue, 23 Jul 2024 13:05:42 GMT  
		Size: 16.1 KB (16053 bytes)  
		MIME: application/vnd.in-toto+json
