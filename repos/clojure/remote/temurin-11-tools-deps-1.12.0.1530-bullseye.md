## `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye`

```console
$ docker pull clojure@sha256:3628755b17335542cf3ab8fa6ec49c018afd18ffb7fbf3d52ff0d30123726a2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:bd2f804dd1af9797a73b9be017bd16845ee05a32de253dbdf73b010fde97ee6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.8 MB (268784491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a24dde334fecb7099a49ac9ebabdef6d0ee7519655770ddb4e35a8dee53af3aa`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb9006d690413bcc8537dd6d44362b29b6f29cc98ee8bdef67705eb8a108294`  
		Last Modified: Wed, 21 May 2025 23:32:28 GMT  
		Size: 145.6 MB (145635750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3edf8ce72f701c1150180d95eea61b32c0c289cc8033c9e558de7482b5cd78fc`  
		Last Modified: Wed, 21 May 2025 23:32:27 GMT  
		Size: 69.4 MB (69397902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241f5a7c19e605a840fe4f87470897942974712e8e005c5d582fe5219b7c3aff`  
		Last Modified: Wed, 21 May 2025 23:32:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:66ce8b7cca71a83dd3792f20754d704fbf10863bff05dfff8df478d1cbc1fc32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7288981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a40e7771ba6c24bdedbdbcc4747c4bb14e2598c790e3f2ad425dc96a6370fc`

```dockerfile
```

-	Layers:
	-	`sha256:678457802504ebf76f5faf42605506cd538ace109a64bc9de5192417ac14f214`  
		Last Modified: Wed, 21 May 2025 23:32:26 GMT  
		Size: 7.3 MB (7274731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:260c0ac89b2ae213965640afccf888ece8facd9d936bee53759bf90c9bf050d4`  
		Last Modified: Wed, 21 May 2025 23:32:26 GMT  
		Size: 14.2 KB (14250 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:567ce232aec19342c42ca10cd7c373e75839b36fe927dc282cdb43a5e9af4b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.2 MB (264199817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822e820767568e77d0ff15e4ccf499fab0d0fec6e100af39ccc9e715133d64fb`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Wed, 21 May 2025 22:28:12 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626f26a615782c69600564ba12c678922a75744e8c81f143bbe524275b9c11f7`  
		Last Modified: Thu, 22 May 2025 08:11:15 GMT  
		Size: 142.4 MB (142420720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db981f7fd858c10404457403f2ba3ef9a99e1b4af58c1e7dcf204f5025a71af`  
		Last Modified: Thu, 22 May 2025 08:15:58 GMT  
		Size: 69.5 MB (69530696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e7d687da4f5dbbbc6ce5429a178bab3fc8d9c652f62696e1dded8eb9bee0da`  
		Last Modified: Thu, 22 May 2025 08:15:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:cb14282aec64d24aa2ccab57b445bd67c7b37dfd8922ffa41bbec4433f3fc52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7294818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207d6f1af026d85d88ddec63a7ad606d0e2c0e55b689be659247e080674f3211`

```dockerfile
```

-	Layers:
	-	`sha256:0610b455e62034c2bb338913de3c3ec1a31a0bc5e8606edc702dba30697a3823`  
		Last Modified: Thu, 22 May 2025 08:15:56 GMT  
		Size: 7.3 MB (7280448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aea4e0cb91fad888673afb218d60ed3aa2d3854108b3d3d7dc273c1ca98fb614`  
		Last Modified: Thu, 22 May 2025 08:15:55 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
