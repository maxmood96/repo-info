## `clojure:temurin-25-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:247d1a1e4fdfc8fd844539e382657879d0577034be85c47a9b610fc27093832d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:cdaa0d2aced3d7479cc02f1422e86e6b09a5d7f711771bd97190022c9034ca22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215363660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b9f0d1d5d8fe62ef035ba798d298dd9b5f0156a93b8fc13975ca6eccc5b8e1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:56:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:56:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:56:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:56:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:56:21 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:56:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:56:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:56:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:56:35 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:56:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:437b5b60e3a4b64e2c621589a67483eeef6d4b3fc4926655006ef41bd44f71dd`  
		Last Modified: Mon, 08 Dec 2025 22:16:49 GMT  
		Size: 53.8 MB (53756413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67dfbc97782bb4ef5510715f43433bb0a8145e3caa8d14c9d55f353cb09197b0`  
		Last Modified: Mon, 08 Dec 2025 23:57:12 GMT  
		Size: 92.0 MB (92045289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ba39baa49664295553dec3bc52fe74031ca655ccee020998f32383a7328a1b`  
		Last Modified: Mon, 08 Dec 2025 23:57:12 GMT  
		Size: 69.6 MB (69560918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fdb34b4821c3597859505e903054c878da3767d36aa9a5951d9cc5aeb08cfa`  
		Last Modified: Mon, 08 Dec 2025 23:57:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c4d37635b47530c3481769797ba146a21e64130bf60c9edae189e84f4fe38e`  
		Last Modified: Mon, 08 Dec 2025 23:57:01 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:fd570904e331a3776b0ee2fdf6a782d399f765070374491df4287fb02e5b896b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bc8451a27ba8fd916c8787b68897e09736d845b83aa23d78dd9b1418f05d83`

```dockerfile
```

-	Layers:
	-	`sha256:08cf90310179ff0587b99cf358b98ddc223ed7b14e69064cff99d6ed313d096f`  
		Last Modified: Tue, 09 Dec 2025 04:45:49 GMT  
		Size: 7.3 MB (7347007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66c13d3060129aba6861e7524fabd8cbd91f38ce92c263eeabd2c469427bf98b`  
		Last Modified: Tue, 09 Dec 2025 04:45:50 GMT  
		Size: 16.4 KB (16446 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bc6bd645ce81d099215764cac840aae5e2e41cd1990ed2f1636741f725e3b26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (212999317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82c66c25f3c04d12b90a23b1941f8e1f1d2b9b7ffb35ed9e8b39bad9e4e1eec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Tue, 09 Dec 2025 00:03:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:03:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:03:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:03:42 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 00:03:42 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:03:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 00:03:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 00:03:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:03:56 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:03:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:24bca79f74a34f86894c8fcdc6ce8d7dc3c11dd0c76b7e9fa80c7c64df65d166`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 52.3 MB (52257713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b78a4bf9c76a6a9314447be88b28314f5f3da6c99844402b32067a74715001`  
		Last Modified: Tue, 09 Dec 2025 00:04:41 GMT  
		Size: 91.1 MB (91052516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacb96f1a8c5d591020eec7428b5d949555ea1923e32d2f2b1c838fed3c6afa7`  
		Last Modified: Tue, 09 Dec 2025 00:04:35 GMT  
		Size: 69.7 MB (69688050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a36895153194012fb29ad8343a6af9b9c84ff2e355bbd0e40356180d446768`  
		Last Modified: Tue, 09 Dec 2025 00:04:25 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6a8aace3a59628fe736a99832681abd7898789ef7380d922be0758b26f2e09`  
		Last Modified: Tue, 09 Dec 2025 00:04:26 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:658eb137258551524f8e89bb9bd60a753c841698a8fcd0b8e8f4570b22f80363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7368716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de31f7ad226a32ba39c4ef8d423094362b4addd03db2a32663b17ebc6a71b672`

```dockerfile
```

-	Layers:
	-	`sha256:cc3467c175f315157a93269917c1ae210629c33a2489f7b46bddf7ed882681c6`  
		Last Modified: Tue, 09 Dec 2025 04:45:58 GMT  
		Size: 7.4 MB (7352127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d37bba8bf3ef59fa9083a9c8cea640a65695da59077587d1fe052890f72f8436`  
		Last Modified: Tue, 09 Dec 2025 04:45:59 GMT  
		Size: 16.6 KB (16589 bytes)  
		MIME: application/vnd.in-toto+json
