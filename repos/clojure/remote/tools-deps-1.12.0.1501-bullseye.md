## `clojure:tools-deps-1.12.0.1501-bullseye`

```console
$ docker pull clojure@sha256:3f49df7344d7ca30d47350ca488f4611110f5fcf2dcd28a0d0cb24c436e99f7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.0.1501-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e9f6f4f0eb6efb55687affc26b7ba3e54bd1b03082e830759ee5cc3caad78a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280516254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7229527aff6de84f09671c00ae04e1fc1f5d03a4b2696caec10c10a9c2fa727`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:de97e8062e06250e3c3cef0d40cfe62111bb4b74bcf6221e25a06452dacffcf6`  
		Last Modified: Tue, 14 Jan 2025 01:33:36 GMT  
		Size: 53.7 MB (53739164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e507e3370c39d3ae5d83e1c80b581563edb3de60678b6d4b53cc9f1b6ea4ec72`  
		Last Modified: Fri, 31 Jan 2025 02:18:16 GMT  
		Size: 157.6 MB (157585869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113b5a49f920252f4c257b3fcc8bdb5adcbaf18b144e6e249fdb4270443c7dbb`  
		Last Modified: Fri, 31 Jan 2025 02:18:14 GMT  
		Size: 69.2 MB (69190177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e7295e251904e443a6aa9f675f223fa43e3410f8e21a4e4e4066c45b619b94`  
		Last Modified: Fri, 31 Jan 2025 02:18:13 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e398151b3846b1a61d07fe5c0d452322d4d3aae56096f922d55e608f87df98`  
		Last Modified: Fri, 31 Jan 2025 02:18:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1501-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:97be94ed1bf71eeffd714c5c1a18830fc521ed8f3c4bab509020845f3c187b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7224830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6bcd50f57e639840bda5f75e7c1bf632f84ac48f154f1a01fac9c3d168f83c`

```dockerfile
```

-	Layers:
	-	`sha256:e7394b6dd8470c5ad25c376396412f472d214c0d918c90bfcaa65b883f394d58`  
		Last Modified: Fri, 31 Jan 2025 02:18:13 GMT  
		Size: 7.2 MB (7208333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41edd439eecb0b8cf645a636d0153b6cfa30219815acf7f144d98f188e0a3578`  
		Last Modified: Fri, 31 Jan 2025 02:18:13 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1501-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d3548e9f04c96716c659fd064e631d3f9e7c51e04d97f1a7ef5cd99dd1bf1c7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.4 MB (277417949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:082d5f1ee1380c46b137240b782b550d8c18a907ef72be6dad45f49de9d28b42`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1270858b2b9cb5d47abd119b946534b70ff7d09f29c425fc07b280e5c28971c6`  
		Last Modified: Tue, 14 Jan 2025 01:36:12 GMT  
		Size: 52.2 MB (52246060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b9222735831f6fd3481eee72a48b5b08e308836b70040ea266b1e403cbd850`  
		Last Modified: Fri, 31 Jan 2025 05:20:59 GMT  
		Size: 155.9 MB (155859332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555409a38646bf01dfbe0ca368bdb229544c07810ad8271d48157b2305d941fd`  
		Last Modified: Fri, 31 Jan 2025 05:25:41 GMT  
		Size: 69.3 MB (69311514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03148d0ee9271bbdcaa536f5ebb788acd6211bcfccf57ac03bc12e0f0b3397f`  
		Last Modified: Fri, 31 Jan 2025 05:25:38 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8264ef43930e45e47d9bfda11c05df68c1579456ba76403578f5acd0bf0158e8`  
		Last Modified: Fri, 31 Jan 2025 05:25:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1501-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e78ae47d7198403eae19e4c185c18be7f877a5af3fe57df174ef439816b2212e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7230095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be9af588697a614db490c57fb9198fe1d629b536b426b715330258640101675`

```dockerfile
```

-	Layers:
	-	`sha256:4a85b9816bdc9ea2c0c5de18d3a82a6cadaf453a0363c5025e17d22c834f9296`  
		Last Modified: Fri, 31 Jan 2025 05:25:39 GMT  
		Size: 7.2 MB (7213456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e244d3233796e31dde470ea91a745f8672369add98d9538a0c5ce714cdbd658a`  
		Last Modified: Fri, 31 Jan 2025 05:25:38 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
