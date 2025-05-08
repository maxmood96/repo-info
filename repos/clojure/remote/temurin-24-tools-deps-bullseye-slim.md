## `clojure:temurin-24-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:f6d269f98b9a456d405c474b6f48d9507cd831aa540a8750942f794655a2f7c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e4639745f0e79235ea4ff95d81b0a4709dd9deaf39d90eb338444889df150d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179200540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc2efb5b41394ff0c1697f55e37e04916728a018135a9d1f9c36be2e6f3cffa`
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
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa68a62cb8bccdd71a78956328127202ae644e89a1d8f2e1a1f67d9b969d500`  
		Last Modified: Mon, 05 May 2025 17:08:26 GMT  
		Size: 90.0 MB (89952019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e89092e80ea2cfd6c4c12a9eb64597df65347cffc9131f0936b5b2122fac5c1`  
		Last Modified: Mon, 05 May 2025 17:08:25 GMT  
		Size: 59.0 MB (58992878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca403cfe64dd9c22d6c17fa2c6f45e4cea9fa2b98528d94795c7fb07009eef0`  
		Last Modified: Mon, 05 May 2025 17:08:24 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89d63e1c42f9a35fd128a20e21c4ba186d011831e87453d32e4c47955c3c012`  
		Last Modified: Mon, 05 May 2025 17:08:24 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dd8ee7fb55e1d6c957581fb00e476584f011b0b67937ae0283f574d9210c1662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5085585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7649131fb15ed2f50ab2be1b3cba62fa3eaaf9fd7cf3f320a8894ced9e4dadfd`

```dockerfile
```

-	Layers:
	-	`sha256:a5ccf58348ab62bb3195f0a604c3eb77ec19fd82b4b6757ea6727e22d7f4ad0e`  
		Last Modified: Mon, 05 May 2025 17:08:24 GMT  
		Size: 5.1 MB (5069713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56247ef63f92d5d48311b2d7b77d2e634036c3438f08fa8d57762d525a27618a`  
		Last Modified: Mon, 05 May 2025 17:08:24 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3f6b08b9138ccc110274733d8cd09c6e4799323be7455f2f3ca2819bba1dbcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176964167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa11c6880ac47fd07335ec702a6d018b6cc12d7afc9402693ceccafb60c6b918`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
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
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Thu, 08 May 2025 17:04:53 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af99c2ce0ba7c28d6ec5d791ae9e290374a008adadaef9c91928b11cc64c6f5`  
		Last Modified: Wed, 30 Apr 2025 01:51:53 GMT  
		Size: 89.1 MB (89091225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae6022624aad591eba77575fa23bc17ab36387243af07139829cb6d9bb5ee8b`  
		Last Modified: Wed, 30 Apr 2025 01:51:50 GMT  
		Size: 59.1 MB (59127260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7931681adf1e9d075252c07ad9a041ba0e4eef82d3380eab6989be43ff54fef`  
		Last Modified: Wed, 30 Apr 2025 01:51:48 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0337406b70a500aecdb660ed921c4a1eea7c8c3adee4ae9b36a0712c8bdabe3`  
		Last Modified: Wed, 30 Apr 2025 01:51:47 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:94b509feaa9833085317d2c830a70efa28609fec746d6fd5d9d1733dc74706d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5091432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ced7fb09a003e6e95349b13a374e73ce364fd0a1ede1d884021568fa63d6b47`

```dockerfile
```

-	Layers:
	-	`sha256:94e42c2fd6fbfec65a8dda04fb481b6ac32937cc62d31f5f44f4337ba39ee195`  
		Last Modified: Tue, 06 May 2025 00:50:19 GMT  
		Size: 5.1 MB (5075442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d39de1f05a7f914fe590880495f61635cd83a9efc5e8dde70cb758023c6c795`  
		Last Modified: Tue, 06 May 2025 00:50:19 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json
