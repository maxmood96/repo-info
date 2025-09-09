## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:b6e9cc9dfed49712bd02fe4bdf0fd9657efc5c0b73f0c9520dd568558107d1c3
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
		Last Modified: Mon, 08 Sep 2025 21:43:56 GMT  
		Size: 157.8 MB (157804810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f457a24c8a4606ea589bbc565939b918c1e71d5be278020f2fe0da0aea4a2b`  
		Last Modified: Mon, 08 Sep 2025 21:43:54 GMT  
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
$ docker pull clojure@sha256:fce242958c39c2b8bb757c1b2cbb1bd9d40b01c26c9942cec27d2fc3a92a8098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244115467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9028bd24c3bf07324455b386f9e153ccca23416038d8a0da754c114db1afca91`
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
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a88517b6197f7a20d6e986cf50966f045ceffa14e5503380ee7bc964424c74`  
		Last Modified: Tue, 02 Sep 2025 05:13:22 GMT  
		Size: 156.1 MB (156081197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d01d322b5fa8cba22a9746babcef848f8d84729ff3ea55123f87628cf7d8643`  
		Last Modified: Wed, 03 Sep 2025 06:16:07 GMT  
		Size: 59.3 MB (59282736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50231439ce10a22ad785bb55caa14fdd337a9c1d7f634b89d3a9a8fbba01bfea`  
		Last Modified: Tue, 02 Sep 2025 09:06:37 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9970711b3b54d3b586f97dbf4bbf7c75a07333d08e090f3a88d4650e8b9d712`  
		Last Modified: Tue, 02 Sep 2025 09:06:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b0be600f0c05fa0f075295f541a8c4d62d899215bcbab09c33fa42d1d11fc2b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5334338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7542f95058354d6439ee7479a1ed03f4f37d2f8f66c6f9ffadbe1376de7c7abc`

```dockerfile
```

-	Layers:
	-	`sha256:a9bcf90d23b1f41b27330d10212fa2d2771abe9ce46f400f8d23b9468c2bc20a`  
		Last Modified: Tue, 02 Sep 2025 09:40:48 GMT  
		Size: 5.3 MB (5317621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7848d4f3d6443503aa702e37117026459a65f454eb33c0a501add251c5453cd2`  
		Last Modified: Tue, 02 Sep 2025 09:40:48 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
