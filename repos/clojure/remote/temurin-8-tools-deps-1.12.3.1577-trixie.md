## `clojure:temurin-8-tools-deps-1.12.3.1577-trixie`

```console
$ docker pull clojure@sha256:2965ef28485de81d7eef9d740a24413ff08e82d40d2ac9f3e9846c9140948028
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:1e45169e85b476dfd49aaff433bb01c350afb386f525976fc76aa512a9720831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189559846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552113c2ab3847c1441b776a8fcf37dbd836aeebc0231accd8c1608287f96c88`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:04:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:04:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:04:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:04:23 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:04:23 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:04:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:04:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:04:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf46fad3b76649e4dd7e094bca196d94a716ce50a02237884f5671250179a90`  
		Last Modified: Sat, 08 Nov 2025 18:05:12 GMT  
		Size: 54.7 MB (54733343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b11102f14152ae5d5bc22a0bf0bc2d806d9272d8722e964af57d08cb039ff3`  
		Last Modified: Sat, 08 Nov 2025 18:05:14 GMT  
		Size: 85.5 MB (85540231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9236e91a77e98447ba51e89fc30e37dd20c49cb88343dfac18da39f3d80a68ec`  
		Last Modified: Sat, 08 Nov 2025 18:05:09 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:10e4fa3c0cd610d793b4d6188aa85d0be48c798d17794379f66ced4508e9fad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7602679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4030ac7972aadc5e5b90e857fd92aadd6132c4de72696c710ee6e5f90dfc43f1`

```dockerfile
```

-	Layers:
	-	`sha256:22a8c9a649dd4975c015dba7c484fa43c8f0a0e9ff62b0246a24aed693d30716`  
		Last Modified: Sat, 08 Nov 2025 19:40:11 GMT  
		Size: 7.6 MB (7588509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17c313724f6f4f89243c42a4f91dc43eaafaec33dd88ae6071cdfbb62f250969`  
		Last Modified: Sat, 08 Nov 2025 19:40:12 GMT  
		Size: 14.2 KB (14170 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f8bcc79210531abd404c08ef1a8f3e92d00b1b7831de3e11ec999efce22da6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188829402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e08890296f5ee7bf4a70390e29f20acb9083ee97c6e80c7054d0872440528023`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:03:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:03:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:03:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:03:41 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:03:41 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:03:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:03:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:03:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3278ba9c9347d1a223a2b37dfe060b9d29a96b7f6eb34f46bcc992c635f0e8bc`  
		Last Modified: Sat, 08 Nov 2025 18:04:40 GMT  
		Size: 53.8 MB (53815012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4dcb96c6dc40699a32e5d9d133c62cff856e73a66551370fd46faa861faf02`  
		Last Modified: Sat, 08 Nov 2025 18:04:33 GMT  
		Size: 85.4 MB (85363313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e3fed9fc655ac1762a03df012c6d4bebd5de9449f949b4842ef50012dcd245`  
		Last Modified: Sat, 08 Nov 2025 18:04:28 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:65e76ff9a5fffb1c17716a522e7680c9b69e45ed4c1acd63e18ef9e53f4264c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a2021545a4417d6bde8f73b829865938a8cf0dc5d81822ad3cec5f2d04fe16`

```dockerfile
```

-	Layers:
	-	`sha256:6a686c5d128888ffa9cd2834ebad76b767ee7c6e79951b9b668f476cd9afb8d4`  
		Last Modified: Sat, 08 Nov 2025 19:40:18 GMT  
		Size: 7.6 MB (7596237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b147a4788f465caf0675cea92d3d9f841e1ec30571c5c4b3a347d20b11fdbd38`  
		Last Modified: Sat, 08 Nov 2025 19:40:19 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:75de82795742efd48bd96dddfbac17aceb496102dc08ee17444e4356440bcfdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196235400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24fe746cbd2722f9dd71756d5569559c6db7fdee9dd711d25aed4564293853ee`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 19:11:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 19:11:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 19:11:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 19:11:39 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 19:11:40 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 19:21:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 19:21:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 19:21:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15756aee0cd03dba616edf460afe9c03ef7dde5b1013400db300db86aaac11c3`  
		Last Modified: Sat, 08 Nov 2025 19:13:28 GMT  
		Size: 52.2 MB (52175136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2099dc2bef0d8cd485a5098c5e1c3d2adf26a5583d7384037ce9566347e0326`  
		Last Modified: Sat, 08 Nov 2025 19:22:10 GMT  
		Size: 90.9 MB (90949491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c76b83a82299919f26faabb6cb6ed49e1714b0447a1bd4361da0f17870320e63`  
		Last Modified: Sat, 08 Nov 2025 19:22:04 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.3.1577-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d76c700c7a4112107d92bab7ab2409faed1ebbe85dc1507fa2160a5b10057f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7607739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05eb974a5760c65dff5ea1e22986a3268bbc258ff2fbd4c6c3fa5a0815435cb0`

```dockerfile
```

-	Layers:
	-	`sha256:84bdd75d174b6941bb8e4fce29c8bdf3f2a987dd13668135fc96aa886b25519c`  
		Last Modified: Sat, 08 Nov 2025 22:55:42 GMT  
		Size: 7.6 MB (7593521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6faf60f0d2419890c4c5df9e9e221ce0906e37c0e19344f6a4625752775e4ce8`  
		Last Modified: Sat, 08 Nov 2025 22:55:43 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json
