## `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm-slim`

```console
$ docker pull clojure@sha256:13252c11137805e22f2743297fee3a876ecca362aa494216b964f56cca465247
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ef43654d82aa20301a62c2f97cae40e5d6e7ef5a1bd3e60474a75787322eb157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243354975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632d3ae2580a36c7faee2e580d65241cb170a96bdf8e2970026f45e6b5a7e58b`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce7a8b4aa9ed9834f354637482636628dc522e276209399bacb0e576edb7d62`  
		Last Modified: Tue, 08 Apr 2025 01:36:01 GMT  
		Size: 145.6 MB (145598938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d886f7c84963c15cf168a23e34366389ac10be3923609065a3aebbb0005fceff`  
		Last Modified: Tue, 08 Apr 2025 01:36:00 GMT  
		Size: 69.5 MB (69528131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5970510db9be12785979f46866dbd1892607489eed1ad31f5a64f11b82dbcadb`  
		Last Modified: Tue, 08 Apr 2025 01:35:58 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c1b3f0cccb1d9e35528f1b1505707aa769fb88ce58e5209f16c64d4a1c107ce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4948416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab24e2378f221adb486c90d48fbac6c0f379cad3cf5da4c5f694f20b62db943`

```dockerfile
```

-	Layers:
	-	`sha256:1e3e6e74b8a4bc666f752cdce6ea55d251e5132d820d49c9baac800b6b652975`  
		Last Modified: Tue, 08 Apr 2025 01:35:58 GMT  
		Size: 4.9 MB (4934106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec9b662490d482409fca430b23de6f5f3b350f7efbdcc9aa70b09e834fbd79d`  
		Last Modified: Tue, 08 Apr 2025 01:35:58 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm-slim` - linux; arm64 variant v8

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

### `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

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
