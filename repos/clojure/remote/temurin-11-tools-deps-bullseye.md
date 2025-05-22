## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:65bd870ac48c2ea57a54bd173772c125a9fe029ffe13064b758e2e87e0cc57c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

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

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:94efb1b6ce173c570d64426fc5f389f4cc79a2c754f5356888256af9256af0b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.2 MB (264196412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8f3bb03a49bc4a9dbb2dd96ecbfdc43ee46e2017317825b6dadce2230ce18a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d401d739612ca72cd16913778c2bd866095cacc150ddab122a79a1fc7cbacc5`  
		Last Modified: Tue, 06 May 2025 00:25:06 GMT  
		Size: 142.4 MB (142420730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303466606faeeb976ba5df0e6ca05cccb8544aeb66de1d40041d816ab2461e8a`  
		Last Modified: Tue, 06 May 2025 00:29:30 GMT  
		Size: 69.5 MB (69529057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67d06a3e2d8d402d05d36c6adef3cf4d8f5753f7c43fc5eb113aeb231b6c00c`  
		Last Modified: Tue, 06 May 2025 00:29:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a732ddcaf3ac362dfb84ad503269bc493176b7b393f1b74335e6661ab48f8f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7246783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:328e3f5d8fd9c47609036526e8278648acd2b276801c6feeb089c95293b59f94`

```dockerfile
```

-	Layers:
	-	`sha256:5c68dca8a0a8a62a588f3288f365675452608934d04ea13dd95fed38c5b83cc0`  
		Last Modified: Tue, 06 May 2025 00:29:28 GMT  
		Size: 7.2 MB (7232413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1501ef82543266a506583a78f3e6a50fa4aae0baeb0bf6ccf57fa4e4c194897`  
		Last Modified: Tue, 06 May 2025 00:29:27 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
