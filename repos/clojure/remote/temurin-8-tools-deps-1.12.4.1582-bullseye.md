## `clojure:temurin-8-tools-deps-1.12.4.1582-bullseye`

```console
$ docker pull clojure@sha256:98a97e458a34e10e0aa505581148bdb33bf96865184f4453eb2baf826a5f63ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1582-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a99266679115998d38173cd128ebdc1a16006aa5d1a7bd63779ca6cbcef0ed08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (178047146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6118a0774a07ab18fa422c7bb55d95cbc9b1bd7decda7252a950b09459461f0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:51:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:51:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:51:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:51:45 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:51:45 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:52:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:52:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:52:00 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a7c526c92d4197761c0b6f117cffd4d7ee1595be0c9522b5491bcdb36caf0a`  
		Last Modified: Tue, 30 Dec 2025 00:52:39 GMT  
		Size: 54.7 MB (54733371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ba8278a75b95171fa04f169bf6b8ad9a34f1f26132ff8e0e4153d3032ba917`  
		Last Modified: Tue, 30 Dec 2025 00:52:30 GMT  
		Size: 69.6 MB (69556691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c63b5f61ac9a48a8814882ff0e52da03d214e1bb92a6e07e45c99be61eca38`  
		Last Modified: Tue, 30 Dec 2025 00:52:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1582-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a9d0a0fba45c9db6fd9558b4ce646af79f6c6c32f3d72a91b591b5fdde00a30e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7531471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056dba1df00bb65388bce899bb4f7765efba863065b8a7a1a029422e8258cdd7`

```dockerfile
```

-	Layers:
	-	`sha256:f6f9c4d2ea744985c4b3faaea51baea800e8586de29dedf99edb8d0b8cf572e2`  
		Last Modified: Tue, 30 Dec 2025 04:48:29 GMT  
		Size: 7.5 MB (7517277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:705ca14b8984dbcb182245bc5e7b909e89a1f9516981e4eda616e3f8cc468c5a`  
		Last Modified: Tue, 30 Dec 2025 04:48:30 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1582-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:71b0fca42fdfd542d23ff9bfcc9d70c50638384f451bce6778055ac53c387ad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.8 MB (175760414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a31e7641664811c00010eb8fb775286ff7d829886de3ce99c71f776d3261e0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:54:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:54:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:54:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:54:45 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:54:45 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:55:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:55:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:55:00 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9cc7bc8e086c95eb3e992d2c623bd505740ab0a6afcbc89656d0bb477878489f`  
		Last Modified: Mon, 29 Dec 2025 22:27:00 GMT  
		Size: 52.3 MB (52257770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2bfb012c9a27a360a6e1f6dc9f0fbd09d681d1877632fe3f271d51efd10115`  
		Last Modified: Tue, 30 Dec 2025 00:55:29 GMT  
		Size: 53.8 MB (53814992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dc5fc967de5ad524684261bf4a228a59fc9d9f1cd9ab293138acda2efc8546`  
		Last Modified: Tue, 30 Dec 2025 00:55:29 GMT  
		Size: 69.7 MB (69687009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c57d31847d05d001419789b05a4fe992442ec05b00f15463873cf27944d0208`  
		Last Modified: Tue, 30 Dec 2025 00:55:25 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1582-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2f1c0c7b6541d3b37bfdb37916165026c53c8db3fab163d0768fa7746b2e6b12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7537386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991f01e0bfd33f62ad1b7d7468fc4e921bf865c0808cba735147c37b458526be`

```dockerfile
```

-	Layers:
	-	`sha256:41a7a7992b9fcb7f257bf77cd961bb3f79555f00075f1528b3378a4cfdccf8f2`  
		Last Modified: Tue, 30 Dec 2025 04:48:36 GMT  
		Size: 7.5 MB (7523074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39eb8fe4878d2fe09f706341ac65e3c0409b38274469062774fde1cd8c6ee27f`  
		Last Modified: Tue, 30 Dec 2025 04:48:37 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json
