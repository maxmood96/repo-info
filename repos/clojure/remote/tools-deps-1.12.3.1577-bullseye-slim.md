## `clojure:tools-deps-1.12.3.1577-bullseye-slim`

```console
$ docker pull clojure@sha256:46e430029172621244259b535cc1eaf81f17b54c14e529763b0481614c8ebeca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.3.1577-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b997a8563a296941b2e36c59e92beb8b6f826f01c5a2be48029257c96094358b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181446116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb34d3da4e7c94d08c9bb9bfdfa8ac71580eb283ca2b7675ebfc0f654324b1e1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d207cc66da44f4d060efb9a20dc200ca0e6b10c76276d0c1db9c735eaee1d506`  
		Last Modified: Tue, 21 Oct 2025 00:19:22 GMT  
		Size: 30.3 MB (30258365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131c941ae5882e62dcc21ad1a149cc43329fd1af8575c0a8d4cc84460e05730b`  
		Last Modified: Tue, 21 Oct 2025 02:25:04 GMT  
		Size: 92.0 MB (92036051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebef83a98b80457338ed994f91eb1c321db1ead507586c09c7ece22e60deddf`  
		Last Modified: Tue, 21 Oct 2025 02:25:02 GMT  
		Size: 59.2 MB (59150658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73e9a223dd3b0c4e140718739c903308a0be98c8bf353c0f691e9e37c309562b`  
		Last Modified: Tue, 21 Oct 2025 02:24:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbeb86fe72b246952ad8216ad7b9dc88566fbb259704b972453efc7e0ed7533`  
		Last Modified: Tue, 21 Oct 2025 02:24:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6592010c561042c5d0583bfae3045a142f3c4e5f096c875f6e1e1a6354e85773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a188661e0d74eec57f186ffe59c33c2a99dec4a5605ec2b60f31814e27b400`

```dockerfile
```

-	Layers:
	-	`sha256:56a14cea3c8297ca812c3796f5d942abb92148618715373129ca1f66095adfe7`  
		Last Modified: Tue, 21 Oct 2025 09:44:23 GMT  
		Size: 5.3 MB (5259413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b8a71c088cbf563357962d65a93567ba848770edfb00c104a28696903e6b03a`  
		Last Modified: Tue, 21 Oct 2025 09:44:23 GMT  
		Size: 16.6 KB (16568 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.3.1577-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e8f56fb637e4d60b0beae681ba6b263056f3a37adc11c275b5cf46ced81a6647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179082057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47fc5ef8347e857eb0810ffd0223c4e765438c7acb7de335b33ce29cdcc091b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:40bdde71139ce202a6b0b5346000bda907331b21efec94960489d60568d26752`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.7 MB (28748401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e49c0966f7e49c42ad8d669f0bd6b0799370277eacc8bb34283869f02377fd7`  
		Last Modified: Tue, 21 Oct 2025 02:30:25 GMT  
		Size: 91.0 MB (91045213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c326bd9e4c1cc26605600721a2706a1e7e086d875e2408c6e0b55b7375d8e780`  
		Last Modified: Tue, 21 Oct 2025 02:30:21 GMT  
		Size: 59.3 MB (59287402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb704df97669e5b5f3a5a310edac105183a4cba425a0c68df86535276de04b8`  
		Last Modified: Tue, 21 Oct 2025 02:30:15 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4150ae0a1694002659471da510b429683f9cdc11136118a7df352e9d4b8f8f5`  
		Last Modified: Tue, 21 Oct 2025 02:30:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.3.1577-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d18daa6b37036808ce3a9356da74c5c0bddc4321b8943f82a6e8aab2cd1fb40d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f253f44870c3583251708cbc4f68ae86e248ab8726b12e86fa6e05fe7e21dc53`

```dockerfile
```

-	Layers:
	-	`sha256:d696eed35de4db2825003da27029da093bfd8edf5cf3905fd904c31a6b53e059`  
		Last Modified: Tue, 21 Oct 2025 09:44:29 GMT  
		Size: 5.3 MB (5265166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20f6c63fb10d928d8b18515eb627f177588502c9314ec1a56663856a9fbe88ce`  
		Last Modified: Tue, 21 Oct 2025 09:44:30 GMT  
		Size: 16.7 KB (16710 bytes)  
		MIME: application/vnd.in-toto+json
