## `clojure:temurin-11-tools-deps-1.11.4.1474-bullseye-slim`

```console
$ docker pull clojure@sha256:b967266d832b241d82670eca70507e6bb4e0477cf152584bfe40961046d4d19a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.11.4.1474-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9a34125327f656bbd0392e4f52650a72b05621f334102d4fa7cfd560e26cb55d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235550908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1eaa8be74eea914720e0be03cfa7b520c977c006e0ad073f0f18e5273733128`
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
	-	`sha256:33db916bb907dfef8d8a50f261533078da1e159ead8f29e71db8059d4b618a21`  
		Last Modified: Sat, 17 Aug 2024 01:59:34 GMT  
		Size: 145.6 MB (145550049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237260ab0185fd85991321505f848835b720775c32f28139c293df5c92d2cb4d`  
		Last Modified: Sat, 17 Aug 2024 01:59:33 GMT  
		Size: 58.6 MB (58571925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce73bd71e059c9332eb57b2d02c6dcb70f6f77e4766a057e64b265f1289c901e`  
		Last Modified: Sat, 17 Aug 2024 01:59:32 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.11.4.1474-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5ba6714d51762194673b9d0adf3c184c572c4fffe4dd7b9fc8ac0f8666dc3425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4963764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b19c0aebbbdf2b475abfd7c1b0c4266d7d4f3984b2030f6acbb2e1971c439a2`

```dockerfile
```

-	Layers:
	-	`sha256:94f980dc678e9cae16434314418bbe2885246f4b13c74864c6685118a4fb959c`  
		Last Modified: Sat, 17 Aug 2024 01:59:32 GMT  
		Size: 4.9 MB (4949826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2d05d2ffc33389e6317360d6f1632125feef4143180ac3f8856ff0ecf61e348`  
		Last Modified: Sat, 17 Aug 2024 01:59:32 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.11.4.1474-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f29db34e499fa98c00f07eed7b98b02c6a13aa5f350c7a1b27161f87f774ed70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231132788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f516c644716d550aa2e5e7916b53f80d65c97a3834e4923d111ea8896ba8fb`
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
	-	`sha256:22370484e38a0ef27288ca6587751610a0a45506dc7bb989f771395ec0cf965b`  
		Last Modified: Tue, 13 Aug 2024 06:26:26 GMT  
		Size: 142.4 MB (142356447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c536ed7cb455014b6fbc7694fd44816761277b6745535381a8254235f7cb08`  
		Last Modified: Tue, 13 Aug 2024 06:29:31 GMT  
		Size: 58.7 MB (58699610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a2919ac662b8c3fdc7a0f7777d3170f5180c0746ae6d0d031d4d4059d5093b`  
		Last Modified: Tue, 13 Aug 2024 06:29:29 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.11.4.1474-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a4ba6c1dcd254ab1f1546dbc772555d14eea3e5ca65da877927b81421a8a5f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4970661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f6bf1f39b7eff038213a14f5b2112dba3378133aef25c0c5d51281e40c8a30`

```dockerfile
```

-	Layers:
	-	`sha256:2ba526ec2e7a41ded08a064e343b973b9c02d8de43a65f3f896007fe8b9067a2`  
		Last Modified: Tue, 13 Aug 2024 06:29:29 GMT  
		Size: 5.0 MB (4956182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f121625451c92f5421580e1e62fe74709af998627485524bc7dd6206a8de4b12`  
		Last Modified: Tue, 13 Aug 2024 06:29:29 GMT  
		Size: 14.5 KB (14479 bytes)  
		MIME: application/vnd.in-toto+json
