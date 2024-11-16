## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:67238fcc4068575babe5b5c8bab44a321fa7d9b0fbb5d69ae54018110286110b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cc62abef772e9e44f5bd7cffe8055f4d1a9c408801a81a3b86d32529b7cc8ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243153580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06414b8eb41f6724a72cfd35933703647b7ff19b8ddd032d0ce5ee80b41bfa03`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83baf59a67d947dc9824aadb6cf423f67240e67315274a50ac0a9fb8a198439`  
		Last Modified: Sat, 16 Nov 2024 04:50:12 GMT  
		Size: 144.5 MB (144536721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa2aa935fa1e924fc724d9b7007e5c2fa4e054168e6f1a1f2399fa2d65a5bdb`  
		Last Modified: Sat, 16 Nov 2024 04:50:11 GMT  
		Size: 69.5 MB (69487828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3b200f1d5741eb661a58d8ae92bbdcd79bf368f793021f24e4862b0401856e`  
		Last Modified: Sat, 16 Nov 2024 04:50:10 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6067dd31be428d9d37dbbdc57cb67fb8d524b13e319665f8985209c5bfc774e7`  
		Last Modified: Sat, 16 Nov 2024 04:50:10 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a7d48a4ba658617bb0889a30b194cabee0b43e7196f7bae9f6b4197d76aae742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4936507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f4ce40e86c4311e4d7b15ee6d7be02a375e65612d4b316df769f4da264bcdb`

```dockerfile
```

-	Layers:
	-	`sha256:9573a52aa17a9130fffa5daf8b1b333bf375e40d15eb003a12e8c30f6531b3a4`  
		Last Modified: Sat, 16 Nov 2024 04:50:10 GMT  
		Size: 4.9 MB (4920628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f2476351c7e80dafd0a8dd9af0fc8b93938ccca680bbb71fa7048aa54ca797`  
		Last Modified: Sat, 16 Nov 2024 04:50:10 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7423646698e32874569a99c3eb570ea925b30235e157f4766679d067b38ec1db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241854078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca775a6069db6b1c00b53cbc09caca36c0bfa8670f15e5c51a54bd41780a214`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c5d41bfe745c6af4de4be9a0503d5f4ef52f33df043735185d7e7ffc08e3a0`  
		Last Modified: Sat, 16 Nov 2024 05:29:55 GMT  
		Size: 143.4 MB (143360977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ae83d7efb37de65a10794f039dc951bc8a95ba9a9b989bb503a730ea575199`  
		Last Modified: Sat, 16 Nov 2024 05:34:25 GMT  
		Size: 69.3 MB (69334702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4bcb6576baa3446695401e5e4086ea59e4934b861b742f714d5723c5cd538b`  
		Last Modified: Sat, 16 Nov 2024 05:34:23 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d6c71c9a7201c7ce92ae6218b95f6c9113c8823fe38adc7835a26006dd3158`  
		Last Modified: Sat, 16 Nov 2024 05:34:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b7545e5c819ab61d4d39154313e90534399be090d45c2fead363188a78c85a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4942391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa9e63e6a355cd849b288515da7e54a77296283361f9b0522544bde059b2755`

```dockerfile
```

-	Layers:
	-	`sha256:d3a73ab928391eb985f944149bd61376655e4438ea2e21b867bd88ff35aec17b`  
		Last Modified: Sat, 16 Nov 2024 05:34:24 GMT  
		Size: 4.9 MB (4926394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4036a5405e69473104ef43e3cd0ae5376015bf6dd4acaac53588f7e0943d68ed`  
		Last Modified: Sat, 16 Nov 2024 05:34:23 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
