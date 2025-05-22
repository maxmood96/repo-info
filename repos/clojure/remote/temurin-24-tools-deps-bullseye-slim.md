## `clojure:temurin-24-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:60d614fd974349ec3962b261e59476a2df9c0a9e931667f4e1eba1cfd6a417b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:936568a299d4a2b3e09a5dfa7486aaef49f1f0b4714f09d54dd67eddbfe1f3be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179203207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4cecb44a45718f331311143db7aa90e2ee5820f65a30e19543ee28cbc1e07d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b017c5e0640baf60ca49edc47354a0529a041cb95f6dfd2d805f3cf6fed6cfe`  
		Last Modified: Wed, 21 May 2025 23:33:53 GMT  
		Size: 90.0 MB (89952020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fee2dc06ca5d0260bf75a2472d7d0be4a8a757cbeb759b4c3f22388d8220fe4`  
		Last Modified: Wed, 21 May 2025 23:33:53 GMT  
		Size: 59.0 MB (58994208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82e69e98947cb2416a766f6f43da4e60d10db308da0bfd407cd84921caa93ab`  
		Last Modified: Wed, 21 May 2025 23:33:52 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372a48543fe9526906ba2548ba73e5ad81d58a9b65b553ef9a7d9dc668b5c59c`  
		Last Modified: Wed, 21 May 2025 23:33:52 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2b198cfcb95c09ab66c4cb0211435c90524fabb13a56d976b0469d8606d18a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9da917bbbf050d89ab0acd0f7390bc66bb3ac3eb4603c31ceded05a6cfd28b1`

```dockerfile
```

-	Layers:
	-	`sha256:251d65cbea4429376f73c4cf559df5d5ce04dfc14a3e454d2f0b5479e8b0fab1`  
		Last Modified: Wed, 21 May 2025 23:33:52 GMT  
		Size: 5.1 MB (5117636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79eaabe616f6217e59e89b84649dbbea9b4c6b75ee1151a79f51cba2454c3214`  
		Last Modified: Wed, 21 May 2025 23:33:52 GMT  
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
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af99c2ce0ba7c28d6ec5d791ae9e290374a008adadaef9c91928b11cc64c6f5`  
		Last Modified: Wed, 30 Apr 2025 01:51:53 GMT  
		Size: 89.1 MB (89091225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
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
