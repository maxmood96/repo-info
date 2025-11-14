## `clojure:temurin-21-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:b5667cb214e06d45acb827497b7804573dd85ae7c37053c7be523ceacb8ac0cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:cce8ba158054024d4aa001da46d5655a21abb6c85c8eb978f53397267641ab09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281144763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb38bc5d28f3b52f0b5ec680bc5e64fb3066eb883d196bc6596f7353608b236`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:54:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:54:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:54:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:54:50 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:54:51 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:55:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:55:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:55:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:55:05 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:55:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aba529ddea5cb85c4de127dffefbb48f54200185871e77994fd1cfb0749f1ee`  
		Last Modified: Fri, 14 Nov 2025 00:55:30 GMT  
		Size: 157.8 MB (157825981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1a4ce0aa9822e83903d57e1c8c0a70961058fa715a8a4ed0aebadeb4b71772`  
		Last Modified: Fri, 14 Nov 2025 00:55:41 GMT  
		Size: 69.6 MB (69561044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6024fe585151865abd8e9820e179356bb2c2894bce3d2df33941352abe48e6a`  
		Last Modified: Fri, 14 Nov 2025 00:55:36 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9a352a303f14a3c1c2fed35e208a88d560cb908a1650d87ef19a05cff41164`  
		Last Modified: Fri, 14 Nov 2025 00:55:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:79eb22a7e59ba80e46a1714042378e3c23e0c26f3955654567e95d3a8410b5ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7414548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657d3e46754a3d9f1d3a79f7dff4f7c8d0e41ff29f4d119d0c8a2ddb81ab5653`

```dockerfile
```

-	Layers:
	-	`sha256:2d693ec13e47223a58c1c16b841ac8599346bd00018fb27656464c9784a6b075`  
		Last Modified: Fri, 14 Nov 2025 01:45:51 GMT  
		Size: 7.4 MB (7398771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21901c06dccdcc0c210b0841736a7a7cec2a1dc118cdc906b6d5196b07c944b9`  
		Last Modified: Fri, 14 Nov 2025 01:45:52 GMT  
		Size: 15.8 KB (15777 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3643eb4c413a0f441a6336c42bb6c65883c5c41d426ec8880007bfbc688fdcb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278054852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac77600dee4405400347b86a41317f7286ef727987d8c41893d958f735c46ae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:44:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:44:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:44:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:44:19 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:44:20 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:44:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:44:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:44:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:44:33 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:44:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7db1c132d3d9e577fbb5ae618177df1f6a3410e87628490f7540adc0ec5603d9`  
		Last Modified: Mon, 10 Nov 2025 03:57:42 GMT  
		Size: 156.1 MB (156107621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35f4f1a58539586e3f12cad73ba4d5aaf4c4e4ae80b636fa6beef120d1509d1`  
		Last Modified: Sat, 08 Nov 2025 18:45:28 GMT  
		Size: 69.7 MB (69688218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4fbfb0afb5c38598113a4aaa5180c0b05cd98544acf18244181f136005966a`  
		Last Modified: Sat, 08 Nov 2025 18:45:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3633a7598e96df078c877abc54578c1fa9cc10f6154195b38d93a10950628f3`  
		Last Modified: Sat, 08 Nov 2025 18:45:22 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:47c91bf7e15ee0b976e4342be3f8d6035a3e8fdf5414b2b8cd43457cb59d6784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51ca82c4383b41f0f7128c59fe171ad892f63028ed36bdc4d73888940cb4a6b`

```dockerfile
```

-	Layers:
	-	`sha256:914365cb147ae8f2876e34d30c657c79420ba16ec659c578c8c311936e0332ae`  
		Last Modified: Sat, 08 Nov 2025 22:46:25 GMT  
		Size: 7.4 MB (7403870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67c0aeb5253f54cfead611ba198ac0f7b9c1ad2d58df3c7300d0a767b9887b8e`  
		Last Modified: Sat, 08 Nov 2025 22:46:26 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
