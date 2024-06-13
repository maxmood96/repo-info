## `clojure:temurin-11-tools-deps-1.11.3.1456-bullseye`

```console
$ docker pull clojure@sha256:bc42dcefbc88acd6461028df10fcde88bb56095487a6590bd22723f2f4c64943
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.11.3.1456-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:28d8884f708e0705ab599002bb7587c16093202a6432b5a8a9c5b292dc9568e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269420834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0580d282effe40fd7b685b1ff724258ef1265f6eb7b83588603bb3426d3eecdd`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
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
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d0bc80bdef4c94e792ecd12931c5f998377d0365ad287e2c5840339e296fe9`  
		Last Modified: Wed, 05 Jun 2024 06:10:20 GMT  
		Size: 145.5 MB (145505192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba9256b5c4ade5e89233ce0ecb43b250b2eeca54262786046644684bb28a5ce`  
		Last Modified: Wed, 05 Jun 2024 06:10:19 GMT  
		Size: 68.8 MB (68815595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6995c214fa2e0bdbd05181db42b4edd43d8760cc95ee834867d4d11717f08a6a`  
		Last Modified: Wed, 05 Jun 2024 06:10:16 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.11.3.1456-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:74e239081714a895c3929f5ecae44c190aa297f5666a9532b78ccf3d8b992033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7013566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e56addaf5c45111e5300a5e48b38bc48778ad856f58a1e40c2f3c8c04b8b05`

```dockerfile
```

-	Layers:
	-	`sha256:ff668ce713da11ddf8680928485a202d0a10c6f5fc0a501d739cebdec7956023`  
		Last Modified: Wed, 05 Jun 2024 06:10:17 GMT  
		Size: 7.0 MB (6999751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cf5b841526eccc6e3bd375df6af6ccd13cb2c4abebae2bf8b4c37424533de62`  
		Last Modified: Wed, 05 Jun 2024 06:10:16 GMT  
		Size: 13.8 KB (13815 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.11.3.1456-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:74603cb938889c5deb88307a6cde48cf9dbea098fb5b9e23e7ad0742f9d634e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.0 MB (264973439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ffdd15cc3ca195ccec3c63fb199ad2f315fd23a48e11be8fbf2b2e7be47b87`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
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
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea49f9e62a428fca7628cb048c62c23b0cc38218d89f23a0c414cc08355b9351`  
		Last Modified: Thu, 13 Jun 2024 11:29:59 GMT  
		Size: 142.3 MB (142304041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ea1e73713f155958889468e183ead867a7245abda1fafcbcbf0be264997a0b`  
		Last Modified: Thu, 13 Jun 2024 11:33:38 GMT  
		Size: 68.9 MB (68929167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c233a84e132ac6fdaee9d48ac36d5ad93a75ea7228ee57cf5eff6915f7421b`  
		Last Modified: Thu, 13 Jun 2024 11:33:36 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.11.3.1456-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6ea6316d85ba19ef17e6fb7c66392525b8a70f1a8e7b2ab4f05163d91f507211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7019873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47c93a0a7bbf46eb6fae4de8ca035a23a43472d6610a52ba3e2b7f4f261ba781`

```dockerfile
```

-	Layers:
	-	`sha256:cc4c3e6061b6849d30fbd03fb4a3f9189931b1f25ebf831a7097005ccbbfdb9f`  
		Last Modified: Thu, 13 Jun 2024 11:33:36 GMT  
		Size: 7.0 MB (7005473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9e14d2c719e014f18e8e13431091456ec9b9e1953d965f68bdb10e7f1cd43ef`  
		Last Modified: Thu, 13 Jun 2024 11:33:35 GMT  
		Size: 14.4 KB (14400 bytes)  
		MIME: application/vnd.in-toto+json
