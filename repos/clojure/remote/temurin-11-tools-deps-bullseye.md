## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:a81129a54d400e7d42ba479248083e42afffe113b0221af10223e3f1193c499f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:c02fe790cc7752a969fd880fb27852896a44151a74f64b9b4c1793833045ee10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.3 MB (268280677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8747fdbcde7cdae0cfbf6895f54d844ee008d09b192c70dcddf67c655b3be46`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:54:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:54:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:54:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:54:22 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:54:22 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:56:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:56:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:56:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77cc60b7a7e3a10b01d1482a31a5151f36247462f4c7ff5b464f0e8fd172aa9a`  
		Last Modified: Tue, 30 Dec 2025 00:55:20 GMT  
		Size: 145.0 MB (144966626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf06134d5fbe0eb514c2ad244d19487e5c346a7429e341943ad958cbf3e5c82`  
		Last Modified: Tue, 30 Dec 2025 00:56:49 GMT  
		Size: 69.6 MB (69556966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad44a38fae5f13fbd3bff32382f0ecceb8b9081eb6db70f41f53ce73f3674bb`  
		Last Modified: Tue, 30 Dec 2025 00:56:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2a6168e2c0269f0fc92258330340a49a824a3034cb7e39cab9e6f816b65b78ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7429216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164bdfa3a89a0e6cca7c2f669ef6f93faf9dbe7748d2ca6f6bef0c7d0e23d4f9`

```dockerfile
```

-	Layers:
	-	`sha256:921086884cc0d6af05ee3e7f0b7e34cbbb518d440ccb44888747f15d3d051a75`  
		Last Modified: Tue, 30 Dec 2025 04:36:45 GMT  
		Size: 7.4 MB (7415808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec7e05e66bb5ea26f99a670fee411ab2662e9be6c443eb38dd8a9899f1577ddc`  
		Last Modified: Tue, 30 Dec 2025 04:36:46 GMT  
		Size: 13.4 KB (13408 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c3c8e7ecb2d7455fb68b2d7feaa94cac3a268a1c08830989a77b3bd950098698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263676518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ee6511ee6c26b62937d63f7642801f775a7b753fc86c5d8cf87521c4d83966`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:57:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:57:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:57:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:57:12 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 00:57:12 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:57:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 00:57:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 00:57:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9cc7bc8e086c95eb3e992d2c623bd505740ab0a6afcbc89656d0bb477878489f`  
		Last Modified: Mon, 29 Dec 2025 22:27:00 GMT  
		Size: 52.3 MB (52257770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8822f43404454d2b02268a8db7554651006c196b88ba452f8f618c99d0e2f82`  
		Last Modified: Tue, 30 Dec 2025 00:58:08 GMT  
		Size: 141.7 MB (141731574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe54163bc1f648f504f7a973788eeaf581ea3c317fa0428f43d79a0e89c0b73`  
		Last Modified: Tue, 30 Dec 2025 00:57:58 GMT  
		Size: 69.7 MB (69686530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ba7aa3c1f4236462eeac674268136e7f6d8c7eca7603719fd5b25dac2963ef`  
		Last Modified: Tue, 30 Dec 2025 00:57:53 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:28f38120ff1e51a7d8d6ee990b04d25042b3d3c3d55542d2f1244ed856b493e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4330299bdf05f829c204f3d18fdc1a58be97871b0b6eec5f3394268eb750de21`

```dockerfile
```

-	Layers:
	-	`sha256:bc0fdae202246095e01dc357f0944eb0a6c04dc7f706f2abad496dbc66976a89`  
		Last Modified: Tue, 30 Dec 2025 04:36:51 GMT  
		Size: 7.4 MB (7421525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c32d9d03b6a61db90b5b1e80f8e327596dff279ac723786acdc35a023e30dbb1`  
		Last Modified: Tue, 30 Dec 2025 04:36:52 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json
