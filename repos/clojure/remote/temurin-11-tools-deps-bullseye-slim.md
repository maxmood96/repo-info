## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:0e02dc78abb4d187ba3ed70e1baa3aa6b0bc68fb7deedb613a654d1d0bdcabb6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:42fc3ed05ba35ea88ad32753e133f4b56d33548e646394de857f184fdd022297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235551028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5bee1919c41641b9b7aa8671aa3c0efc4cff0bd9da8061809d086e6076e34a6`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d460ff4f4bb28d6ac2fb7cc1a24bfca42a2ce4a705f9d0b6d9e397830deb48d`  
		Last Modified: Fri, 23 Aug 2024 20:02:15 GMT  
		Size: 145.6 MB (145550028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4995103abf76bf1cc3343919e83a84fdceacd87ebe32ff080fdf1a7c9dfed6a2`  
		Last Modified: Fri, 23 Aug 2024 20:02:14 GMT  
		Size: 58.6 MB (58572066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1d0e843d7c9c302586295dc753e301e2e25d11ac21e37af4bb431db1c59f9f`  
		Last Modified: Fri, 23 Aug 2024 20:02:12 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:29ec6428e4cd4b20b3c832e18539f92471b8efd12711495b48127e52f905487b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4963764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0298910b5f791d499c6f87662c5d9046c86e6fc7e24ee2c8f37b8ea090086a0a`

```dockerfile
```

-	Layers:
	-	`sha256:6f602e6867750cde415ec8437e97e6e4fd600ff0dfc7739061b8be8249491c45`  
		Last Modified: Fri, 23 Aug 2024 20:02:13 GMT  
		Size: 4.9 MB (4949826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10a14c7d61e47fb4ec225194052718423a8f70df14a00913261b1bad8ef776b9`  
		Last Modified: Fri, 23 Aug 2024 20:02:12 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6fdfc5500ec0ca89ed1003e8e92d54d275f90e5fb7fbec4abb7c8c66d7e19fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231131175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab12b2ebe265ed9a85498751e84c7b835835e44c0f1fabe1d5885555384b928`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97190d565d6e988e1267474ec2deb103d496585fb03fad3f32525640389e705a`  
		Last Modified: Sat, 17 Aug 2024 06:04:04 GMT  
		Size: 142.4 MB (142354792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06ac6ba42cb478d5d8822f508ae780ec3d85b2fd0bb866bb5da215c998bc96d`  
		Last Modified: Sat, 17 Aug 2024 06:08:56 GMT  
		Size: 58.7 MB (58699651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b086ad5b5b18708389f959edeb3874ce3e5749fa77e6ed7dbe8a505a337f15`  
		Last Modified: Sat, 17 Aug 2024 06:08:54 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e1901d03fdf75094d61e6281e91c6f41e3b3c490d7496d92644268a90ae2d04f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4970660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44ab45af28d259c4cc93d522b2620f8e19b7339c5041c88991a848f0cb7d98a`

```dockerfile
```

-	Layers:
	-	`sha256:b61dfa06c84fa1de1f2c429d8699a832720abd9ed4768c92e9af266cd722f77a`  
		Last Modified: Sat, 17 Aug 2024 06:08:55 GMT  
		Size: 5.0 MB (4956182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1df14e25bd13f2e8782c7c147b6bc7e8bac47a44ef11b7249d9a76d9340bcafb`  
		Last Modified: Sat, 17 Aug 2024 06:08:54 GMT  
		Size: 14.5 KB (14478 bytes)  
		MIME: application/vnd.in-toto+json
