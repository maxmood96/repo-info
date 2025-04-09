## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:ed6f5a50dee422b2e0909f089a88db5fa1b9cd7db1094da6d21046684b1b66cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:77e02e275884273d1cd44379c47178a297cc1c8cd89d82592383bdae843b4d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143972265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a6db4f2281ef3e72f017a638207fae39736f3c9da1d30ec521e48e32e8f4a7e`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325ad4a26daff3f3f9b2514c1221e1e79ad239cd6cbb149d36e5d01f6eeb8197`  
		Last Modified: Wed, 09 Apr 2025 02:48:46 GMT  
		Size: 54.7 MB (54721245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d5e94e6118bbfcad814b123b73403fbbeff1f917a8a33792d4ed7413f332c9`  
		Last Modified: Wed, 09 Apr 2025 02:48:46 GMT  
		Size: 59.0 MB (58992955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3890afd77777cad45711f4b9401877885a87c484fa4ebc365081330c590bd32d`  
		Last Modified: Wed, 09 Apr 2025 02:48:45 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:29a58abeee5e6e62b14737474136af7e0987f4f5f91d0d80672edd06e0d0256e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5254914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1873ec108439731cbeb695c43888753fdc8e382ffadf942fb2ab7ecc6fdc09c`

```dockerfile
```

-	Layers:
	-	`sha256:acb4c96aa312d0e52886d9681b77c45923272eedfa75b5be3ac2a383c687e3ab`  
		Last Modified: Wed, 09 Apr 2025 02:48:45 GMT  
		Size: 5.2 MB (5240623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b0523fc28832b094e58fafb5a55646906d79aa353a9df532acef631ae1cdf60`  
		Last Modified: Wed, 09 Apr 2025 02:48:45 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0b4c650075d5387bdac3e43bc45ebd6e99001729024d9a6236d76118b3805393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141700314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608091a708ab2258294ea8322cf81fd94e88424f428a30fb1f67ec9cffd370ff`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0861fe7ff88c49bb4627c613a692e3a36a03b94a53527929464db92b49b9e55`  
		Last Modified: Wed, 09 Apr 2025 17:14:06 GMT  
		Size: 53.8 MB (53822769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888e31fbfc8e011420a6e41c70a66d1e1d7940a977d89fb68b27caec4560f964`  
		Last Modified: Wed, 09 Apr 2025 17:18:26 GMT  
		Size: 59.1 MB (59127401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3d7dd1f36e47d280d16ca1c5b98255ce6200f8a69336dbe9ae67ec136e394a`  
		Last Modified: Wed, 09 Apr 2025 17:18:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fa0a23c2bcaaa561a1917743ecc41a65abaf81cd02b49193c38c65cb97a4ba05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5261462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771495534fbdcf44c0945ebf70bf319d56e6106a7bb1004eca727d6db278f0b3`

```dockerfile
```

-	Layers:
	-	`sha256:dfe334c79d6f6a6c2423c1d6d08061e21a42d78f616abfb202191e48df78cb22`  
		Last Modified: Wed, 09 Apr 2025 17:18:25 GMT  
		Size: 5.2 MB (5247053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca5391638bdbbaca3937ef92bbc3fc3174b2f5acaaea27db0b9b344faa8855ae`  
		Last Modified: Wed, 09 Apr 2025 17:18:24 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
