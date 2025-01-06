## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:e795dea6eaa41e5d33193cf381b65a95898905e1994e9282d5f48f7651ce439f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9f5f2fbbcd3d0289f927bd4127c359c577d3087ee17b12bae07452e957157f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268500917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d278508445991c1998896f9952b243ad1903f20d70cd8dd1eab63d48ecde0b`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bc7e2a73a9912a1b4a3fb43d5f2958398d1c5b09c59456af83d777680c7c6d`  
		Last Modified: Tue, 24 Dec 2024 22:37:51 GMT  
		Size: 145.6 MB (145601503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbf86b82f3ed5df2b5b65b6b59f4601cda8f594e19d2f83cf51260aec650065`  
		Last Modified: Tue, 24 Dec 2024 22:37:50 GMT  
		Size: 69.2 MB (69159814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d1ffa70185c368dfe5b1ccf1cf7b327ec0d3b102d6115a79b3b8cc8f40cd2d`  
		Last Modified: Tue, 24 Dec 2024 22:37:50 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ca3f5540e017a747e8a6d9aa5db3a48dc60e3128f7c52ef7b1d2b80cd68aa8a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7238886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355859d6851cf1b827aaa8a66df3c6bafe226a97f4a7ef036d9e1309bae87920`

```dockerfile
```

-	Layers:
	-	`sha256:cfc5845def32a54ab9accc7ae2a06ad6d92ed7b0ca259bc4f607bd41b66610ef`  
		Last Modified: Tue, 24 Dec 2024 22:37:50 GMT  
		Size: 7.2 MB (7224634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7f72a02a67c46db909c301ef68ff1d18171c1d43b474b98258ae31919afc5bd`  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:836fb7bb9ba2f94c59f9e15f7d88cf71b6da5ac76e1f380739db2ca9d107e70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263921251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c72e0700816276a3c0220e4632677f76a72816a92a35cad77eda7231e9cd79`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac580959112f2958e7f4b4eb9b360444b899d195029d8e7b71a031c4435f09e7`  
		Last Modified: Wed, 25 Dec 2024 07:20:01 GMT  
		Size: 142.4 MB (142388995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43c897ab17d6be4d7f6bf7714dba38b3159350ef91bc30ae4bf3b90458c5358`  
		Size: 69.3 MB (69285915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67480591efe92e9825bd54646f112cc8f6ae0a4e2ccc0df7a3974842f2ab5f05`  
		Last Modified: Wed, 25 Dec 2024 07:22:57 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:fad4c537d8c45a89adcc07fed7a49a07c6fd2b4308ba6beb743125675a1c0fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7244721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e9769423f5d0ef232c08e5eb40e7470bb3d27052f272885f5a0895814da8e3`

```dockerfile
```

-	Layers:
	-	`sha256:c400c007b2f7474d620d9c5f96430be9d1b3e7459835974e4f3b592aa4338ec9`  
		Last Modified: Wed, 25 Dec 2024 07:22:58 GMT  
		Size: 7.2 MB (7230351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff45cff8a509ae25d2eb4ee91da26e031b77407304444074dff7b4c723df5931`  
		Last Modified: Wed, 25 Dec 2024 07:22:57 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
