## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:6041d8c13211afe78b10da3ba5404aa2b8c3cf41c087a4103e0ce352f93fd8c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c4faa67a3b6d90a5d78e7a3132da9f9bcfd7e0dabd4a6f0e936bc7b6d29f5613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243332488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2ed4c8eea3f648bda4eb801f0f89a81354a4e879515110e428064e8d771348`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c3f094590a7fec40ae0283dcf9fd416ea841f3118b88d0f7e400c862982ef6`  
		Last Modified: Mon, 17 Mar 2025 23:20:59 GMT  
		Size: 145.6 MB (145598933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbeac823709e1761d465493c128b2548fcd723886e554cc76d6e66b406b799d7`  
		Last Modified: Mon, 17 Mar 2025 23:21:05 GMT  
		Size: 69.5 MB (69528046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fc7d2fa951bf288002b926eab9fef7b1dfd10b53420a7db2c8dc3926e50799`  
		Last Modified: Mon, 17 Mar 2025 23:20:56 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:21d5c588fb5e1d7d7549e72eec68c6cffdf65597cdd586390042239247f06368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4947048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbafec17ad5d32b252bc7afa67a27d27db76d5cd8c99f0d11b542ce8d0ca5d6b`

```dockerfile
```

-	Layers:
	-	`sha256:9b132cf48b33b7d8025bdc77f0abdabdf7a98b8a7cb51e89d9e5273f52b79116`  
		Last Modified: Mon, 17 Mar 2025 23:20:56 GMT  
		Size: 4.9 MB (4932738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bb33a7b047cf3230dbb40ae27c9af2dac49b97c610847f154b190e2a8092af5`  
		Last Modified: Mon, 17 Mar 2025 23:20:56 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:08992c475217e1b96312af597eed67d6c5b45f8783b98b4f1227599e97712c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 MB (239808217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd62e28acff185ddebbe78af9750f8007f19ebf14cc925720385ff624117ee95`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b425acc2f1f4873ee144d51baaf0a367cbde63f3db4253e7861a3a55a08708a`  
		Last Modified: Tue, 18 Mar 2025 00:10:48 GMT  
		Size: 142.4 MB (142385384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b31952d4ac58ede3a1c02a42c002515c3def6b426f8aadd006bd7d95b11fb1`  
		Last Modified: Tue, 18 Mar 2025 00:10:46 GMT  
		Size: 69.4 MB (69378152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06ca3be849b6e1b15e83bac3bcc49ef53ad8a8a0453c4692e7e8040c07d2575`  
		Last Modified: Tue, 18 Mar 2025 00:10:44 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:26cd45367939cad12fe4f00b59d140cb243d60514060a669859459ad4d0bfcf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4953545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a33e7e3f70bbb4db1c75ee4161d012e52191ffd4d054386ebe2d2458e91d9e`

```dockerfile
```

-	Layers:
	-	`sha256:9ce254386d4b9ce7883dcae7ebee2c54cbf7d54e8f2d5d54c509bab156322d21`  
		Last Modified: Tue, 18 Mar 2025 00:10:45 GMT  
		Size: 4.9 MB (4939117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6b49659f90265f8fab7b04aefcfd2519644f3de5aa629f0d8c41deb5e855b9a`  
		Last Modified: Tue, 18 Mar 2025 00:10:44 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
