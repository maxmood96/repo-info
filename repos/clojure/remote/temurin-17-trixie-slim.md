## `clojure:temurin-17-trixie-slim`

```console
$ docker pull clojure@sha256:b5ed42cacff9cd76e96e4282136356ade6951ab5042bd8040c100b8194565747
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:754b75dc2d4be7f8a043593183a0ce13bd2023eb04f2a371bd0d29db95ee4aa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246113874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82727e7109b90f4b5de014a9a311b062c603e20585d1c1c27517a7d1d12f44e1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1745798400'
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
	-	`sha256:3ae34fc80ed56f2b3a9a0b682b58e28e57fe981f5e514c3f687044f4b967608f`  
		Last Modified: Mon, 28 Apr 2025 21:08:25 GMT  
		Size: 29.8 MB (29753912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88a9e6e9439e1e71dc15cf1210c05634bbd063835a1bd6b1be16383dd15dd8c`  
		Last Modified: Tue, 13 May 2025 17:53:52 GMT  
		Size: 144.6 MB (144634958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0953565df9ea772364f47d625ab43415aca16103446c7402b81c4421b76ec6d`  
		Last Modified: Tue, 13 May 2025 17:53:51 GMT  
		Size: 71.7 MB (71723965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d133eb9e49ded403bf070237c8128088486f27f87378038690cd234cd839580d`  
		Last Modified: Tue, 13 May 2025 17:53:50 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ca2388017d2a92a2934c63bac990a79197f84328722a9df6aa9862eb0265cd`  
		Last Modified: Tue, 13 May 2025 17:53:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d0a3bc6b293ef821fc58bfab3afc994172c884a856ad12fe965f8327122ba38e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5082542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b3a32499749fad62a81f836a701d7bc5e34ef948aeb598324a28d7a670828c`

```dockerfile
```

-	Layers:
	-	`sha256:b432fa5d86fb236abd67ce2111a47f0cddec0ab5c451aa6b47d0e490e025991e`  
		Last Modified: Tue, 13 May 2025 17:53:50 GMT  
		Size: 5.1 MB (5066687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c129f46d097dc2b3b6bc744852685bc3afbeb20de6934a6feb9ce2140b94993e`  
		Last Modified: Tue, 13 May 2025 17:53:50 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6f709dc0750c67d9cc016b29b9b190b3629ed0599843be88904738c6dd077af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245290048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daaf34f1fd16a3ec768a1c9d8bec32bf02e873d1b31fcafcef295485f6750bd9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1745798400'
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
	-	`sha256:d0342bfffaba1a8be0950e44b5334c6cf9a05d9eedd81a042ec7813ac91850a4`  
		Last Modified: Mon, 28 Apr 2025 21:23:36 GMT  
		Size: 30.1 MB (30130233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1862c5660d0d55c936747bbb44d2f2a5a6c318c406ceb110d2aac1c4519264`  
		Last Modified: Tue, 13 May 2025 18:01:43 GMT  
		Size: 143.5 MB (143512634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d7dac7317d6e16558e8bc9ba4e6d01bbf9dbda8a4cf1d851e7ccba061b5746`  
		Last Modified: Tue, 13 May 2025 18:03:26 GMT  
		Size: 71.6 MB (71646144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a0110d4502c8ec26b1a0d12b365d5e073b1577431825681f38ed8719f04463`  
		Last Modified: Tue, 13 May 2025 18:03:23 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f0e28c097e8252696ab8487b60904a2183948e4e6174d96135d188310ca020`  
		Last Modified: Tue, 13 May 2025 18:03:23 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6f7032e52da44597110f15d945dca67b1467a385adf3f13428cc5902d433381d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5088429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc473bbb7d0622b9b1b698edf41767730558902480f19515f793852e9d47da81`

```dockerfile
```

-	Layers:
	-	`sha256:10be57bff03180dcb84d6a75fa385b4817ee55ecaf8ae189ca1d8c6549ce8f15`  
		Last Modified: Tue, 13 May 2025 18:03:24 GMT  
		Size: 5.1 MB (5072456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7331aa816c89115dce4ff1e16d18e9752ef13e460d4b09ce297b067a0d5a5cf5`  
		Last Modified: Tue, 13 May 2025 18:03:23 GMT  
		Size: 16.0 KB (15973 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:4cbbed505e4cfd77dfc5ede74eef1bec6f3162ab4c194865d874d3d3b8731a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237313457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e329c560a0d839ed82b8721380bb4791976a6e2459b4fc3d34525ad5d7066500`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1745798400'
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
	-	`sha256:2efa8ce97d282fc76ea2985fc31102becef655447ddbf9bdd3209771347a0182`  
		Last Modified: Mon, 28 Apr 2025 21:11:27 GMT  
		Size: 29.8 MB (29825462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b674b6d2790c8572b4f337294d5779bf8394dac4c40b0e834eaff345e3fc45`  
		Last Modified: Tue, 13 May 2025 18:14:24 GMT  
		Size: 134.7 MB (134673562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3750763831b681d31709375b8d2f37a1e040c6866ca0e217ec22a5af700743`  
		Last Modified: Tue, 13 May 2025 18:20:09 GMT  
		Size: 72.8 MB (72813392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239cb4d71270e05aa3478b52ec841c57d19ae0e6e9d3f21ac20b67873bbd69f0`  
		Last Modified: Tue, 13 May 2025 18:20:07 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bacfb4074269eadedb17671e5bce47bc419b4e806e5b142f50029f7e3851f02`  
		Last Modified: Tue, 13 May 2025 18:20:07 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1162ccde9e9bc28f07562cd53d2184f48dbf42777fe628c545cb900741a654be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5078465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d21a03d44bbf6da2e94a8a0e00c4b6c9136ae10665e3e0ba32bd81c90c8de8`

```dockerfile
```

-	Layers:
	-	`sha256:eb58ac5e17a549ca623372a5fe0eb68b077c77818bf065567cc7b93995f4d82b`  
		Last Modified: Tue, 13 May 2025 18:20:07 GMT  
		Size: 5.1 MB (5062611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc48267d1a8015d81cfa4df364728dda19db1e41109e0af7869a38529cea97a0`  
		Last Modified: Tue, 13 May 2025 18:20:07 GMT  
		Size: 15.9 KB (15854 bytes)  
		MIME: application/vnd.in-toto+json
