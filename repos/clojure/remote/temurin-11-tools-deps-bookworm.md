## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:40d6d3f981ced60a157e23d4b7a25c4ff65d11fe8877086c3355a3061465b13a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:56f0308537a39cf5ea993ab34542a3899011b8b2aeaaee0d49b69b57631a5dcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.8 MB (274843204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031d16c4b4d0a654f8b15e468d5ee51cee59af8bdc14f210d25809f7107ccdf4`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8d44ca6cc752b99923758be2367191ae97f0a90f471ef881774f6e435c53d`  
		Last Modified: Tue, 24 Dec 2024 22:37:43 GMT  
		Size: 145.6 MB (145601501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e507d8256b31f4ea7e2915508dd4479e7d98154c22d4f659274e793dece4711`  
		Last Modified: Tue, 24 Dec 2024 22:37:42 GMT  
		Size: 80.7 MB (80743995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a733fb5d82aec6f8e91f4a433f4798b77625cc509ca59c3ba275086829da4aef`  
		Last Modified: Tue, 24 Dec 2024 22:37:41 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6aaaaded0d70f8a85df160f98bb7d0e8c0184b748959de1a6ab2ca1b93120950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7205409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a95482948b6888c29eec1d28a9667012fdb617f7c8da08635fdb75a1cce5122`

```dockerfile
```

-	Layers:
	-	`sha256:1eb51a0d99cf0e8b8531db53eb490191858daf7fd9af311d551b0c7e6aab5e7e`  
		Last Modified: Tue, 24 Dec 2024 22:37:42 GMT  
		Size: 7.2 MB (7191157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d6df5d54444d960cf75160e9bf55631491b345d215ac085bf2e8cdf4576cb55`  
		Last Modified: Tue, 24 Dec 2024 22:37:41 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cfbe6329c4bcbbf714d7d5972e6c38453a251954771fb61b98db579fa7e40abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.3 MB (271320541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182e7e68040dea6522ab62c4358d34eae0c11e53477eebe3b74c96d7b66fc553`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb1fb38c4aae2b158e647c7a0f4eee97d660316bc66f4210ccf7d627d6c2d22b`  
		Last Modified: Tue, 03 Dec 2024 15:09:24 GMT  
		Size: 142.4 MB (142389035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327bf870d8c3c4c7febb25f9531d8e6ef3c2a9aa9447488d7037358296779cee`  
		Last Modified: Tue, 03 Dec 2024 15:13:43 GMT  
		Size: 80.6 MB (80605184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa710fb300b16932de3500d6a7354dbc992816cffb2c71bfe4fd1494cc2d200`  
		Last Modified: Tue, 03 Dec 2024 15:13:41 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b4c5ad0c2c8287826cfb535f457ee48485ac2d86766bd8c1c93ea9df22d973b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7222103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce2a696c4647c2626d9e48598d82ba3f9610cee80088591275c6d6ff44c79a7`

```dockerfile
```

-	Layers:
	-	`sha256:6514adc08d1400743ab94db55dc0529f2bcae0eac14409e6a100a0a336a40875`  
		Last Modified: Tue, 03 Dec 2024 15:13:41 GMT  
		Size: 7.2 MB (7207733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2a50fac8f8da9516e8839095685eb81cdf4fa045511b3abf7f40c0bd3cb3c29`  
		Last Modified: Tue, 03 Dec 2024 15:13:41 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
