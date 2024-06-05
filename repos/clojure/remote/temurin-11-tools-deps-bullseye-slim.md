## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:a714aebdb21bbbdf22c89c51cf01a1270d753ff6a632121c98b713ee0f13156d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:74d150dea63e919dddec907ce71b27aa676a8b47acb1c77e58cd7447312eafa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235359302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9032f2a1c65447ecc9098acd6f84633fff10faa0fde314d58b1962f6deabe5b2`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173559f4941d0f6fd9dad904f826952192d6d4459cfee940b5cd84cc874c8df9`  
		Last Modified: Wed, 05 Jun 2024 06:10:18 GMT  
		Size: 145.5 MB (145505194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0f5c2b298e7fbbb896132f5fbd737943b2670e1cec00a3451d48f07ce817ee`  
		Last Modified: Wed, 05 Jun 2024 06:10:17 GMT  
		Size: 58.4 MB (58419530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c791224dc5adc73ec2dab1c1fe36d90569edc92b9a602988da5025b471dfd5e`  
		Last Modified: Wed, 05 Jun 2024 06:10:16 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:df96679f3c39488398d4d335c2ee16b224ee9a64f6dbd93b10ea54f67270df5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4923119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c86e77e14a0f029f1da759969682d372e40b8fee298733f65a2d810458247a5`

```dockerfile
```

-	Layers:
	-	`sha256:bd715727d0a33b5716a6e456431580719e0228d4f31e1ea778fb755ea18e69f3`  
		Last Modified: Wed, 05 Jun 2024 06:10:16 GMT  
		Size: 4.9 MB (4909233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca47f96a0513350f78a757d6237f4333d7a578869be7dac8e82121cff7ed97cf`  
		Last Modified: Wed, 05 Jun 2024 06:10:16 GMT  
		Size: 13.9 KB (13886 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d2721e400676cdf2e80d389e2290069d6915ed73f6a0a56034ac384c2359e4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230931710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282dee4efd2c31c4e0ca865ff1608e93ff62a4b7a9cc5e2c5f8bc1a058e40b5c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bee46db14de2b6d22df6eb9fb0966505bf53959a6234b8fa9d81dfed2c330b64`  
		Last Modified: Wed, 05 Jun 2024 13:55:39 GMT  
		Size: 142.3 MB (142304041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268b38253059a323bf4eaca9df5ece1a48a33abcb2fd90771f94ed013558063d`  
		Last Modified: Wed, 05 Jun 2024 14:00:15 GMT  
		Size: 58.5 MB (58540114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06394da63f7df1f129b3b78c7d14de57e267fddce1eeefe435e2bc3a8155636b`  
		Last Modified: Wed, 05 Jun 2024 14:00:12 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d51ded0da8ece6af643cda8c194f29911fdb70a60f33e176419bef66102f0c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4930018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513ce20de4c25486397547cc0eac486986d916e0f1a0f3a88edb29c303972b06`

```dockerfile
```

-	Layers:
	-	`sha256:b85c44ed174acbff5bf6ce629f7487ffffdf2d62b271df3e9dad8ab56cc961f0`  
		Last Modified: Wed, 05 Jun 2024 14:00:13 GMT  
		Size: 4.9 MB (4915589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3acbbd101315d916a2ddf2250b56cb6d269c09d25bf3c77a09af9da61055a3aa`  
		Last Modified: Wed, 05 Jun 2024 14:00:12 GMT  
		Size: 14.4 KB (14429 bytes)  
		MIME: application/vnd.in-toto+json
