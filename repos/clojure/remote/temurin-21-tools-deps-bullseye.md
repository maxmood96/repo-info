## `clojure:temurin-21-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:5b566811e4056a8eb3a80a37aabc360310416e269216ef7ae0ffa4a8001c51b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f9db43f754f4aba4a640d4abc91914d8345295b7afc3389767a4324087e0887a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281117733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7065fc8a22f75b82df9cb5c20874a495ef243823b8a9ce25c1623d446878e9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be4a2e3fd56d9c5737a9d1e95716c81030d93f4e219a52e34b167744b933e48`  
		Last Modified: Mon, 08 Sep 2025 21:43:39 GMT  
		Size: 157.8 MB (157804766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a23eb0d0840ee397ff9154aecd4cbc7c1b7ac7bf62f81ccf12db00dc560928`  
		Last Modified: Mon, 08 Sep 2025 21:43:38 GMT  
		Size: 69.6 MB (69556532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232a39b98cbe0950803278ae6fd7d5ed333f64337faf53ae81959d4669dce9a8`  
		Last Modified: Mon, 08 Sep 2025 22:27:34 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72e3f54844eeee637659548e9aab795a42ca8d4d8d15dfdc1f83b702ba4ce2d`  
		Last Modified: Mon, 08 Sep 2025 22:27:34 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7311c07e174fe3c4c8813cc3725696ff28b50bef6ebcf14ced9927fd84d0f0a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ce1f93d113fa57d34835c13b778e763da8a75906e187fc15a2a8a68da68f2a`

```dockerfile
```

-	Layers:
	-	`sha256:fa7901cb1f87716a5761e03ffb84265460ddf5ed9d8f1f821160d3b8a92b40cd`  
		Last Modified: Tue, 09 Sep 2025 00:39:52 GMT  
		Size: 7.4 MB (7399445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:632c91ce092e8ed96d0b47261a7e575d33c4c354442a77302c88b61d25cafe8b`  
		Last Modified: Tue, 09 Sep 2025 00:39:53 GMT  
		Size: 16.5 KB (16496 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a3340224b123b38deba2f7a81181bbd673c68ab0e25225718a7cce0cc3a29fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278014706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3195e2f37bf44a866b1dbce7a51640f270271eb0c4448d8a3a273e7260cc2085`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d85684edae712c924c02a44e0565244d0b64d6fcc27713700ee6f14b8b4711`  
		Last Modified: Wed, 03 Sep 2025 06:17:45 GMT  
		Size: 156.1 MB (156081199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46785782832b6c2515cc8de16beafc1fffcb6cfcfcb3794d61746a0965faf15`  
		Last Modified: Tue, 02 Sep 2025 08:17:51 GMT  
		Size: 69.7 MB (69684053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e653f0ac542f882e3d2b66839b58580ff726192ec5297dc694ec9b41b2a43ef0`  
		Last Modified: Tue, 02 Sep 2025 08:17:46 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b543d764fda86c58cd50affb2f0251b1b2f71d027f04016ad2758ec8c7f3d96f`  
		Last Modified: Tue, 02 Sep 2025 08:17:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:8aa3e0ad016cd7cff774e112cde291f22742478b1622bd728f73334b54adbb1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7421207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ab7fbd991451e5bb5282d12b1585e3cf11c0dff30792aca765669d8a4d4453`

```dockerfile
```

-	Layers:
	-	`sha256:6c29450ec402dfd87fdd0ae43c561d8cc97e2f052d47209a88a9f01040c61f65`  
		Last Modified: Tue, 02 Sep 2025 09:40:46 GMT  
		Size: 7.4 MB (7404568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:036a4c3fb117c8527d70525215a3002481281e3a4214af25de221dbaafe36586`  
		Last Modified: Tue, 02 Sep 2025 09:40:47 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
