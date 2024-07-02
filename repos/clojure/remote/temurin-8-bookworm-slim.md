## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:fff570ea4bbf50334ae9567e868d6400f146194a58b3ee6fd0038c8c259d9c48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:11d1747864fb5f0bc13541f392a6ef92b9452cc02b41f3ac054a3a6d48aaeced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.8 MB (201793755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c9512b19fc0b2a103c65694740ab2dfea3cb66c70fa368dcd73144aa687cc09`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 28 May 2024 15:17:11 GMT
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67239cc877a6101bf3fb1c13317b0c57107dd689de9789082b293e58071ee73c`  
		Last Modified: Tue, 02 Jul 2024 07:06:51 GMT  
		Size: 103.6 MB (103600228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535bcb95a163d47cec69db1e29fc7fb35f707e6c51866f9d428cd925632f6a2b`  
		Last Modified: Tue, 02 Jul 2024 07:06:52 GMT  
		Size: 69.1 MB (69066604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea1e1e4e5c5b491c0d2ef09d6e23f14d6efed34a9c0411b89e7c5532d080f0c`  
		Last Modified: Tue, 02 Jul 2024 07:06:51 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a105559a9992096844bcc8359c1b61cc6804d1f1575d8a83d2aebf1e7a7c2fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4741447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f06e3ec7855fa734c83f0e1494d7db8052d11df92b3bf0089e7fc5ad3786498`

```dockerfile
```

-	Layers:
	-	`sha256:f024f3ae647ea0f1ac31743ee664e9cf17b1867a9dcd42c4703ac0fff28a5037`  
		Last Modified: Tue, 02 Jul 2024 07:06:51 GMT  
		Size: 4.7 MB (4727527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31466392b4ffbe0be381ab6087041224423c487f487be5b030785f596da18452`  
		Last Modified: Tue, 02 Jul 2024 07:06:51 GMT  
		Size: 13.9 KB (13920 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d2c78635ae272e06e8826248ce6cb9b70181ce63df25d8cf695de8b2e92ac81a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.7 MB (200675971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34f82b931e7f2ffaeb7443f91e7251c35fcf8c510517fbddd70608fabe10f88`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 28 May 2024 15:17:11 GMT
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
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8e9955909963a2b800ef8a6c38d1789dfcd456bd65bc576b28c027fb670687`  
		Last Modified: Tue, 02 Jul 2024 09:11:53 GMT  
		Size: 102.7 MB (102700444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167341930175b1cb0a711f8851aeea5dc313ce843c7c37026cf464b961fcccfa`  
		Last Modified: Tue, 02 Jul 2024 09:15:53 GMT  
		Size: 68.8 MB (68818320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0532462fbbf06810339854790eab574b0e90e02aaf300bfd946fbfd5841f1585`  
		Last Modified: Tue, 02 Jul 2024 09:15:51 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fa6fdbc67c65aa5322669c04235499e99182727b197d260a515ba37dc7cb3fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4748372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:589b99db45ed8afdf18248b7bfa39b1efef63e7ccd17007c08a9496583f9400c`

```dockerfile
```

-	Layers:
	-	`sha256:59329e4aaa4d70564f457292f596a72fbf5612c0df130bc51099bc630c8a8f4b`  
		Last Modified: Tue, 02 Jul 2024 09:15:51 GMT  
		Size: 4.7 MB (4733912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deeb517b22029fabb2a29fd03c03a4ba71ae1a56f3d9209e8b5e08adce66d177`  
		Last Modified: Tue, 02 Jul 2024 09:15:51 GMT  
		Size: 14.5 KB (14460 bytes)  
		MIME: application/vnd.in-toto+json
