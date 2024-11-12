## `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm-slim`

```console
$ docker pull clojure@sha256:3f4f284ab3301de68cb8bdd1fbc0b095d8a4f5c031d0073703eee4bc264ae216
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5b3e381d1dfd391cc28b0b470e2a5eaafe942aa3a80c37bc063752461501faf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.2 MB (202249848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30244f711491c9d28912478a53ad66475c27f0dde3a055d1700e6521b80171d4`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7a192d7abb87ea6817f11edea3d238ff07ef089fd6d0b74247de7e77232453`  
		Last Modified: Tue, 12 Nov 2024 02:22:46 GMT  
		Size: 103.6 MB (103633891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fa05a8bec5759acbba6106a1800ddc69d74f22a08414cca07a23e6966dc5da`  
		Last Modified: Tue, 12 Nov 2024 02:22:46 GMT  
		Size: 69.5 MB (69487320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624c788c9a4206e369d9cf475932a4c2e81ab6c7d1c65c6c407aa095adce9eb8`  
		Last Modified: Tue, 12 Nov 2024 02:22:44 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b1a73038aa70c44cfdad359c280a8ea5522887e619be8ba4fc2ed5f5f6e86f46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5057094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c743eada6d60882963f8c6dd1692ced61de6b99d4c48e14b10697034a5c5e8`

```dockerfile
```

-	Layers:
	-	`sha256:89a532f2bab8e0857f09f068500956ebb3afad16dd5411b7e82ddb9adb160a64`  
		Last Modified: Tue, 12 Nov 2024 02:22:46 GMT  
		Size: 5.0 MB (5042798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51b9b8af95d6f45e6bdf597dd020c5a33ca6f3172bb06147f817e4904d0f56fb`  
		Last Modified: Tue, 12 Nov 2024 02:22:44 GMT  
		Size: 14.3 KB (14296 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7e1b53f7ebd1ba4ee567361b256fbf90293fc9775b4783fa2d062b8b5f5292b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 MB (201250038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45a2ba09b447a4a28964360c0fc4b3c9cb4b40a4a62778c3c7c44fc7527fa5a`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa401c93c47e90bf34a831f8ca7797d9e56e8ef8fbe8eff2482c076a1fb2d97`  
		Last Modified: Thu, 24 Oct 2024 08:52:33 GMT  
		Size: 102.7 MB (102747729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad6590b03fdc729a5b06919c4f6ab6152bfec02c4023994555677123de51043`  
		Last Modified: Thu, 24 Oct 2024 08:58:42 GMT  
		Size: 69.3 MB (69345323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7760046391ad4246805cd1c2a4452cc93813fd156a17d270851a54d2d3ed5b`  
		Last Modified: Thu, 24 Oct 2024 08:58:40 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1479-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3f9df6acc0378e9dc0dfe545902c3aacefef1209f0336e7d17fa65c86de4ad66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5063468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354d64d1f848925e7f7cd403c189036494f2e7fe44615431dcb34f5b6589e206`

```dockerfile
```

-	Layers:
	-	`sha256:b0351716bff807daa147c1ddd1e15410fb51ec5d0959a7933989c99032123340`  
		Last Modified: Thu, 24 Oct 2024 08:58:40 GMT  
		Size: 5.0 MB (5049227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77cb9260372b26d9a61e94baa9c4b4cc45957df22de71e483c653f44197193f0`  
		Last Modified: Thu, 24 Oct 2024 08:58:40 GMT  
		Size: 14.2 KB (14241 bytes)  
		MIME: application/vnd.in-toto+json
