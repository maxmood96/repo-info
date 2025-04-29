## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:b352c27c3cdbb831b49a5bb3cf62087423573a6703ae5e0201d3a95cfdc3a1af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5c90b2c936d2cdb4c732b2ba7b5aaebe5625c9a7fe24644f2da7db61155b529d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143964253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fedf5c0537e37929a8505fde389edb2fb2d4b2c32dc9cbd58d46af043aab2b6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
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
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6907e7a95a9eb9260700c6794ec9f337aaefea96179dda4d1e82835f67ea05b6`  
		Last Modified: Mon, 28 Apr 2025 22:06:16 GMT  
		Size: 54.7 MB (54716148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367fdbaa928c8eae0b7fc7d481505880642616ff2a4885e784e2c638777f06a4`  
		Last Modified: Mon, 28 Apr 2025 22:06:16 GMT  
		Size: 59.0 MB (58992858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee4ca7476658877c77848188c93aaca822e6063adc72d201e2593a174ecbd49`  
		Last Modified: Mon, 28 Apr 2025 22:06:14 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ec9a812bf6ef2422e5687638b970a47b831cea755f106af808f7e124e813a721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5254968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf08042bc0d220840081d78570ac6e160f94a16f0a05b55d92fb76356d37a2e`

```dockerfile
```

-	Layers:
	-	`sha256:c3107a378f4eee84b6f6e859b0eb7d4456f10dace9633ac4a1c4ab13c0f679b8`  
		Last Modified: Mon, 28 Apr 2025 22:06:14 GMT  
		Size: 5.2 MB (5240677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6494e97153f10c50bab1aa40cc785795b63b345cd98a00c170c7becc3430db46`  
		Last Modified: Mon, 28 Apr 2025 22:06:14 GMT  
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
