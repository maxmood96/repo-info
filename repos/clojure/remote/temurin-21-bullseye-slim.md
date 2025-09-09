## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:0ed881be8db358370f4ee33e2da4387d92f13e81165c96b8be2afda243834968
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4b28f63ad210413c740c6e78c78185a59a05492ada5c1b655f06b5bc6f40b0b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247212624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b2413c5466667e5fb67b26931dc6ff94408734dd3b09303d6574798e5d6eb8`
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
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3809af818d2486a747da840762832e35df73443a2bcd335bc2974b6efab5ad4c`  
		Last Modified: Tue, 09 Sep 2025 04:01:25 GMT  
		Size: 157.8 MB (157804810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f457a24c8a4606ea589bbc565939b918c1e71d5be278020f2fe0da0aea4a2b`  
		Last Modified: Tue, 09 Sep 2025 04:01:17 GMT  
		Size: 59.2 MB (59150702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54972e1c8dab830898c28b2fbbe63da3a35ac595674fe615666836856dbd1801`  
		Last Modified: Mon, 08 Sep 2025 23:04:00 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5dcb99ece8c1c293cf0903242dcf52c11ceae90c4a68b805cf71378e97e4947`  
		Last Modified: Mon, 08 Sep 2025 23:04:00 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2cf354b3d95e4fe669c72ec6e0913d0c7e2ee69959c56003d93390f027d0c6c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5328440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6b77d7888ef20e798bdac4dd6b0ac2773fedb329e7d17fd8c3c74669b6213d`

```dockerfile
```

-	Layers:
	-	`sha256:80ff99256808f70920706e22556523ab7b685027b7ccaa9cfc33346e3dbd1ad7`  
		Last Modified: Tue, 09 Sep 2025 00:39:57 GMT  
		Size: 5.3 MB (5311865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7ef29547578a80dd7e16ef1cf36dd5187c51705dfd8439ce315d8fffeb68935`  
		Last Modified: Tue, 09 Sep 2025 00:39:59 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ccd4685a5f2b049a5d252d213de202a7d5e1c6938197c787103930603a88fd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244115489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a990975bc295ac34e37167c680f989ae8c0f8b4932dcdeef1cf52acc833cfb6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
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
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1c2c39a2f9b63f51255bb40620bffbbc66324b911a74269054b571a4bc7449`  
		Last Modified: Mon, 08 Sep 2025 23:43:48 GMT  
		Size: 156.1 MB (156081188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f705711b19ab8fd72cc639e77ef3f0bd7d939263571a986d01edd62137628d4`  
		Last Modified: Tue, 09 Sep 2025 20:31:56 GMT  
		Size: 59.3 MB (59282803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37167810fddeecd2929661bfa65d61d15716c7117530fef2f391fa74e43de3d`  
		Last Modified: Tue, 09 Sep 2025 00:45:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832b929e9099c551a5cb771e651811829b0855f85c1fa12d7409de08c600bfb0`  
		Last Modified: Tue, 09 Sep 2025 00:45:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3b45a2f3a997c39542a4f620b51a67dfe19427c76d1ac4be4b9c44e91733e1b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5333537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a1b9382392e62cf29bf0a80b8e54f63b3411de3acd52361684327db794c242`

```dockerfile
```

-	Layers:
	-	`sha256:5464044de717029a8200a147b4b846473dcd8e887b7932311a79f634c3a3469e`  
		Last Modified: Tue, 09 Sep 2025 03:39:42 GMT  
		Size: 5.3 MB (5317621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f657262b9f24ac6a744b3c872eb8a0c9433b0ab472bde3a20ead2526d2c1d15`  
		Last Modified: Tue, 09 Sep 2025 03:39:43 GMT  
		Size: 15.9 KB (15916 bytes)  
		MIME: application/vnd.in-toto+json
