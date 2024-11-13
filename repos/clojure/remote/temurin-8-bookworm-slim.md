## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:93f4197d9efe525a7cc540a935bb87069c7ba9111e7b7a7644e43b28b7a5cd90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

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

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4de11c8af2ad3b8985a231ee55573476956886ab0e80df0e1ef66ab4ce10e663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201240626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fece0a1be0222f0dc093f4ab9e370f9f5d808a2b8e8c0ee39963faca6329814`
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
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef15dc57ce7f9bbb1604ca8ae2a03de99446ab0622ed7e470579354a436a41a2`  
		Last Modified: Wed, 13 Nov 2024 01:02:08 GMT  
		Size: 102.7 MB (102747715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26095bc2e7fb98993b3224ed4ac0013130461b02d4c5ee4066da370e24764ad3`  
		Last Modified: Wed, 13 Nov 2024 01:06:26 GMT  
		Size: 69.3 MB (69334910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad58a63dc189acdedc64867e34bc9a28477d7524adb73a0c192c6e5aed65b3b`  
		Last Modified: Wed, 13 Nov 2024 01:06:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:83605c450fb7c9a3dfcaf57da3bda43bbb7700809d641136b7a3b0cce7b9e7ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5063676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d80c2b97eb9bf4a2143c6bd087072de6b565df6d1ecbd70397e8b6b181b302`

```dockerfile
```

-	Layers:
	-	`sha256:0d1156fd55e5b584a9cd751969662821213d738727bf804fe9e40b8f0aeb1256`  
		Last Modified: Wed, 13 Nov 2024 01:06:24 GMT  
		Size: 5.0 MB (5049263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec1999d2063be65f47caaa4ad02b1ecb93f82268176b227c76defadf6e51f18d`  
		Last Modified: Wed, 13 Nov 2024 01:06:24 GMT  
		Size: 14.4 KB (14413 bytes)  
		MIME: application/vnd.in-toto+json
